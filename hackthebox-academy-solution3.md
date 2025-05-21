# Hack The Box Solution 3

### 1. What is the name of the last modified file in the "/var/backups" directory?
**Answer:**  RUN `ls -t` command which prints files and folders time-wise (last modified file first)
```bash
cd /var/backups
ls -t | head -n 1
```


### 2. What is the inode number of the "shadow.bak" file in the "/var/backups" directory?
**Answer:** Index number is also known as `inode number`. To find out it RUN `ls -i` command.
Here for solution
```bash
# We already set location to `/var/backups` during solving the previous question
ls -i shadow.bak
```
