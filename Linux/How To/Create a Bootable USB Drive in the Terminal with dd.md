### How to Create a USB Drive in the Terminal with dd

**WARNING!**
`dd` is a very powerful tool. Use with extreme caution!

You can use `dd` to make a bootable drive for any OS.

`dd` stands for **D**ata **D**uplicator which copies blocks from one device to another. `dd` can also be used to make or restore backups.

---
1. **Format the USB drive**
List all of the disks:

	lsblk
If the drive is mounted, you need to unmount it. Use this command (replace the X with the right letter):

	umount /dev/sdX
After unmounting, we can format the drive. **(WARNING: THIS WILL ERASE EVERYTHING ON YOUR DRIVE. IF YOU ACCIDENTALLY CHOOSE THE WRONG DRIVE, THERE IS NOTHING YOU CAN DO TO RECOVER YOUR DATA.)**

	mkfs.vfat /dev/sdb -I

2. **Flash the image to the USB drive with dd**

	dd if=~/path/to/image/file of=/dev/sdX
Clarification:
**if** stands for **i**nput **f**ile. This specifies the location of the image you want to flash.
**of** stands for **o**utput **f**ile. This specifies where the image is going to be flashed to.

---

**Monitor Progress**
If you want to monitor progress on `dd`, run this:

	pgrep -l ‘^dd$’

This will give you the process number of `dd`. Run this command to view the progress this far:

	kill -USR1 <process_number>

---
**Miscellaneous**
For more details on `dd`, see the man page:

	man dd

or run

	dd --help
