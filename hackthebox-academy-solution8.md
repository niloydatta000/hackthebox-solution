# Hack The Box Solution 8

### 1.  Use the "systemctl" command to list all units of services and submit the unit name with the description "Load AppArmor profiles managed internally by snapd" as the answer.
**Answer:** RUN  `systemctl list-units --type=service` command
```bash
systemctl list-units --type=service | grep "Load AppArmor profiles managed internally by snapd" | awk '{print $1}'
```
