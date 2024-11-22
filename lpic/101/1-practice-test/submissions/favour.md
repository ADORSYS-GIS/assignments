1) B
2) BIOS : - makes use of MBR and a /boot partion
          - doesn't have secure boot 
          - supports a maximum of 2TB storage 
   submissions
           
   UEFI : - makes use of GPT and an efi system partition
          - Has secure boot 
          - supports more than 2TB storage 
3) ```lsmod```
   ``` modprobe dummy ```

4) /proc: contains information about the hardware devices generated while the sytem is running and kernel messages.  
   /sys: contains kernerl libraries and kernel files.

   
5) C  
6)Differnces between apt and dpkg
apt: advanced package mangement tool
     which is user friendly
     apt allows resolving of package  dependencies automatically and it downloads from the remote repositories and local files
dpkg : low level package management tool
       none user friendly
       dpkg does not allow resolving of package dependencies automatically and it downloads packages from local files

 7) apt-get full upgrade
    apt-get dist-upgrade   

9)  B

10) cat /var/log/syslog | grep error|  wc -l

11) Hard Links : A hard link is an exact copy of the source file changes made in the source file take effect on the hard link.
    A hard link has the same inode as the source file.
    It can be created only for files in thesame filesystem.
    If the source file is deleted the hard link will still exist with all the contents of the source file .
    It is created with the command ``` ln <sourcefile> <hardlink>```

    soft links : A soft link is a short cut to the original file once the file is deleted the soft link points to nothing. soft links also link to directories and can be created for files across different file sytems.
    command ```ln -s <sourcefile> <hardlink>```
 
  12) ```find /etc -type f -name "*.conf*" ntime -7```
  
  13) The cron daemon is background process used to execute scheduled tasks    
      ```0 0 * * * backup.sh``` 

 14)  B
 15) ```blkid``` 
     ``` ls -lha /dev/disk/by-uuid```
 16)  ext3 : Older file system supports files up to 2TB. 
     supports 32bits format
       ext4 : it is a 64bits format newer which supports files larger than 2TB with increased reliablity more reliable.
      supports really large filesytem volumes and is a feature of newer versions of linux operating systems.
17) ```mkfs -t <type of filesystem> <device> size```
18) /etc/fstab file displays detailed file system information,mount points, the filesystem type and uuids.

  

19) The BIOS does a Power-On-Self-test checks the state of the hard components
    The bootloader then loads the kernel to memory
    The kernel takes over the operating system boot process and runs  the initialisation scripts which then starts the other programs and interfaces. 




      
     

   
