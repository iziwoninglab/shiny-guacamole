Ubuntu is a Linux distribution based on Debian and composed mostly of free and open-source software. Ubuntu is officially released in three editions: Desktop, Server, and Core for Internet of things devices and robots. Ubuntu is a popular operating system for cloud computing, with support for OpenStack.


## File and Directory Management Linux Commands


``` bash
ssh
```

``` bash
ls
```
 
``` bash
pwd
```
 		
``` bash
cd
```

``` bash
touch
```
 
``` bash
echo
```

``` bash
nano
```

``` bash
vim
```

``` bash
cat
```

``` bash
shred
```

``` bash
mkdir
```
 
``` bash
cp
```
 
``` bash
mv
```
 
``` bash
rm
```

``` bash
rmdir
```
``` bash
ln
```
## Enable sudo without a password for a user

Open a Terminal window and type:

```
sudo visudo
```

In the bottom of the file, add the following line:

```
$USER ALL=(ALL) NOPASSWD: ALL
```
Where `$USER` is your username on your system. Save and close the sudoers file (if you haven't changed your default terminal editor (you'll know if you have), press Ctl + x to exit `nano` and it'll prompt you to save).

---
## Networking

In Ubuntu, networking can be managed using various tools and utilities, including the following:

1. **NetworkManager**: NetworkManager is a system service that manages network connections and devices. It provides a graphical user interface (GUI) for configuring network settings, as well as a command-line interface (CLI) for advanced configuration. NetworkManager is the default network management tool in Ubuntu.

2. **Netplan**: [Netplan](../netplan) is a command-line utility for configuring network interfaces in modern versions of Ubuntu. It uses YAML configuration files to describe network interfaces, IP addresses, routes, and other network-related parameters. [Netplan](../netplan) generates the corresponding configuration files for the underlying network configuration subsystem, such as systemd-networkd or NetworkManager.

3. **ifupdown**: ifupdown is a traditional command-line tool for managing network interfaces in Ubuntu. It uses configuration files located in the ﻿/etc/network/ directory to configure network interfaces, IP addresses, routes, and other network-related parameters.

To manage networking in **Ubuntu**, you can use one or more of these tools depending on your needs and preferences. For example, you can use the NetworkManager GUI to configure basic network settings and use [Netplan](../netplan) or ifupdown for advanced configuration. You can also use the command-line tools to automate network configuration tasks or to configure networking on headless servers.

---



## System Management Commands

clear - Clear the console.
useradd - Add a new user to the system.
sudo - Run a command with administrative privileges.
adduser - Add a new user to the system with more options than useradd.
su - Switch to another user account.
exit - Close the current terminal or log out of the current user account.
sudo passwd - Change the password for the current user.
sudo passwd [username] - Change the password for another user.
sudo apt - A package manager used to install, update and remove software packages on Debian-based systems.
2sudo apt update & install - Update package lists and install packages.
finger - Display information about a user.
man - Display the manual page of a command.
whatis - Display a brief description of a command.
which - Locate a command and display its path.
whereis - Locate the binary, source, and manual page files for a command.
wget - Download files from the web.
curl - Transfer data to or from a server.
zip - Compress files into a zip archive.
unzip - Extract files from a zip archive.
less - View a file one page at a time.
## File Comparison and Manipulation Commands
head - Display the first lines of a file.
tail - Display the last lines of a file.
cmp - Compare two files byte by byte.
diff - Display the differences between two files.
sort - Sort the lines of a file.
find - Search for files in a directory hierarchy.
chmod - Change the permissions of a file or directory.
chown - Change the owner of a file or directory.
## Networking Management & Monitoring Commands
ifconfig - Configure network interfaces.
ip address - Display IP address information.
ip address | grep eth0 - Display the IP address of the eth0 interface.
ip address | grep eth0 | grep inet | awk - Display the IP address of the eth0 interface using awk.
resolvectl status - Display the current DNS resolver configuration.
ping - Test network connectivity by sending packets to a host.
netstat - Display network connections, routing tables, and interface statistics.
-tulpn - Display active listening ports and associated programs.
ss - Display socket statistics.
iptables - Configure and administer the netfilter firewall.
ufw - A user-friendly interface to manage iptables firewall rules.
## System Information & Process Management Commands
uname - Print system information, including kernel name, network node hostname, kernel release, and kernel version.
neofetch - Display system information in a colorful and visually appealing way.
cal - Display a calendar of the current month or year.
free - Display the amount of free and used system memory.
df and df-H - Display disk usage statistics for a file system.
ps - Report a snapshot of current processes.
top - Display dynamic real-time information about running processes.
kill - Send a signal to terminate a process.
pkill - Send a signal to terminate one or more processes based on their name.
systemctl - Control the systemd system and service manager.
history - Display previously executed commands.
sudo reboot - Reboot the system with administrative privileges.
shutdown - Shutdown or reboot the system.