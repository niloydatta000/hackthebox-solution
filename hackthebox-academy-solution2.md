# Hack The Box Solution 2

### 1. What is the name of the hidden "history" file in the htb-user's home directory?
**Answer:**  RUN `ls --all` command or
```bash
ls -a
```
and find the hiddden file that contains "history" on filename.

### 2. What is the index number of the "sudoers" file in the "/etc" directory?
**Answer:** Index number is also known as `inode number`. To find out it RUN `ls -i` command.
Here for solution
```bash
ls /etc -i sudoers
```
