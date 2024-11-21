**part 1**

Q1 journalstl

Q2 /etc/resolve

Q3 password

Q4 Server_name D

Q5 : : 1

Q6 chmod -R

Q7 LDD_SHARELIBRARY

Q8 systemctl stop ssh.service

Q9 root

Q10 /etc/crontab

**PART 2**

Q11 C

Q12 C

Q13 C

Q14 B

Q15 C

Q16 C

Q17 B

Q18 A

Q19 B

Q20 B

**PART 3**

Q21
``crontab -e `` and add 0 2 * * 5 /path/backup.sh

Q22
|HARD LINK |SOFTLINK |
| -- | -- |
|-created using ln command | created using ln -s command |
|-deleting the original file does not affect the link | deleting the orinal file makes the link invalid|
|multiple names point to the same inode number | file point to a different inode number |

Q23

to configure eth0, use the command sudo ifconfig eth0 up/etc/network/interfaces  ```sh
auto eth0
iface eth0 inet static
    address 192.168.1.100
    netmask 255.255.255.0
    gateway 192.168.1.1
    dns-nameservers 8.8.8.8 8.8.4.4
    
Q24

   `` sudo find /home/user -type f -exec chmod 0644 ()
    sudo find /home/user -type d exec chmod 0755 ()
    ```
Q25
specifies the order of names service lookups for various database
eg ; ``hosts: files dns``

Q26 

Q27
|iptables | ufw |
| -- | -- |
|low level complex | more user friendly and high level |
|requires deep understanding of its syntax | easier to understand |
 

