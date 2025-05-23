# Hack The Box Solution 5

### 1.  How many files exist on the system that have the ".log" file extension?
**Answer:**  RUN `find / -name *.log` command
```bash
find / -name *.log 2>/dev/null | wc -l
```

### 2. How many total packages are installed on the target system?
**Answer:**  To find all Debian packages RUN `dpkg -l` command in irrespective of **Kali** or **Ubuntu**. Installed packages will start with ***ii*** string
```bash
dpkg -l | grep "^ii" | wc -l
```
