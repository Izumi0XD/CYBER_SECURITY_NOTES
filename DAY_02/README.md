1# ♦ Day 02
</br>
</br>

## ◙ ***Introduction to Linux***
 </br>
Linux is an open source opersting system (OS) {Meaning it is free to install}. There are several kinds of Linux operating systems and it is mostly used in cyber sequrity purposes due to its flexiblity and it also has a very great environment for learning cyber security Thingy. </br>

## ◙ ***Setting Up The Linux Device***
</br>

### • 1. Download Virtual Box or Vmware : 
</br>

We will need a platform where we can instal all our virtual machines {OS} instead of installing it directly in the PC thst we can use multiple operaating systems in a single device so we can practice in [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### • 2. Download Kali Linux : 
</br>

Kali Linux is a Linux distribution designed for digital forensics and penetration testing. It is maintained and funded by Offensive Security. The software is based on the Debian Testing branch: most packages Kali uses are imported from the Debian repositories. [Kali Linux](https://www.kali.org/get-kali/)

### • 3. ***Basic Linux commands for beginner's*** :

• ***ls*** : Lists directory contents. </br>
• ***pwd*** : Prints the current working directory. </br>
• ***cd*** : Changes the current directory. </br>
• ***mkdir*** : Creates a new directory. </br>
• ***rm*** : Removes files or directories. </br>

</br>

### • 4. ***Networking Commands*** :
</br>

• ***ifconfig*** : Configures network interfaces. </br> 
• ***ping*** : Checks the network connection to a server
• ***netstat*** : Displays network connections, routing tables, and interface statistics. </br> 
• ***traceroute*** : Traces the route packets take to a network host. </br> 
• ***nslookup*** : Queries internet domain name servers. </br> 

Here is a diagrammatic representation of how the ls command works:

     +--------+
     |  User  |
     +--------+
          |
          v
     +--------+
     |  Shell |
     +--------+
          |
          v
     +--------+
     | Kernel |
     +--------+
          |
          v
     +---------+
     | FileSys |
     +---------+

### • 5. ***Service and Logs*** :


• ***service*** : Manages system services
• ***systemctl*** : Controls the systemd system and service manager
• ***journalctl*** : Queries and displays messages from the journal


6. ***System Administration Commands*** :


• ***sudo*** : Executes a command as another user, typically the superuser
• ***apt-get*** : Manages packages (installation, updates)
• ***top*** : Displays tasks and system resource usage
• ***chmod*** : Changes file permissions
• ***chown*** : Changes file owner and group


7. ***Linux File System / Directories*** :


• ***/*** : Root directory
• ***/bin*** : Essential command binaries
• ***/etc*** : Configuration files
• ***/home*** : User home directories
• ***/var*** : Variable files like logs
• ***/usr*** : User programs and data
