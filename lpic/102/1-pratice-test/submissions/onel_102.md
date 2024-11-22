### PART 1
1. journalctl
2. /etc/resolve.conf
3. password
4. ServerName directive
5. 00:00:00:00:00:00
6. -R
7. LD_LIBRARY_PATH
8. systemctl stop ssh.service
9. route 
10. /etc/crontab

 ### PART2
11. B
12. C
13. C
14. B
15. C
16. C
17. B
18. A
19. B
20. B
### PART3
21. 0 2 * *  ./backup.sh
 22. |hardlink | softlink |
     |:-----| ------: |
     | Can only be used in thesame filesystem as the target|Can be used across different filesystems |
     | Direct reference to the Inode | points to the file's path |
     | created ln -s | ln |
23. ```
    auto eth0
    iface eth0 inet static
        address 192.168.0.100
        netmask 255.255.255.0
        gateway 192.168.1.1
         dns-nameservers 8.8.8.8   8.8.4.4 
24. ```
     sudo find /home/user -type f -exec chmod 0644 () \ ; sudo find /home/user/ -type -d -exec chmod 0755 () \
    ```
25. Regarding the name of the remote network nodes, there are two basic ways the operating system
can implement to match names and IP numbers i.e to use a local source or to use a remote server to
translate names into IP numbers and vice versa. The methods can be complementary to each
other and their priority order is defined in the Name Service Switch configuration file i.e /etc/nsswitch.conf
```

passwd:         files systemd
group:          files systemd
shadow:         files
gshadow:        files

```
26. create a file /etc/hosts.allow and add
  ```
    sshd: ALL
  ```
and the configure an exception in the file /etc/hosts.allow for SSH connections from the
sshusers' network
sshd: sshusers
The changes take effect immediately, there is no need to restart any service. 
27. * ufw :  This  program  is  for managing a Linux firewall and aims to provide an
       easy to use interface for the user
    * iptables : Iptables and ip6tables are used to set up, maintain,  and  inspect  the
       tables  of IPv4 and IPv6 packet filter rules in the Linux kernel
