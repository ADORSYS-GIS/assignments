### **LPIC-102 Practice Test**  
This test simulates the **LPIC-102** exam structure and difficulty level. The LPIC-102 exam tests skills related to advanced Linux administration, including networking, security, and system maintenance.  

**Time Allowed**: 90 minutes  
**Maximum Marks**: 100  
**Passing Marks**: 60  

---

### **Part 1: Fill in the Blank** *(20 Marks)*  

1. The **journalctl** command is used to query and manage the `syslog` facility. *(2 Marks)*  

2. To set up a DNS resolver, the file **/etc/resolve.conf** is used to configure the nameservers. *(2 Marks)*  

3. The `chage` command is used to manage **password** policies for user accounts. *(2 Marks)*  

4. In Apache's configuration file, the directive to allow a specific domain is **Allow** *(2 Marks)*  

5. The IPv6 loopback address is represented as **::1**. *(2 Marks)*  

6. To apply file permissions recursively in one command, you would use the **-R** option with the `chmod` command. *(2 Marks)*  

7. The environment variable **LD_LIBRARY_PATH** specifies the location of shared library files on Linux. *(2 Marks)*  

8. The command to stop the SSH service on a systemd-based Linux distribution is **sudo systemctl stop ssd**. *(2 Marks)*  

9. The **route** command is used to display and manipulate the kernel routing table. *(2 Marks)*  

10. The default location of the crontab files for all users is **/etc/crontab**. *(2 Marks)*  

---

### **Part 2: Multiple Choice Questions** *(30 Marks)*  

11. Which of the following commands enables a network interface? *(3 Marks)*  
    A. `ifconfig eth0 down`  
    B. `ip link set eth0 up`  
    C. `systemctl start network`  
    D. `service eth0 up`  

C

12. What is the purpose of the `/etc/hosts.allow` file? *(3 Marks)*  
    A. Define IP routing rules.  
    B. Configure IP masquerading.  
    C. Define access control rules for daemons using TCP Wrappers.  
    D. Configure default gateway settings.  

C

13. What does the `umask 022` command accomplish? *(3 Marks)*  
    A. Sets permissions to `777` for new files.  
    B. Sets default permissions for new files to `755`.  
    C. Sets default permissions for new files to `644`.  
    D. Blocks access to all users.  

B

14. Which of the following commands can be used to troubleshoot DNS issues? *(3 Marks)*  
    A. `ping`  
    B. `dig`  
    C. `traceroute`  
    D. `ls`  

B

15. Which file contains information about all available groups on the system? *(3 Marks)*  
    A. `/etc/shadow`  
    B. `/etc/passwd`  
    C. `/etc/group`  
    D. `/etc/gshadow`  

C

16. What does the `iptables -F` command do? *(3 Marks)*  
    A. Blocks all incoming traffic.  
    B. Deletes all rules in all chains.  
    C. Flushes NAT table entries only.  
    D. Disables IP forwarding.
 
 C    

18. What does the command `ssh-copy-id` do? *(3 Marks)*  
    A. Copies the SSH service configuration.  
    B. Sets up passwordless SSH login by copying the public key to the target server.  
    C. Transfers files using SSH.  
    D. Starts the SSH service.  

B

19. Which command is used to check disk quotas for a user? *(3 Marks)*  
    A. `quota`  
    B. `df`  
    C. `du`  
    D. `mount`  

A

20. What does the `export` command do in a shell? *(3 Marks)*  
    A. Deletes a shell variable.  
    B. Sets a variable for child processes.  
    C. Shows running processes.  
    D. Sets the default shell.
 B   

21. Which of the following commands will change the default runlevel in a systemd-based Linux distribution? *(3 Marks)*  
    A. `init`  
    B. `systemctl set-default`  
    C. `runlevel`  
    D. `telinit`  

B
---

### **Part 3: Practical and Short Answer Questions** *(50 Marks)*  

21. **[Practical]**  
    Write the command to schedule a job that runs a script named `backup.sh` every Friday at 2 AM using `crontab`. *(5 Marks)*  
  - 0 2 * * 5 /path/to/backup.sh
      
22. **[Short Answer]**  
    Explain the difference between `hard links` and `soft links`. Provide an example command to create each. *(5 Marks)*  
   - Hard Link: Direct reference to the inode. Cannot cross filesystems. Created using ln.
   - Soft Link (Symbolic): Points to the file's path. Can cross filesystems. Created using ln -s
     
23. **[Practical]**  
    Configure a static IP address on a network interface `eth0` in a Debian-based system. Write the configuration that would go in the `/etc/network/interfaces` file. *(10 Marks)*  

  auto eth0
iface eth0 inet static
    address 192.168.1.100
    netmask 255.255.255.0
    gateway 192.168.1.1
    dns-nameservers 8.8.8.8 8.8.4.4

25. **[Practical]**  
    A user accidentally changed the permissions of all files in `/home/user` to `000`. Write a command to recursively restore the permissions to `644` for files and `755` for directories. *(5 Marks)*  
   - sudo find /home/user -type f -exec chmod 0644 {}; sudo find /home/user -type d -exec chmod 0755 {};
     
25. **[Short Answer]**  
    Explain the purpose of `/etc/nsswitch.conf`. Include an example of a line in the file. *(5 Marks)*  
   -  to determine the sources from which to obtain name-service information in a range of categories, and in an order such as hostname and user authentification

26. **[Practical]**  
    Write a sequence of commands to secure an SSH server so that only users in the `sshusers` group can log in. *(10 Marks)*  
- add all the users to the group
`sudo usermod -aG sshusers usersname`
- edit SSH service to allow access to the users in the ssh group /etc/ssh/sshd_config\
add this line **AllowGroups sshusers** to
`sudo nano /etc/ssh/sshd_config`
- restart the SSH service to update
`sudo systemctl restart sshd`
     
27. **[Short Answer]**  
    What are the key differences between `iptables` and `ufw`? *(5 Marks)*
    - ufw is just a frontend for iptables to make it easier to manage. If you create your rules with ufw, you will see them when you run iptables -L -n -v.
    - iptables gives you more flexibility, but it's also slightly more complicated to configure 

---
