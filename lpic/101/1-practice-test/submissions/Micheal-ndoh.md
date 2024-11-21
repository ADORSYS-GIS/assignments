1= lscpu**(B)**

2= **BIOS** in terms of boot process uses the `Master Boot Record(MBR)` as it's Bootloader while **UEFI(unified extensible firmware interface)** uses the `Grub(Grand unified bootloader)` or grub2 as it's bootloader and and  the maximum number of partitions on a BIOS system is `4` while in UEFI is `128`. The UEFI offers a more faster and secured booting interface with new improved configurable features on the boot menu than the BIOS. The BIOS uses the `SYS V(5) init` to manage it's processes and services while the UEFI uses `systemd`

3= Use the `lsmod` command to list all modules loaded on your linux system. To load a new kernel either you use the **insmod** `(loads the kernel but without its dependencies)` or *modprobe* `(proferable because it loads both the kernel and its dependencies). using modprobe to load dummy : sudo modprobe dummy

4= /proc holds the running processes and programs of a system while /sys holds add-on applications files and configurations

5=apt install package **(C)**

6= **apt** is a more advanced high level package manager that has the ability of searching the internet scanning through repositories to install a specific package and is more human friendly.
**dpkg** is a low level package manager which is more system friendly that it communicates faster and directly with the computer system.

7=sudo apt autoremove

9=tail

10= cat /var/log/syslog | grep error | wc -l

11= Hard link are files that are directly linked to each other any thing written in one applies to the other. Softlinks are pointers to a file. when a softlink main target is deleted the softlink can not access the data another  but when a hardlink is deleted the same data can be accessed on the other file. soft links can be accessed accross different file systems while hard links can ony be access on the system file system

12=find /etc -type f -name "*.conf" -mtime -7

13=The cron daemon is used for scheduling tasks or processes to be executed at a given time
    Example: 0 0 * * * /home/user/backup.sh

14=B

15=cat /etc/fstab | awk '{print $1}'

>17=firstly use the **lsblk** command lists all disks then create a new partition like using  **fdisk /dev/sda**
 >To format with the ext4 systemuse **mkfs.ext4 /dev/sda1** 
then create a mount point
**mkdir /data**
lastly mount the new partiton to /data **mount /dev/sda1 /data**

18= /etc/fstab holds configuration of mounted systems


19=when the computer is powered on the computer does power on self test which for initialization of hardware devices and system units if they are functioning then the boot loader loads the kernal and initramfs from the /boot directory  then the firmware loads the first stage of bootloader which the boot sector and the second stage which is the loading the kernel the the initramfs is used as a temporary filesystem which is used for the initialization of the kernel and the system initializtion begins where startuo scripts and services needed to manage the system executed



# LPIC 2
## PART 1

1=journalctl

2=

3=passwd 

4=

5=

6= -R

7=LD_LIBRARY_PATH

8=systemctl stop ssh 

9=traceroute

10=/etc/crontab

 ## PART 2
 
11=B

12=C

13=C

14=B

15=C

16= C
 
17=B

18=A

19=B

20=D

## Practical

21= * 2 5 * * ./backup

### 22=
**Hardlinks**
- Hardlinks are links that have thesame inodes and any modification on one applies to the other
- Hardlinks are created using the following commands
- Hardlinks can not be accessed across different filesystems 
- When a hardlink is deleted the data on the other file remains accessible
```shell
ln <nameofname>
```
Or with the cp command using the -l flag
```shell
cp -l 
```
**Softlink**
- Softlinks are pointers to a file or a directory
- Softlinks can be access accross different filesystems
- When the target file is deleted the softlinks can not able to access the file's  data anymore
- To create a softlink use the ln command with the -s flag 
```shell
ln -s <nameoffile>
```
24= For 
find /home/user -type f -exec chmod 644 {} \; -o -type d -exec chmod 755 {} \;

25= It holds the configurations of the name service switch
e.g hosts: files

27= **iptables** it's a low levelprogram for managing IPv4/IPv6 packet filtering. it's more computer friendly

**ufw**  it's a high level program for managing a netfilter firewall and more user friendly to use
