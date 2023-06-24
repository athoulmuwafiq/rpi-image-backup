# rpi-image-backup
Shell script to backup and restore a Raspberry Pi image from and to an sdcard

## Purpose
This script is used to create an as-small-as-possible image dump from an sdcard containing a raspberry pi operating system. It does not use dd to dump the whole sdcard, it clone partition by partition with partclone and save the partition layout and the MBR. 

## Requirements
The script runs on a linux distribution of your choice. You must have the following tools installed:

* sfdisk
* partclone
* dd
* blkid



```
./rpi-image-backup --backup -d /dev/sdb -n scnshift -b ./backup
```
```
./rpi-image-backup --restore -d /dev/sdb -n scnshift -b ./backup/scnshift/YYYY-MM-DD
```

