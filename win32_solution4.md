# Windows Solution 4

### Identify one of the non-standard update services running on the host. Submit the full name of the service executable (not the DisplayName) as your answer.
**Answer:** RUN `Get-Service` command to see services on the system.
```powershell
$standardUpdateServices = @("wuauserv", "UsoSvc", "BITS", "DoSvc") # All Standard Update Services

 gsv | ? {$_.Name -match "update" -or $_.DisplayName -match "update" -and  $_.Name -notin $standardUpdateServices  -and $_.Status -eq "Running"} | select Name, DisplayName, Status
```
The answer should be the `Name` selected with concatenated by **".exe"** as service executable fullname is required.

A more complicated command exists I have known from the internet which I didn't apply because of its complexity. This methd is not checked hence not guaranteed which is:

```powershell
$standardUpdateServices = @("wuauserv", "UsoSvc", "BITS", "DoSvc") # All Standard Update Services

Get-WmiObject Win32_Service | Where-Object {$_.Name -match "update" -or $_.DisplayName -match "update" -and  $_.Name -notin $standardUpdateServices -and $_.State -eq "Running"} | Select-Object  Name, DisplayName, State, StartMode, PathName
```
The correct answer may lie on `PathName` which shows full path of the service executable location.
