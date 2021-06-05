### How to change the network interface name

---
Run the ```ifconfig``` or ```ip a``` command to list all of the interface names.

Execute this command to disable the interface:

	sudo ifconfig <interface_name> down
	
Set the new interface name:

	ip link set <interface_name> name <new_interface_name>
	
Enable the interface:

	sudo ifconfig <new_interface_name> up
