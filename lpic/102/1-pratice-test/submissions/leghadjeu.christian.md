Part 1.
1. Answer= journalctl
2.
3. Answer= Aging
4. Anwer=
5.
6. Answer= -R
7. Answer= LD_LIBRARY_PATH
8. Answer= systemctl stop ssh.service
9.
10. Answer= /etc/crontab
Part 2.
11. Answer= B. ip link set eth0 up
12. Answer=D. Configure default gateway settings.
13.  Answer= C. Sets default permissions for new files to 644
14.  Answer=B. dig
15.  Answer= C. /etc/group
16.  nswer= B. Deletes all rules in all chains.
17.  Answer= B. Sets up passwordless SSH login by copying the public key to the target server.
18. Answer= A. quota
19. Answer= B. Sets a variable for child processes.
20. Answer= B. systemctl set-default
Part 3.

21. To schedule a job using the crontab command, we enter the following line in the file that pops after enterring the `crontab -e` command and ensuring that the backup.sh file is exectutable;
     ```
     0 2 * * 5 <path to directory>/backup.sh
    ```
22.
| hard links | soft links |
| -- | -- |
| They cannot point to files on different filesystems |  They can point to files on different filesystems without been broken |
| They have the same inodes as their target files | they have different inodes as their target files  |

23.
24. To change the permissions of the all files to 644 and directories to  755 we can execute;
```
find /home/user -type f -exec chmod 644 '{}' \; && find /home/user -type d -exec chmod 755 '{}' \;
```
