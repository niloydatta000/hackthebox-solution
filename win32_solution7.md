# Windows Solution 7

### Find the SID of the bob.smith user.
**Answer:** RUN `Get-WmiObject -Class Win32_UserAccount` command.
```powershell
Get-WmiObject -Class Win32_UserAccount -Filter "Name='bob.smith'" | Select-Object Name, SID
```

### What 3rd party security application is disabled at startup for the current user?
**Answer:** OPEN `Task Manager` and go to `Startup` tab.
Look at the "Status" coliumn and find "Disabled". Select the preferred one.
**{No CommandLine}**

