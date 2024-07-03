# ♦ Day 10
</br>
</br>

## ◙ ***TRYHACKME ROOM***
 </br>
 
# ♦ [RootMe](https://tryhackme.com/r/room/rrootme) : 
   ⇨ A ctf for beginners, can you root me? 
   </br>
   </br>
### ◙ Step-By-Step Guide 



### • 1. Start yor machine and set up your Vpn and stuff as shown in previous Repo's

### • 2. AS the Task 2 is asking for how many ports are iopen so we are exactly gonna scan the ports and this process of gathering informations bya scanning and stuff is is also known as ***RECONNAISSANCE*** as like a professional name for doint scanning and stuff. Anyway we will do scanning using nmap and cammaod for taht is :
    nmap -sV >IP add<
</br>
⇨ as we can see that the there are 2 services are alive 
     Service   Version 
  1.  ssh    - OpenSSH               (Secure Shell) </br>
  2.  http   - Apache httpd 2.4.29   (Hypertext Transfer Protocol).


### • 3. Thw next task is to find hidden directory as we already know that for finding hidden directories we use ***gobuster***.
    gobuster dir -u >IP add< -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

⇨ As we can see that there are 5 hidden directories in total whaich are as
1. /css -  just a basic css page.
2. /js  -  is a java script page.
3. /uplaods  -  a page where all the uplaoded file are being stored.
4. /panel  -  an interface based page where we can uplaod files.
5. /server  -  a permission denied page.
