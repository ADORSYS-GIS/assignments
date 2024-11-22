1. B
   
2. The difference between bios and uefi is that bios is an older firmware and uses the MBR boot partioninng scheme whereas uefi is a more modern firware and uses the GUID Partioning Table allow for faster boot compared to the bios

3. command: modeprobe  use: sudo modeprobe dummy

4. /proc and /sys are all pseudofilesystem that use virtualisation to represent process./proc is use to represent running process used by the kernel while the /sys is use to represent kernel parameters and hardware devices use by our system.

5. C

6. The main difference is that apt is an advanced package manager and is more user friendly compared to dpkg.

7. sudo apt-get remove orphan_package               

8. to configure a flie using yum edit the file /etc/yum.repos.d/file.repo using nanno and use yum repolist to view changes

9. B 

10. cat /etc/log/syslog | nl

11. A hard link is file that points to a specific inode as the original file and has the  following  chacteristic: same checksum value, cannot span multiple filesytem, and whose content is preserved even if the original file get deleted. on the otherhad a softlink also called symlink is a file that points to another file and not the original file. ti has characteristis like: span across multiple filesystem and is content is deleted if the file is pointing to get deleted

12. find /etc -name "*.conf" -mtime -7

13. A cron daemon allows us to schedule jobs to be executed at specific times. for example an : 00 12 * * * backup.sh 

14. B

15. sudo blkid

16. ext3: oldder tha ext4 , add more journaling to the ext2 while
 ext4: default linux fillesystem, allows data intergrety on filesystem

17. partion creation: fdisk /dev/sda this will lead to where you will be provided with some menu like n to create your partion format partion : mkfs.ext4 /dev/sda : mount partion first make dir, mnt /data and then mount now mnt /dev/sda
