## Sample answer
### Sectioin 1: System Architecture
1) B
2) BIOS(Basic Input and Output System): makes use of the MBR partitioning scheme. It is slow in terms of booting.Bios disk support is up to2TB.In terms of extensibility, it is difficult to update or extend.

UEFI(Unified Extensible Firmware Interface): makes use of the GPT partitioning scheme.It is faster as compared to the BIOS. It has a disk size support of  over 2TB. It reads it's entries from the NVRAM that points to pre-defined EFI applications in ESP. Here the pre-defined EFI apps are bootloaders,OS sectors, tools for system diagnostics and repair etc. UEFI can be easily updated or extended.

3) ```sh
   -> ~ lsmod
   -> ~ modprobe dummy
   ```
4) `/proc`: a pseudo filesystem that provides real-time data about the syste's processes and hardware, the data being read directly from the kernel.
  `/sys`: stores data about system devices.

### Section 2: Linux Installation and Package Management
5) C
6) `apt`: It's a high level  package manager with automatic dependency resolution.If the repository of a given package is not found in the *source.lst* ,  `apt` goes further looking for it.
   `dpkg`: It's a low level  package manager with manaul dependency resolution. If the repository(or the link to the repository) is not found in the *source.lst*, `dpkg` does not go urther looking for it online.
7) ```sh
   -> ~ sudo apt-get autoremove
   -> ~ sudo apt-get purge
   ```
8)The conifiguration file for `yum` and related utils are located in `/etc/yum.conf`.

### Section 3: GNU and Unix Commands
9) A
10) ```sh
    -> ~ cat /var/log/syslog | grep error | wc -l
    ```
    OR
    ```sh
    -> ~ cat /var/og/syslog | grep -c error
    ```
11) `Hard links`: It is a direct *reference* to the **inode** of the original file. Here the original file and link have the same inode. If changes are made on either of them, the changes are reflected on each.Hard links can't be made across different many filesystems. Hard links can't be made on directories.
To create a `hard link`, do:
```sh
-> ~ ln (original file) (hard link)
```
`Soft links`: It is a *pointer* to the path of a file rather than the file itself. They do not share the same *inode* as the original file. This feature makes it possible for `soft links` to be used across several file systems or to directories.
 To make a `soft link`, do:
```sh
-> ~ ln -s (original file) (soft link)
```
12) ```sh
    -> ~ find /etc -mtime 7 *.conf
    ```
13) A `cron` daemon is a daemon for scheduling jobs for it to be executed at a particular time.
    ```sh
    00 00 * * * backup.sh
    ```

### Section 4: Devices, Filesystems, and FHS
14) B
15) ```sh
    -> ~ blkid
    ```
16) `ext3`: Has journaling. The maximum file size is **2TB**. The maximum file system size is **16TB**.
    `ext4`: Mostly used, with maximum file size **16TB** and maximum file system size **1EB**.
17) For partitioning, you can use `fdisk` for MBR and `gdisk` for GPT.
    ```sh
    -> ~ gdisk /dev/sdb
    -> ~ mkfs -t ext4 /dev/sdb
    -> ~ mount -t ext4 -o remount,ro /dev/sdb /data
    ```
18) `etc/fstab`: shows what file system should be mounted on which directory.
   **Example**:
    ```sh
    -> ~ mount -t ext4 -o remount,ro /dev/sda /mnt
    ```
    ### Bonus
    
  - After the POST, the BIOS activates basic components to load the system. It also checks on the hardware components for any failure as soon as the machine is powered on.
  - BIOS loads the bootstrap(1st stage of the bootloader) and bootstrap loads the second stage of the bootloader responsible for presenting boot options and loading the kernel.
  - GRUB(the bootloader), localises the kernel in the storage and loads it into memory.
  - The kernel calls on the initramfs in order to have access to root file system.
  - As soon as the root file system is available, the kernel mounts all file systems configured in the `/etc/fstab` file and will execute the 1st program, a utility(`init`; that's responsible for starting system processes, managing services and providing a framework for booting the OS).
  - Once the `init` is loaded, `initramfs` is removed from RAM.
  - The system is initialized , user space is started, leading to the login prompt or graphical interface.
     
