 # Hack The Box Solution  1
 
 ### 1. Find out the machine hardware name and submit it as the answer.
 **Answer:** RUN  `uname --machine` or
 ```bash
 uname -m
 ```
 
 ### 2. What is the path to htb-student's home directory?

**Answer:** `/home/htb-student`  **RULE:** `/home/<username>`

### 3. What is the path to the htb-student's mail?

**Answer:** `/var/mail/htb-student` **RULE:** RUN `ls /var` to find `mail` directory exists then find *<username>* in the *mail* directory.
```bash
ls /var
cd /var/mail
ls -la
```

### 4. Which shell is specified for the htb-student user?

**Answer:** `/bin/bash` 

If any doubt about shell identity, RUN `grep <username> /etc/passwd` command on the shell. The last part is the shell specified.
For this user,
```bash
grep htb-student /etc/passwd
```
OUTPUT like
```
htb-student:x:1001:1001::/home/htb-student:/bin/bash
```

### 5.  Which kernel release is installed on the system? 

**Answer:** RUN  `uname --kernel-release` or
 ```bash
 uname -r
 ```
 
 ### 6. What is the name of the network interface that MTU is set to 1500?
 
 **Answer:** RUN `ip link show` or `ip a` then look for `mtu 1500` in each interface. The answer lies in between two colons(:) of the interface.
 ```bash
 ip a
 ```
 
