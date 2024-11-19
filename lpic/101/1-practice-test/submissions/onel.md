## ONEL'S ATTEMPT
### SECTION 1
1. A & B
2. | BIOS         | UEFI          |
   | :----------- | ------------: |
   | Supports only 4 primary partitions | Supports up to 128 partitions      |
   | can partition disk of space less than 2 TB         | can partition disk of space greater than 2 TB          |
   | uses the MBR for it's partiont table | uses GPT for it's partion table |
   | Doesn't use the extensible firmware interface           | uses an extensible firmware interface |
   | uses 32 bits | uses 128 bits|
3. The command
 ```
lsmod
```
is used to view all currently loaded kernel modules. 
* To load the module **dummy** simply use the `modprobe` command followed by the name of the module you would want to add
 that is :
  ```
  modprobe dummy
  ```
4. #### The /proc
   The /proc directory contains files with information regarding running processes and hardware resources. Some of these
files include :
*/proc/cpuinfo
*/proc/meminfo
*/proc/interrupts
 #### The /sys
  The /sys directory has the specific purpose of storing device information and kernel data related to hardware.
  These directory has some subdirectories like ;
  * /sys/firmware/
  * /sys/devices/
  * /sys/kernel/
### section 2
5. B & C
6. | apt | dpkg |
   | :---| ----:|
   |it is more user Oriented | more machine oriented|
   |cannot reconfigure | can reconfigure using the dpkg-reconfigure command |
   |install using apt-get install package | install using dpkg -i package.deb |
   |purge using apt-get remove --purge | purge using dpkg -P |
7. ```
   apt-get remove --purge package
   ```
8. 
9. B
10. ```
     grep -i error /var/log/syslog | wc -l
    ```
11. |Hardlink | Softlink|
    |:---|-------:|
    |consumes less space|consumes more space|
    |must be in thesame filesystem as the target | can be in a different filesystem from that of the target |
    |modifications in the target are also applied on the hardlink | modifications on the target file doesn't affect the softlink|
    |useful even after the target is deleted | deleting the target makes the softlink useless |
    |has thesame inode as the target | has a different inode from that of the target|
 12. ```
     sudo find /etc -iname "*.conf" -mtime 7  
     ```
13. The cron daemon is a background process that is awaken every minute to check if the is a job to execute. It helps automate commands that a repeatedly done at particular time
    .
    ```
     0 24 * * * ./backup.sh
    ```
14. B & C
15. ```
    ls -lha /dev/disk/by-uuid
    ``` 
    
16. |etx3 | ext44|
    |:----|------:|
    |supports maximum file size of 2TB|supports maximum file size of 16TB|
    |supports maximum filesystem of 16TB | supports maximum filesystem of 1EB|
17.  * Say the device was named sdb ,
     * ```
       sudo fdisk /dev/sdb
       ```
       so as to get into the fdisk interface
     * then enter `n` so as to manually start customizing the new partition
     * then choose a desired Partin number based on thee boundaries which will be provided
     * then enter the where you would want the first sector should be still respecting the boundaries
     * then enter where you would want the last sector should be or enter the size you would want for the partition
     * You can review and verify the partition by checking the partition table by entering `v`
     * then enter `t` to change the partition type
     * then choose partition type by entering it's number if you don't know it's number you can enter `l` to see all the octal numbers
     * then write and save using the command `w` and then `q`
18. The /etc/fstab file stores all mounted file systems on a linux system .
  * with this you precise the filesystem,mount point,type,options,dump,pass
19. * Power On: The system firmware (BIOS/UEFI) performs Power on self test  and initializes hardware.
    * Bootloader: The firmware loads the bootloader (grub) from the storage device's boot sector or EFI partition.
    * Kernel Loading: The bootloader locates the kernel, loads it into memory, and passes control.
    * Operating System Start: The kernel initializes the system with the help of the initramd and starts the user space, leading to the login prompt or graphical interface.


                
