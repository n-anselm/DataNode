### Install Arch Linux (i686, No GUI, VirtualBox)

Boot from the Arch Linux ISO.

After the ISO has booted and you're in the shell, verify that you have an internet connection by entering this:

	ping -c3 gnu.org

*If you're installing Arch on a physical machine, it is best to connect the machine to Wi-Fi via ethernet, and then run this command to connect:*

	wifi-menu

After you're connected, sync the clock with this command:

	timedatectl set-ntp true

Next, run this command to list the drives (lsblk stands for “list block devices”):

	lsblk

To partition the disk of your choice, enter this:

	cfdisk /dev/sdx

This will load the disk partitioner.
  
If you are installing Arch to a newer physical hardware and the disk's capacity is over two terabytes, choose “gpt”, else choose “dos”. Dos will work with UEFI systems.
  
Create a new boot partion of 128MB. (If you are going to use a different bootloader than Grub, you might need to make this partition 256 or 512 megabytes.)
  
Make the partition primary.
  
Set the boot flag (make the partition bootable) by pressing “b” with the partition selected. (Pressing “b” multiple times will toggle the boot flag.)
  
Create another partition with the rest of the memory and make it primary as well.
  
Write the changes to the disk.
  
The partitions should now be configured like this:
  
```Boot partition (128MB) = /dev/sdx1 (bootable)```  
```Main partition = /dev/sdx2 (root partition)```

Quit the partitioner.

Format both of the partitions as ext4:

	mkfs.ext4 /dev/sdx1

	mkfs.ext4 /dev/sdx2

Mount the root partition:

	mount /dev/sdx1 /mnt

Make a directory called “boot” to mount the boot partition on:

	mkdir /mnt/boot

Mount the boot partition to that location:

	mount /dev/sdx1 /mnt/boot

Verify that the disks are configured correctly and mounted in the right place:

	lsblk

Next, run the pacstrap command, which will essentially install Arch for you (vim is optional):

	pacstrap /mnt base base-devel linux linux-firmware vim

Generate an fstab file, which contains a list of all the drives that Linux might try to load when you're booting up.

	genfstab /mnt

*NOTE: This command will make an fstab file that uses the device id (/dev/sdx) of the drive instead of the UUID of the drive to identify the drive. The device id can change, while the UUID is permanent. To prevent any issues, make the fstab file use the UUID:*

	genfstab -U /mnt

If you already have run genfstab without the “-U” option already, run this:

	genfstab -U /mnt >> /mnt/etc/fstab

Now, chroot into the Arch installation:

	arch-chroot /mnt /bin/bash

Install the network manager and Grub:

	pacman -S networkmanager grub

Make systemd start the network manager at boot:

	systemctl enable NetworkManager

Next, configure Grub:

	grub-install /dev/sdx

*NOTE: Do not write “dev/sdx1” or “dev/sdx2”. You need to configure Grub on the entire drive.*

Generate the Grub configuration file:

	grub-mkconfig -o /boot/grub/grub.cfg

Make sure that the output contains “Found linux image” and “Found initrd image”, else Grub will not be able to boot the Linux kernel.  

Next, you need to edit the locale file:

	vim /etc/locale.gen

Search for your language and uncomment the lines containing “UTF-8” and “ISO”. Save and exit (:wq).  

Now generate the locale:

	locale-gen

Also, you need to define your language in the locale.conf file (the file does not exist yet):

	vim /etc/locale.conf

Enter this if your language is English:  
  
```LANG=en\_US.UTF-8```
  
Save the file and exit.  

Set your hostname:

	vim /etc/hostname

Enter the name that you want there, save, and exit.  

Set your time zone:

	ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

Set a password for the root user:

	passwd

Exit out of the chroot environment:

	exit

Unmount all of the mounted partitions:

	umount -R /mnt

Reboot

	reboot

Boot into your new Arch Linux installation!

---
### Install Arch Linux (UEFI Boot, x86_64, XFCE4 DE, With SSH on VirtualBox)

If you're installing Arch on VirtualBox, create a new machine, go to Settings, and follow the next two steps.

No matter which settings you choose, make sure that the “Enable EFI (special OSs only)” option is checked (Settings > System > Motherboard).

Also, in Settings > Network > Adapter 1, change the adapter option so that the adapter is attached to “Bridged Adapter” instead of “NAT”. Then go to the Advanced tab and enable the “Allow All” option in "Promiscuous Mode". This is for logging in to the virtual machine via SSH.

Boot from the Arch .iso file.

If you're installing Arch on Virtualbox and want to do it from the host via SSH, follow these steps:

Enter this command to install *reflector* and *openssh*:

    pacman -Syy reflector openssh

Start SSH:

    systemctl start sshd
	
Create a password for the root user:

    passwd
	
Find out the IP address:

	ip a
	
On the host machine, enter this to log in to the virtual machine:

    ssh root@<ip_address>

If you're installing Arch on a physical machine, it is best to connect the machine to Wi-Fi via ethernet, and then run this command to connect:

    wifi-menu

Verify that you are connected:

    ping -c3 gnu.org

Enter this command to synchronize the network time protocol:

    timedatectl set-ntp true

Create a mirror list to utilize the fastest available servers:

    reflector -c <your\_country\_name> -a 6 --sort rate --save /etc/pacman.d/mirrorlist

Refresh the servers:

    pacman -Syy

Type this to list all the block devices (drives):

    lsblk

Make note of the disk name that you want to install Arch on. Here it will be referred to as */dev/sdx*.

Enter the disk configuration tool gdisk by entering this:

    gdisk /dev/sdx

Type in “n” for new and press Enter to create a boot partition. Also press Enter for the “Partition number” and “First sector”. For the “Last sector” enter “+200M” to create a 200MB UEFI boot partition. In the next option enter “ef00” to change the type to EFI and hit Enter.

Type in “n” again to create the root partition. Again, press Enter for the “Partition number” and “First sector”. Press Enter for “Last sector” if you want the partion to take all of the remaining space; else, enter the size that you want it to be. Also press enter for the “Hex code or GUID”.

Press “w" to write the changes to the disk.

To list the current disk configuration:

    lsblk

Format */dev/sdx1* (the boot partition) as FAT32:

    mkfs.fat -F32 /dev/sdx1

Format */dev/sdx2* (the root partition) as ext4:

    mkfs.ext4 /dev/sdx2

Mount the root partition on */mnt*:

    mount /dev/sdx2 /mnt

Create */boot/efi* directories for mounting the boot partition:

    mkdir -p /mnt/boot/efi

Mount the boot partition on */mnt/boot/efi*:

    mount /dev/sdx1 /mnt/boot/efi
	
You can type “lsblk” again to see the disk configuration.

Now you can install Arch to /mnt and also install the vim text editor:

    pacstrap /mnt base base-devel linux linux-firmware vim


Generate the filesystem table (based on the UUID of the partitions) and append that information to */mnt/etc/fstab*:

    genfstab -U /mnt >> /mnt/etc/fstab
	
Type this if you want to see the contents of the fstab file:

    cat /mnt/etc/fstab

Chroot into the new Arch installation:

    arch-chroot /mnt

To set the time zone, enter this:

    ln -sf /usr/share/zoneinfo/<region>/<city> /etc/localtime

Synchronize the hardware and system clock:

    hwclock --systohc

Edit the locale:

    vim /etc/locale.gen

If your language is English (US), for example, uncomment “en_US.UTF-8 UTF-8” in the file, save, and exit.

Generate the locale:

    locale-gen

Create the locale.conf file:

    echo LANG=en\_US.UTF-8 >> /etc/locale.conf

Set the hostname:

    echo <your\_hostname> > /etc/hostname

Configure the hosts file:

    vim /etc/hosts

Enter this into the */etc/hosts* file:

```
127.0.0.1	localhost  
::1			localhost  
127.0.1.1	<hostname>.localdomain		<hostname>
```

Set a password for the root user:

    passwd

Install the Grub bootloader and some other packages (if you're on VirtualBox, also install the package “virtualbox-guest-utils”):

    pacman -S grub efibootmgr networkmanager network-manager-applet dialog os-prober mtools dosfstools linux-headers cups reflector openssh git xdg-utils xdg-user-dirs

Install the Grub bootloader:

    grub-install --target=x86\_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB

Create a Grub configuration file:

    grub-mkconfig -o /boot/grub/grub.cfg

Make sure that the output contains “Found linux image” and “Found initrd image”. If it does not, Grub has not found a Linux image to boot from.

Enable the network manager at startup:

    systemctl enable NetworkManager

Enable ssh at startup (optional):

    systemctl enable sshd

Enable the cups printing manager at startup (optional):

    systemctl enable org.cups.cupsd

Create a new user with a user directory and who is in the wheel group:

    useradd -mG wheel <username>

Set a password for the new user:

	passwd <username>

Give the new user sudo priviledges:

    EDITOR=vim visudo

Uncomment the line containing “%wheel ALL=(ALL) ALL”  
  
Exit the chroot environment:

	exit

Unmount all mounted partitions:

    umount -a

Reboot the machine:

    reboot

Log in again and enter this command to install the Xfce desktop environment and some other packages (if you're on VirtualBox you also have to install the “xf86-video-vmware” package):

    sudo pacman -S xorg lightdm lightdm-gtk-greeter xfce4 xfce4-goodies

Enable the lightdm display manager:

    sudo systemctl enable lightdm

Reboot:

    reboot

Boot into your new Arch Linux installation!
