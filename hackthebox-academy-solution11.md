# Hack The Box Solution 11

### 1. How many partitions exist in our Pwnbox? (Format: 0)
**Answer:** RUN `lsblk` to see all partitions.
```bash
lsblk - l | grep 'part' | wc -l
```
