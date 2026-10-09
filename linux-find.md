# Find / Findstr

% find, findstr, linux, cpts

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file
#cat/POSTEXPLOIT #cpts
```
dir n:\*cred* /s /b
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-2
#cat/POSTEXPLOIT #cpts
```
dir n:\*secret* /s /b
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-in-a-file-findstrhttpsdocsmicrosoftcomen-uswindows-serveradminist
#cat/POSTEXPLOIT #cpts
```
findstr /s /i cred n:\*.*
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-3
#cat/POSTEXPLOIT #cpts
```
Get-ChildItem -Recurse -Path N:\ -Include *cred* -File
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-in-a-file
#cat/POSTEXPLOIT #cpts
```
Get-ChildItem -Recurse -Path N:\ | Select-String "cred" -List
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-4
#cat/POSTEXPLOIT #cpts
```
find /mnt/Finance/ -name *cred*
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - using-find-to-search-for-files-with-keytab-in-the-name
#cat/POSTEXPLOIT #cpts
```
find / -name *keytab* -ls 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - using-find-to-search-for-files-with-keytab-in-the-name-2
#cat/POSTEXPLOIT #cpts
```
262169 4 -rw-rw-rw- 1 root root 216 Oct 12 15:13 /opt/specialfiles/carlos.keytab
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - confirming-the-socks-listener-is-started
#cat/POSTEXPLOIT #cpts
```
TCP 127.0.0.1:1080 0.0.0.0:0 LISTENING
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - background
#cat/POSTEXPLOIT #cpts
There are indeed processes running in the context of the `backupadm` user, such as `wsmprovhost.exe`, which is the process that spawns when a Windows Remote PowerShell session is spawned. Kerberos "Double Hop" Problem

```
[DEV01]: PS C:\Users\Public> tasklist /V | findstr backupadm
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - windows-cmd---findstr
#cat/POSTEXPLOIT #cpts
Interacting with Common Services

```
n:\Contracts\private\secret.txt:file with all credentials
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - assess-the-web-application-and-use-a-variety-of-techniques-to-gain-rem
#cat/POSTEXPLOIT #cpts
Students will begin by spawning the target machine. Once it's active, they will use Firefox to navigate to `http://STMIP:STMPO`, ensuring that `Burp Suite` is running and properly configured to proxy the traffic. This se

```
echo '' > shell.php
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - assess-the-web-application-and-use-a-variety-of-techniques-to-gain-rem-2
#cat/POSTEXPLOIT #cpts
```
bash-session
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - while-looking-at-inlanefreights-public-records-a-flag-can-be-seen-find
#cat/POSTEXPLOIT #cpts
There are multiple methods that students can utilize to find the flag. The first method is whereby students search on [Hurricane Electric](https://bgp.he.net/) for `inlanefreight.com` and check the `TXT` record to find `

```
nslookup -type=TXT inlanefreight.com
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - while-looking-at-inlanefreights-public-records-a-flag-can-be-seen-find-2
#cat/POSTEXPLOIT #cpts
```
shell-session
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - using-the-examples-shown-in-this-section-find-a-user-with-the-password-2
#cat/POSTEXPLOIT #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
Import-Module .\DomainPasswordSpray.ps1
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - utilizing-techniques-learned-in-this-section-find-the-flag-hidden-in-t
#cat/POSTEXPLOIT #cpts
Using the same `RDP` session established from question 1 of this section, students need to run `PowerShell` as administrator then run `dsquery`, attaining the flag `HTB{LD@P_I$_W1ld}` in the description field of the acco

```
dsquery * -filter "(&(objectCategory=user)(userAccountControl:1.2.840.113556.1.4.803:=2)(adminCount=1)(description=*))" -limit 5 -attr SAMAccountName description
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - elf-executable-examination
#cat/POSTEXPLOIT #cpts
The binary probably connects using a SQL connection string that contains credentials. Using tools like [PEDA](https://github.com/longld/peda) (Python Exploit Development Assistance for GDB) we can further examine the fil

```
Find the GDB manual and other documentation resources online at:
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - elf-executable-examination-2
#cat/POSTEXPLOIT #cpts
The binary probably connects using a SQL connection string that contains credentials. Using tools like [PEDA](https://github.com/longld/peda) (Python Exploit Development Assistance for GDB) we can further examine the fil

```
(No debugging symbols found in ./octopus_checker)
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-the-password-for-the-admin-user-on-httpappinlanefreightlocal
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo python3 joomla-bruteforce/joomla-brute.py -u http://app.inlanefreight.local -w /usr/share/metasploit-framework/data/wordlists/http_default_pass.txt -usr admin
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - leverage-the-directory-traversal-vulnerability-to-find-a-flag-in-the-r
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP dev.inlanefreight.local` Then, students need to navigate to `http://dev.inlanefreight.lo

```
php
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - leverage-the-directory-traversal-vulnerability-to-find-a-flag-in-the-r-2
#cat/POSTEXPLOIT #cpts
At last, students will be able to print out the flag file "flag_6470e394cbf6dab6a91682cc8585059b.txt", which is under the directory `/var/www/dev.inlanefreight.local/`:

```
cat ../../flag_6470e394cbf6dab6a91682cc8585059b.txt
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-writable-directories
#cat/POSTEXPLOIT #cpts
```
find / -path /proc -prune -o -type d -perm -o+w 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-writable-files
#cat/POSTEXPLOIT #cpts
```
find / -path /proc -prune -o -type f -perm -o+w 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-with-the-setuid-bit-set-that-was-not-shown-in-the-section-
#cat/POSTEXPLOIT #cpts
Students subsequently need to search for binaries with the `SETUID` bit on using `find`:

```
find / -user root -perm -4000 -exec ls -ldb {} \; 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-with-the-setgid-bit-set-that-was-not-shown-in-the-section-
#cat/POSTEXPLOIT #cpts
Using the same SSH connection from the previous question, students need to use `find` to find binaries with the `SETGID` bit on:

```
find / -user root -perm -6000 -exec ls -ldb {} \; 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-file-with-the-setgid-bit-set-that-was-not-shown-in-the-section--2
#cat/POSTEXPLOIT #cpts
```
:~$ find / -user root -perm -6000 -exec ls -ldb {} \; 2>/dev/null
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - passing-credentials-to-wevtutil
#cat/POSTEXPLOIT #cpts
```
cmd-session
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - executing-systempropertiesadvancedexe-on-target-host
#cat/POSTEXPLOIT #cpts
Before proceeding, we should ensure that any instances of the `rundll32` process from our previous execution have been terminated.

```
rundll32.exe 6300 N/A
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - executing-systempropertiesadvancedexe-on-target-host-2
#cat/POSTEXPLOIT #cpts
Before proceeding, we should ensure that any instances of the `rundll32` process from our previous execution have been terminated.

```
rundll32.exe 5360 N/A
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - executing-systempropertiesadvancedexe-on-target-host-3
#cat/POSTEXPLOIT #cpts
Before proceeding, we should ensure that any instances of the `rundll32` process from our previous execution have been terminated.

```
rundll32.exe 7044 N/A
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - performing-attack-and-parsing-password-hashes
#cat/POSTEXPLOIT #cpts
This [PoC](https://github.com/GossiTheDog/HiveNightmare) can be used to perform the attack, creating copies of the aforementioned registry hives:

```
HiveNightmare v0.6 - dump registry hives as non-admin users
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-banner-grab-of-the-services-listening-on-the-target-host-and
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry `STMIP inlanefreight.local` to the `/etc/hosts` file, as it will be needed for all of the questions for this section:

```
sudo sh -c 'echo "STMIP inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-banner-grab-of-the-services-listening-on-the-target-host-and-2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.197.76 inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit-
#cat/POSTEXPLOIT #cpts
(Students need to make sure that the `STMIP inlanefreight.local` entry is present in `/etc/hosts`, as done in Question 1.) Students need to perform a DNS Zone Transfer using `dig` on the `inlanefreight.local` domain, to

```
dig AXFR inlanefreight.local @STMIP
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--2
#cat/POSTEXPLOIT #cpts
```
DiG 9.16.15-Debian axfr inlanefreight.local @10.129.197.76
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--3
#cat/POSTEXPLOIT #cpts
```
global options: +cmd
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--4
#cat/POSTEXPLOIT #cpts
```
Query time: 88 msec
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--5
#cat/POSTEXPLOIT #cpts
```
SERVER: 10.129.197.76#53(10.129.197.76)
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--6
#cat/POSTEXPLOIT #cpts
```
WHEN: Wed Aug 10 09:49:04 BST 2022
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - perform-a-dns-zone-transfer-against-the-target-and-find-a-flag-submit--7
#cat/POSTEXPLOIT #cpts
```
XFR size: 14 records (messages 1, bytes 448)
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - enumerate-the-accessible-services-and-find-a-flag-submit-the-flag-valu
#cat/POSTEXPLOIT #cpts
Subsequently, students need to download the flag file "flag.txt" using `get` then print its contents out, to attain `HTB{0eb0ab788df18c3115ac43b1c06ae6c4}`:

```
get flag.txt
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-idor-vulnerability-to-find-a-flag-submit-the-flag-value-as-you
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry `STMIP careers.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP careers.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-idor-vulnerability-to-find-a-flag-submit-the-flag-value-as-you-2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 careers.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - exploit-the-http-verb-tampering-vulnerability-to-find-a-flag-submit-th
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry "`STMIP dev.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP dev.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - exploit-the-http-verb-tampering-vulnerability-to-find-a-flag-submit-th-2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 dev.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit-
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry `STMIP ir.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP ir.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit--2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 ir.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit--3
#cat/POSTEXPLOIT #cpts
Afterward, students need to navigate to `http://ir.inlanefreight.local/wp-content/themes/twentytwenty/404.php` so that the PHP reverse shell code is executed: (Students can choose to upgrade the dumb TTY terminal to an i

```
cat /var/www/html/flag.txt
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-ssrf-to-local-file-read-vulnerability-to-find-a-flag-submit-th
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry `STMIP tracking.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP tracking.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-ssrf-to-local-file-read-vulnerability-to-find-a-flag-submit-th-2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 tracking.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-ssrf-to-local-file-read-vulnerability-to-find-a-flag-submit-th-3
#cat/POSTEXPLOIT #cpts
Subsequently, students need to navigate to `http://tracking.inlanefreight.local` and inject the "Track Now" field with a JavaScript payload that will trigger an SSRF to read a local file from the system, "flag.txt" in th

```
javascript
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-xxe-vulnerability-to-find-a-flag-submit-the-flag-value-as-your
#cat/POSTEXPLOIT #cpts
After adding the VHost entry, students need to navigate to `http://shopdev2.inlanefreight.local`, for which they will be prompted to enter a username and password. As explained in the module's section, weak credentials a

```
undefined
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root
#cat/POSTEXPLOIT #cpts
After spawning the target machine, students need to add the entry `STMIP monitoring.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP monitoring.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root-2
#cat/POSTEXPLOIT #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 monitoring.inlanefreight.local" >> /etc/hosts'
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root-3
#cat/POSTEXPLOIT #cpts
Thereafter, students need to use these credentials to login: Once logged in, students will find a terminal that contains three text files "todo.txt", "note.txt", and "contact.txt". Reading the contents of the files provi

```
HTTP
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/POSTEXPLOIT #cpts
Students then need to use `xfreerdp` on 127.0.0.1 and `PWNPO` that was specified in the set local port forward, supply the credentials `hporter:Gr8hambino!` (which were found by dumping LSA secrets in Question 1 of `Expl

```
xfreerdp /v:127.0.0.1:PWNPO /u:hporter /p:Gr8hambino! /drive:home,$(pwd)
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/POSTEXPLOIT #cpts
Once successfully connected to the Windows target (`xfreerdp` might seem to to be hanging, however, it is not but takes some time), students need to change directories to `C:\Share`, and use the `net use` command to see

```
cd C:\Share
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-3
#cat/POSTEXPLOIT #cpts
Once successfully connected to the Windows target (`xfreerdp` might seem to to be hanging, however, it is not but takes some time), students need to change directories to `C:\Share`, and use the `net use` command to see

```
net use
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-4
#cat/POSTEXPLOIT #cpts
Then, students need to run `Snaffler`, to notice from its output that there is a share of the name "Department Shares":

```
.\Snaffler.exe -s -d inlanefreight.local -o snaffler.log -v data
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-5
#cat/POSTEXPLOIT #cpts
```
` ``;;;;, `;;; ;;`;; ;;;'''' ;;;'''' ;;; ;;;;'''' ;;;;``
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-6
#cat/POSTEXPLOIT #cpts
After `crackmapexec` finishes enumerating the share, students need to print the JSON file `/tmp/cme_spider_plus/172.16.8.3.json` and investigate the files that were discovered:

```
cat /tmp/nxc_hosted/nxc_spider_plus/172.16.8.3.json
```

## Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - Find / Findstr - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-7
#cat/POSTEXPLOIT #cpts
After downloading the PowerShell script successfully, students need to print its contents out to find the password `!qazXSW@`:

```
cat IT\\Private\\Development\\SQL\ Express\ Backup.ps1
```

