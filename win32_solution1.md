# Windows Solution 1

### What is the Build Number of the target workstation?
**Answer:** RUN `Get-ComputerInfo | Select-Object WindowsBuildNumber` for Windows 10 or above, for Older systems
```powershell
Get-WmiObject -Class Win32_OperatingSystem | Select-Object BuildNumber
```
### Which Windows NT version is installed on the workstation?
**Answer:** RUN `Get-ComputerInfo | Select-Object WindowsVersion` for Windows 10 or above, for Older systems
```powershell
Get-WmiObject -Class Win32_OperatingSystem | Select-Object Version
```

I ran `Get-WmiObject -Class Win32_OperatingSystem | Select-Object BuildNumber, Version` for solving two questions at single command.

**Pro Tip:** RUN 
```powershell
[System.Environment]::OSVersion.Version
```
You will see all required information shortly with this **.NET** framework. Make NT Version by combining like this *Major.Minor.Build*
