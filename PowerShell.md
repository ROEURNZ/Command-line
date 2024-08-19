
# How to use PowerShell in Windows

## How to open PowerShell

```powershell
Win + X, then select Windows PowerShell
```
- **Press Win + X, then select Windows PowerShell**

## How to get started with PowerShell

# PowerShell Commands Guide

## Create a new directory (folder):

```powershell
New-Item -ItemType Directory -Path "folder_name"
```
Example: `New-Item -ItemType Directory -Path "NewFolder"`

## Create a new file:

```powershell
New-Item -ItemType File -Path "file_name.txt"
```
Example: `New-Item -ItemType File -Path "newfile.txt"`

## Insert data into a file:

```powershell
Set-Content -Path "file_name.txt" -Value "Your text here"
```
Example: `Set-Content -Path "newfile.txt" -Value "Hello, World!"`

## To append data instead of overwriting:

```powershell
Add-Content -Path "file_name.txt" -Value "Additional text"
```
Example: `Add-Content -Path "newfile.txt" -Value "Another line"`

## Copy file data from an existing file to a new one:

```powershell
Copy-Item -Path "existing_file.txt" -Destination "new_file.txt"
```
Example: `Copy-Item -Path "original.txt" -Destination "copy.txt"`

## Rename a file:

```powershell
Rename-Item -Path "old_file_name.txt" -NewName "new_file_name.txt"
```
Example: `Rename-Item -Path "oldfile.txt" -NewName "newfile.txt"`

## Remove a file:

```powershell
Remove-Item -Path "file_name.txt"
```
Example: `Remove-Item -Path "unwantedfile.txt"`

## Remove a folder:

```powershell
Remove-Item -Path "folder_name" -Recurse -Force
```
Example: `Remove-Item -Path "OldFolder" -Recurse -Force`

- `-Recurse` removes all files and subdirectories.
- `-Force` runs the command without confirmation prompts.

## Check folder contents:

```powershell
Get-ChildItem -Path "folder_name"
```
Example: `Get-ChildItem -Path "NewFolder"`

## To see the contents of the current directory:

```powershell
Get-ChildItem
```

## Reveal the local file (open file location in Explorer):

```powershell
Invoke-Item -Path "."
```
Example: If you are in the folder where the file is located, just type `Invoke-Item -Path "."` and press Enter.

## Move directory (relocate files):

```powershell
Move-Item -Path "folder_name" -Destination "destination_path"
```
Example: `Move-Item -Path "NewFolder" -Destination "C:\NewLocation\"`

## To move a single file:

```powershell
Move-Item -Path "file_name.txt" -Destination "destination_path"
```
Example: `Move-Item -Path "newfile.txt" -Destination "C:\NewLocation\"`

## List all files, including hidden ones:

```powershell
Get-ChildItem -Force
```
Example: `Get-ChildItem -Force`

## Check for a word within a file:

```powershell
Select-String -Path "file_name.txt" -Pattern "word_to_search"
```
Example: `Select-String -Path "newfile.txt" -Pattern "Hello"`

## To search within all .txt files in a directory:

```powershell
Select-String -Path "*.txt" -Pattern "word_to_search"
```

## Navigate to a directory:

```powershell
Set-Location -Path "folder_name"
```
Example: `Set-Location -Path "Documents"`

## To move to the parent directory:

```powershell
Set-Location -Path ".."
```

## To go to the root directory:

```powershell
Set-Location -Path "\"
```

## Clear the PowerShell screen:

```powershell
Clear-Host
```

## View the content of a text file:

```powershell
Get-Content -Path "file_name.txt"
```
Example: `Get-Content -Path "newfile.txt"`

## Display IP configuration:

```powershell
Get-NetIPAddress
```

## Ping a network address:

```powershell
Test-Connection -ComputerName "address"
```
Example: `Test-Connection -ComputerName "google.com"`

## View a list of running processes:

```powershell
Get-Process
```

## Kill a running process:

```powershell
Stop-Process -Name "process_name" -Force
```
Example: `Stop-Process -Name "notepad" -Force`

- `-Name` specifies the name of the process.
- `-Force` forces termination.

## Change file attributes:

```powershell
Set-ItemProperty -Path "file_name.txt" -Name IsReadOnly -Value $true
```
Example: `Set-ItemProperty -Path "newfile.txt" -Name IsReadOnly -Value $true` (sets the file as read-only)

To remove the read-only attribute:

```powershell
Set-ItemProperty -Path "file_name.txt" -Name IsReadOnly -Value $false
```

## View the current directory path:

```powershell
Get-Location
```

## Copy a directory and its contents:

```powershell
Copy-Item -Path "source_path" -Destination "destination_path" -Recurse
```
Example: `Copy-Item -Path "C:\OldFolder" -Destination "C:\NewFolder" -Recurse`

- `-Recurse` copies all subdirectories, including empty ones.

## Compare the contents of two files:

```powershell
Compare-Object -ReferenceObject (Get-Content -Path "file1.txt") -DifferenceObject (Get-Content -Path "file2.txt")
```
Example: `Compare-Object -ReferenceObject (Get-Content -Path "oldfile.txt") -DifferenceObject (Get-Content -Path "newfile.txt")`

## View system information:

```powershell
Get-ComputerInfo
```

## Get help for a specific command:

```powershell
Get-Help command_name
```
Example: `Get-Help Copy-Item`

## View a list of available commands:

```powershell
Get-Command
```

## Check disk usage and information:

```powershell
Get-Volume
```

## Shutdown or restart the computer:

### Shutdown:

```powershell
Stop-Computer
```
Example: Immediate shutdown: `Stop-Computer`

### Restart:

```powershell
Restart-Computer
```
Example: Immediate restart: `Restart-Computer`

## Find a file or folder by name:

```powershell
Get-ChildItem -Path "C:\" -Recurse -Filter "file_name"
```
Example: `Get-ChildItem -Path "C:\" -Recurse -Filter "newfile.txt"`

## Additional Commands:

### Create a hidden folder:

```powershell
New-Item -ItemType Directory -Path ".folder_name"
```
Example: `New-Item -ItemType Directory -Path ".SecretFolder"`

### Remove hidden attribute from a folder:

```powershell
Rename-Item -Path ".folder_name" -NewName "folder_name"
```
Example: `Rename-Item -Path ".SecretFolder" -NewName "SecretFolder"`

### List all hidden files and folders:

```powershell
Get-ChildItem -Force
```

### Change the title of the PowerShell window:

```powershell
$host.ui.RawUI.WindowTitle = "Your_Title_Here"
```
Example: `$host.ui.RawUI.WindowTitle = "My PowerShell"`

### Change the color of the PowerShell text and background:

```powershell
$Host.UI.RawUI.BackgroundColor = "Black"
$Host.UI.RawUI.ForegroundColor = "Green"
Clear-Host
```

### View network connections:

```powershell
Get-NetTCPConnection
```

### View active network connections and listening ports:

```powershell
Get-NetTCPConnection -State Listen
```

### View the routing table:

```powershell
Get-NetRoute
```

### Flush DNS cache:

```powershell
Clear-DnsClientCache
```

### Release and renew IP address:

```powershell
Release-NetIPAddress
Renew-NetIPAddress
```

### Map a network drive:

```powershell
New-PSDrive -Name "X" -PSProvider FileSystem -Root "\\server\share" -Persist
```
Example: `New-PSDrive -Name "Z" -PSProvider FileSystem -Root "\\MyServer\MyShare" -Persist`

### Disconnect a mapped network drive:

```powershell
Remove-PSDrive -Name "X"
```
Example: `Remove-PSDrive -Name "Z"`

### Enable or disable a network adapter:

Enable:

```powershell
Enable-NetAdapter -Name "Interface Name"
```
Example: `Enable-NetAdapter -Name "Ethernet"`

Disable:

```powershell
Disable-NetAdapter -Name "Interface Name"
```
Example: `Disable-NetAdapter -Name "Ethernet"`

### View all installed drivers:

```powershell
Get-WmiObject Win32_PnPSignedDriver
```


### View detailed information about a specific driver:

```powershell
Get-WmiObject Win32_PnPSignedDriver | Where-Object { $_.DeviceName -eq "driver_name" }
```
Example: `Get-WmiObject Win32_PnPSignedDriver | Where-Object { $_.DeviceName -eq "e1000" }`

### View system uptime:

```powershell
(Get-CimInstance Win32_OperatingSystem).LastBootUpTime
```

### View the list of installed programs:

```powershell
Get-WmiObject -Class Win32_Product
```

### View the list of environment variables:

```powershell
Get-ChildItem Env:
```

### Set a new environment variable:

```powershell
[System.Environment]::SetEnvironmentVariable("VARIABLE_NAME", "value", "User")
```
Example: `[System.Environment]::SetEnvironmentVariable("PATH", "C:\NewPath", "User")`

### View the list of services:

```powershell
Get-Service
```

### Start a service:

```powershell
Start-Service -Name "service_name"
```
Example: `Start-Service -Name "wuauserv"` (Windows Update service)

### Stop a service:

```powershell
Stop-Service -Name "service_name"
```
Example: `Stop-Service -Name "wuauserv"` (Windows Update service)

### View the list of users:

```powershell
Get-LocalUser
```

### Add a new user:

```powershell
New-LocalUser -Name "username" -Password (ConvertTo-SecureString "password" -AsPlainText -Force) -FullName "User Full Name" -Description "Description"
```
Example: `New-LocalUser -Name "newuser" -Password (ConvertTo-SecureString "password123" -AsPlainText -Force) -FullName "New User" -Description "New user account"`

### Delete a user:

```powershell
Remove-LocalUser -Name "username"
```
Example: `Remove-LocalUser -Name "newuser"`

### Add a user to a group:

```powershell
Add-LocalGroupMember -Group "groupname" -Member "username"
```
Example: `Add-LocalGroupMember -Group "Administrators" -Member "newuser"`

### Remove a user from a group:

```powershell
Remove-LocalGroupMember -Group "groupname" -Member "username"
```
Example: `Remove-LocalGroupMember -Group "Administrators" -Member "newuser"`

### Create a new text file and open it in Notepad:

```powershell
notepad "file_name.txt"
```
Example: `notepad "newfile.txt"`

### Open a website in the default browser:

```powershell
Start-Process "http://www.example.com"
```
Example: `Start-Process "http://www.google.com"`

### Open a specific file with its default application:

```powershell
Start-Process "file_name.extension"
```
Example: `Start-Process "document.pdf"`

### Create a new folder and navigate into it:

```powershell
New-Item -ItemType Directory -Path "folder_name" | Set-Location
```
Example: `New-Item -ItemType Directory -Path "NewFolder" | Set-Location`

### List all files and folders with detailed information:

```powershell
Get-ChildItem -Path "." -Recurse | Format-List
```

### Create a symbolic link:

```powershell
New-Item -ItemType SymbolicLink -Path "link_name" -Target "target_path"
```
Example: `New-Item -ItemType SymbolicLink -Path "MyLink" -Target "C:\TargetFolder"`

### Create a hard link:

```powershell
New-Item -ItemType HardLink -Path "link_name" -Target "target_path"
```
Example: `New-Item -ItemType HardLink -Path "MyLink" -Target "C:\TargetFile.txt"`

### Create a directory junction:

```powershell
New-Item -ItemType Junction -Path "link_name" -Target "target_path"
```
Example: `New-Item -ItemType Junction -Path "MyLink" -Target "C:\TargetFolder"`

### View the list of open files:

```powershell
Get-Process | Where-Object { $_.MainWindowTitle -ne "" }
```

### View the list of open files on a remote system:

```powershell
Invoke-Command -ComputerName "remote_system" -ScriptBlock { Get-Process | Where-Object { $_.MainWindowTitle -ne "" } }
```
Example: `Invoke-Command -ComputerName "RemotePC" -ScriptBlock { Get-Process | Where-Object { $_.MainWindowTitle -ne "" } }`

### Enable the viewing of open files:

```powershell
Set-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters" -Name "EnableOplocks" -Value 1
```

### Disable the viewing of open files:

```powershell
Set-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters" -Name "EnableOplocks" -Value 0
```

### View the list of shared resources:

```powershell
Get-SmbShare
```

### Create a new shared folder:

```powershell
New-SmbShare -Name "share_name" -Path "folder_path" -FullAccess "Everyone"
```
Example: `New-SmbShare -Name "MyShare" -Path "C:\SharedFolder" -FullAccess "Everyone"`

### Delete a shared folder:

```powershell
Remove-SmbShare -Name "share_name"
```
Example: `Remove-SmbShare -Name "MyShare"`

### View the list of network interfaces:

```powershell
Get-NetAdapter
```

### View the list of wireless networks:

```powershell
Get-NetAdapter | Where-Object { $_.MediaType -eq "802.11" } | Get-NetAdapterStatistics
```

### Connect to a wireless network:

```powershell
netsh wlan connect name="network_name"
```
Example: `netsh wlan connect name="MyWiFi"`

### Disconnect from a wireless network:

```powershell
netsh wlan disconnect
```

### View the list of wireless profiles:

```powershell
netsh wlan show profiles
```

### Export a wireless profile:

```powershell
netsh wlan export profile name="profile_name" folder="C:\path\to\folder" key=clear
```
Example: `netsh wlan export profile name="MyWiFi" folder="C:\WiFiProfiles" key=clear`

### Import a wireless profile:

```powershell
netsh wlan add profile filename="C:\path\to\profile.xml"
```
Example: `netsh wlan add profile filename="C:\WiFiProfiles\MyWiFi.xml"`

### View the list of firewall rules:

```powershell
Get-NetFirewallRule
```

### Enable a firewall rule:

```powershell
Set-NetFirewallRule -Name "rule_name" -Enabled True
```
Example: `Set-NetFirewallRule -Name "File and Printer Sharing (Echo Request - ICMPv4-In)" -Enabled True`

### Disable a firewall rule:

```powershell
Set-NetFirewallRule -Name "rule_name" -Enabled False
```
Example: `Set-NetFirewallRule -Name "File and Printer Sharing (Echo Request - ICMPv4-In)" -Enabled False`

### View the list of scheduled tasks:

```powershell
Get-ScheduledTask
```

### Create a new scheduled task:

```powershell
Register-ScheduledTask -Action (New-ScheduledTaskAction -Execute "powershell.exe" -Argument "-File 'C:\BackupScript.ps1'") -Trigger (New-ScheduledTaskTrigger -Daily -At 2am) -TaskName "Backup"
```

### Delete a scheduled task:

```powershell
Unregister-ScheduledTask -TaskName "task_name" -Confirm:$false
```
Example: `Unregister-ScheduledTask -TaskName "Backup" -Confirm:$false`

### Run a scheduled task:

```powershell
Start-ScheduledTask -TaskName "task_name"
```
Example: `Start-ScheduledTask -TaskName "Backup"`

### View the list of installed updates:

```powershell
Get-HotFix
```

### View detailed information about a specific update:

```powershell
Get-HotFix -Id "KB123456"
```
Example: `Get-HotFix -Id "KB123456"`

### Uninstall an update:

```powershell
wusa.exe /uninstall /kb:123456 /quiet /norestart
```
Example: `wusa.exe /uninstall /kb:123456 /quiet /norestart`

### View the list of running services:

```powershell
Get-Service
```

### View detailed information about a specific service:

```powershell
Get-Service -Name "service_name"
```
Example: `Get-Service -Name "wuauserv"`

### Configure a service to start automatically:

```powershell
Set-Service -Name "service_name" -StartupType Automatic
```
Example: `Set-Service -Name "wuauserv" -StartupType Automatic`

### Configure a service to start manually:

```powershell
Set-Service -Name "service_name" -StartupType Manual
```
Example: `Set-Service -Name "wuauserv" -StartupType Manual`

### Configure a service to be disabled:

```powers