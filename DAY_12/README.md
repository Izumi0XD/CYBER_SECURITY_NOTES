# ♦ Day 12
</br>
</br>

## ◙ ***Getting into Win 7***
 </br>
 
# ♦ Getting into Win 7 : 
   ⇨ In this session we will be learning how to get into a windowsn device and can collect data or spying onto the host pc, for this we will be using a Windows professional device in our local nettwork(Virtual Machine). 
   </br>
   </br>
### ◙ Step-By-Step Guide 

### • 1. Reconnaissance : First of all we will be checking our local network if there arne any other devices connected or not (Note: for this to work in VM make sure both the devices are in same network settings preferrably "NAT Network" </br>
For scanning our local network we will be using ***arp scan*** by using following commands:

    sudo arp-scan -l -I eth1

After this we have to check which one of the device is tht we are looking for so for that we will use ***nmap*** to identify operating systems of all the devices individaually by using:

    sudo nmap -O >Ip add<

### • 2. Search For Vulnerability : Now we will be searching for the vulnerabilities of the ip we confirmed by doing nmap scans now for vulnerability searching we will be using the following command

    namp -Pn -sV --script vuln -oN vuln-win7-nmap.txt >IP add<

As we can see from above report tht there is a vulnerability availabe by the name "ms17-010".


### • 3. Now we would like to get some details on the this Vulnerability, for that we will be using ***"Searchsploit"*** :

    searchexploit ms17-010

As we acan see there are 6 exploits for this vulnerability, we will be using the one which can be done (Metasploit) cuz it most efficient and easy to do


### • 4. METASPLOIT : The Metasploit Project is a computer security project that provides information about security vulnerabilities and aids in penetration testing and IDS signature development. </br>

• Now to acess metasploit we have to type a command 

    msfconsole

• After getting into msfconsole we have to search for the vulnerability ***"ms17-010"***


• Now select the 1st one with the name ***"Eternalblue"*** by using command ***"use 0"***

    use 0

 
