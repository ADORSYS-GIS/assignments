### **LPIC-101 Practice Test**

**Time Allowed: 90 minutes**  
**Maximum Marks: 100**

---

#### **Section 1: System Architecture** (20 Marks)

1. **[Multiple Choice]**  
   Which of the following commands will display detailed CPU information on a Linux system?  
   A. `cat /proc/meminfo`  
   B. `lscpu`  
   C. `top`  
   D. `uname -r`  
   *(2 Marks)*  
B

2. **[Short Answer]**  
   What is the difference between `BIOS` and `UEFI` in terms of boot process and functionality?  
   *(5 Marks)*  
- BIOS uses the Master Boot Record (MBR) to save information about the hard drive data while UEFI uses the GUID partition table (GPT).
- BIOS is slower while UEFI is faster interms of the boot speed
- The BIOS has 16 bits architecture while UEFI has a 32 and 64 bits architecture
- The disk size support of the BIOS can be up to 2TB maximum while that of UEFI is over 2TB
- The BIOS is difficult to update and extend while UEFI is easy to update and extend

4. **[Practical]**  
   Use a command to determine which kernel modules are loaded in the current system. Explain how to load a new module named `dummy`.  
   *(5 Marks)*  
- The lsmod command which stands for 'list modules'
- 
5. **[Short Answer]**  
   Explain the purpose of the `/proc` and `/sys` directories in Linux.  
   *(8 Marks)*

- The '/proc' and '/sys' directories in linux are similar in their functionality. However, the '/proc' directory contains files with information regarding running processes and hardware resources while the /sys directory has the specific purpose of storing device information and kernel data related to hardware.
  
#### **Section 2: Linux Installation and Package Management** (20 Marks)

5. **[Multiple Choice]**  
   Which of the following commands installs a package using the APT package manager?  
   A. `yum install package`  
   B. `dpkg -i package.deb`  
   C. `apt install package`  
   D. `rpm -ivh package.rpm`  
   *(2 Marks)*  
C

6. **[Short Answer]**  
   Describe the difference between `apt` and `dpkg`.  
   *(5 Marks)*  
- 'apt' is a high-level package manager with automatic dependency resolution, while 'dpkg' is a lower-level tool that requires manual dependency handling. 'apt' is more user-friendly and widely used for package management on Linux systems.
- 'apt' is a higher-level tool that streamlines the process of installing, upgrading, and removing software packages. It automatically handles dependencies, ensuring that all required components are installed alongside the requested package. This simplifies the installation process for users while 'dpkg' is a lower-level tool that directly interacts with the system to manage individual Debian packages meaning It does not perform dependency resolution automatically, meaning users have to manually install any required dependencies.
- 
7. **[Practical]**  
   Write a command to find and remove orphaned packages in a Debian-based system.  
   *(3 Marks)*  

8. **[Practical]**  
   On a Red Hat-based system, explain how to configure a new YUM repository with the base URL `http://repo.example.com`. Provide a sample `.repo` file configuration.  
   *(10 Marks)*  

---

#### **Section 3: GNU and Unix Commands** (30 Marks)

9. **[Multiple Choice]**  
   Which command is used to display the last 10 lines of a file?  
   A. `head`  
   B. `tail`  
   C. `cat`  
   D. `less`  
   *(2 Marks)*  
B

10. **[Practical]**  
    Write a command to count the number of lines containing the word "error" in the file `/var/log/syslog`.  
    *(3 Marks)*  

grep "error" /var/log/syslog | wc -l

12. **[Short Answer]**  
    Explain the difference between `hard links` and `soft links` in Linux. How do you create each?  
    *(10 Marks)*  
- Hard links can only exist within the same filesystem while Soft links can point to files or directories on a different filesystem
- Hard links do not occupy additional disk space, as they reference the same inode as the original file while Soft links occupy a small amount of disk space, as they contain the path reference.
- Hard links work even if the original file or directory is moved, as they directly reference the inode while Soft link becomes a dangling link, pointing to a non-existent file if the original file or directory is deleted
- Accessing a hard-linked file is usually faster than accessing a symbolic link, as there’s no need to resolve the link
- We create a hard link using **ln** command with no parameters (for instance: **ln original file hard_link**) while we create a soft link using **ln -s** (for instance: **ln -s original file soft_link**)
  
13. **[Practical]**  
    Use the `find` command to locate all `.conf` files in `/etc` that have been modified in the last 7 days.  
    *(5 Marks)*
    
find /etc -type f -name "*.conf" -mtime -7

15. **[Short Answer]**  
    Explain the purpose of the `cron` daemon. Provide an example of a cron job that runs a script named `backup.sh` every day at midnight.  
    *(10 Marks)*  

Its primary purpose is to automate repetitive tasks, such as: Backups, Maintenance tasks (for example disk space monitoring, log rotation), Updates and installations, and Monitoring system resources (for example; CPU, memory, disk usage)
An example include: 0 0 * * * /path/to/backup.sh

#### **Section 4: Devices, Filesystems, and FHS** (30 Marks)

14. **[Multiple Choice]**  
    What does the command `df -h` display?  
    A. List of directories and files  
    B. Disk usage in human-readable format  
    C. Free memory  
    D. Filesystem errors  
    *(2 Marks)*

    B

16. **[Practical]**  
    Use a command to display the UUID of all mounted filesystems.  
    *(3 Marks)*

blkid -o list
    
17. **[Short Answer]**  
    Explain the difference between ext3 and ext4 filesystems. Mention at least two features of ext4 that make it better.  
    *(8 Marks)*  
- Ext3 has a maximum file size limit of 16 GB, while ext4 supports files up to 16 TB.
- Ext3 has a maximum partition size limit of 32 TB, while ext4 supports partitions up to 1 EB (1 exabyte).
- Ext3 introduced journaling, which records changes to the file system before applying them to the actual data. This ensures data consistency and allows for faster recovery from system crashes or power failures. Ext4 also uses journaling, but with improved efficiency and additional features.

Two features that make ext4 better is;
- By allocating space only when data is written, ext4 reduces disk fragmentation and improves write performance. This feature is particularly beneficial for systems with high write operations, such as databases or logging applications.
- The extents-based allocation scheme in ext4 allows for more efficient handling of large files and reduces fragmentation. This results in better performance and improved data integrity.

17. **[Practical]**  
    You have added a new disk to the system. Write the steps to create a new partition, format it with an ext4 filesystem, and mount it permanently at `/data`. Include all commands.  
    *(10 Marks)*  
- We start by listing all available disks and partitions using the command **sudo fdisk -l** and noting the disk and name we intend to carryout the partition on
- Next, we run the command sudo fdisk /dev/sda if /dev/sda is the disk we want to work with.
- Once in the fdisk menu we select the **n** option to create a new partition and follow the prompt to allocate our partition size making sure that our default is primary for partition type.
- Next we use the command **mkfs.ext4 /dev/sda1** to format the new partition with an ext4 filesystem
- We now create a new directory to serve as the mount point for the new partition using **sudo mkdir /data** and mount the partition to the /data directory using the command **sudo mount /dev/sda1 /data**
- Then edit the  **/etc/fstab** file to add a permanent mount entry for the new partition using the command **sudo vi /etc/fstab**
- Finally conclude by adding the UUID of the new partition at the end of the file and then save and exit. The UUID can be check using **blkid**
  
18. **[Short Answer]**  
    What is the purpose of the `/etc/fstab` file? Provide an example entry for mounting a filesystem.  
    *(7 Marks)*
- Automate the mounting of file systems during boot.
- Provide a centralized location for configuring file system mounts.
- Allow for easy modification of file system mounts without editing system scripts.

#### **Bonus Question** *(Optional - 10 Marks)*  
Explain the boot process in Linux from powering on the machine to a fully loaded OS, detailing the role of GRUB, the kernel, and system initialization.
---
when the machine is power on, the Bios then look into the master boot record (MBR) which is the first sector of the hard disk and locate the Bootloader. Bootloader formerly called the bootstrap is a program responsible for starting the Linux kernel and the most common bootloader today is the GRUB2. After the Bootloader have started the kernel, it starts the initialRamDisk(initRD). InitRD is a temporary file system that is only used during the boot process. InitRD creates an image  of the filesystem on a reserved area of the main memory that only contain files and directories that are required for the system start. InitRD then starts the init process which is the first process started on the linux system and always has a process ID1. Init then start all other processes and as soon as the init have started, the InitRD is therefore no longer required and therefore switch off.

### **Answer Key and Instructions for Scoring** 
- Award marks based on accuracy, detail, and clarity in the answers. 
- Practical questions should be tested on a Linux environment to validate the commands.
- Submit your answer under the submissions dir.
 
