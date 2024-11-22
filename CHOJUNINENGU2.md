- 1: journalctl
- 2: /etc/resolv.conf
- 3: password expiration
- 4: ___________________________
- 5: ::1 .
- 6 :-R
- 7: LD_LIBRARY_PATH
- 8: systemctl stop ssh
- 9: route
- 10: /var/spool/cron/crontabs
# part two
- 11 B 
- 12 C
- 13 C
- 14 B
- 15 C
- 16 B 
- 17 B
- 18 A
- 19 B
- 20 B
# Part 3
- 21 : 0 2 * * 5 /path/to/backup.sh
- 22 :
  
| hardlinks | softlinks |
|------------|-----------|
| These are direct references to the same inode on the filesystem | These are shortcuts that point to the original file path.
| If the original file is deleted,it has no effect on the hardlink |  If the original file is deleted, the soft link becomes broken |
 | ln a.txt b.txt | ln -s a.txt c.txt |

- 23 : ____________________________________________________

- 24 : 
* find /home/user -type f -exec chmod 644
* find /home/user -type d -exec chmod 755


- 25 : _____________________________________

- 26 : _____________________________________
- 27 : _____________________________________________
