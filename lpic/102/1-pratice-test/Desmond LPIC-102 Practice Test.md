# LPIC-102 Practice Test

### Part 1: Fill in the Blank

1. jouirnalctl
2. /etc/resolve.conf
3. password
4. /etc/hosts.allow
5. ::1/128
6. -R
7. LD_PATH
8. systemctl stop ssh.service
9. ip route
10. /var/spool/cron
***

11. B. ip link set eth0 up
12. C. Define access control rules for daemons using TCP Wrappers.
13. C. Sets default permissions for new files to 644.
14. B. dig
15. C. /etc/group
16. D. Disables IP forwarding.
17. B. Sets up passwordless SSH login by copying the public key to the target server.
18. A. quota
19. B. Sets a variable for child processes.
20. B. systemctl set-default

***

### Part 3: Practical and Short Answer Questions
21. 0  2  *  *  5  ./backup.sh
22. | hardlinks | softlinks |
    |-----------|-----------|
    | points to the same data as the actual file | points to a path pointing to the original file |
    | have the same inode as the original file | inode differs from the original file |
    | created with `ln <target-file> <hardlink-name>` | created by `ln -s <target-file> <softlink-name>` |
23. ```bash
    ip link set 198.162.0.1 dev eth0
    ```
24. ```bash
    chmod -R 755 /home/user ;; find /home/user -type f exec chmod 655 {} \;
    ```
25. /etc/nsswitch.conf is a file that describes the set of rules and order the system follows while resolving names for services like dns services
    example of a line is  `passwd:         files systemd`
27. 
    
28. 
