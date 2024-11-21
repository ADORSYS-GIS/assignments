1. `journalctl`
2. /etc/resolve.conf
3. password
4. ServerName Directive
5. 00:00:00:00:00:00
6. R
7. LDD_LIBARY_PATH
8. `systemctl stop sshd.service`
9. route
10. /etc/crontab
11. C
12. A
13. C
14. B
15. C
16. C
17. B
18. A
19. B
20. B
21. 0 2 * * 5 ./backu.sh
22.
- Hard Link Direct reference to the inode while Soft Link Points to the file's path.
23.
 eth0
- iface eth0 inet static
- address 192.168.1.100
- netmask 255.255.255.0
- gateway 192.168.1.1
- dns-nameservers 8.8.8.8 8.8.4.4
24. `sudo find /home/user -type f -exec chmod 0644 && sudo find /home/user -type d -exec chmod 0755`
25. to determine the order and sources of name service lookups for various databases and services.
26.
- add all the users to the group
`sudo usermod -aG sshusers usersname`
- edit SSH service to allow access to the users in the ssh group /etc/ssh/sshd_config\
add this line **AllowGroups sshusers** to
`sudo nano /etc/ssh/sshd_config`
- restart the SSH service to update
`sudo systemctl restart sshd`
27. iptables has more features while ufw has less features for trouble shooting.
