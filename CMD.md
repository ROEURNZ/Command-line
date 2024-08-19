# How to use Command Prompt in Windows

How to use Command Prompt in Windows

```cmd
    Win + R 
```

- **Press cmd in the shell and enter to run the command prompt**

## How to get started with the command prompt


## How to open Command Prompt



```cmd
mkdir folder_name
```
Example: `mkdir NewFolder`

## Create a new file:

```cmd
echo. > file_name.txt
```
Example: `echo. > newfile.txt`

Or using type nul:

```cmd
type nul > file_name.txt
```
Example: `type nul > newfile.txt`

## Insert data into a file:

```cmd
echo Your text here > file_name.txt
```
Example: `echo Hello, World! > newfile.txt`

## To append data instead of overwriting:

```cmd
echo Additional text >> file_name.txt
```
Example: `echo Another line >> newfile.txt`

## Copy file data from an existing file to a new one:

```cmd
copy existing_file.txt new_file.txt
```
Example: `copy original.txt copy.txt`

## Rename a file:

```cmd
ren old_file_name.txt new_file_name.txt
```
Example: `ren oldfile.txt newfile.txt`

## Remove a file:

```cmd
del file_name.txt
```
Example: `del unwantedfile.txt`

## Remove a folder:

```cmd
rmdir /s /q folder_name
```
Example: `rmdir /s /q OldFolder`

- `/s` removes all files and subdirectories.
- `/q` runs the command in quiet mode (no confirmation prompt).

## Check folder contents:

```cmd
dir folder_name
```
Example: `dir NewFolder`

## To see the contents of the current directory:

```cmd
dir
```

## Reveal the local file (open file location in Explorer):

```cmd
start .
```
Example: If you are in the folder where the file is located, just type `start .` and press Enter.

## Move directory (relocate files):

```cmd
move folder_name destination_path
```
Example: `move NewFolder C:\NewLocation\`

## To move a single file:

```cmd
move file_name.txt destination_path
```
Example: `move newfile.txt C:\NewLocation\`

## List all files:

```cmd
dir /a
```
Example: `dir /a`

## Check for a word within a file:

```cmd
find "word_to_search" file_name.txt
```
Example: `find "Hello" newfile.txt`

## To search within all .txt files in a directory:

```cmd
find "word_to_search" *.txt
```

## Navigate to a directory:

```cmd
cd folder_name
```
Example: `cd Documents`

## To move to the parent directory:

```cmd
cd ..
```

## To go to the root directory:

```cmd
cd \
```

## Clear the Command Prompt screen:

```cmd
cls
```

## View the content of a text file:

```cmd
type file_name.txt
```
Example: `type newfile.txt`

## Display IP configuration:

```cmd
ipconfig
```

## Ping a network address:

```cmd
ping address
```
Example: `ping google.com`

## View a list of running processes:

```cmd
tasklist
```

## Kill a running process:

```cmd
taskkill /IM process_name.exe /F
```
Example: `taskkill /IM notepad.exe /F`

- `/IM` specifies the image name of the process.
- `/F` forces termination.

## Change file attributes:

```cmd
attrib +r file_name.txt
```
Example: `attrib +r newfile.txt` (sets the file as read-only)

To remove the read-only attribute:

```cmd
attrib -r file_name.txt
```

## View the current directory path:

```cmd
echo %cd%
```

## Copy a directory and its contents:

```cmd
xcopy source_path destination_path /E /H /C /I
```
Example: `xcopy C:\OldFolder C:\NewFolder /E /H /C /I`

- `/E` copies all subdirectories, including empty ones.
- `/H` copies hidden files and folders.
- `/C` continues copying even if errors occur.
- `/I` assumes the destination is a directory.

## Compare the contents of two files:

```cmd
fc file1.txt file2.txt
```
Example: `fc oldfile.txt newfile.txt`

## View system information:

```cmd
systeminfo
```

## Get help for a specific command:

```cmd
command_name /?
```
Example: `xcopy /?`

## View a list of available commands:

```cmd
help
```

## Check disk usage and information:

```cmd
chkdsk
```

## Shutdown or restart the computer:

### Shutdown:

```cmd
shutdown /s /t 0
```
Example: Immediate shutdown: `shutdown /s /t 0`

### Restart:

```cmd
shutdown /r /t 0
```
Example: Immediate restart: `shutdown /r /t 0`

## Find a file or folder by name:

```cmd
dir /s /p file_name
```

## Additional Commands:

### Create a hidden folder:

```cmd
mkdir folder_name
attrib +h folder_name
```
Example: `mkdir SecretFolder` and `attrib +h SecretFolder`

### Remove hidden attribute from a folder:

```cmd
attrib -h folder_name
```
Example: `attrib -h SecretFolder`

### List all hidden files and folders:

```cmd
dir /a:h
```

### Change the title of the Command Prompt window:

```cmd
title Your_Title_Here
```
Example: `title My Command Prompt`

### Change the color of the Command Prompt text and background:

```cmd
color [attr]
```
Example: `color 0A` (black background, green text)

### View network connections:

```cmd
netstat
```

### View active network connections and listening ports:

```cmd
netstat -an
```

### View the routing table:

```cmd
route print
```

### Flush DNS cache:

```cmd
ipconfig /flushdns
```

### Release and renew IP address:

```cmd
ipconfig /release
ipconfig /renew
```

### Map a network drive:

```cmd
net use X: \\server\share
```
Example: `net use Z: \\MyServer\MyShare`

### Disconnect a mapped network drive:

```cmd
net use X: /delete
```
Example: `net use Z: /delete`

### Enable or disable a network adapter:

Enable:

```cmd
netsh interface set interface "Interface Name" admin=enabled
```
Example: `netsh interface set interface "Ethernet" admin=enabled`

Disable:

```cmd
netsh interface set interface "Interface Name" admin=disabled
```
Example: `netsh interface set interface "Ethernet" admin=disabled`

### View all installed drivers:

```cmd
driverquery
```

### View detailed information about a specific driver:

```cmd
driverquery /v /fo list
```

### View system uptime:

```cmd
systeminfo | find "System Boot Time"
```

### View the list of installed programs:

```cmd
wmic product get name,version
```

### View the list of environment variables:

```cmd
set
```

### Set a new environment variable:

```cmd
setx VARIABLE_NAME "value"
```
Example: `setx PATH "C:\NewPath"`

### View the list of services:

```cmd
sc query
```

### Start a service:

```cmd
net start service_name
```
Example: `net start wuauserv` (Windows Update service)

### Stop a service:

```cmd
net stop service_name
```
Example: `net stop wuauserv` (Windows Update service)

### View the list of users:

```cmd
net user
```

### Add a new user:

```cmd
net user username password /add
```
Example: `net user newuser password123 /add`

### Delete a user:

```cmd
net user username /delete
```
Example: `net user newuser /delete`

### Add a user to a group:

```cmd
net localgroup groupname username /add
```
Example: `net localgroup administrators newuser /add`

### Remove a user from a group:

```cmd
net localgroup groupname username /delete
```
Example: `net localgroup administrators newuser /delete`

### Create a new text file and open it in Notepad:

```cmd
notepad file_name.txt
```
Example: `notepad newfile.txt`

### Open a website in the default browser:

```cmd
start http://www.example.com
```
Example: `start http://www.google.com`

### Open a specific file with its default application:

```cmd
start file_name.extension
```
Example: `start document.pdf`

### Create a new folder and navigate into it:

```cmd
mkdir folder_name && cd folder_name
```
Example: `mkdir NewFolder && cd NewFolder`

### List all files and folders with detailed information:

```cmd
dir /s /b
```

### Create a symbolic link:

```cmd
mklink link_name target_path
```
Example: `mklink MyLink C:\TargetFolder`


Sure, let's continue with more CMD commands:

### Create a hard link:

```cmd
mklink /H link_name target_path
```
Example: `mklink /H MyLink C:\TargetFile.txt`

### Create a directory junction:

```cmd
mklink /J link_name target_path
```
Example: `mklink /J MyLink C:\TargetFolder`

### Create a shortcut:

```cmd
mklink link_name target_path
```
Example: `mklink Shortcut.lnk C:\TargetFile.txt`

### View the list of open files:

```cmd
openfiles
```

### View the list of open files on a remote system:

```cmd
openfiles /query /s remote_system
```
Example: `openfiles /query /s \\RemotePC`

### Enable the viewing of open files:

```cmd
openfiles /local on
```

### Disable the viewing of open files:

```cmd
openfiles /local off
```

### View the list of shared resources:

```cmd
net share
```

### Create a new shared folder:

```cmd
net share share_name=folder_path
```
Example: `net share MyShare=C:\SharedFolder`

### Delete a shared folder:

```cmd
net share share_name /delete
```
Example: `net share MyShare /delete`

### View the list of network interfaces:

```cmd
netsh interface show interface
```

### View the list of wireless networks:

```cmd
netsh wlan show networks
```

### Connect to a wireless network:

```cmd
netsh wlan connect name=network_name
```
Example: `netsh wlan connect name=MyWiFi`

### Disconnect from a wireless network:

```cmd
netsh wlan disconnect
```

### View the list of wireless profiles:

```cmd
netsh wlan show profiles
```

### Export a wireless profile:

```cmd
netsh wlan export profile name=profile_name key=clear
```
Example: `netsh wlan export profile name=MyWiFi key=clear`

### Import a wireless profile:

```cmd
netsh wlan add profile filename=profile.xml
```
Example: `netsh wlan add profile filename=MyWiFi.xml`

### View the list of firewall rules:

```cmd
netsh advfirewall firewall show rule name=all
```

### Enable a firewall rule:

```cmd
netsh advfirewall firewall set rule name="rule_name" new enable=yes
```
Example: `netsh advfirewall firewall set rule name="File and Printer Sharing (Echo Request - ICMPv4-In)" new enable=yes`

### Disable a firewall rule:

```cmd
netsh advfirewall firewall set rule name="rule_name" new enable=no
```
Example: `netsh advfirewall firewall set rule name="File and Printer Sharing (Echo Request - ICMPv4-In)" new enable=no`

### View the list of scheduled tasks:

```cmd
schtasks /query
```

### Create a new scheduled task:

```cmd
schtasks /create /tn "task_name" /tr "task_run_command" /sc schedule
```
Example: `schtasks /create /tn "Backup" /tr "C:\BackupScript.bat" /sc daily /st 02:00`

### Delete a scheduled task:

```cmd
schtasks /delete /tn "task_name"
```
Example: `schtasks /delete /tn "Backup"`

### Run a scheduled task:

```cmd
schtasks /run /tn "task_name"
```
Example: `schtasks /run /tn "Backup"`

### View the list of installed updates:

```cmd
wmic qfe list
```

### View detailed information about a specific update:

```cmd
wmic qfe where HotFixID="KB123456" get /format:list
```
Example: `wmic qfe where HotFixID="KB123456" get /format:list`

### Uninstall an update:

```cmd
wusa /uninstall /kb:123456
```
Example: `wusa /uninstall /kb:123456`

### View the list of running services:

```cmd
sc query
```

### View detailed information about a specific service:

```cmd
sc qc service_name
```
Example: `sc qc wuauserv`

### Configure a service to start automatically:

```cmd
sc config service_name start=auto
```
Example: `sc config wuauserv start=auto`

### Configure a service to start manually:

```cmd
sc config service_name start=demand
```
Example: `sc config wuauserv start=demand`

### Configure a service to be disabled:

```cmd
sc config service_name start=disabled
```
Example: `sc config wuauserv start=disabled`

### View the list of environment variables:

```cmd
set
```

### Set a new environment variable:

```cmd
setx VARIABLE_NAME "value"
```
Example: `setx PATH "C:\NewPath"`

### View the list of user accounts:

```cmd
net user
```

### Add a new user account:

```cmd
net user username password /add
```
Example: `net user newuser password123 /add`

### Delete a user account:

```cmd
net user username /delete
```
Example: `net user newuser /delete`

### Add a user to a group:

```cmd
net localgroup groupname username /add
```
Example: `net localgroup administrators newuser /add`

### Remove a user from a group:

```cmd
net localgroup groupname username /delete
```
Example: `net localgroup administrators newuser /delete`

### View the list of groups:

```cmd
net localgroup
```

### Create a new group:

```cmd
net localgroup groupname /add
```
Example: `net localgroup developers /add`

### Delete a group:

```cmd
net localgroup groupname /delete
```
Example: `net localgroup developers /delete`

### View the list of shared folders:

```cmd
net share
```

### Create a new shared folder:

```cmd
net share sharename=folderpath
```
Example: `net share MyShare=C:\SharedFolder`

### Delete a shared folder:

```cmd
net share sharename /delete
```
Example: `net share MyShare /delete`

### View the list of network connections:

```cmd
netstat
```

### View active network connections and listening ports:

```cmd
netstat -an
```

### View the routing table:

```cmd
route print
```

### Add a static route:

```cmd
route add destination mask subnet_mask gateway
```
Example: `route add 192.168.1.0 mask 255.255.255.0 192.168.1.1`

### Delete a static route:

```cmd
route delete destination
```
Example: `route delete 192.168.1.0`

### View the list of open files:

```cmd
openfiles
```

### View the list of open files on a remote system:

```cmd
openfiles /query /s remote_system
```
Example: `openfiles /query /s \\RemotePC`

### Enable the viewing of open files:

```cmd
openfiles /local on
```

### Disable the viewing of open files:

```cmd
openfiles /local off
```

### View the list of shared resources:

```cmd
net share
```

### Create a new shared folder:

```cmd
net share share_name=folder_path
```
Example: `net share MyShare=C:\SharedFolder`

### Delete a shared folder:

```cmd
net share share_name /delete
```
Example: `net share MyShare /delete`

### View the list of network interfaces:

```cmd
netsh interface show interface
```

### View the list of wireless networks:

```cmd
netsh wlan show networks
```

### Connect to a wireless network:

```cmd
netsh wlan connect name=network_name
```
Example: `netsh wlan connect name=MyWiFi`

### Disconnect from a wireless network:

```cmd
netsh wlan disconnect
```

### View the list of wireless profiles:

```cmd
netsh wlan show profiles
```

### Export a wireless profile:

```cmd
netsh wlan export profile name=profile_name key=clear
```
Example: `netsh wlan export profile name=MyWiFi key=clear`

### Import a wireless profile:

```cmd
netsh wlan add profile filename=profile.xml
```
Example: `netsh wlan add profile filename=MyWiFi.xml`

### View the list of firewall rules:

```cmd
netsh advfirewall firewall show rule name=all
```

### Enable a firewall rule:

```cmd
netsh advfirewall firewall set rule name="rule_name" new enable=yes
```
Example: `netsh advfirewall firewall set rule name="File and Printer Sharing (Echo Request - ICMPv4-In)" new enable=yes`

### Disable a firewall rule:

```cmd
netsh advfirewall firewall set rule name="rule_name" new enable=no
```
Example: `netsh advfirewall firewall set rule name="File and Printer Sharing (Echo Request - ICMPv4-In)" new enable=no`

### View the list of scheduled tasks:

```cmd
schtasks /query
```

### Create a new scheduled task:

```cmd
schtasks /create /tn "task_name" /tr "task_run_command" /sc schedule
```
Example: `schtasks /create /tn "Backup" /tr "C:\BackupScript.bat" /sc daily