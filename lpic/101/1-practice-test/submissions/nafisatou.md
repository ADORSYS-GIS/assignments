Section 1.
(1) B

(2) The Bios also known as the 'basic input output system' and UEFI 'unified extensible firmware interfaCe' are both are both types of firmware used to initialize the  hardware during the boot process and start the operating system.
     the bios is responsible for starting,initializing the hardware and prepare the system for looding the operating system.while the UEFI is the newer version of bios that is responsible for starting up the operating system automatically
UEFI generally provides faster boot times and improved system performance, its more efficient booting process and support for modern perfomance compare to the older BIOS.

(3) lsmod shows which modules is presntly loaded in the kernel .

(4) 
The /proc directory used to expose information about processes . On most modern Unix-like systems, including Linux, the filesystem mounted on this mount point. In Linux and several other Unix-linux
 it was used to expose all kinds of other information that has nothing to do with processes. For example, networking information, information about the hardware and the CPU, information about block devices.
 wile the /sys is the newer version of the /proc,which is more precise on the also processes to list in the kernel version .therefore developers sees it more reliable and efficient than the /proc so it now widely used .
    the /sys differenciates each processes where it should be place for example(all block devices are stored under'lsblk' and so on .which is easier to locate all your processes.
    
 SECTION 2
 (5) C
 
 (6) apt is a high level package manager tool for dependencies and repositories or updates while dpkg is a low level tool that istall and manges,remove and provide information about debain packages dpkg is the package manager for debian.
 
 (7) To remove orphaned packages in linux we use the --purge command .(orphan packages are packages that a no longer used but consumed disk space )
      while to find the orphan package
      
 (8)









SECTION 3
(9) B

(10).

(11)  Hard links are links that are direct reference to the inode.when you creat a hardlink to a file botk the original file and the link share thesame inode .(inode metadata of a file)
      hardlink can be created using the (ln command) the you put the path to the file.
      While Softlink also known as the symbolic link is the pointer to the path of the file rather than the file itself. unlike hardlink symbolic link do not share thesame inode 
      this means symbolic link can point to a file in diffrent files systems .symbolic links are created using the command (ln -s).
      
(12) 


(13) THE cron daemon is a clock daemon that runs commands at specific date and time .you can specify the specific time and date you want your machine to run and set it using the cron daemon .
      cron daemon help you remember a specific tasks that will be run at a particular time and date even when you forgot.
      some common example is; 
     00 00 * * * /backup.sh
       (00 00 indicates midnight--0 minutes and 0 hours--and the *s mean every day of every month.
       
 (14) B
 
 (15) lsblk
 
 (16) ext3 and ext4 are both files systems that works in different ways.ext3 is a journald version of ext2 due is delay allocation technique. the
         Ext3 filesystem was efficient for small files but causes high metadata over head and poor performance when dealing with large files especially 
           while performing delete operations whick keeps a entry for every single block files, and big files have many blocks files which will led to huge mappings that will be slow to handle.
         THEN there was the need to discover knew ext file systems that could do this tasks easily which was the ext4.the ext4 was more faste r,relaible and high perfomance in the filesystems 
            which could ha handle many tasks at once.
            the main difference between ext3 and ext4 is their perfomance.with ext4 being the best of perfomance 
                two feautures of ext4 that makes it better.
                   - it is faster compar to other filesystems 
                   - its relaible and can perform many tasks at a time
                   
(17)  steps to creat a new partition.
        using the (fdisk)  command.
     - use lsblk to see the disk partition number that you have 
     - fdisk /dev/sda1
    - after this you select weather to make a primary or extended partition
    - select then use;
       - p to list the partition table
       - n to creat new partition 
       - d to delete 
       

to mount a file permanently under /data.
    - mount /dev/sda1 /mnt/data
    -note if the mount point does not exit it will not mount so you have to make a directory first(mkdir)
    
(18) the purpose The fstab (/etc/fstab) (or file systems table) file is a system configuration file on Debian systems.
The fstab file typically lists all available disks and disk partitions,
and indicates how they are to be initialized or otherwise integrated into the overall system's file system.


   
