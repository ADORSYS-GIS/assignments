## Part 1: Fill in the Blank (20 Marks)

The ___  logger_______ command is used to query and manage the syslog facility. 

To set up a DNS resolver, the file ___    /etc/resolv.conf__________ is used to configure the nameservers. 

The chage command is used to manage ___  _password_________ policies for user accounts.

In Apache's configuration file, the directive to allow a specific domain is _____________. 

The IPv6 loopback address is represented as _____  ::1________. 

To apply file permissions recursively in one command, you would use the ______-R_______ option with the chmod command. 

The environment variable   ___LB_LIBRARY_PATH_________ specifies the location of shared library files on Linux. 

The command to stop the SSH service on a systemd-based Linux distribution is _____sudo service ssh stop________. 

The ____route_________ command is used to display and manipulate the kernel routing table.

The default location of the crontab files for all users is ________/var/spool/cron____.

## Part 2: Multiple Choice Questions (30 Marks)

11.   B. ip link set eth0 up
  
12.  C. Define access control rules for daemons using TCP Wrappers.
      
13.  B. Sets default permissions for new files to 755.
    
14.  B. dig

15.C. /etc/group
      
16.  B. Deletes all rules in all chains.

17.   B. Sets up passwordless SSH login by copying the public key to the target server.
    
18.  A. quota
   
19. B. Sets a variable for child processes
    
20.   B. systemctl set-default
    
    

## Part 3: Practical and Short Answer Questions (50 Marks)

  21.  Write the command to schedule a job that runs a script named backup.sh every Friday at 2 AM using crontab. 

    ```sh
    crontab -e
    0 2 * * fri <job to be run>
    ```


22.    Explain the difference between hard links and soft links. Provide an example command to create each. 
    - a hard link points to the inode of the file 
   and if the original file is deleted it doesn't affect the hard link until it is deleted itself 
   and also a hard link can only be used within the same filesystem.
```sh
ln original_file hard_link
```
   - a soft link points to the file path making it more flexible accrss different filesystems 
    but if the original file is deleted the soft link become useless.
  ```sh
     ln original_file  soft_link
```

  23. Configure a static IP address on a network interface eth0 in a Debian-based system. Write the configuration that would go in the /etc/network/interfaces file. 
    - **ifconfig** to have the ip address infos
    ```sh
    - sudo nano /etc/network/interfaces
    ```
    in this file write:
    eth0
    inet 192.168.0.167 
     netmask 255.255.255.0 
      broadcast 192.168.0.255
      
   24.  A user accidentally changed the permissions of all files in /home/user to 000. Write a command to recursively restore the permissions to 644 for files and 755 for directories. 

    ```sh
    sudo find parent/ -type d | xargs sudo  chmod -R 755
    sudo find parent/ -type f | xargs sudo  chmod -R 644
    ```

   25. Explain the purpose of /etc/nsswitch.conf. Include an example of a line in the file. 
    - it helps the system to find information when you want to log in or about your network.

  26. Write a sequence of commands to secure an SSH server so that only users in the sshusers group can log in.
    ```sh
    sudo nano /etc/ssh/ssh_config
    ```
    edit this file as follows:
    - Permitlogin no
    - PermitGrouplogin yes



   27. [Short Answer]
    What are the key differences between iptables and ufw? 
    - ufw is a program for managing a netfilter firewall and aims to provide an easy to use interface for the user.
    - iptables:  are used to set up, maintain, and inspect the tables of IPv4 and IPv6 packet filter rules in the Linux kernel.

