# Hack The Box Solution 9

### 1. What is the Type of the service of the "dconf.service"?
**Answer:** Find out the location of **"dconf.service"** file using `find` command. If it is located into a single directory then
```bash
filepath=$(find / -type f -name "dconf.service" 2>/dev/null)
cat "$file" | grep "^Type" | awk -F'=' '{print $2}'
```
