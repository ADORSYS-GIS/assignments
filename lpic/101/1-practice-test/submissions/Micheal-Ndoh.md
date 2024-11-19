1= lscpu**(B)**

2= **BIOS** in terms of boot process uses the `Master Boot Record(MBR)` as it's Bootloader while **UEFI(unified extensible firmware interface)** uses the `Grub(Grand unified bootloader)` or grub2 as it's bootloader and and  the maximum number of partitions on a BIOS system is `4` while in UEFI is `128`. The UEFI offers a more faster and secured booting interface with new improved configurable features on the boot menu than the BIOS. The BIOS uses the `SYS V(5) init` to manage it's processes and services while the UEFI uses `systemd`

3= Use the `lsmod` command to list all modules loaded on your linux system. To load a new kernel either you use the **insmod** `(loads the kernel but without its dependencies)` or *modprobe* `(proferable because it loads both the kernel and its dependencies). using modprobe to load dummy : sudo modprobe dummy

4= /proc holds the running processes and programs of a system while /sys holds add-on applications files and configurations

5=apt install package **(C)**

6= apt is a more advanced high level package manager that has the ability of searching the internet scanning through repositories to install a specific package and is more human friendly.
dpkg is a low level package manager which is more system friendly that it communicates faster and directly with the computer system.

