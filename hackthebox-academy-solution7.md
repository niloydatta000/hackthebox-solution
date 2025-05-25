# Hack The Box Solution 7

### 1. Which option needs to be set to create a home directory for a new user using "useradd" command?
**Answer:** `--create-home` OR `-m`

**Example:**
```bash
sudo useradd -m -d /home/new_user -s /bin/bash -G wheel,users new_user
```

### 2. Which option needs to be set to lock a user account using the "usermod" command?
**Answer:** `--lock` OR `-L`

**Examle:**
```bash
sudo usermod -L test_user
```

### 3. Which option needs to be set to execute a command as a different user using the "su" command?
**Answer:** `--command` OR `-c`

**Example:**
```bash
su -c 'whoami' test_user
```
