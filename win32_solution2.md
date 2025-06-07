# Windows Solution 2

### Find the non-standard directory in the C drive. Submit the contents of the flag file saved in this directory.
**Answer:** RUN `Get-ChildItem -Path C:\` command to see all files & folders in C drive and find a non-standard directory. Suppose the name of the directory is *academy* and exact filename is *flag.txt*.
```powershell
Get-ChildItem -Path C:\ -Directory
Set-Location C:\academy

# Check if flag file exists in the directory 
Get-ChildItem -Filter "*flag*" # This will show exact filename with extension

# Get the content of `flag.txt` file
Get-Content flag.txt
```
