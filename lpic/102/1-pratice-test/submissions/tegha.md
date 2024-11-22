1. journalctl

2. /etc/resolve.conf

3. change for expiration date

4. allow

5. 127.0.0.0

6. -R

7. LD_LIBRARY_PATH

8. sudo systamctl stop ssh

9. route

10. /var/spool/cron

11. B

12. C

13. B

14. B

15. B

16. C

17. B

18. A

19. B

20. D

21. 0 2 * * 5 /path/to/backup.sh 

22. Hard Link: Direct reference to the inode. Cannot cross filesystems. Created using ln. Soft Link (Symbolic): Points to the file's path. Can cross filesystems. Created using ln -s.

23.

24. find /home/user -type f -exec chmod 644 {} \; -o -type d -exec chmod 755 {} \;  

25. The /etc/nsswitch.conf file configures the system's Name Service Switch (NSS). It specifies the sources for resolving various system databases, such as:

26. steps:sudo groupadd sshusers; sudo usermod -aG sshuser username;sudo nano /etc/ssh/sshd_config;AllowGroups sshusers;sudo systemctl restart sshd

27. iptables: More flexible, complex, and powerful but requires more skils.whereas UFW: Simpler, easier to configure, ideal for beginners. 
