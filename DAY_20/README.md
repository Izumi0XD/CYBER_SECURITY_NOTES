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
