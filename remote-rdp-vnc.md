# RDP / VNC

% rdp, vnc, xfreerdp, cpts

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - rdp
#cat/ATTACK/CONNECT #cpts
To access the directory, we can connect to `\\tsclient\`, allowing us to transfer files to and from the RDP session.

```
rdesktop 10.10.10.132 -d HTB -u administrator -p 'Password0@' -r disk:linux='/home/user/rdesktop/files'
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - rdp-2
#cat/ATTACK/CONNECT #cpts
```
xfreerdp /v:10.10.10.132 /d:HTB /u:administrator /p:'Password0@' /drive:linux,/home/plaintext/htb/academy/filetransfer
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - rdp-3
#cat/ATTACK/CONNECT #cpts
![c0eb6778582d4993378c236daa3ac693.png](:/420ed224385e4eaa824f2da9286cbddc) *Enable Restricted Admin Mode to allow PtH*

```
xfreerdp /v:10.129.201.126 /u:julio /pth:64F12CDDAA88057E06A81B54E73B949B
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - connecting-via-freerdp
#cat/ATTACK/CONNECT #cpts
We can connect via command line using the command: Introduction to Active Directory Enumeration & Attacks

```
xfreerdp /v: /u:htb-student /p:Academy_student_AD!
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - xfreerdp-to-the-attack01-parrot-host
#cat/ATTACK/CONNECT #cpts
We also installed an `XRDP` server on the `ATTACK01` host to provide GUI access to the Parrot attack host. This can be used to interact with the BloodHound GUI tool which we will cover later in this section. In sections

```
xfreerdp /v: /u:htb-student /p:HTB_@cademy_stdnt!
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - rdp-login
#cat/ATTACK/CONNECT #cpts
Attacking RDP

```
1. Certificate issuer is not trusted by this system.
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - adding-the-disablerestrictedadmin-registry-key
#cat/ATTACK/CONNECT #cpts
Once the registry key is added, we can use `xfreerdp` with the option `/pth` to gain RDP access: Attacking RDP

```
[09:24:10:115] [1668:1669]
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-cflagtxt-file-on-ms01
#cat/ATTACK/CONNECT #cpts
Subsequently, students need to connect to `MS01` using RDP, having the opportunity to use drive redirection:

```
xfreerdp /v:172.16.7.50 /u:AB920 /p:weasal /drive:share,/home/htb-student/Desktop /dynamic-resolution
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-cflagtxt-file-on-ms01-2
#cat/ATTACK/CONNECT #cpts
```
shell-session
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/ATTACK/CONNECT #cpts
The hex string can be decoded to reveal the password `Sup3rS3cur3maY5ql$3rverE`. Students need to move laterally to the next machine, authenticating to 172.16.7.50 as `mssqlsvc:Sup3rS3cur3maY5ql$3rverE`:

```
xfreerdp /v:172.16.7.50 /u:mssqlsvc /p:'Sup3rS3cur3maY5ql$3rverE' /dynamic-resolution
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-2
#cat/ATTACK/CONNECT #cpts
Students need to authenticate as `CT059:charlie1` to `172.16.7.50`:

```
xfreerdp /v:172.16.7.50 /u:CT059 /p:charlie1 /dynamic-resolution
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - what-is-the-sid-of-the-child-domain
#cat/ATTACK/CONNECT #cpts
After spawning the target machine, students first need to connect to it with `xfreerdp` using the credentials `htb-student_adm:HTB_@cademy_stdnt_admin!`:

```
xfreerdp /v:STMIP /u:htb-student_adm /p:HTB_@cademy_stdnt_admin!
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-cflagtxt-file-on-ms01-3
#cat/ATTACK/CONNECT #cpts
```
┌─[✗]─[htb-student@skills-par01]─[~]
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o-3
#cat/ATTACK/CONNECT #cpts
```
┌─[htb-student@skills-par01]─[~/Desktop]
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - perform-an-analysis-of-cappsrestart-oracleserviceexe-and-identify-the-
#cat/ATTACK/CONNECT #cpts
Students need to first connect to the spawned target with the credentials `cybervaca:&aue%C)}6g-d{w` using RDP while specifying a shared drive:

```
xfreerdp /v:STMIP /u:cybervaca /p:'&aue%C)}6g-d{w' /dynamic-resolution /drive:share,/home/htb-ac-594497
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - what-is-the-ip-address-of-the-eth0-interface-under-the-serverstatus---
#cat/ATTACK/CONNECT #cpts
After spawning the target machine, students need to first connect to the target with the credentials `cybervaca:&aue%C)}6g-d{w` using RDP:

```
xfreerdp /v:STMIP /u:cybervaca /p:'&aue%C)}6g-d{w' /dynamic-resolution
```

## RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - RDP / VNC - what-is-the-hardcoded-password-for-the-database-connection-in-the-mult
#cat/ATTACK/CONNECT #cpts
After spawning the target machine, students need to connect to the target with the credentials `administrator:xcyj8izxNVzhf4z` using RDP:

```
xfreerdp /v:STMIP /u:administrator /p:xcyj8izxNVzhf4z /dynamic-resolution
```

