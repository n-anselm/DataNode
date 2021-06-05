### Installing the MATE desktop environment

---
###### On Debian:

	sudo apt install ubuntu-mate-desktop

---
###### On Kali Linux (specific): 

Open ```/etc/apt/sources.list``` with sudo in an editor.

Add these two lines and save the file:

deb http://kali.download/kali kali-rolling main non-free contrib
deb-src http://kali.download/kali kali-rolling main non-free contrib

Update the system:

	sudo apt update
	
Install MATE:

	sudo apt-get install mate-core mate-desktop-environment-extra mate-desktop-environment-extras
	
Reboot the system.

---
###### On Arch Linux:

    sudo pacman -S mate mate-extra
