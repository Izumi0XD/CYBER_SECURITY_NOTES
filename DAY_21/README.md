# ♦ Day 21
</br>
</br>

## ◙ ***Wi-Fi Hacking -2***
 </br>
 
# ♦ Overview : 
   ⇨ In this is session we will try to understand a manual approach to performing a wireless penetration test. Unlike automated tools such as `wifite`, this guide focuses on detailed, hands-on methodologies for evaluating the security of a Wi-Fi network. Wireless penetration testing involves simulating attacks to identify vulnerabilities and strengthen network defenses.
   </br>
   </br>
### ◙ 1. What Is A Wireless Penetration Test ?
   ⇨ Wireless penetration testing involves manually identifying and examining connections between devices connected to a Wi-Fi network, such as laptops, tablets, smartphones, and IoT devices. This type of testing is performed on-site, as proximity to the wireless signal is necessary for effective analysis.

### ◙ 2.  Goals of a Wireless Pen Test ? 
   ⇨  The goal of a wireless penetration test is to identify and exploit vulnerabilities manually, focusing on weaknesses that are most easily exploited. This approach contrasts with automated tools like `wifite`, which perform similar tasks but with less granular control over the testing process.

### ♦ Step-By-Step Guide :

### ◙ 1. Wireless Reconnaissance : 

 ⇨ ***AIM :*** To manually gather information about available wireless networks.

***Tools Rquired :***
• Car or transportation vehicle
• Laptop with a Wi-Fi antenna
• Wireless network adapter
• Packet capture and analysis software

***Process :***
• Conduct War Driving to manually sniff out Wi-Fi signals.
• Collect encrypted information protected by WPA2 using your setup, which includes manual configuration and monitoring.

### ◙ 2. Identifying Wireless Networks :

***AIM :*** To manually scan and identify wireless networks.

***Tools Required :***
• `airodump-ng`

***Process :***
• Set your wireless card to "monitor" mode manually.
• Use `airodump-ng` to scan traffic on different channels and specify channels manually to streamline data collection.

### ◙ 3. Searching for Vulnerabilities : 

***AIM :*** To manually identify vulnerabilities, focusing on the 4-way handshake process.

***Process :***
• Capture the 4-way handshake by manually initiating and monitoring traffic.
• Analyze the captured data to identify vulnerabilities in the pre-shared key manually, rather than relying on automated tools

### ◙ 4. Further Explorations : 

***AIM :*** TO manually exploit identified vulnerabilities to gain unauthorized access.

***Tools Required :***
• Aircrack-ng suite

***Process :***
• Manually de-authenticate a legitimate client to capture the handshake.
• Use Aircrack-ng to manually crack the captured handshake and extract the password, rather than using automated scripts.


***AIM :*** To document the penetration testing process and findings manually.

***Process :***
• Create a detailed report that includes:
• Executive summary
• Technical risks and vulnerabilities
• Detailed exploitation process
• Recommendations for mitigation
• Ensure all findings are documented comprehensively for manual review.

### ◙ 6. Remediation & Security Controls :

***AIM :*** To implement manual security controls to prevent future vulnerabilities.

***NOTE :***
• Enable MAC filtering and Network Access Control (NAC) solutions.
• Consider deploying wireless honeypots to detect and analyze unauthorized access attempts.

### ◙ 7.  Other Wireless Attacks :

In addition to manual exploitation of the 4-way handshake, other manual attacks include deploying rogue access points to intercept network traffic. This method involves manually overpowering legitimate access points and requires significant hands-on intervention tools like `wifite` are available but offer less granular control over the testing process.

