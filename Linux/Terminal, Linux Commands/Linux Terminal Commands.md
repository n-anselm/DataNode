### Linux Terminal Commands
Note: More commands will be added with time.

Command | Description
-----|-----
[[#cal]] | Display a calendar
[[#cat]] | Concatenate files and print on the standard output
[[#cd]] | Change the current/working directory
[[#clear]] | Clear the terminal screen
[[#cp]] | Copy files and/or directories
[[#date]] | Display the current date and time
[[#echo]] | Display a line of text
[[#exit]] | Exit the shell
[[#find]] | Search for files in a directory hierarchy
[[#grep]] | Search for patterns
[[#groups]] | Show the groups that are assigned to a user
[[#history]] | Show list of commands that were run in the terminal
[[#locate]] | Find files by name
[[#ls]] | List directory contents
[[#mkdir]] | Create a new directory/folder
[[#mv]] | Move or rename files
[[#pwd]] | Print name of current/working directory
[[#reset]] | Reinitialize the terminal
[[#rm]] | Remove files or directories
[[#rmdir]] | Remove empty directories
[[#shutdown]] | Halt, power-off, or reboot the machine
[[#sudo]] | Execute a command as another user
[[#update-grub]] | Generate a grub config file
[[#wc]] | Count newlines, words, or bytes
[[#wget]] | Non-interactive network downloader
[[#whoami]] | Print the username of the current user

---
#### cal
Display a calendar

---
### cat
(con**cat**enate)
Concatenate files and print on the standard output

---
#### cd
(**c**hange **d**irectory)
Change the current/working directory

---
#### clear
Clear the terminal screen

---
#### cp
(**c**o**p**y)
Copy files and/or directories

---
#### date
Display the current date and time

---
#### echo
Display a line of text

---
#### exit
Exit the shell

---
#### find
Search for files in a directory hierarchy

---
#### grep
Search for patterns

**Examples**
Search for "hello world" in a file:

	grep 'hello world' <file-to-search>

You can also pipe output into this program to filter results:

	history | grep 'cd'

---
#### groups
Show the groups that are assigned to a user

**Examples**
Show groups assigned to the current user:

	groups

Show groups assigned to another user:

	groups <username>

---
#### history
Show list of commands that were run in the terminal

---
#### locate
Find files by name

---
#### ls
(**l**i**s**t)
List directory contents

Argument(s) | Description
-----|-----
\-a, --all | show hidden files
\-A, --almost-all | do not list implied . and . .
\-l | use a long listing format
\-r, --reverse | reverse order while sorting
\-R, --recursive | list subdirectories recursively
\-S | sort by file size, largest first
\-t | sort by time, newest first

---
#### mkdir
(**m**a**k**e **dir**ectory)
Create a new directory/folder

**Examples**

	mkdir <directory-name>
	
Multiple directories can be created at once:

	mkdir <directory1> <directory2> <directory3> ...

---
#### mv
(**m**o**v**e)
Move or rename files

---
#### pwd
(**p**rint **w**orking **d**irectory)
Print name of current/working directory

---
### reset
Reinitialize the terminal

---
#### rm
(**r**e**m**ove)
Remove files or directories

---
#### rmdir
Remove empty directories

---
#### shutdown
Halt, power-off, or reboot the machine

Argument(s) | Description
-----|-----
\-H, --halt | halt the machine
\-P, --poweroff | power-off the machine
\-r, --reboot | reboot the machine
\-h | equivalent to --poweroff, overidden by --halt
\-c | cancel a pending shutdown

---
#### sudo
(**su**peruser **do**)
Execute a command as another user

---
#### update-grub
Generate a grub config file
`update-grub` actually executes this command: 

	sudo grub-mkconfig -o /boot/grub/grub.cfg

---
#### wc
(**w**ord **c**ount)
Count newlines, words, or bytes

---
#### wget
(**W**orld **W**ide **W**eb **get**)
Non-interactive network downloader

---
#### whoami
(**who am I**)
Print the username of the current user

This command does the same thing:

	echo $USER
