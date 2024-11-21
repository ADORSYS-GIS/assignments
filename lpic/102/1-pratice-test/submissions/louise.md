## Part 1
1. journalctl
2. /etc/resolve.conf
3. password
4. virtualhost
5. ::1
6. -R
7. LD_LIBRARY_PATH
8. systemctl stop ssh
9. ```ip route```
10. /user/bin/crontab
    ## Part 2
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
    ## Part 3
21. 0 2 * * 5 ./backup.sh
22. |hard links   |soft links  |
    |---|--|
    |points to the inode of the file|points to the path of the file|
    |if file is deleted the link is still valid|if file is deleted link become broken|
    |link can not be created to a file that does not exit|link can still be created but it's broken|
    |```ln command``` creates hard link| ```ln -s command``` creates soft link|
 23. us ```nano``` to get into the file so you can edit it. set the ip address and netmask, save file and restart network serve
 24. ```umask 0022```
 25.    /etc/nsswitch.conf is a file that stores information about network services and user service switches. e.g shadow: files
 26. ``` sudo usermod -aG sshusers username``` then modify /etc/ssh/sshd.conf to specify group. Restart service with command ```sudo systemctl restart ssh.
 27. |iptables|ufw|
 28. |-------|----|
 29. |low level firewall manager|high level firewall manage|
 30. |not easy to use|easy to use|
