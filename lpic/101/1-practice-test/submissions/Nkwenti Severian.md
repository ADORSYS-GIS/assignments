1. A
2. 
  - The BIOS is limited to 2TB of disk space while the the UEFI(unified extensible firmware interface) can take 2TB and above.
  - The BIOS loads the bootloader from the Master Boot Record while the UEFI loads from the GPT(GUID partition table) partition table.
  - The BIOS doesn't provide secure boot while the UEFI provides secure boot.
3.
- We use the command `lsmod` to list all currently loaded modules.
- To load a new module, we use `modprobe` command followed by the name of the module. `modprobe <module_name>`
- so in this case it will be `modprobe dummy` .
4.
  The /proc directory stores configuration files. this files are used by the system for many purposes; such as the **cmdline** which stores boot parameter passed to the kernel. We have the **cpuinfo** and **meminfo** which store info detailled information about the cpu and memory respectively.
  while the /sys stores system files such as; the **module** which contains information about loaded modules and also the **block** which has information about block devices.
5. C
6.
- dpkg is a low level package manager meaning it has limited features while apt is a high level package manager and has more features tthan dpkg
- apt is used to install packages remotely while dpkg is used to install packages locally; meaning dpkg is used to install already downloaded packages while apt downloads from repositories and installs them.
- apt is more user-friendly while dpkg is less user-friendly.
7. Orphaned package are like abandoned package, packages that are not more upgraded nor updated by the developper. So we use `sudo apt autoremove` .
8. You need to create a file with the **.repo** extension and you add the URL inside.
9. B
10. We use the `cat <apath_to_the_file> | grep "error" | wc -l`
11.
- Hardlinks are links that point to inode of a file called the target file. They are created using `ln <target_file> <hard_link>` while a hard link points to the path of the file. they created using `ln -s <target_file> <soft_link>`.
- hard links don't consume any extra disk space while softlink consume extra disk space.
- hardlinks can't be used accross different file system while softlinks can.
12. `find /etc -type f -name ".conf" -mtime -7`
13. a Crond is a service that execute task at a specificied time. Running a script every midnight we use `0 0 * * * ./backup.sh` . the two zeros means at zero minurte and zero hour.
14. B
15. We use the `blkid` command.
16.
- Ext4 has a better journaling mechanism than Ext3
- Ext4 has a has a higer size limit of over 16TB while Ext3 is just 2TB
- Ext4 can contain more subdirectories than Ext3
17.
- FIrstly we need to identify the device using `lsblk or fdisk` , then we format it with ext4 using `sudo mkfs.ext4 <device_name>`
- Next you create the mount point `sudo mkdir /mnt?data` then you mount it using `sudo mount <device_name> /mnt/data` .
18. Is a file that contains all the filesystem and their metadata.
19.
- When the machine is powered on, the first process that takes place is the POST(Powe on self test). This checks for hardware failure.
- The BIOS takes over initializing hardware components for the boot process and loads the boot loader from the first sector of the MBR.
- The boot loader loads the operating system kernel selected by the user passing parameters to it from the cmdline.
- The kernel now initializes startup scripts. 



