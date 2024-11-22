## Part 1: Fill in the Blank
1) journalctl
2) /etc/resolve.conf
3) age
4) httpd.conf
5) hexadecimal values
6) -R
7) LD_LIBRARY_PATH
8) systemctl stop ssh
9) netstat -r
10) /etc/crontab

## Part 2: Multiple Choice Questions
11) B
12) C
13) C
14) B
15) C
16) C
17) B
18) A
19) B
20) B

## Part 3: Practical and Short Answer Questions 
21) ```sh
    -> ~ sudo vi /etc/crontab
    00 02 * * 4 /path/to/backup.sh
    ```
22) |Hard links    | Soft links       |
    |-------------------|------------------------|
    |It is a *reference* to the inode of the original file.|It is a *pointer* to the path to the file. |
    |It shares the same inode as the original file.|It does not share the same inode as the original file |
    |It can't me made for directories or across several file systems.|It can be made for directories and across several file systems.|

23) Configuring a static IP address on a network interface `eth0`:
     ```sh
        -> ~ sudo ifconfig eth0 192.168.5.1 netmask 255.255.255.0
     ```
24) ```sh
        -> chmod -R 755 path/to/directory
    ```
25) The `/etc/nsswitch` is a configuration file that is used to configure which services are to be used to determine information such as hostnames, passowrd files, and group files.
    **Example**:
     ```sh
      passwd:      files systemd
     ```
26) ```sh
        -> ~ chmod g+s sshusers/
    ```
27) `ufw` is more simple to use, and writes its iptables rules in the *background*. While, `iptables` are the low-level kernel technology which implements *firewall rules*.
     
