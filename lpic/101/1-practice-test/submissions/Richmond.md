> Part 1

1. rsyslog

2. /etc/resolv.conf

3.  password

4. /etc/apache2/conf-available

5. ::1

6. -R

7. LD-LIBARY-PATH

8. systemctl stop sshd

9. ip route , netstat -r, route

10. /var/spool/cron or /etc/crontab

> Part 2

11. B

12. C

13. C 

14. B

15. C

16. C

17. A

18. A

19. B

20. B

> Part 3

21.
` 00 02 * * */5 /path/to/backup.sh`

22.
A hard link cannot span across multiple filesystems but softlinks can .
A hardlink cannot be created for a directory whereas a softlink can.
eg of hardlink ln file.txt hlink.txt
eg of softlink ln -s dir slink

23. static ip addresses cannot be changed. the remain thesame no matter what we do.
so it cannot be configured


24. `chmod -u user 644 *`


25.
 /etc/nsswitch is used to set rules that are used in /etc/resolv.conf to 
to resolve different domain names. It is the protocol used to resolve 
different domain names.
eg hosts:          files mdns4_minimal [NOTFOUND=return] dns


26.
```
vim /etc/host.deny
ALL: ssh.hostname
ALL EXCEPT in. fingerd: .group.sshusers
```
27. 
- ufw is a firewall utility that is used to secure remote access to your computer through ports.
- iptable is used to inspect ipv4 and ipv6 tables.
