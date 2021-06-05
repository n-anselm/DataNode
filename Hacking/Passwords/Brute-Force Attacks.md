### Brute-force attacks

---

The brute-force attack is still one of the most popular password cracking methods. Nevertheless, it is not just for password cracking. Brute-force attacks can also be used to discover hidden pages and content in a web application. This attack is basically a “hit-and-try” until you succeed. This attack sometimes takes longer, but its success rate is higher.

---

###### What is a brute-force attack?

A brute-force attack is when an attacker uses a set of predefined values to attack a target and analyze the response until he succeeds. Success depends on the set of predefined values. If it is larger, it will take more time, but there is better probability of success. The most common and easiest to understand example of the brute-force attack is the dictionary attack to crack the password. In this method, attacker uses a password dictionary that contains millions of words that can be used as a password. Then the attacker tries these passwords one by one for authentication. If this dictionary contains the correct password, the attacker will succeed.

In a traditional brute-force attack, the attacker just tries the combination of letters and numbers to generate the password sequentially. However, this traditional technique will take longer when the password is long. These attacks can take several minutes to several hours or several years, depending on the system used and length of password.

To prevent password cracking by using a brute-force attack, one should always use long and complex passwords. This makes it hard for the attacker to guess the password, and brute-force attacks will take too much time. Most of the time, WordPress users face brute-force attacks against their websites. Account lock out is another way to prevent the attacker from performing brute-force attacks on web applications. However, for offline software, things are not as easy to secure.

Similarly, for discovering hidden pages, the attacker tries to guess the name of the page, sends requests, and sees the response. If the page does not exist, it will show response 404, and on success, the response will be 200. In this way, it can find hidden pages on any website.

Brute-force is also used to crack the hash and guess a password from a given hash. In this, the hash is generated from random passwords and then this hash is matched with a target hash until the attacker finds the correct one. Therefore, the higher the type of encryption (64-bit, 128-bit or 256-bit encryption) used to encrypt the password, the longer it takes to break.

---

###### What is a reverse brute-force attack?

A reverse brute-force attack is another term that is associated with password cracking. It takes a reverse approach in password cracking. In this, the attacker tries one password against multiple usernames. Think like if you know a password but do not have any idea of the usernames. In this case, you can try the same password and guess the different user names until you find the working combination.

Now, you know that a brute-forcing attack is mainly used for password cracking. You can use it in any software, any website, or any protocol, which doesn't block requests after a few invalid trials.

---

### Popular tools for brute-force attacks

---
###### Aircrack-ng

This is a popular wireless password-cracking tool that is available for free. This tool comes with a WEP/WPA/WPA2-PSK cracker and analysis tools to perform attacks on WIFi 802.11. Aircrack NG can be used for any NIC which supports raw monitoring mode.

It basically performs dictionary attacks against a wireless network to guess the password. As you already know, success of the attack depends on the dictionary of passwords. The better and effective the password dictionary, the more likely it is that it will crack the password.

It is available for Windows and Linux platforms. It has also been ported to run on iOS and Android platforms. Download Aircrack-ng from this link: [http://www.aircrack-ng.org/](http://www.aircrack-ng.org/).

---

###### John the Ripper

John the Ripper is another excellent tool that does not need any introduction. It has been a favorite choice for performing brute-force attacks for long time. This free password-cracking software was initially developed for Unix systems. Later, developers released it for various other platforms. Now, it supports fifteen different platforms including Unix, Windows, DOS, BeOS, and OpenVMS. You can use this to either identify weak passwords or to crack passwords for breaking authentication.

This tool is very popular and combines various password-cracking features. It can automatically detect the type of hashing used in a password. Therefore, you can also run it against encrypted password storage.

Basically, it can perform brute-force attacks with all possible passwords by combining text and numbers. However, you can also use it with a dictionary of passwords to perform dictionary attacks.

Download John the Ripper from this link: [http://www.openwall.com/john/](http://www.openwall.com/john/).

---

###### Rainbow Crack

Rainbow Crack is also a popular brute-forcing tool used for password cracking. It generates rainbow tables for using while performing the attack. In this way, it is different from other conventional brute-forcing tools. Rainbow tables are pre-computed. It helps in reducing the time in performing the attack.

The good thing is that there are various organizations which have already published the pre-computer rainbow tables for all Internet users. To save time, you can download these rainbow tables and use them in your attacks.

This tool is still in active development. It is available for both Windows and Linux and supports all the latest versions of these platforms.

Download Rainbow Crack and read more about this tool from this link: [http://project-rainbowcrack.com/](http://project-rainbowcrack.com/).

---

###### Cain and Abel

This password-cracking tool can help you in cracking various kind of passwords by performing brute-force attacks, dictionary attacks, and cryptanalysis attacks. Cryptanalysis attacks are done by using rainbow tables.

It is worth mentioning that some virus scanners detect it as malware. Avast and Microsoft Security Essentials report it as malware and block it in the system. If it is in your system, you should first block your antivirus.

Its basic functions:

- Sniffing the network
- Cracking encrypted passwords using dictionary attack
- Brute-force and cryptoanalysis attacks
- Recording VoIP conversations
- Decoding scrambled passwords
- Recovering wireless network keys
- Revealing password boxes
- Uncovering cached passwords
- Analyzing routing protocols

The latest version of the tool has many features, and has added sniffing to perform Man in the Middle attacks.

Download Cain and Abel from this link: [http://www.oxid.it/cain.html](http://www.oxid.it/cain.html).

---

###### L0phtCrack

L0phtCrack is known for its ability to crack Windows passwords. It uses dictionary, brute-force, hybrid attacks, and rainbow tables. The most notable features of L0phtCrack are scheduling, hash extraction from 64 bit Windows versions, multiprocessor algorithms, and network monitoring and decoding. If you want to crack the password of a Windows system, you can try this tool.

Download L0phtCrack from this link: [http://www.l0phtcrack.com](http://www.l0phtcrack.com/.).

---

###### Ophcrack

Ophcrack is another brute-forcing tool specially used for cracking Windows passwords. It cracks a Windows password by using LM hashes through rainbow tables. It is a free and open-source tool. In most cases, it can crack a Windows password in a few minutes. By default, Ophcrack comes with rainbow tables to crack passwords of less than 14 characters which contain only alphanumeric characters. Other rainbow tables are also available to download. Ophcrack is also available as LiveCD.

Download Ophcrack from this link: [http://ophcrack.sourceforge.net](http://ophcrack.sourceforge.net/.).

---

###### Crack

Crack is one of the oldest password cracking tools. It is a password cracking tool for the UNIX system. It is used to check weak passwords by performing dictionary attacks.

Download Crack from this link:[http://www.crypticide.com/alecm/software/crack/c50-faq.html](http://www.crypticide.com/alecm/software/crack/c50-faq.html).

---

###### Hashcat

Hashcat claims to be the fastest CPU based password cracking tool. It is free and comes for Linux, Windows and Mac OS platforms. Hashcat supports various hashing algorithms including LM Hashes, MD4, MD5, SHA-family, Unix Crypt formats, MySQL, Cisco PIX. It supports various attacks including the brute-force attack, combinator attack, dictionary attack, fingerprint attack, hybrid attack, mask attack, permutation attack, rule-based attack, table-lookup attack and toggle-case attack.

Download Hashcat from this link: [https://www.hashcat.net](https://www.hashcat.net/).

*NOTE: Some of this data might be outdated.*
