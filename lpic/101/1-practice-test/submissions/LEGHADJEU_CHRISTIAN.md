Section 1:
1. answer= B. `lscpu`
2.
| BIOS | UEFI |
| -- | -- |
| it supports a maximum of 4 partitions | it supports a maximum of 128 partitions |
| it supports a maximum disk size of 2TB | It spports a disk size of more than 2TB |
| it is an old firmware | it is more recent and has more features like GUI | 
3. The lsmod comand is used to used to list which kernel modules are currently loaded in the system.
To load the module dummy, the dummy module files needs to be added to the  /lib/modules/ directory 
and it's corresponding configuration files in the /etc/modeprobe.d directory and then we can run the `modprobe dummy` command to load it to the kernel.
4. The /proc directory contains data about running processes and processing device related information suchas cpu info, memory info
 while the /sys directory contains system related data like kernel data.
Section 2:
5. anwer= C. apt install package
6.
| apt | dpkg |
| -- | -- |
| apt is a high level package manager | dpkg is low level package manager |
| apt has advanced features such as installing a package with it's corresponding dependencies | while dpkg just installs the package without it's dependencies |
7. `sudo apt purge`
8. To configure a new Yum repository a new .repo file needs to be added under the /etc/yum.repo.d/ directory with the line https://rpms.gis-adorsysrepo.net/adorsys/remi.repo in the file.

Section 3:
9. answer= B. tail
10. command: ```grep "error" /var/log/syslog | wc -l```
11. 
| hard links | soft links |
| -- | -- |
| they have the same inode as the target file | they do not have the same inode as the target file |
| they cannot cut ac0oss different file systems | they can  cut across different file systems |
| can be created using the `ln` command | they can be created with the `ln -s` |
12. command: `find /etc type f -name .conf -mtime -7`
13. The cron daemon is a service that manages the scheduling and the execution of crons or automated jobs with the help of the `crontab` command. The cron jobs can be scheduled with the `crontab -e` command which allows us to edit the /etc/crontab file.
To schedule of a cron job that runs a script named backup.sh every day at midnight, the file should be executable and the following line is to be added to this file:
```
0 0 * * * backup.sh
```
Section 4:
14. answer= B. Disk usage in human-readable format
15. command: ` lsblk -o UUID`
16.
| ext3 | ext4 |
| -- | -- |
| It supports a maximum file system size of 16TB and 2TB max file size |  It supports a maximum file system size of 1EiB and 16TB max file size |

17. The newly added let's say it's given the name  by the system /dev/sda, to create new partition we can use the parted,fdisk,or gdisk utilities.
Using the fdisk utility to manipulate it's partition table;
- we can use the command `sudo fdisk /dev/sda2 ` since root priveleges are require.
-   Then entering  `n` to create a new partition.
- Then inputing the  Partition number.
-  Then the first sector and then the last sector.
-  After that the new partion will be craeted.
 Ater creating the partition with the fdisk utility, we can format it with an ext4 filesystem using the command:
```
mkfs.ext4 /dev/sda1
```
To permanently mount our disk /dev/sda on /data directory, we can add the line `mount /dev/sda /data` to a start up script such as the ~/.bashrc

18. The /etc/fstab file is the file that is used to provide description about the filesystem that can be mounted on a linux system.
  It serves as reference when a new file system is to be mounted.
 
 BONUS.
- The POST (power-on self-test) process is executed to identify simple hardware failures as soon
as the machine is powered on.
- The BIOS activates the basic components to load the system.
- The BIOS loads the first stage of the GRUB from the MBR.
- The first stage of the GRUB bootloader calls the second stage of the bootloader, responsible for
presenting boot options and loading the kernel.
