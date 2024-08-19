# How to use Terminal in Linux

## How to open Terminal

```bash
Ctrl + Alt + T
```
- **Press Ctrl + Alt + T to open the terminal**

## How to get started with the terminal

# Bash Commands Guide

## Create a new directory (folder):

```bash
mkdir folder_name
```
Example: `mkdir NewFolder`

## Create a new file:

```bash
touch file_name.txt
```
Example: `touch newfile.txt`

## Insert data into a file:

```bash
echo "Your text here" > file_name.txt
```
Example: `echo "Hello, World!" > newfile.txt`

## To append data instead of overwriting:

```bash
echo "Additional text" >> file_name.txt
```
Example: `echo "Another line" >> newfile.txt`

## Copy file data from an existing file to a new one:

```bash
cp existing_file.txt new_file.txt
```
Example: `cp original.txt copy.txt`

## Rename a file:

```bash
mv old_file_name.txt new_file_name.txt
```
Example: `mv oldfile.txt newfile.txt`

## Remove a file:

```bash
rm file_name.txt
```
Example: `rm unwantedfile.txt`

## Remove a folder:

```bash
rm -r folder_name
```
Example: `rm -r OldFolder`

- `-r` removes all files and subdirectories.

## Check folder contents:

```bash
ls folder_name
```
Example: `ls NewFolder`

## To see the contents of the current directory:

```bash
ls
```

## Reveal the local file (open file location in File Manager):

```bash
xdg-open .
```
Example: If you are in the folder where the file is located, just type `xdg-open .` and press Enter.

## Move directory (relocate files):

```bash
mv folder_name destination_path
```
Example: `mv NewFolder /home/user/NewLocation/`

## To move a single file:

```bash
mv file_name.txt destination_path
```
Example: `mv newfile.txt /home/user/NewLocation/`

## List all files, including hidden ones:

```bash
ls -a
```
Example: `ls -a`

## Check for a word within a file:

```bash
grep "word_to_search" file_name.txt
```
Example: `grep "Hello" newfile.txt`

## To search within all .txt files in a directory:

```bash
grep "word_to_search" *.txt
```

## Navigate to a directory:

```bash
cd folder_name
```
Example: `cd Documents`

## To move to the parent directory:

```bash
cd ..
```

## To go to the root directory:

```bash
cd /
```

## Clear the Terminal screen:

```bash
clear
```

## View the content of a text file:

```bash
cat file_name.txt
```
Example: `cat newfile.txt`

## Display IP configuration:

```bash
ifconfig
```

## Ping a network address:

```bash
ping address
```
Example: `ping google.com`

## View a list of running processes:

```bash
ps aux
```

## Kill a running process:

```bash
killall process_name
```
Example: `killall gedit`

## Change file permissions:

```bash
chmod +r file_name.txt
```
Example: `chmod +r newfile.txt` (sets the file as readable)

To remove the read-only attribute:

```bash
chmod -r file_name.txt
```

## View the current directory path:

```bash
pwd
```

## Copy a directory and its contents:

```bash
cp -r source_path destination_path
```
Example: `cp -r /home/user/OldFolder /home/user/NewFolder`

- `-r` copies all subdirectories, including empty ones.

## Compare the contents of two files:

```bash
diff file1.txt file2.txt
```
Example: `diff oldfile.txt newfile.txt`

## View system information:

```bash
uname -a
```

## Get help for a specific command:

```bash
command_name --help
```
Example: `cp --help`

## View a list of available commands:

```bash
compgen -c
```

## Check disk usage and information:

```bash
df -h
```

## Shutdown or restart the computer:

### Shutdown:

```bash
sudo shutdown now
```
Example: Immediate shutdown: `sudo shutdown now`

### Restart:

```bash
sudo reboot
```
Example: Immediate restart: `sudo reboot`

## Find a file or folder by name:

```bash
find / -name file_name
```
Example: `find / -name newfile.txt`

## Additional Commands:

### Create a hidden folder:

```bash
mkdir .folder_name
```
Example: `mkdir .SecretFolder`

### Remove hidden attribute from a folder:

```bash
mv .folder_name folder_name
```
Example: `mv .SecretFolder SecretFolder`

### List all hidden files and folders:

```bash
ls -a
```

### Change the title of the Terminal window:

```bash
echo -ne "\033]0;Your_Title_Here\007"
```
Example: `echo -ne "\033]0;My Terminal\007"`

### Change the color of the Terminal text and background:

```bash
echo -e "\e]P0color"
```
Example: `echo -e "\e]P0A"` (black background, green text)

### View network connections:

```bash
netstat
```

### View active network connections and listening ports:

```bash
netstat -an
```

### View the routing table:

```bash
route -n
```

### Flush DNS cache:

```bash
sudo systemd-resolve --flush-caches
```

### Release and renew IP address:

```bash
sudo dhclient -r
sudo dhclient
```

### Map a network drive:

```bash
sudo mount -t cifs -o username=user,password=pass //server/share /mnt/share
```
Example: `sudo mount -t cifs -o username=user,password=pass //MyServer/MyShare /mnt/share`

### Disconnect a mapped network drive:

```bash
sudo umount /mnt/share
```
Example: `sudo umount /mnt/share`

### Enable or disable a network adapter:

Enable:

```bash
sudo ifconfig eth0 up
```
Example: `sudo ifconfig eth0 up`

Disable:

```bash
sudo ifconfig eth0 down
```
Example: `sudo ifconfig eth0 down`

### View all installed drivers:

```bash
lsmod
```

### View detailed information about a specific driver:

```bash
modinfo driver_name
```
Example: `modinfo e1000`

### View system uptime:

```bash
uptime
```

### View the list of installed programs:

```bash
dpkg --list
```

### View the list of environment variables:

```bash
printenv
```

### Set a new environment variable:

```bash
export VARIABLE_NAME="value"
```
Example: `export PATH="/new/path:$PATH"`

### View the list of services:

```bash
systemctl list-units --type=service
```

### Start a service:

```bash
sudo systemctl start service_name
```
Example: `sudo systemctl start apache2`

### Stop a service:

```bash
sudo systemctl stop service_name
```
Example: `sudo systemctl stop apache2`

### View the list of users:

```bash
cut -d: -f1 /etc/passwd
```

### Add a new user:

```bash
sudo adduser username
```
Example: `sudo adduser newuser`

### Delete a user:

```bash
sudo deluser username
```
Example: `sudo deluser newuser`

### Add a user to a group:

```bash
sudo usermod -aG groupname username
```
Example: `sudo usermod -aG sudo newuser`

### Remove a user from a group:

```bash
sudo deluser username groupname
```
Example: `sudo deluser newuser sudo`

### Create a new text file and open it in a text editor:

```bash
nano file_name.txt
```
Example: `nano newfile.txt`

### Open a website in the default browser:

```bash
xdg-open http://www.example.com
```
Example: `xdg-open http://www.google.com`

### Open a specific file with its default application:

```bash
xdg-open file_name.extension
```
Example: `xdg-open document.pdf`

### Create a new folder and navigate into it:

```bash
mkdir folder_name && cd folder_name
```
Example: `mkdir NewFolder && cd NewFolder`

### List all files and folders with detailed information:

```bash
ls -l
```

### Create a symbolic link:

```bash
ln -s target_path link_name
```
Example: `ln -s /home/user/TargetFolder MyLink`

### Create a hard link:

```bash
ln target_path link_name
```
Example: `ln /home/user/TargetFile.txt MyLink`

### Create a directory junction:

```bash
ln -s target_path link_name
```
Example: `ln -s /home/user/TargetFolder MyLink`

### View the list of open files:

```bash
lsof
```


### View the list of open files on a remote system:

```bash
ssh user@remote_system lsof
```
Example: `ssh user@RemotePC lsof`

### Enable the viewing of open files:

```bash
sudo sysctl fs.file-max=100000
```

### Disable the viewing of open files:

```bash
sudo sysctl fs.file-max=4096
```

### View the list of shared resources:

```bash
smbclient -L //server -U user
```
Example: `smbclient -L //MyServer -U user`

### Create a new shared folder:

```bash
sudo nano /etc/samba/smb.conf
```
Add the following lines to the file:
```bash
[share_name]
   path = /path/to/folder
   available = yes
   valid users = user
   read only = no
   browsable = yes
   public = yes
   writable = yes
```
Then restart the Samba service:
```bash
sudo systemctl restart smbd
```

### Delete a shared folder:

Edit the `/etc/samba/smb.conf` file and remove the corresponding share configuration, then restart the Samba service:
```bash
sudo systemctl restart smbd
```

### View the list of network interfaces:

```bash
ip link show
```

### View the list of wireless networks:

```bash
nmcli dev wifi
```

### Connect to a wireless network:

```bash
nmcli dev wifi connect "network_name" password "password"
```
Example: `nmcli dev wifi connect "MyWiFi" password "password123"`

### Disconnect from a wireless network:

```bash
nmcli dev disconnect iface wlan0
```

### View the list of wireless profiles:

```bash
nmcli connection show
```

### Export a wireless profile:

```bash
nmcli connection export id "profile_name" file_name
```
Example: `nmcli connection export id "MyWiFi" MyWiFi.nmconnection`

### Import a wireless profile:

```bash
nmcli connection import type wifi file file_name
```
Example: `nmcli connection import type wifi file MyWiFi.nmconnection`

### View the list of firewall rules:

```bash
sudo ufw status
```

### Enable a firewall rule:

```bash
sudo ufw allow "rule_name"
```
Example: `sudo ufw allow "Apache Full"`

### Disable a firewall rule:

```bash
sudo ufw deny "rule_name"
```
Example: `sudo ufw deny "Apache Full"`

### View the list of scheduled tasks:

```bash
crontab -l
```

### Create a new scheduled task:

```bash
crontab -e
```
Add a new line in the format:
```bash
* * * * * /path/to/command
```
Example: `0 2 * * * /home/user/BackupScript.sh`

### Delete a scheduled task:

Edit the crontab file and remove the corresponding line:
```bash
crontab -e
```

### View the list of installed updates:

```bash
apt list --installed
```

### View detailed information about a specific update:

```bash
apt show package_name
```
Example: `apt show apache2`

### Uninstall an update:

```bash
sudo apt remove package_name
```
Example: `sudo apt remove apache2`

### View the list of running services:

```bash
systemctl list-units --type=service
```

### View detailed information about a specific service:

```bash
systemctl status service_name
```
Example: `systemctl status apache2`

### Configure a service to start automatically:

```bash
sudo systemctl enable service_name
```
Example: `sudo systemctl enable apache2`

### Configure a service to start manually:

```bash
sudo systemctl disable service_name
```
Example: `sudo systemctl disable apache2`

### View the list of environment variables:

```bash
printenv
```

### Set a new environment variable:

```bash
export VARIABLE_NAME="value"
```
Example: `export PATH="/new/path:$PATH"`

### View the list of user accounts:

```bash
cut -d: -f1 /etc/passwd
```

### Add a new user account:

```bash
sudo adduser username
```
Example: `sudo adduser newuser`

### Delete a user account:

```bash
sudo deluser username
```
Example: `sudo deluser newuser`

### Add a user to a group:

```bash
sudo usermod -aG groupname username
```
Example: `sudo usermod -aG sudo newuser`

### Remove a user from a group:

```bash
sudo deluser username groupname
```
Example: `sudo deluser newuser sudo`

### Create a new text file and open it in a text editor:

```bash
nano file_name.txt
```
Example: `nano newfile.txt`

### Open a website in the default browser:

```bash
xdg-open http://www.example.com
```
Example: `xdg-open http://www.google.com`

### Open a specific file with its default application:

```bash
xdg-open file_name.extension
```
Example: `xdg-open document.pdf`

### Create a new folder and navigate into it:

```bash
mkdir folder_name && cd folder_name
```
Example: `mkdir NewFolder && cd NewFolder`

### List all files and folders with detailed information:

```bash
ls -l
```

### Create a symbolic link:

```bash
ln -s target_path link_name
```
Example: `ln -s /home/user/TargetFolder MyLink`

### Create a hard link:

```bash
ln target_path link_name
```
Example: `ln /home/user/TargetFile.txt MyLink`

### Create a directory junction:

```bash
ln -s target_path link_name
```
Example: `ln -s /home/user/TargetFolder MyLink`

### View the list of open files:

```bash
lsof
```

### View the list of open files on a remote system:

```bash
ssh user@remote_system lsof
```
Example: `ssh user@RemotePC lsof`

### Enable the viewing of open files:

```bash
sudo sysctl fs.file-max=100000
```

### Disable the viewing of open files:

```bash
sudo sysctl fs.file-max=4096
```

### View the list of shared resources:

```bash
smbclient -L //server -U user
```
Example: `smbclient -L //MyServer -U user`

### Create a new shared folder:

```bash
sudo nano /etc/samba/smb.conf
```
Add the following lines to the file:
```bash
[share_name]
   path = /path/to/folder
   available = yes
   valid users = user
   read only = no
   browsable = yes
   public = yes
   writable = yes
```
Then restart the Samba service:
```bash
sudo systemctl restart smbd
```

### Delete a shared folder:

Edit the `/etc/samba/smb.conf` file and remove the corresponding share configuration, then restart the Samba service:
```bash
sudo systemctl restart smbd
```

### View the list of network interfaces:

```bash
ip link show
```

### View the list of wireless networks:

```bash
nmcli dev wifi
```

### Connect to a wireless network:

```bash
nmcli dev wifi connect "network_name" password "password"
```
Example: `nmcli dev wifi connect "MyWiFi" password "password123"`

### Disconnect from a wireless network:

```bash
nmcli dev disconnect iface wlan0
```

### View the list of wireless profiles:

```bash
nmcli connection show
```

### Export a wireless profile:

```bash
nmcli connection export id "profile_name" file_name
```
Example: `nmcli connection export id "MyWiFi" MyWiFi.nmconnection`

### Import a wireless profile:

```bash
nmcli connection import type wifi file file_name
```
Example: `nmcli connection import type wifi file MyWiFi.nmconnection`

### View the list of firewall rules:

```bash
sudo ufw status
```

### Enable a firewall rule:

```bash
sudo ufw allow "rule_name"
```
Example: `sudo ufw allow "Apache Full"`

### Disable a firewall rule:

```bash
sudo ufw deny "rule_name"
```
Example: `sudo ufw deny "Apache Full"`

### View the list of scheduled tasks:

```bash
crontab -l
```

### Create a new scheduled task:

```bash
crontab -e
```
Add a new line in the format:
```bash
* * * * * /path/to/command
```
Example: `0 2 * * * /home/user/BackupScript.sh`

### Delete a scheduled task:

Edit the crontab file and remove the corresponding line:
```bash
crontab -e
```

### View the list of installed updates:

```bash
apt list --installed
```

### View detailed information about a specific update:

```bash
apt show package_name
```
Example: `apt show apache2`

### Uninstall an update:

```bash
sudo apt remove package_name
```
Example: `sudo apt remove apache2`

### View the list of running services:

```bash
systemctl list-units --type=service
```


### View detailed information about a specific service:

```bash
systemctl status service_name
```
Example: `systemctl status apache2`

### Start a service:

```bash
sudo systemctl start service_name
```
Example: `sudo systemctl start apache2`

### Stop a service:

```bash
sudo systemctl stop service_name
```
Example: `sudo systemctl stop apache2`

### Restart a service:

```bash
sudo systemctl restart service_name
```
Example: `sudo systemctl restart apache2`

### Enable a service to start at boot:

```bash
sudo systemctl enable service_name
```
Example: `sudo systemctl enable apache2`

### Disable a service from starting at boot:

```bash
sudo systemctl disable service_name
```
Example: `sudo systemctl disable apache2`

### Check if a service is enabled:

```bash
systemctl is-enabled service_name
```
Example: `systemctl is-enabled apache2`

### Check if a service is active:

```bash
systemctl is-active service_name
```
Example: `systemctl is-active apache2`

### View the list of all services:

```bash
systemctl list-units --type=service
```

### View the list of failed services:

```bash
systemctl --failed
```

### Reload the configuration of a service:

```bash
sudo systemctl reload service_name
```
Example: `sudo systemctl reload apache2`

### Mask a service (prevent it from being started):

```bash
sudo systemctl mask service_name
```
Example: `sudo systemctl mask apache2`

### Unmask a service:

```bash
sudo systemctl unmask service_name
```
Example: `sudo systemctl unmask apache2`

### View the logs of a service:

```bash
journalctl -u service_name
```
Example: `journalctl -u apache2`

### View the last 100 lines of a service's log:

```bash
journalctl -u service_name -n 100
```
Example: `journalctl -u apache2 -n 100`

### Follow the logs of a service in real-time:

```bash
journalctl -u service_name -f
```
Example: `journalctl -u apache2 -f`

### View the list of all units (services, sockets, targets, etc.):

```bash
systemctl list-units
```

### View the list of all installed unit files:

```bash
systemctl list-unit-files
```

### View the dependencies of a service:

```bash
systemctl list-dependencies service_name
```
Example: `systemctl list-dependencies apache2`

### View the status of the system:

```bash
systemctl status
```

### Reboot the system:

```bash
sudo systemctl reboot
```

### Shutdown the system:

```bash
sudo systemctl poweroff
```

### Suspend the system:

```bash
sudo systemctl suspend
```

### Hibernate the system:

```bash
sudo systemctl hibernate
```

### Hybrid-sleep the system (suspend to both RAM and disk):

```bash
sudo systemctl hybrid-sleep
```

### View the current runlevel:

```bash
runlevel
```

### Change the runlevel (target):

```bash
sudo systemctl isolate target_name
```
Example: `sudo systemctl isolate multi-user.target`

### View the default target:

```bash
systemctl get-default
```

### Set the default target:

```bash
sudo systemctl set-default target_name
```
Example: `sudo systemctl set-default graphical.target`

### View the list of available targets:

```bash
systemctl list-units --type=target
```

### View the list of active timers:

```bash
systemctl list-timers
```

### Start a timer:

```bash
sudo systemctl start timer_name
```
Example: `sudo systemctl start apt-daily.timer`

### Stop a timer:

```bash
sudo systemctl stop timer_name
```
Example: `sudo systemctl stop apt-daily.timer`

### Enable a timer:

```bash
sudo systemctl enable timer_name
```
Example: `sudo systemctl enable apt-daily.timer`

### Disable a timer:

```bash
sudo systemctl disable timer_name
```
Example: `sudo systemctl disable apt-daily.timer`

### View the list of active sockets:

```bash
systemctl list-sockets
```

### Start a socket:

```bash
sudo systemctl start socket_name
```
Example: `sudo systemctl start ssh.socket`

### Stop a socket:

```bash
sudo systemctl stop socket_name
```
Example: `sudo systemctl stop ssh.socket`

### Enable a socket:

```bash
sudo systemctl enable socket_name
```
Example: `sudo systemctl enable ssh.socket`

### Disable a socket:

```bash
sudo systemctl disable socket_name
```
Example: `sudo systemctl disable ssh.socket`

### View the list of active targets:

```bash
systemctl list-units --type=target
```

### Start a target:

```bash
sudo systemctl start target_name
```
Example: `sudo systemctl start multi-user.target`

### Stop a target:

```bash
sudo systemctl stop target_name
```
Example: `sudo systemctl stop multi-user.target`

### Enable a target:

```bash
sudo systemctl enable target_name
```
Example: `sudo systemctl enable multi-user.target`

### Disable a target:

```bash
sudo systemctl disable target_name
```
Example: `sudo systemctl disable multi-user.target`

### View the list of active mount points:

```bash
systemctl list-units --type=mount
```

### Start a mount point:

```bash
sudo systemctl start mount_name
```
Example: `sudo systemctl start home.mount`

### Stop a mount point:

```bash
sudo systemctl stop mount_name
```
Example: `sudo systemctl stop home.mount`

### Enable a mount point:

```bash
sudo systemctl enable mount_name
```
Example: `sudo systemctl enable home.mount`

### Disable a mount point:

```bash
sudo systemctl disable mount_name
```
Example: `sudo systemctl disable home.mount`

### View the list of active swap units:

```bash
systemctl list-units --type=swap
```

### Start a swap unit:

```bash
sudo systemctl start swap_name
```
Example: `sudo systemctl start swap.target`

### Stop a swap unit:

```bash
sudo systemctl stop swap_name
```
Example: `sudo systemctl stop swap.target`

### Enable a swap unit:

```bash
sudo systemctl enable swap_name
```
Example: `sudo systemctl enable swap.target`

### Disable a swap unit:

```bash
sudo systemctl disable swap_name
```
Example: `sudo systemctl disable swap.target`

### View the list of active paths:

```bash
systemctl list-units --type=path
```

### Start a path:

```bash
sudo systemctl start path_name
```
Example: `sudo systemctl start tmp.path`

### Stop a path:

```bash
sudo systemctl stop path_name
```
Example: `sudo systemctl stop tmp.path`

### Enable a path:

```bash
sudo systemctl enable path_name
```
Example: `sudo systemctl enable tmp.path`

### Disable a path:

```bash
sudo systemctl disable path_name
```
Example: `sudo systemctl disable tmp.path`

### View the list of active slices:

```bash
systemctl list-units --type=slice
```

### Start a slice:

```bash
sudo systemctl start slice_name
```
Example: `sudo systemctl start user.slice`

### Stop a slice:

```bash
sudo systemctl stop slice_name
```
Example: `sudo systemctl stop user.slice`

### Enable a slice:

```bash
sudo systemctl enable slice_name
```
Example: `sudo systemctl enable user.slice`

### Disable a slice:

```bash
sudo systemctl disable slice_name
```
Example: `sudo systemctl disable user.slice`

### View the list of active scopes:

```bash
systemctl list-units --type=scope
```

### Start a scope:

```bash
sudo systemctl start scope_name
```
Example: `sudo systemctl start session-1.scope`

### Stop a scope:

```bash
sudo systemctl stop scope_name
```
Example: `sudo systemctl stop session-1.scope`

### Enable a scope:

```bash
sudo systemctl enable scope_name
```
Example: `sudo systemctl enable session-1.scope`

### Disable a scope:

```bash
sudo systemctl disable scope_name
```
Example: `sudo systemctl disable session-1.scope`

### View the list of active services:

```bash
systemctl list-units --type=service
```

### Start a service:

```bash
sudo systemctl start service_name
```
Example: `sudo systemctl start apache2`

### Stop a service:

```bash
sudo systemctl stop service_name
```
Example: `sudo systemctl stop apache2`

### Enable a service:

```bash
sudo systemctl enable service_name
```
Example: `sudo systemctl enable apache2`

### Disable a service:

```bash
sudo systemctl disable service_name
```
Example: `sudo systemctl disable apache2`

### View the list of active sockets:

```bash
systemctl list-units --type=socket
```

### Start a socket:

```bash
sudo systemctl start socket_name
```
Example: `sudo systemctl start ssh.socket`

### Stop a socket:

```bash
sudo
```

### For example


```bash
   composer create-project laravel/laravel:^11.0 app
```
![Video](./Assets/thumbnail-image.png) [Watch the Video](./Assets/Bash%20command.mp4)
