### PART 1
1. journalctl
2. /etc/resolv.conf
3. password
4. Virtualhost
5. 00:00:00:00:00:00
6. -R
7. PATH
8. sudo systemctl stop sshd
9. route
10. /var/spool/cron/contabs
### PART 2
11. B
12. C
13. C
14. B
15. C
16. B
17. B
18. A
19. B
20. B
### PART 3
21. 0 2 * * 5 backup.sh
  
22. |Hard links|Soft links|
    |----------|----------|
    |They point to the file itself|They point to the path of the file|
    |The can not span across filesystems|They can span across filrsystems|
    |They occupy more diskspace|They occupy less diskspace|
    |They have the same inode as the file they are point to|They have an inode different from that of the file they are point to|
    |They can be created using the command `ln`|They can be created using the command `ln -s`|
23. \# Primary network interface

    
    auto eth0 inet static
    
    address 192.168.1.152
    
    netmask 255.255.255.0
    
    gateway 192.168.1.1
    
    dns-nameservers 8.8.8.8
    
25. find /home/user -type f | xargs chmod 644 ; find /home/user -type d | xargs chmod 755
26. The file /etc/nsswitch.conf defines rules used to resolve database names. An example of a line in the file is
    `hosts:          files mdns4_minimal [NOTFOUND=return] dns`
27. chgrp sshusers login
28. Iptables are administration  tools  for IPv4/IPv6 packet filtering and NAT while ufw is a tool for managing a Linux firewall and aims to provide an easy to use interface for the user.
