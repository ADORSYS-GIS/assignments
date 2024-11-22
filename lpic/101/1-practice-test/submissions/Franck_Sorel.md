LPIC_101 Practice Test

Section 1 :System Architecture

    A. cat /proc/meminfo and B. lscpu

    Difference between BIOS(Basic input/output Sytem) and UEFI(Unified extended firmware interface) In term of boot process : the BIOS can only load the bootloader from the MBR (in the first sector of the disk) rather than the UEFI. In terms of functionnality : The UEFI(Unified extended firmware interface) has more much funcionnality than BIOS such as graphical mode.

    lsmod is the command used to list all the loaded kernel modules in the current system. And for load a new kernel modules call dummy we needs to use the modprobe command sudo modprobe dummy

    /proc : store informations about running processes
    /sys : contains information for hardware devices connected to the computer

Section 2:

    apt install package

    apt is an advance package manager with more features for handle packages
    dpkg is for debian package tools

    sudo dpkg -r $(sudo dpkg -S orphaned | awk {$1})

    We should use the command : yum-config-manager --add-repo http://repo.example.com

Section 3 :

    A. head

    cat /var/log/syslog | grep "error" | wc -l

    hard link : point to the inode of the file command : ln </path/to/thefile> soft link : point to a link. command : ln -s <path/to/thefile>

    find /etc -type f -name .*.conf

    cron is use to schedule a task in linux 0 * * * * /path/to/thefile

Section 4

    B. Disk usage in humand readable format

    The command blkid for display UUID of all the mounted file system

The difference between ext3 and ext4 file system is that, the ext4 the upgradable version of ext3, means that it has more features likes, the maximum file size is 16TB for ext4 and for ext3 is 2TB, the highest limit of subdirectory is 64 000 for ext4 and 32 000 for the other one.

17.fdik

    The /etc/fstab store information about how filessystems are mounted and accessed. That's an example : /dev/sda1 /media/franck/usb.key vfat rw,uid=franck,gid=franck 0 0

Bonus Question :

Boot process in linux :

X user press the power on button of the computer, and it's the beginning of different process: The firmware (BIOS or UEFI) begin by testting all the hardware component of the machine to verify integrity of them. If all it's good, the firmware load the bootloader GRUB. Depending of the installation, it can be GRUB Legacy or GRUB2 (widely-used in our days). The roles of bootloader is to load the kernel and it use a set of argument : the cmdline. And after that, the kernel, which is the basic component of each OS ensure the hardware communication with the OS itself. It contains a certains amount of modules it manage running processes, and it main purpose it to manage hardware devices and load the OS itself. (It does not means that the kernel is not a part of OS) And and the end system initialization take place and finalize the process and the login page is display on the screnn allows user to have acces to software in OS.
