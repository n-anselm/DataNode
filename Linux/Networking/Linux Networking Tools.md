### ping

The **`ping`** command is used to check if a remote system is running or up. In short, this command is used to detect whether a system is connected to the network or not. You can ping either an IP address or a domain name. A ping operation can fail if ping access is denied by a network firewall.

Syntax:

	ping <ip_address>

or

	ping website.com

---

### host

This command is used to obtain network address information about a remote system connected to your network. This information usually consists of the system’s IP address, domain name address, and sometimes the mail server.

Syntax:

	host website.com

---

### finger

One can obtain information about the user on the network and the **`who`** command is used to see which users are currently online on your system. The **`who`** command lists all users currently connected, along with when, how long, and where they logged in. **`finger`** can operate on large networks, though most systems block it for security reasons.

Syntax:

	finger website.com

---

### traceroute

This command is use to track the sequence of computer networks. You can track the route to check through which devices you are connected to a host. **`mtr`** or **`xmtr`** tools can also be used to perform both pings and traces. Options are available for specifying parameters like the type of service (**\-t**) or the source host (**\-s**).

---

### netstat

This command is used to check the status of ports whether they are open, closed, waiting, and masquerade connections. The Network Statistic (netstat) command displays connection information, routing table information, etc.

---

### tracepath

**`tracepath`** performs a very similar function to that of the traceroute command. The main difference between these commands is that tracepath doesn’t take complicated options. This command doesn’t require root privileges.

	tracepath website.com

---

### dig

**`dig`** (Domain Information Groper) queries DNS related information like a record, cname, mxrecord etc. This command is used to solve DNS related queries.

Syntax:

	dig website.com

---

### hostname

This command is used to see the hostname of your computer. You can change hostname permanently in `/etc/hostname` or `etc/sysconfig/network`. After changing the hostname you need to reboot the computer.

---

### route

The route command is used to display or modify the routing table. To add a gateway use (**\-n**).

---

### nslookup

You can use the `nslookup` (name server lookup) command to find out DNS related queries or testing and troubleshooting a DNS server.

Syntax:

	nslookup website.com
