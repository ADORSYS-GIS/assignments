LPIC-102 Practice Test
1.logger

2./etc/named.conf

3.password aging

4.ServerName

5.::1

6. -R

7.LD_LIBRARY_PATH

8.sudo systemclt stop ssh

9. route

10.var/spool/cron/crontabs



Part2: 

11. ip link set eth0 up

12. Define access control rules for daemons using TCP Wrappers

13.set default permissions for new files to 644

14.dig

15./etc/group

16. Flushes NAT table entries only

17. B. Setes up passewordless SSH login by by copying the public key to the target server 

18. A.quota

19. B.Sets a variable for child processes

20. B.systemctl set-default



Part 3: 

21. * 2 * 5 * /backup.sh

22. hard link point to the inode of the file rather than a soft link which point to the path 

23. step 1: sudo touch /etc/network/interfaces
step 2: input the configuration inside 
auto eth0
iface eth0 inet static
    address 192.168.1.100
    netmask 255.255.255.0
    gateway 192.168.1.1
    dns-nameservers 8.8.8.8 1.1.1.1
    
    24.sudo find /home/user -type f -exec chmod 644 {} \; sudo find /home/user -type d -exec chmod 755 {} \;
    
    25. /etc/nsswitch.conf is a configuration file that specifies the order used by the NSS (Name Service Switch)
    
    26. step 1 : sudo groupadd sshusers
    step 2 : used sudo nano /etc/ssh/sshd_config
    add those line insides : AllowGroups sshusers AND DenyGroups *
    step 3 restart the service : sudo systemctl restart sshd

27.iptables is a low-level, command-line for configuring iptables, while ufw is more user-friendlly for firewall rules management
