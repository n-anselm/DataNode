### How to get the public IP address of a device

---
#### Method 1

	curl ifconfig.me

#### Method 2

	curl 'https://api.ipify.org'

#### Method 3

	wget http://checkip.dyndns.org/ -q -O - | grep -Eo '\<[[:digit:]]{1,3}(\.[[:digit:]]{1,3}){3}\>'
