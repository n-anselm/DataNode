![[linux_file_system_structure.png]]

Folder | Description
-------|-------
/bin | Linux commands
/boot | Contains files that aren't used by the operating system, but by the bootloader
/etc | Additional programs and data files
/lib | C programming library directory
/mnt | Mount directory; usually reserved for mounting filesystems
/opt | Optional add-on applications
/root | Root home directory. It is not same as /
/sbin | System binaries
/proc | Running processes
/tmp | Temporary directory
/home | User directories
/var | Directory for system logs

---

### File System Paths
There are two paths to navigate in a filesystem:

- Absolute path
- Relative path

An absolute path always begins with a “/”. This indicates that the path starts at the root directory. An example of an absolute path is:

```
cd /var/log/samba
```

A relative path does not being with a "/". It identifies a location relative to your current position. An example of a relative path is:

(If you're in the /var directory)
```
cd log
```
