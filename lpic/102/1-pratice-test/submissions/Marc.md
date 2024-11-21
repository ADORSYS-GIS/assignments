## part1

1 - ***logger*** command.

2 - /etc/resolve.conf

3 password aging

4 Allow

5 ::1

6 -R option

7 LD_LIBRARY_PATH

8 sudo systemctl stop ssh

9 ***route*** command

10 /var/spool/cron/crontab

## part2

11 B

12 C

13 C

14 B

15 C

16 B

17 B

18 A

19 B

20 B

## part3

21 To schedule a job that runs backup.sh every Friday at 2 AM using crontab we first run the ***crontab -e*** command , then we add the : 0 2 * * 5 /path/to/backup.sh

22 Hard Links: Directly reference the inode of a file, making it the exact copy of the original file. Deleting the original file does not remove the hard link.
 example , ln /path/to/original /path/to/hardlink . While Soft Links (Symbolic Links): Point to the file path not the inode ,they break if the original file is moved or deleted.
 example , ln -s /path/to/original /path/to/symlink . 

23  auto eth0
iface eth0 inet static
    address 192.168.64.6
    netmask 255.255.255.0
    gateway 192.168.64.1
    dns-nameservers 8.8.8.8 8.8.4.4





24 To restore permissions in /home/user to 644 for files and 755 for directories 
find /home/user -type f -exec chmod 644  
find /home/user -type d -exec chmod 755 

24


25 Purpose of /etc/nsswitch.conf , this  file controls how various databases are searched. It specifies the order of sources such as files, dns, ldap.
Example line in file ;  hosts: files dns
the example configures the system to check /etc/hosts first, then use dns for hostname resolution.

26   Secure an SSH server to allow only users in the sshusers group  , Firstly

 Create the group if it does not  exist using : sudo groupadd sshusers
 
Then add users to the sshusers group :
sudo usermod -aG sshusers username1
sudo usermod -aG sshusers username2

After creating Users ,restrict the SSH access in the SSH configuration file , this is done by : sudo nano /etc/ssh/sshd_config

then add the line: AllowGroups sshusers

then restart the SSH service for it to work which is done using : sudo systemctl restart ssh



27 Key differences between iptables and ufw:


•	iptables: A powerful, low-level tool for configuring firewall rules , this  requires more manual configuration and is better for advanced users.

•	ufw: A user-friendly frontend for managing iptables rules. It simplifies tasks like allowing or blocking ports and is mostly used by less experienced users.
Example:




























