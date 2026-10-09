# Nmap

% nmap, recon, scan, cpts

## Nmap - Nmap - Nmap - Nmap - Nmap - testssl
#cat/RECON #cpts
à test

```
$lang=FIXMEfr-en;$client=FIXME;$mission=FIXME;ssh phoenix 'lang=$lang;client=$client;mission=$mission;mkdir -p /home/htg/missions/$client/$mission; for url in $(urls); do /opt/testssl.sh-3.0.8/testssl.sh --log --jsonfile-pretty "/home/htg/missions/$client/$mission/<url>.json" --phone-out -E --full <url> && python3 /opt/auto-system-master/ssl-tls/testssl-to-xls-v2.0.py -i "/home/htg/missions/$client/$mission/<url>.json" -o "/home/htg/missions/$client/$mission/<url>.xls" -l "$lang"; done;nmap -A -iL urls -oA /home/htg/missions/$client/$mission/nmap-a; nmap -sU -sV -iL urls -oA /home/htg/missions
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-range
#cat/RECON #cpts
```
sudo nmap 10.129.2.0/24 -sn -oA tnet | grep for | cut -d" " -f5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-range-2
#cat/RECON #cpts
```
sudo nmap -sn -oA tnet 10.129.2.18-20 | grep for | cut -d" " -f5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-list
#cat/RECON #cpts
```
sudo nmap -sn -oA tnet -iL hosts.lst | grep for | cut -d" " -f5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-multiple-ips
#cat/RECON #cpts
```
sudo nmap -sn -oA tnet 10.129.2.18 10.129.2.19 10.129.2.20 | grep for | cut -d" " -f5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - find-a-specific
#cat/RECON #cpts
```
locate scripts/smb
```

## Nmap - Nmap - Nmap - Nmap - Nmap - reporting
#cat/RECON #cpts
![aa02219f1584cb0c6c4ffe5c178c4c83.png](:/6aeacb41917045578fb5d0dbb6b5292a)

```
xsltproc target.xml -o target.html
```

## Nmap - Nmap - Nmap - Nmap - Nmap - network-monitoring
#cat/RECON #cpts
TCPDUMP

```
sudo tcpdump -i eth0 host 10.10.14.2 and 10.129.2.28
```

## Nmap - Nmap - Nmap - Nmap - Nmap - import-nmap-xml-file
#cat/RECON #cpts
```
db_import
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap
#cat/RECON #cpts
```
db_nmap
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap-2
#cat/RECON #cpts
```
/opt/auto-system-master/flow-matrix/port-scanners-to-matrix.py -i aew.preprod.upsideo.fr.2.xml -o aew.preprod.upsideo.fr.ports.xls -t nmap
```

## Nmap - Nmap - Nmap - Nmap - Nmap - ike---udp500
#cat/RECON #cpts
```
ike-scan -M -A <target>
```

## Nmap - Nmap - Nmap - Nmap - Nmap - ike---udp500-2
#cat/RECON #cpts
```
ike-scan -A --pskcrack <target>
```

## Nmap - Nmap - Nmap - Nmap - Nmap - ike---udp500-3
#cat/RECON #cpts
```
psk-crack hashfile.txt --dictionary <file>
```

## Nmap - Nmap - Nmap - Nmap - Nmap - testing-proxy-routing-functionality
#cat/RECON #cpts
```
Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
```

## Nmap - Nmap - Nmap - Nmap - Nmap - traffic-routing-through-iptables-routes
#cat/RECON #cpts
```
sudo nmap -v -A -sT -p3389 172.16.5.19 -Pn
```

## Nmap - Nmap - Nmap - Nmap - Nmap - proxychaining-through-the-icmp-tunnel
#cat/RECON #cpts
```
3389/tcp open ms-wbt-server Microsoft Terminal Services
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap-3
#cat/RECON #cpts
```
sudo nmap -v -A -iL hosts.txt -oN /home/htb-student/Documents/host-enum
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap-result-highlights
#cat/RECON #cpts
Initial Enumeration of the Domain

```
53/tcp open domain Simple DNS Plus
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap-result-highlights-2
#cat/RECON #cpts
Our scans have provided us with the naming standard used by NetBIOS and DNS, we can see some hosts have RDP open, and they have pointed us in the direction of the primary `Domain Controller` for the INLANEFREIGHT.LOCAL d

```
80/tcp open http Microsoft IIS httpd 7.5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cme-options-smb
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
crackmapexec smb -h
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cme-options-smb-2
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
[--sam | --lsa | --ntds [{drsuapi,vss}]] [--shares] [--sessions] [--disks] [--loggedon-users] [--users [USER]]
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cme-options-smb-3
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
[--pattern PATTERN [PATTERN ...] | --regex REGEX [REGEX ...]] [--depth DEPTH] [--only-files]
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cme-options-smb-4
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
[--no-output] [-x COMMAND | -X PS_COMMAND] [--obfs] [--amsi-bypass FILE] [--clear-obfscripts]
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cme-options-smb-5
#cat/RECON #cpts
Credentialed Enumeration - from Linux

```
k, --kerberos Use Kerberos authentication from ccache file (KRB5CCNAME)
```

## Nmap - Nmap - Nmap - Nmap - Nmap - scanning-the-pivot-target
#cat/RECON #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
22/tcp open ssh
```

## Nmap - Nmap - Nmap - Nmap - Nmap - confirming-port-forward-with-nmap
#cat/RECON #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
NSE: Loaded 45 scripts for scanning.
```

## Nmap - Nmap - Nmap - Nmap - Nmap - using-nmap-with-proxychains
#cat/RECON #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
Initiating Ping Scan at 12:30
```

## Nmap - Nmap - Nmap - Nmap - Nmap - nmap-4
#cat/RECON #cpts
Attacking FTP

```
sudo nmap -sC -sV -p 21 192.168.2.142
```

## Nmap - Nmap - Nmap - Nmap - Nmap - ftp-bounce-attack
#cat/RECON #cpts
An FTP bounce attack is a network attack that uses FTP servers to deliver outbound traffic to another device on the network. The attacker uses a `PORT` command to trick the FTP connection into running commands and gettin

```
FTP command misalignment detected ... correcting.
```

## Nmap - Nmap - Nmap - Nmap - Nmap - enumeration
#cat/RECON #cpts
Depending on the SMB implementation and the operating system, we will get different information using `Nmap`. Keep in mind that when targetting Windows OS, version information is usually not included as part of the Nmap

```
sudo nmap 10.129.14.128 -sV -sC -p139,445
```

## Nmap - Nmap - Nmap - Nmap - Nmap - banner-grabbing
#cat/RECON #cpts
Attacking SQL Databases

```
Host discovery disabled (-Pn). All addresses will be marked 'up', and scan times will be slower.
```

## Nmap - Nmap - Nmap - Nmap - Nmap - enumeration-2
#cat/RECON #cpts
DNS holds interesting information for an organization. As discussed in the Domain Information section in the [Footprinting module](https://academy.hackthebox.com/course/preview/footprinting), we can understand how a comp

```
53/tcp open domain ISC BIND 9.11.3-1ubuntu1.2 (Ubuntu Linux)
```

## Nmap - Nmap - Nmap - Nmap - Nmap - host---a-records
#cat/RECON #cpts
These `MX` records indicate that the first three mail services are using a cloud services G-Suite (aspmx.l.google.com), Microsoft 365 (microsoft-com.mail.protection.outlook.com), and Zoho (mx.zoho.com), and the last one

```
sudo nmap -Pn -sV -sC -p25,143,110,465,587,993,995 10.129.14.128
```

## Nmap - Nmap - Nmap - Nmap - Nmap - open-relay
#cat/RECON #cpts
From an attacker's standpoint, we can abuse this for phishing by sending emails as non-existing users or spoofing someone else's email. For example, imagine we are targeting an enterprise with an open relay mail server,

```
25/tcp open smtp
```

## Nmap - Nmap - Nmap - Nmap - Nmap - submit-the-contents-of-the-cflagtxt-file-on-ms01
#cat/RECON #cpts
Students need to run `Nmap` to discover more hosts in the `172.16.7.0/24` subnet:

```
sudo nmap -p 88,445,3389 --open 172.16.7.0/24
```

## Nmap - Nmap - Nmap - Nmap - Nmap - submit-the-contents-of-the-cflagtxt-file-on-ms01-2
#cat/RECON #cpts
```
└──╼$ sudo nmap -p 88,445,3389 --open 172.16.7.0/24
```

## Nmap - Nmap - Nmap - Nmap - Nmap - submit-the-contents-of-the-cflagtxt-file-on-ms01-3
#cat/RECON #cpts
```
└──╼ $nmap -A 172.16.7.50
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-is-the-value-of-the-flag-cookie
#cat/RECON #cpts
```
└──╼ [★]$ nc -nvlp 9001
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-your-scans-what-is-the-commonname-of-host-1721655
#cat/RECON #cpts
Students then need to perform an `Nmap` scan against the host `172.16.5.5`. Under port 3389, students will find that the `SSL-Cert` has the `fully qualified name` of the host as `ACADEMY-EA-DC01.INLANEFREIGHT.LOCAL`:

```
sudo nmap -A -v -Pn 172.16.5.5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - from-your-scans-what-is-the-commonname-of-host-1721655-2
#cat/RECON #cpts
```
└──╼ $sudo nmap -A -v -Pn 172.16.5.5
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-host-is-running-microsoft-sql-server-2019-1500200000-ip-address-n
#cat/RECON #cpts
Using the same SSH connection established in the previous question, students need to perform an `Nmap` scan against the entire `172.16.5.0/23` subnet; for easier finding of the SQL Server, the output of `Nmap` will be sa

```
sudo nmap -A -Pn -T5 -oG ./nmapOutput 172.16.5.0/23
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-host-is-running-microsoft-sql-server-2019-1500200000-ip-address-n-2
#cat/RECON #cpts
```
└──╼ $sudo nmap -A -Pn -T5 -oG ./nmapOutput 172.16.5.0/23
```

## Nmap - Nmap - Nmap - Nmap - Nmap - initial-enumeration
#cat/RECON #cpts
We can start with an Nmap scan of common web ports. I'll typically do an initial scan with ports `80,443,8000,8080,8180,8888,10000` and then run either EyeWitness or Aquatone (or both depending on the results of the firs

```
sudo nmap -p 80,443,8000,8080,8180,8888,10000 --open -oA web_discovery -iL scope_list
```

## Nmap - Nmap - Nmap - Nmap - Nmap - initial-enumeration-2
#cat/RECON #cpts
As we can see, we identified several hosts running web servers on various ports. From the results, we can infer that one of the hosts is Windows and the remainder are Linux (but cannot be 100% certain at this stage). Pay

```
sudo nmap --open -sV 10.129.201.50
```

## Nmap - Nmap - Nmap - Nmap - Nmap - using-eyewitness
#cat/RECON #cpts
or clone the [repository](https://github.com/FortyNorthSecurity/EyeWitness), navigate to the `Python/setup` directory and run the `setup.sh` installer script. EyeWitness can also be run from a Docker container, and a Win

```
eyewitness -h
```

## Nmap - Nmap - Nmap - Nmap - Nmap - using-aquatone
#cat/RECON #cpts
In this example, we provide the tool the same `web_discovery.xml` Nmap output specifying the `-nmap` flag, and we're off to the races.

```
cat web_discovery.xml | ./aquatone -nmap
```

## Nmap - Nmap - Nmap - Nmap - Nmap - cve-2020-1938-ghostcat
#cat/RECON #cpts
Tomcat was found to be vulnerable to an unauthenticated LFI in a semi-recent discovery named [Ghostcat](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-1938). All Tomcat versions before 9.0.31, 8.5.51, and 7.0.10

```
8009/tcp open ajp13 Apache Jserv (Protocol v1.3)
```

## Nmap - Nmap - Nmap - Nmap - Nmap - discoveryfootprinting
#cat/RECON #cpts
Splunk is prevalent in internal networks and often runs as root on Linux or SYSTEM on Windows systems. While uncommon, we may encounter Splunk externally facing at times. Let's imagine that we uncover a forgotten instanc

```
sudo nmap -sV 10.129.201.50
```

## Nmap - Nmap - Nmap - Nmap - Nmap - discoveryfootprintingenumeration
#cat/RECON #cpts
We can quickly discover PRTG from an Nmap scan. It can typically be found on common web ports such as 80, 443, or 8080. It is possible to change the web interface port in the Setup section when logged in as an admin.

```
sudo nmap -sV -p- --open -T4 10.129.201.50
```

## Nmap - Nmap - Nmap - Nmap - Nmap - discoveryfootprintingenumeration-2
#cat/RECON #cpts
We can quickly discover PRTG from an Nmap scan. It can typically be found on common web ports such as 80, 443, or 8080. It is possible to change the web interface port in the Setup section when logged in as an admin.

```
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
```

## Nmap - Nmap - Nmap - Nmap - Nmap - use-what-youve-learned-from-this-section-to-generate-a-report-with-eye
#cat/RECON #cpts
Subsequently, students need to run an `Nmap` scan, passing the scope list file for the `-iL` parameter, and saving the output using all formats:

```
sudo nmap STMIP -p 80,443,8000,8080,8180,8888,10000 --open -oA webDiscovery -iL scopeList
```

## Nmap - Nmap - Nmap - Nmap - Nmap - use-what-youve-learned-from-this-section-to-generate-a-report-with-eye-2
#cat/RECON #cpts
```
└──╼ [★]$ sudo nmap 10.129.42.195 -p 80,443,8000,8080,8180,8888,10000 --open -oA webDiscovery -iL scopeList
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-does-the-header-on-title-page-say-when-opening-the-aquatone_repor
#cat/RECON #cpts
Using the same output file "webDiscovery.xml" generated by `Nmap` in the previous question, students need to feed it into `aquatone`:

```
cat webDiscovery.xml | aquatone -nmap
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-does-the-header-on-title-page-say-when-opening-the-aquatone_repor-2
#cat/RECON #cpts
```
└──╼ [★]$ cat webDiscovery.xml | aquatone -nmap
```

## Nmap - Nmap - Nmap - Nmap - Nmap - enumerate-the-splunk-instance-as-an-unauthenticated-user-submit-the-ve
#cat/RECON #cpts
```
└──╼ [★]$ nmap -A -Pn 10.129.201.50
```

## Nmap - Nmap - Nmap - Nmap - Nmap - after-running-the-url-encoded-whoami-payload-what-user-is-tomcat-runni
#cat/RECON #cpts
```
└──╼ [★]$ nmap -p- -sC -Pn 10.129.205.30 --open
```

## Nmap - Nmap - Nmap - Nmap - Nmap - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the
#cat/RECON #cpts
```
└──╼ [★]$ sudo nc -lvnp 7777
```

## Nmap - Nmap - Nmap - Nmap - Nmap - what-user-is-coldfusion-running-as
#cat/RECON #cpts
```
shell-session
```

## Nmap - Nmap - Nmap - Nmap - Nmap - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t
#cat/RECON #cpts
```
└──╼ [★]$ nc -nvlp 9001 &
```

## Nmap - Nmap - Nmap - Nmap - Nmap - connect-to-the-target-system-and-escalate-privileges-by-abusing-the-mi
#cat/RECON #cpts
```
└──╼ [★]$ sudo nc -nvlp 443
```

## Nmap - Nmap - Nmap - Nmap - Nmap - perform-a-banner-grab-of-the-services-listening-on-the-target-host-and
#cat/RECON #cpts
Subsequently, students need to use `Nmap` to enumerate the services running on the target, finding the flag `1337_HTB_DNS` as the version of `BIND`:

```
sudo nmap -sC -sV inlanefreight.local
```

## Nmap - Nmap - Nmap - Nmap - Nmap - perform-a-banner-grab-of-the-services-listening-on-the-target-host-and-2
#cat/RECON #cpts
```
└──╼ [★]$ sudo nmap -sC -sV inlanefreight.local
```

## Nmap - Nmap - Nmap - Nmap - Nmap - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory
#cat/RECON #cpts
```
└──╼ [★]$ nc -nvlp 8443
```

## Nmap - Nmap - Nmap - Nmap - Nmap - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory-2
#cat/RECON #cpts
```
└──╼ [★]$ nc -nvlp 4443
```

## Nmap - Nmap - Nmap - Nmap - Nmap - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your
#cat/RECON #cpts
```
└──╼ [★]$ proxychains nmap -sT -p 21,22,80,8080 172.16.8.120 -Pn
```

## Nmap - Nmap - Nmap - Nmap - Nmap - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt-
#cat/RECON #cpts
```
└──╼ [★]$ proxychains nmap -sT -p22 172.16.9.25
```

## Nmap - Nmap - Nmap - Nmap - Nmap - krb_ap_err_skew
#cat/RECON #cpts
```
impacket.krb5.kerberosv5.KerberosError: Kerberos SessionError: KRB_AP_ERR_SKEW(Clock skew too great)
```

## Nmap - Nmap - Nmap - Nmap - Nmap - krb_ap_err_skew-2
#cat/RECON #cpts
```
ntpdate -u <target> 2026-04-09 02:48:40.63505 (+0200) +25199.773727 +/- 0.008852 10.129.232.88 s1 no-leap CLOCK: step_systime: Operation not permitted
```

## Nmap - Nmap - Nmap - Nmap - Nmap - krb_ap_err_skew-3
#cat/RECON #cpts
```
faketime -f +25199s impacket-getTGT
```

## Nmap - Nmap - Nmap - Nmap - Nmap - dante-dante-sql01-1721615
#cat/RECON #cpts
```
21/tcp open ftp FileZilla ftpd
```

## Nmap - Nmap - Nmap - Nmap - Nmap - vulncicada
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
nmap -p <port>s -sC -sV 10.129.234.48 PORT STATE SERVICE VERSION 53 /tcp open domain Simple DNS Plus 80 /tcp open http Microsoft IIS httpd 10.0 | _http-title: IIS Windows Server | _http-server-header: Microsoft-IIS/10.0 | http-methods: | _ Potentially risky methods: TRACE 88 /tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2025 -07-23 10 :13:51Z) 111 /tcp open rpcbind 2 -4 (RPC #100000) 135 /tcp open msrpc Microsoft Windows RPC 139 /tcp open netbios-ssn Microsoft Windows netbios-ssn 389 /tcp open ldap Microsoft Windows Active Directory LDAP (Domain: cicada.vl0., Site: Defau
```

## Nmap - Nmap - Nmap - Nmap - Nmap - vulncicada-2
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
ntpdate -u cicada.vl
```

## Nmap - Nmap - Nmap - Nmap - Nmap - redelegate
#cat/RECON #cpts
extrait du PDF Joplin: redelegate

```
nmap -Pn -p <port>s -sC -sV 10.129.234.50 Starting Nmap 7.95 ( https://nmap.org ) at 2025 -05-30 14 :50 BST Nmap scan report for 10.129.234.50 Host is up (0.013s latency). PORT STATE SERVICE VERSION 21 /tcp open ftp Microsoft ftpd | ftp-syst: | _ SYST: Windows_NT | ftp-anon: Anonymous FTP login allowed (FTP code 230 ) | 10 -20-24 01 :11AM 434 CyberAudit.txt | 10 -20-24 05 :14AM 2622 Shared.kdbx | _10-20-24 01 :26AM 580 TrainingAgenda.txt 53 /tcp open domain Simple DNS Plus 80 /tcp open http Microsoft IIS httpd 10.0 | _http-server-header: Microsoft-IIS/10.0 | _http-title: IIS Windows Server | ht
```

## Nmap - Nmap - Nmap - Nmap - Nmap - unrested
#cat/RECON #cpts
extrait du PDF Joplin: unrested

```
$TF :/$ sudo nmap --script=$TF Script mode is disabled for security reasons. :/$ #!/bin/bash ################################# ## Restrictive nmap for Zabbix ## #################################
```

## Nmap - Nmap - Nmap - Nmap - Nmap - freelancer
#cat/RECON #cpts
extrait du PDF Joplin: freelancer

```
nmap -Pn -T4 --top-ports 1000 --privileged -sV -A 10.129.20.59 Starting Nmap 7.92 ( https://nmap.org ) at 2024-09-20 08:30 MDT Nmap scan report for freelancer.htb (10.129.20.59) Host is up (0.055s latency). Not shown: 988 filtered tcp ports (no-response) PORT STATE SERVICE VERSION
```

## Nmap - Nmap - Nmap - Nmap - Nmap - pandora
#cat/RECON #cpts
extrait du PDF Joplin: pandora

```
nmap -sU 10.10.11.136 Let us move on to enumerating the UDP port 161 running the SNMP service. SNMP What is SNMP protocol? SNMP stands for Simple Network Management Protocol. It provides a framework for asking a device about its performance and configuration. It is used to manage and monitor all the devices connected over a network. It exposes management data in the form of variables on the managed systems. These variables can then be remotely queried. Let us use this command-line utility known as snmpwalk to scan the SNMP service and obtain all variables of the managed systems and displays t
```

