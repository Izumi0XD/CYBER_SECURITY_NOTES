
# ♦ Day 19
</br>
</br>

## ◙ ***Privillage Escalation with comman commands***
 </br>
 
# ♦ `Sudo` : 
   ⇨  If the binary is allowed to run as superuser by `sudo`, it does not drop the elevated privileges and may be used to access the file system, escalate or maintain privileged access.
</br>
#### Command:

      sudo sudo /bin/sh

   </br>
   </br>

### ♦ `cat` :  

   ⇨  Description: The `cat` command reads data from files and can be used to do privileged reads or disclose files outside a restricted file system. If it has the SUID bit set, it can escalate privileges.
</br>
#### Command: 

   • File Read :

    LFILE=file_to_read
    cat "$LFILE"

   • SUID :

    sudo install -m =xs $(which cat) .

    LFILE=file_to_read
    ./cat "$LFILE"

   • Sudo :

    LFILE=file_to_read
    sudo cat "$LFILE"
