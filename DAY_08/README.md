# ♦ Day 08
</br>
</br>

## ◙ ***Learning to Host a Website***
 </br>
 
# ♦ Website Hosting : 
   ⇨ In this session we will be learning how to demonstrate an e-commerce website that sells huge money bills. It includes a sleek design with a white-blue color scheme, backend functionality to log user IP addresses, and basic user authentication with a login and registration page.

   </br>
   </br>



#### • Requirements :

• Apache Web Server
• Ngrok
• Basic understanding of HTML, CSS, and PHP


### ◙ Step-By-Step Guide 


#### • 1. Installation :

1. **Download and Install Apache:**

```  bash
   sudo apt update
   sudo apt install apache2
   sudo systemctl start apache2
   sudo systemctl enable apache2
   sudo cp -r ~/Desktop/hidden_formfield/* /var/www/html/
   cd /var/www/html
   ls -la
   sudo systemctl start apache2
   ./ngrok http 80
```
#### •2. Ngrok : 

   ⇨ Ngrok is a tool that creates secure tunnels to your localhost, enabling you to expose your local server to the internet. 
   
   ⇨ [Ngrok](https://ngrok.com/)

