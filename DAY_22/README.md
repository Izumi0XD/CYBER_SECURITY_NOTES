# ♦ Day 22
</br>
</br>

## ◙ ***`Port Scanning using Python`***
 </br>
 
# ♦ Port Scanning using Python :
   ⇨ In this session we will be learning to demonstarte a simple port scan detection using Python. 

## ◙ Requirements :

 • Python 3.x
 • Scappy library if not installed

    pip install scapy

### ◙ Step-By-Step Guide 

### • Step-1.  

 ⇨ Create a directory named `port_scan_detection` and get the file tht ive uploaded named same by using the command :

     wget https://raw.githubusercontent.com/Izumi0XD/CYBER_SECURITY_NOTES/main/DAY_22/port_scan_detection.py?token=GHSAT0AAAAAACVPFPDGXNUSFL6OUXPC4HQWZVI37AA 


### • Step-2.  

 ⇨ Navigate to the directory where we have downloaded the script and then execute it :

     python port_scan_detection.py
 
 ⇨ script will now start capturing network traffic and print messages indicating any detected port scans.


## ◙ Workings :

• ***Function `detect_port_scan`*** : 

   ⇨ This function is called for each captured packet. It checks if the packet has a TCP layer and if it contains the SYN or SYN-ACK flags. It then verifies if the destination or source port is less than 1024, which indicates a possible port scan attempt. A message is printed if a port scan is detected.


• ***Sniffing Network Traffic*** : 
 
   ⇨ The `sniff` function from Scapy captures network packets and calls the `detect_port_scan` function for each packet.


## Notes


• ***Permissions*** :
   
   ⇨ Ensure you have the required permissions to capture network packets. This might require running the script with `sudo` in some environments.


• **Enhancements** : 

   ⇨ This is a basic implementation. Consider adding additional checks and features to improve accuracy and reliability based on your specific needs.
 
 
• ***Environment*** : 

   ⇨ The script is suitable for use in Kali Linux or WSL (Windows Subsystem for Linux). Keep the terminal running to monitor network traffic while the script is active.
