### Starting the Tor service

---

Start tor:

    sudo service tor start
	
Ensure that tor is active:

    netstat -nvlp

The running port is 9050. You should find a line that contains this:

`tcp	0	0 127.0.0.1:9050	0.0.0.0:\*`
