### Creating a web server with Python

You can create a quick local web server with Python. Note that this server can be accessed on your local network only. This can either be localhost or another network host. You could serve it cross location with a VPN.

To start a web server run this command:

	python3 -m http.server

This will open a web server on your local network. On your machine, you can go to `localhost:8000` or whatever port is shown in the output in the terminal.

If you want to change the port, do it like this:

	python3 -m http.server <custom_port_number>

The webserver is also accessible over the network using your 192.168.-.- address. (To find your IP address, use the `ip a` or `ifconfig` command.)

*NOTE: This HTTP server has limited security so use it only for development purposes or sharing files locally.*
