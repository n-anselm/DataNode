### How to restart the GNOME desktop environment

---
### Method 1

Run this command in the terminal:

	sudo systemctl restart gdm.service
	
*NOTE: This will log you out of GNOME. Make sure all of your work is saved before you do this.*
	
---
### Method 2

Save all of your open files.
Press **Ctrl+Alt+Backspace**. It will restart GNOME instantly.

---
### Method 3

Run this command in the terminal:

	sudo /etc/init.d/gdm restart
	
---
### Method 4

Run this command in the terminal:

	killall gnome-panel
