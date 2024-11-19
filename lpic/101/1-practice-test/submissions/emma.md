Section A
1-c
2-Difference between BIOS and UEFI
-BIOS is a firmware that can support a maximum partion size of 2TB while UEFI is a firmware that can support a partition size of more than 2TB.
-BIOS depend of partition table while UEFI donot rely on partition table.
-BIOS firmware used partitioning scheme such as MBR(Master Boot Recoder) while UEFI firmware used partition such as GPT(Guid partition table).
-BIOS firware is commonly found in olden machine with HHD as storage unit while UEFI firmware is found in modern machine with SSD as storage unit.
-UEFI firware is more secure and has advance features than BIOS firmware.
3- To know modules which are currently loaded you can use the command below:
  -lsmod 
- To load a module called dummy for example, you do the following steps:
  -Go to your terminal.
  -Type the following command < modprobe dummy >.
  -To check the module you loaded use the lsmod command.
4-The purpose of the /proc directory is to store detail information about processes that are currently running in the system. 
 -The purpose of the /sys directory is to store configuration files about the system.
Section B
5-C
6- Difference between apt and Dpkg
-Both apt and Dpkg are package managers used in Linus(Debian-based) system, the are literally do the same thing, but differ in one way or the other because apt is an advanced version of the Dpkg and has more because it has advanced feaures than Dpkg.
7-Orphaned package are package that are broken or were halted during their installation. The command to find orphaned package, you can use the command apt-cache to search for that orphaned and delete it using apt remove command and also the apt remove --purge to remove the package and all it dependencies and configuration files.
8-The default package manager for all Red hart system is the yum package manager, so to add another
Section c
9-b
10-The command to count for the word error in the file /var/log/syslog is < cat /var/log/syslog | grep "error" | wc -w >.
11- Difference between hard links and soft links are as follows:
 - Hard link is renaming or giving another name to a same 'original file' while soft link is created inother to reference to the another file which is the original file.
 - Hard link donot cuts accross multiple filesystems while soft link do.
 - In hard link, when the original file is deleted, though it is deleted, the data is stored in the filesystem and the hard link point to that data, whilst in soft link once the original file is deleted, the link pointing the file is broken.
12-The command to find that end with .conf in the /etc file, you can use the command < sudo find /etc -name "*.conf" -mtime 604800 >.
13-The purpose of running cron jobs is to automate repetative tasks. An example of cron jos is < * * * * * /root echo " it is time " >> bashup.sh >.
14-b 
15- The command to list the uuid of mounted filesystems is < sudo fdisk -l >.
16- The difference between ext3 and ext4 filesystems 
  - ext3 filesystem is and extended version of ext2 filesystem since it came with a new feature called journald used to view system log, and the ext4 filesystems just offer more features than ext3. One of characteristics of ext4 filesystem is that stored data in an more efficient way and they more reliable.
17- To create a new partition on your filesystem do the following steps:
  -if your filesystem is not yet mounted, you can mount manually using the following commands:
     - sudo mkdir /data
     -sudo mount /dev/sdx /data
-  To partition the filesystem, you can use the tool parted, fdisk of gdisk etc. Using the tool parted, they will prompt you to enter some parameter and you will also have to precise you filesystem type.
18- The purpose of the /etc/fstab is to store information about different filesystem such as filesystem, mountpoint, option, type, dum and pass.
BONUS QUESTION
Boot process
- The Bios load inialise the hardware and load the bootloader after the power-on-self-test.
- The bootloader load the kernel and other utilities before allowing the control to the operating system.
- The /etc/systemd.init locate before the require runlevels, /etc/init.rc.d/ is going to start the init process.
