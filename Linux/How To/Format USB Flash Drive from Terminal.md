To list storage devices:   

    df -h

Unmount the device you wish to format:

    sudo umount /dev/sdc1
	
---
### Format as vFat

To fomat with the vFat File System:

    sudo mkfs.vfat /dev/sdc1
	
---
### Format as exFat

    sudo mkfs.exfat /dev/sdc1
	
---
### Format as ext4

To format with the ext4 File System:

    sudo mkfs.ext4 /dev/sdc1
	
---
### Format as NTFS

To format with the NTFS File System:

    sudo mkfs.ntfs /dev/sdc1

