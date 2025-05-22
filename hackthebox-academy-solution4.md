# Hack The Box Solution  4

### 1. What is the name of the config file that has been created after 2020-03-03 and is smaller than 28k but larger than 25k?
**Answer:** RUN  `find` command
```bash
 find / -type f -name *.conf -newrmt 2020-03-03 -size +25k -size -28k -exec ls -al {} \; 2>/dev/null
```
This will give you details of the file for further verification of the desired file. Choose the filename only
 
### 2.  How many files exist on the system that have the ".bak" extension?
**Answer:** RUN `locate *.bak`command after `updatedb` command to update Database.
```bash
sudo updatedb # Ensure Database is up-to-date
locate *.bak | wc -l # wc command will count for you. You don't need to count files manually -l stands for line count
```

### 3. Submit the full path of the "xxd" binary.
**Answer:** RUN `where xxd` command. If it is unavailable then RUN
```bash
which xxd
```
