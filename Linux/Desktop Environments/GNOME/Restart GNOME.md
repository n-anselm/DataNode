## How to restart the GNOME desktop environment

---

### Method 1

Make sure that all of your work is saved; this action might close all of your open applications.

	dbus-send --type=method_call --print-reply --dest=org.gnome.Shell /org/gnome/Shell org.gnome.Shell.Eval string:'global.reexec_self()'

---
### Method 2

Run this command in the terminal:

	sudo systemctl restart gdm.service
	
*NOTE: This will log you out of GNOME. Make sure all of your work is saved before you do this.*
	
---
### Method 3

Save all of your open files.
Press **Ctrl+Alt+Backspace**. It will restart GNOME instantly.

---
### Method 4

Run this command in the terminal:

	sudo /etc/init.d/gdm restart
	
---
### Method 5

Run this command in the terminal:

	killall gnome-panel
