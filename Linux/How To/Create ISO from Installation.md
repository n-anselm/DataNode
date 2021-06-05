### Create an ISO Image with Linux Live Kit

The Linux Live kit is a set of shell scripts to create your own Linux .iso file from your current Linux installation.

First, you must install a dependency of Linux Live Kit, called squashfs.

Squashfs is a compressed read-only filesystem for Linux. Squashfs is intended for general read-only filesystem use, for archival use (i.e. in cases where a .tar.gz file may be used), and in constrained block device/memory systems (e.g. embedded systems) where low overhead is needed.

You nust install squashfs-tools in your system using the package manager:

    sudo aptitude install squashfs-tools
	
Now you must download the Linux Live kit from its official website: [https://www.linux-live.org/](https://www.linux-live.org/).

If you want, you should remove all unnecessary files from your system (for example man pages and all other files you don't need), to make your Live Linux system as small as possible (this step is optional). You must move the Linux Live kit to /tmp, and if you want, you can read the documentation files in DOC/ to learn how it works. Also, you can edit the .config file if you need to modify some variables.

To start, go to the Linux Live directory and execute the following script:

    sudo ./build

Once you see the root prompt again, it means that the process is complete.  
  
Finally, you'll find a .iso file located in */tmp*.  
  
To make a bootable USB, unpack the generated zip archive (also from */tmp*) to you USB device and run bootinst.sh from the boot subdirectory.
