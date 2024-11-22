1. B
2.
> The UEFI can Identify different partitions ie the boot sector must not always 
be the first sector while BIOS cannot identify different partitions.

> The  UEFI supports more functionalities than BIOS and larger sizes of disk partition
3.
> to list loaded modules : `lsmod`

> to add a module : ` sudo modprobe dummy /` where / is the mount point
4.
> ### /proc
It is used to store currently rnning processes.
It does not hold the same data after reboot.
eg /proc/cmdline
> ### /sys
It is used to store system processes and programs that are neccessary to ensure the 
smooth functioning of a system. eg /sys/systemd 

5. C

6. 
> apt (Advanced Package Manager) is a user friendly high level package manager.
> dpkg is a non-human frienly low level package manager

7.
`sudo apt autoremove`

8.
- To configure a new yum base repo eg nginx.repo,
The following steps can be applied 
` yum repolist` to list all repos
`yum update nginx.repo`

9.B

10.
`grep "error" /var/log/syslog | wc -l`

11.
> hard links cannot  cut across multiple file systems while softlink can.

> hardlinks are not affect if the target file is deleted but softlinks are broken

12. `find /etc -name "*.conf"`

13.
A cron daemond is a daemon that runs on the  background and wakes up every minute
to see what task is there for him to exercute.
```
00 00 * * * /backup.sh
@daily /backup.sh 
mv backup.sh /etc/cron.daily
```
14. B

15.
mount | grep -iw "uuid"

16.
> ext4 is an advanced version of ext3. 
it supports larger size of disk which ext3 cannot.
it can easily adapt to errors changes. and also more flexible than ex
t3.
17. ### steps to mount my new disk
- I will mount it first if it was not mountned authomatically. using 
`mount -t ext4 /dev/new_disk /mnt/data`
- or use `mount /dev/new_disk /mnt/data` and `mkfs.ext4 /mnt/data`
18. 
> The /etc/fstab is used to store the different mounted file systems in tabular manner.
eg /opt  /mnt/data   ext4   rw,nosuid,noatime   0   0
## Bonus Qusetion
> when the power on button is pressed,

- the BIOS initialises a POST test that check the essential hardware components.
- The BIOS loads the boot loader from the MBR partition table
- it is found on the first sector.
- the boot loader loads the kernel into memory and passes parametern to it
- The initramfs contains start up scripts that is used to start the initialization
  process of OS
- the kernel loads the os and starts its exercution
- uptill the login phase where the user need to enter his or her password .
- then the OS takes over from the kernel.
