### SECTION 1 - ANSWERS
1. B
2. - The BIOS uses Master Boot Record(MBR) partitioning scheme while the UEFI uses GUID Partition Table(GPT) partitioning scheme.
   - The BIOS starts the boot process by carrying out a Power-On Self Test(POST) while the UEFI carries out a series of tests to ensure that the system functions correctly.
   - The BIOS uses the fdisk command to partition disk and is limited to only 4 primary partitions while UEFI uses the gdisk command to partition disk and does not have a speficic limit of primary partitions.
3. The command used to determine kernel modules loaded in the current system is lsmod. To load a new module called dummy you can use the command `insmod dummy`
4. The /proc stores information about processes currently been run by the system while the /sys directory stores device information and kernel data related to hardware.
### SECTION 2 - ANSWERS
5. C
6. apt is a tool that provides a more user-friendly interface for package management while dpkg is a tool that provides a low level command line interface for package management
7. dpkg --purge
8. yum addrepos http://repo.example.com
### SECTION 3 - ANSWERS
9. B
10. cat /var/log/syslog | grep 'error' | wc -l

11. |Hard links|Soft links|
    |----------|----------|
    |They point to the file itself|They point to the path of the file|
    |They have the same inode as the file|They have a different inode from that of the file|
    |They cannot span across different filesystems|hey can span across different filesystems|
    |They occupy more disk space|They occupy less disk space|
    |They can still be accessed after the file has been deleted|hey become broken after the file is deleted|
    |Created using the command `ln`|Created using the command `ln -s`|
    
12. sudo find /etc -type f -name '*.conf' -atime -6

13. The cron daemon is used for scheduling a job for it to be executed repeated over a desired timelap.

### SECTION 4 - ANSWERS
14. B
15. blkid
16. - ext3 is an early filesystem that supports journaling why ext4 is a more recent and more efficient filesystem.
    - ext4 supports a max file size of 2TB while ext3 supports a max file size of 16TB.
    - ext4 supports a max filesystem size of 16TB while ext3 supports a max filesystem size of 1EB.
17. - After connecting the new disk to the system, run the command `lsblk` to ensure the system has identified the disk.
    - Run the command `fdisk <DISK_NAME>` to open the write on the disk and create a new partition.
    - Run the command `mkfs.ext4 <DISK_PARTITION>` to format it with an ext4 filesystem.
    - Run the command `mount UUID=<uuid> /data`.
18. The /etc/fstab file is used to store information about the filesystem partition table.
An example entry for mounting a filesystem is an shown below;
<br>
/boot/efi was on /dev/nvme0n1p2 during installation
UUID=38AC-F7F1  /boot/efi       vfat    umask=0077      0       1
/swapfile                                 none            swap    sw              0       0

<br>

### BONUS
After the computer is powered on, the BIOS performs a POST test to ensure that the system functions correctly then goes to the first partition of the disk to load the bootloader(GRUB), then the bootloader goes to load the kernel and the kernel starts the initialization process and the Operating System is loaded in memory.
