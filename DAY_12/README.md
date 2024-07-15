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

### • 2. Search For Vulne
