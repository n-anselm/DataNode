### Starting the Tor service

---

###### Method 1

Start tor:

    sudo service tor start
	
Ensure that tor is active:

    netstat -nvlp

The running port is 9050. You should find a line that contains this:

`tcp	0	0 127.0.0.1:9050	0.0.0.0:\*`

---

###### Method 2

Start tor:

	sudo systemctl start tor.service

Then run this command to find out if Tor is running or not:

	systemctl status tor.service

If you can find the following code in the status output, Tor is ready :

`Bootstrapped 100%: Done`
