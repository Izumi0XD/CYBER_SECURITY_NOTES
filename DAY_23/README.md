# ♦ Day 24
</br>
</br>

## ◙ ***Introduction to the SNORT***
 </br>
 
# ♦ Snort : 
   ⇨ SNORT is a powerful open-source intrusion detection system (IDS) and intrusion prevention system (IPS) that provides real-time network traffic analysis and data packet logging. SNORT uses a rule-based language that combines anomaly, protocol, and signature inspection methods to detect potentially malicious activity.
   </br>
   </br>

### ◙ Requirements : 

   • Latest Version of [SNORT]((https://www.snort.org/downloads).) 
   
   • Libdnet - Install using the following command.

  ```bash
   sudo apt-get install libdnet-dev
  ```

### ◙ Step-By-Step Guide 

   ### • 1. Installation : 

   ##### 1. Download [SNORT]((https://www.snort.org/downloads).)  

   ##### 2. Extartct the Downloaded File :

   ⇨  Unzip the downloaded file and navigate into the extracted directory.
   
   ##### 3. **Install Snort :**    

   ⇨ Run the following commands to install Snort:

   ```bash
   ./configure --enable-sourcefire
   make
   sudo make install
   ```

   ##### 4. **Verify Installation**

   ⇨ Confirm that Snort is installed correctly:

   ```bash
   snort -V
   ```

### ◙ Configuration :

1. ***Create Configuration File***

   Create a configuration file named `snort.conf` in the `/etc/snort` directory. Use the following configuration:

   ```plaintext
   # Set the network interface to monitor
   var RULE_PATH /etc/snort/rules
   var SO_RULE_PATH /etc/snort/so_rules
   var PREPROC_RULE_PATH /etc/snort/preproc_rules
   var WHITE_LIST_PATH /etc/snort/rules
   var BLACK_LIST_PATH /etc/snort/rules
   # Configure the output plugins
   output alert_fast: filename snort.alert
   output log_tcpdump: filename snort.log
   # Include the default Snort rules
   include $RULE_PATH/snort.rules
   include $RULE_PATH/local.rules
   # Include the community rules
   include $RULE_PATH/community.rules
   ```

2. ***Set Up Directories***

   Create the necessary directories:

   ```bash
   sudo mkdir -p /etc/snort/rules
   sudo mkdir -p /etc/snort/preproc_rules
   sudo mkdir -p /etc/snort/so_rules
   ```

3. ***Download and Extract Default Rules***

   Fetch the default Snort rules:

   ```bash
   sudo wget -P /etc/snort/rules https://www.snort.org/rules/snortrules-snapshot-2976.tar.gz
   ```

   Extract the rules:

   ```bash
   sudo tar -xvzf /etc/snort/rules/snortrules-snapshot-2976.tar.gz -C /etc/snort/rules
   ```

4. ***Add Custom Rules***

   Create a file named `local.rules` in the `/etc/snort/rules` directory. You can add custom rules here to monitor specific traffic patterns.

##  ***Usage***

To start Snort, use the following command:

```bash
sudo snort -c /etc/snort/snort.conf -i <interface>
```

Replace `<interface>` with the network interface you wish to monitor.

##  ***Explanation***

Snort is a versatile IDS that helps safeguard your network by analyzing traffic for signs of malicious activity. It operates based on a set of rules, configured in the `snort.conf` file. The default rules cover a broad range of potential threats, while the `local.rules` file allows you to tailor the monitoring to your specific needs.

***Key Points :***

- **Traffic Monitoring:** Snort inspects network packets to identify potential threats.
- **Real-Time Alerts:** It generates alerts for suspicious activity.
- **Integration:** Snort can be integrated with other security tools for enhanced protection.

##  ***Note***

This guide provides a basic setup for Snort. For a more robust security solution, consider adding more rules and customizing your configuration. Remember to run Snort with the necessary permissions and in a suitable environment.
