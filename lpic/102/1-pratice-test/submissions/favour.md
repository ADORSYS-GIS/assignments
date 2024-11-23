1) journalctl
2) ```/etc/resolv.conf``` 
3) password
4) severName
5) ::1 
6) -R 
7) LD_LIBRARY_PATH 
8) ```systemctl stop ssh``` 
9) route
10) ```/var/spool/cron/crontabs``` 
11) B 
12) C
13) C 
14) B 
15) C
16) C

17) B

18) A

19) B

20) B

21) 0 2 * * 5 backup.sh

22) hard links : A Hard link is an exact copy of the original file, can be created for files in different files systems and deleting the original file will not affect the hard link as the content will still exist in the hard link. Example ```ln file.txt hardlink.txt```.
    
    Soft links : A soft link is a shortcut to the original file and it can be created for files in different file systems it carries a different inode from the original file and when the origal file is deleted the soft link points to nothing and will contain nothing. Example ``` Ln -s file.txt hardlink.txt```

23) auto eth
      addres 192.168.0.131
    
    gateway 192.168.0.1
    
24)sudo find /home/ubuntu -type d -exec chmod 777 '{}' \; &&  find /home/ubuntu -type f -exec chmod 644 '{}' \;
 
25) The etc/nsswitch.conf file tells the system which databases to use and in what order to resolve names. Example of line in the file ```passwd:```

26) Edit the /etc/ssh/ssh_config and add the name of the usergroup you would like to give acces to and then deny the rest of the groups

27) Iptables are used to set up, maintain, and inspect the tables of IPv4 and IPv6 packet filter rules in the Linux kernel.
    while ufw is for managing a Linux firewall and aims to provide an easy to use interface for the user.

 
