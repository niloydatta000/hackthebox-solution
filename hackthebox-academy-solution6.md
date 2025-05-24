# Hack The Box Solution  6

### 1.  How many services are listening on the target system on all interfaces? (Not on localhost and IPv4 only)
**Answer:** RUN  `netstat -ltn4` command or
```bash
ss -ltn4 | awk '{print $3}' | grep '0.0.0.0:' | wc -l
```

### 2. Determine what user the ProFTPd server is running under. Submit the username as the answer.
**Answer:** RUN `ps -eo user,comm` command
```bash
ps -eo user,comm | grep proftpd | awk '{print $1}'
```

### 3. + 1  Use cURL from your Pwnbox to obtain the source code of the "https://www.inlanefreight.com" website and filter all unique paths (https://www.inlanefreight.com/directory" or "/another/directory") of that domain. Submit the number of these paths as the answer.
**Answer:** RUN
```bash
curl -s https://www.inlanefreight.com | grep -oP 'https:\/\/www\.inlanefreight\.com\/[^ ]+' | sort -u | wc -l
```
> You may face problems in filtering paths due to regex mismatching.
