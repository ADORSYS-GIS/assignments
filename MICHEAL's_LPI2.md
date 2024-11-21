## PART 1

1=journalctl

2=

3=passwd 

4=

5=

6= -R

7=LD_LIBRARY_PATH

8=systemctl stop ssh 

9=traceroute

10=/etc/crontab
 ## PART 2
 
11=B

12=C

13=C

14=B

15=C

16= C
 
17=B

18=A

19=B

20=D

## Practical

21= * 2 5 * * ./backup

### 22=
**Hardlinks**
Hardlinks are links that have thesame inodes and any modification on one applies to the other
Hardlinks are created using the following commands
Hardlinks can not be accessed across different filesystems 
```shell
ln <nameofname>
```
Or with the cp command using the -l flag
```shell
cp -l 
```
**Softlink**
- Softlinks are pointers to a file or a directory
- Softlinks can be access accross different filesystems
- When the target file is deleted the softlinks can not able to access the file's  data anymore
- To create a softlink use the ln command with the -s flag 
```shell
ln -s <nameoffile>
```
25= It holds the configurations of the name service switch
e.g hosts: files

27=
