# Windows Solution 6

### Use WMI to find the serial number of the system.
**Answer:** RUN `Get-WmiObject` command on PowerShell
```powershell
Get-WmiObject -Class Win32_OperatingSystem | Select-Object SerialNumber
```
