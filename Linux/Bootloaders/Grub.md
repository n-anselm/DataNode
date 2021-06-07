### Grub

---

The Grub config file is located in ```/etc/default/grub```.

---

### Adjust Grub time settings

To change how long Grub waits until it boots the system, open the Grub config file in `/etc/default/grub`.

The default is 5 seconds. Look for the line containing this:

`GRUB_TIMEOUT=5`

You can change the 5 to any number you like. If you don't want Grub to wait at all, set the number to 0.

---
### Disable recovery mode

Open the grub config file located in ```/etc/default/grub```.

Uncomment this line: ```GRUB\_DISABLE\_RECOVERY="true"```
