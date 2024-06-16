# ♦ Day 05

## ◙ TRYHACKME 
  : TryHackMe is a free online platform for learning cyber security, using hands-on exercises and labs, all through your browser!{***A MUST TRY WEBSITE TO LEARN AND PRACTICE CYBERSECURITY***}

### BASIC PENTESTING
  : This machine allows you ot practice app hacking and privellege escalation
  
![image](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/19b9fcb4-51c6-4801-a10e-43e1f302f63b)


### ◙ OWASP
   : The Open Worldwide Application Security Project is an online community that produces freely available articles, methodologies, documentation, tools, and technologies in the fields of IoT, system software and web application security. The OWASP provides free and open resources. {The Open Web Application Security Project maintains a regularly-updated list of the most pressing web application security concerns.}

#### • OWASP TOP 10

##### 1. Broken Access Control
  : is a security vulnerability that occurs ***when a user can gain unauthorized access to certain parts of a web application or system.*** <br />This can include accessing data, modifying content, or performing actions that they should not be able to do. It often happens due to flaws in the design or implementation of access control mechanisms, or mistakes in authentication and authorization processes.
  
##### 2. Cryptographic Failures
  :  refers to ***a security issue that occurs when sensitive data is exposed due to improper implementation of cryptographic protocols or algorithms.*** <br />This can include problems like weak encryption, incorrect key management, insufficient randomness, or inadequate authentication measures
  
##### 3. Injection
  : is a type of vulnerability in computer security ***where an attacker can send malicious code through an application to another system. This can lead to unauthorized access, data breaches, or even complete system compromise.*** <br />It often occurs when user input is not properly sanitized, allowing attackers to inject and execute malicious code

##### 4. Insecure Design
  : ***It occurs when security is not adequately integrated into the application during the design phase, leading to vulnerabilities that can be exploited***

##### 5. Security Misconfiguration
  : is an ***error or vulnerability in the setup of code or systems that allows attackers to access sensitive data.*** <br />It can occur due to improper security settings, maintenance issues, or using default configurations that are not secure

##### 6. Vulnerable and Outdated Components
  : refer to ***using software libraries, frameworks, or other third-party components that have known security vulnerabilities or are no longer actively maintained.*** <br />This can lead to significant security risks as attackers may exploit these vulnerabilities to gain unauthorized access or control.{basically using framework whose vulnerability is well known}
  
##### 7. Identification and Authentication Failures
  :  are ***vulnerabilities related to the mechanisms used to verify the identity and authenticity of users.*** < br/> These failures can lead to unauthorized access, identity theft, or system compromise if not properly implemented or if the authentication scheme is weak.{ Basically a weakness in login system}.

##### 8. Software and Data Integrity Failures
  : occur when an attacker can modify or delete data in an unauthorized manner due to vulnerabilities in the software or poor coding practices. ***Using untrusted software or updates that compromise data integrity.*** < br/> This compromises the trustworthiness and accuracy of the system’s data and operations
##### 9. Security Logging and Monitoring Failures
  : are ***vulnerabilities that occur when a system or application fails to properly log or monitor security events.*** <br /> This can result in attackers gaining unauthorized access without detection, and delays in the response to security incidents
##### 10. Server-Side Request Forgery (SSRF)
  : is ***a web security vulnerability that allows an attacker to cause the server-side application to make requests to an unintended location, such as internal-only services within an organization’s infrastructure.*** < br/> When an attacker tricks the server into accessing internal resources.This can lead to information disclosure or manipulation of internal systems

## ◙ SEARCHSPLOIT 
  : a command line search tool for Exploit-DB that also allows you to take a copy of Exploit Database with you, everywhere you go. { It ia a command line which helps us to find all the known exploits or vulnerabilities mainly use for penetration and stuff.}

  #### • 1 SIMPLE HELP MENU
  ![image](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/4bd52e90-d7d1-4eb2-b321-8f697a9603c2)

  #### •2 SPLIOS OR VULNERABILITIES OF AN ANDROID
  ![image](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/f53634ef-5c3f-41e3-a0d3-b70aea7208c5)


### EXPLOIT DATABASE 
  : Exploit-DB is a widely recognized online public database and platform that provides information about security vulnerabilities, exploits, and their corresponding proof-of-concept code.

## ♦ Defining CVSS, CVE and NVD

• ***CVSS*** – The Common Vulnerability Scoring System (CVSS) is a system widely used in vulnerability management programs. CVSS indicates the severity of an information security vulnerability, and is an integral component of many vulnerability scanning tools.The Common Vulnerability Scoring System (aka CVSS Scores) provides a numerical (0-10) representation of the severity of an information security vulnerability. CVSS scores are commonly used by infosec teams as part of a vulnerability management program to provide a point of comparison between vulnerabilities, and to prioritize remediation of vulnerabilities.

• ***CVE*** – Common Vulnerabilities and Exposures (CVE) is a list of publicly disclosed vulnerabilities and exposures that is maintained by MITRE.Common Vulnerabilities and Exposures (CVE) is a database of publicly disclosed information security issues. A CVE number uniquely identifies one vulnerability from the list. CVE provides a convenient, reliable way for vendors, enterprises, academics, and all other interested parties to exchange information about cyber security issues. Enterprises typically use CVE, and corresponding CVSS scores, for planning and prioritization in their vulnerability management programs. 

• ***NVD*** – The National Vulnerability Database (NVD) is a database, maintained by [NIST](https://nvd.nist.gov/vuln), that is fully synchronized with the MITRE CVE list.

#### ◙ WHAT IS BRUTE-FORCE ATTACK 
  : In cryptography, a brute-force attack consists of an attacker submitting many passwords or passphrases with the hope of eventually guessing correctly. The attacker systematically checks all possible passwords and passphrases until the correct one is found.

#### ◙ WHAT IS HASH CRACKING 
  : Hash cracking is a technique used by penetration testers to recover plain text passwords from their encrypted or hashed forms. Hashes are one-way functions that transform any input into a fixed-length output, making it hard to reverse the process.{ Getting the orignal hidden text in the hash format} 

#### ◙ WHAT IS SERVICE ENUMERATION
  :  A method used to find out the service version that is available on a particular port on the target system. This version information is important, because with this information the penetration tester can search for security vulnerabilities that exist for that software version.{ To find out the available service version on targets device to find out its vulnrabilities}
