# Grep / Awk / Sed / cut

% grep, awk, sed, linux, cpts

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - lookign-for-interesting-files
#cat/CODE #cpts
```
for l in $(echo ".conf .config .cnf");do echo -e "\nFile extension: " $l; find / -name *$l 2>/dev/null | grep -v "lib\ | fonts\ | share\ | core" ;done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - lookign-for-interesting-files-2
#cat/CODE #cpts
```
for i in $(find / -name *.cnf 2>/dev/null | grep -v "doc\ | lib");do echo -e "\nFile: " $i; grep "user\ | password\ | pass" $i 2>/dev/null | grep -v "\#";done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - lookign-for-interesting-files-3
#cat/CODE #cpts
```
for l in $(echo ".sql .db .*db .db*");do echo -e "\nDB File extension: " $l; find / -name *$l 2>/dev/null | grep -v "doc\ | lib\ | headers\ | share\ | man";done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - lookign-for-interesting-files-4
#cat/CODE #cpts
```
find /home/* -type f -name "*.txt" -o ! -name "*.*"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - lookign-for-interesting-files-5
#cat/CODE #cpts
```
for l in $(echo ".py .pyc .pl .go .jar .c .sh");do echo -e "\nFile extension: " $l; find / -name *$l 2>/dev/null | grep -v "doc\ | lib\ | headers\ | share";done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - mounting-bitlocker-encrypted-drives-in-linux-or-macos
#cat/CODE #cpts
It is also possible to mount BitLocker-encrypted drives in Linux (or macOS). To do this, we can use a tool called dislocker. First, we need to install the package using apt:

```
bitlocker2john -i Backup.vhd > backup.hashes
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - mounting-bitlocker-encrypted-drives-in-linux-or-macos-2
#cat/CODE #cpts
It is also possible to mount BitLocker-encrypted drives in Linux (or macOS). To do this, we can use a tool called dislocker. First, we need to install the package using apt:

```
grep "bitlocker\$0" backup.hashes > backup.hash
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - mounting-bitlocker-encrypted-drives-in-linux-or-macos-3
#cat/CODE #cpts
It is also possible to mount BitLocker-encrypted drives in Linux (or macOS). To do this, we can use a tool called dislocker. First, we need to install the package using apt:

```
cat backup.hash
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - nginx
#cat/CODE #cpts
Verifying errors

```
tail -2 /var/log/nginx/error.log
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - nginx-2
#cat/CODE #cpts
Verifying errors

```
ss -lnpt | grep 80
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - nginx-3
#cat/CODE #cpts
Verifying errors

```
ps -ef | grep 2811
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - dangerous-settings
#cat/CODE #cpts
```
cat /etc/mysql/mysql.conf.d/mysqld.cnf | grep -v "#" | sed -r '/^\s*$/d'
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - online-presence
#cat/CODE #cpts
Comment trouver les IPs associées

```
for i in $(cat subdomainlist);do host $i | grep "has address" | grep <url> | cut -d" " -f1,4;done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - online-presence-2
#cat/CODE #cpts
Il est possible de **cut** l'output et de le fournir à [Shodan](/C:/Users/htg/AppData/Local/Programs/Joplin/resources/app.asar/www.shodan.io "www.shodan.io")

```
for i in $(cat subdomainlist);do host $i | grep "has address" | grep inlanefreight.com | cut -d" " -f4 >> ip-addresses.txt;done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - dangerous-settings-2
#cat/CODE #cpts
```
cat /etc/postfix/main.cf | grep -v "#" | sed -r "/^\s*$/d"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - dangerous-settings-3
#cat/CODE #cpts
```
cat /etc/snmp/snmpd.conf | grep -v "#" | sed -r '/^\s*$/d'
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - dangerous-settings-4
#cat/CODE #cpts
On Linux, settings are stored in :

```
cat /etc/samba/smb.conf | grep -v "#\ | \;"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - find-in-a-file
#cat/CODE #cpts
```
grep -rn /mnt/Finance/ -ie cred
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - enumeration
#cat/CODE #cpts
```
dig mx plaintext.do | grep "MX" | grep -v ";"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - ps---check-if-linux-machine-is-domain-joined
#cat/CODE #cpts
```
ps -ef | grep -i "winbind\ | sssd"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - reviewing-environment-variables-for-ccache-files
#cat/CODE #cpts
```
grep -i krb5
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - linux
#cat/CODE #cpts
```
for i in {1..254} ;do (ping -c 1 172.16.5.$i | grep "bytes from" &) ;done
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - linux-2
#cat/CODE #cpts
```
for i in $(seq 1 254); do (ping -c 1 172.16.5.$i | grep "bytes from") & done; wait
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - verifying-errors
#cat/CODE #cpts
Catching Files over HTTP/S

```
user65 2811 1856 0 16:05 ? 00:00:04 `python -m websockify 80 localhost:5901 -D
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - verifying-errors-2
#cat/CODE #cpts
Catching Files over HTTP/S

```
root 6720 2226 0 16:14 pts/0 00:00:00 grep --color=auto 2811
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - dig---mx-records
#cat/CODE #cpts
Attacking Email Services

```
dig mx inlanefreight.com | grep "MX" | grep -v ";"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - the-power-of-hybrid-attacks
#cat/CODE #cpts
Next, we need to start matching that wordlist to the password policy.

```
grep -E '^.{8,}$' darkweb2017_top-10000.txt > darkweb2017-minlength.txt
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - the-power-of-hybrid-attacks-2
#cat/CODE #cpts
This initial `grep` command targets the core policy requirement of a minimum password length of 8 characters. The regular expression `^.{8,}$` acts as a filter, ensuring that only passwords containing at least 8 characte

```
grep -E '[A-Z]' darkweb2017-minlength.txt > darkweb2017-uppercase.txt
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - the-power-of-hybrid-attacks-3
#cat/CODE #cpts
Building upon the previous filter, this `grep` command enforces the policy's demand for at least one uppercase letter. The regular expression `[A-Z]` ensures that any password lacking an uppercase letter is discarded, fu

```
grep -E '[a-z]' darkweb2017-uppercase.txt > darkweb2017-lowercase.txt
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - the-power-of-hybrid-attacks-4
#cat/CODE #cpts
Maintaining the filtering chain, this `grep` command ensures compliance with the policy's requirement for at least one lowercase letter. The regular expression `[a-z]` serves as the filter, keeping only passwords that in

```
grep -E '[0-9]' darkweb2017-lowercase.txt > darkweb2017-number.txt
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - cupp
#cat/CODE #cpts
We now have a generated a username list (`jane_smith_usernames.txt`) and a password list (`jane.txt`), but there is one more thing we need to deal with. CUPP has generated many possible passwords for us, but Jane's compa

```
grep -E '^.{6,}$' jane.txt | grep -E '[A-Z]' | grep -E '[a-z]' | grep -E '[0-9]' | grep -E '([!@#$%^&*].*){2,}' > jane-filtered.txt
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire
#cat/CODE #cpts
Subsequently, students need only to have content types that contain `image/`, so they need to use `grep`, copy the matching ones to the clipboard, and then paste them under "Payload Options" in `Burp Suite`:

```
cat web-all-content-types.txt | grep 'image/' | xclip -se c
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - try-to-exploit-the-upload-form-to-read-the-flag-found-at-the-root-dire-2
#cat/CODE #cpts
```
└──╼ [★]$ cat web-all-content-types.txt | grep 'image/' | xclip -se c
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-host-is-running-microsoft-sql-server-2019-1500200000-ip-address-n
#cat/CODE #cpts
Students will find out that the `172.16.5.130` host is running `Microsoft SQL Server 2019 15.00.2000.00` by reading the output of `Nmap`. However, since the output was saved to a file in the `grepable` format, students i

```
awk '/1433\/open/ {print $2}' nmapOutput
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-host-is-running-microsoft-sql-server-2019-1500200000-ip-address-n-2
#cat/CODE #cpts
```
shell-session
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - try-to-change-the-admins-email-to-flagidorhtbmailtoflagidorhtb-and-you
#cat/CODE #cpts
Students can use `grep` to filter for word "admin" after piping the results of the script:

```
bash script.sh | grep "admin" | jq .
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - try-to-escalate-your-privileges-and-exploit-different-vulnerabilities-
#cat/CODE #cpts
Since students are hunting for privileged users, they need to run the script and use `grep` to search for strings that contain `admin`, finding the user with `uid` 52:

```
bash fuzz | grep -i "admin" | jq .
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - try-to-escalate-your-privileges-and-exploit-different-vulnerabilities--2
#cat/CODE #cpts
```
└──╼ [★]$ bash fuzz | grep -i "admin" | jq .
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - find-another-valid-user-on-the-target-gitlab-instance
#cat/CODE #cpts
Students need to use the script to enumerate valid users:

```
./49821.sh --url http://gitlab.inlanefreight.local:8081 --userlist /opt/useful/SecLists/Usernames/cirt-default-usernames.txt | grep exists
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - find-another-valid-user-on-the-target-gitlab-instance-2
#cat/CODE #cpts
```
└──╼ [★]$ ./49821.sh --url http://gitlab.inlanefreight.local:8081 --userlist /opt/useful/SecLists/Usernames/cirt-default-usernames.txt | grep exists
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - list-current-processes
#cat/CODE #cpts
```
ps aux | grep root
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - unmounted-file-systems
#cat/CODE #cpts
```
cat /etc/fstab | grep -v "#" | column -t
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - installed-packages
#cat/CODE #cpts
```
apt list --installed | tr "/" " " | cut -d" " -f1,3 | sed 's/[0-9]://g' | tee -a installed_pkgs.list
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - scripts
#cat/CODE #cpts
```
find / -type f -name "*.sh" 2>/dev/null | grep -v "src\ | snap\ | share"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - running-services-by-user
#cat/CODE #cpts
```
root 784 0.4 0.5 273512 21680 ? Ssl 12:31 0:00 /usr/sbin/NetworkManager --no-daemon
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - running-services-by-user-2
#cat/CODE #cpts
```
root 790 0.0 0.0 81932 3648 ? Ssl 12:31 0:00 /usr/sbin/irqbalance --foreground
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - running-services-by-user-3
#cat/CODE #cpts
```
root 792 0.1 0.5 48244 20540 ? Ss 12:31 0:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --run-startup-triggers
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - running-services-by-user-4
#cat/CODE #cpts
```
root 889 0.1 0.5 126676 22888 ? Ssl 12:31 0:00 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade-shutdown --wait-for-signal
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - credential-hunting
#cat/CODE #cpts
* * * When enumerating a system, it is important to note down any credentials. These may be found in configuration files (`.conf`, `.config`, `.xml`, etc.), shell scripts, a user's bash history file, backup (`.bak`) file

```
:~$ grep 'DB_USER\ | DB_PASSWORD' wp-config.php
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - logrotate
#cat/CODE #cpts
However, before running the exploit, we need to determine which option `logrotate` uses in `logrotate.conf`.

```
:~$ grep "create\ | compress" /etc/logrotate.conf | grep -v "#"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - shared-object-hijacking
#cat/CODE #cpts
We see a non-standard library named `libshared.so` listed as a dependency for the binary. As stated earlier, it is possible to load shared libraries from custom locations. One such setting is the `RUNPATH` configuration.

```
:~$ readelf -d payroll | grep PATH
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - module-permissions
#cat/CODE #cpts
```
:~$ grep -r "def virtual_memory" /usr/local/lib/python3.8/dist-packages/psutil/*
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - module-permissions-2
#cat/CODE #cpts
```
:~$ ls -l /usr/local/lib/python3.8/dist-packages/psutil/__init__.py
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - sudo
#cat/CODE #cpts
* * * The program `sudo` is used under UNIX operating systems like Linux or macOS to start processes with the rights of another user. In most cases, commands are executed that are only available to administrators. It ser

```
:~$ sudo cat /etc/sudoers | grep -v "#" | sed -r '/^\s*$/d'
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - sudo-policy-bypass
#cat/CODE #cpts
In fact, `Sudo` also allows commands with specific user IDs to be executed, which executes the command with the user's privileges carrying the specified ID. The ID of the specific user can be read from the `/etc/passwd`

```
:~$ cat /etc/passwd | grep cry0l1t3
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - enumerate-the-linux-environment-and-look-for-interesting-files-that-mi
#cat/CODE #cpts
Then, students need to use the `find` command to look for bash scripts. Additionally, each of these scripts should be checked to see they contain a flag starting with "HTB" :

```
find / -name *.sh 2>/dev/null | xargs cat | grep "HTB"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - enumerate-the-linux-environment-and-look-for-interesting-files-that-mi-2
#cat/CODE #cpts
```
$ find / -name *.sh 2>/dev/null | xargs cat | grep "HTB"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target
#cat/CODE #cpts
Now, students need to retrieves a list of installed Python 3 packages by filtering the output of the `apt list --installed` command:

```
apt list --installed | tr "/" " " | cut -d" " -f1,3 | grep "^python3.[0-9][0-9] " | cut -d" " -f1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-2
#cat/CODE #cpts
```
:~$ apt list --installed | tr "/" " " | cut -d" " -f1,3 | grep "^python3.[0-9][0-9] " | cut -d" " -f1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-3
#cat/CODE #cpts
```
python3.11
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-4
#cat/CODE #cpts
Additionally, to see all installed python3 versions, students can create an `installed_pkgs.list` file and search for all instances of python3:

```
cat installed_pkgs.list | grep python3 | sort -u
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-5
#cat/CODE #cpts
```
:~$ apt list --installed | tr "/" " " | cut -d" " -f1,3 | sed 's/[0-9]://g' | tee -a installed_pkgs.list
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-6
#cat/CODE #cpts
```
:~$ cat installed_pkgs.list | grep python3 | sort -u
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-7
#cat/CODE #cpts
```
python3.11 3.11.3-1+focal1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-8
#cat/CODE #cpts
```
python3.11-minimal 3.11.3-1+focal1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-9
#cat/CODE #cpts
```
python3.8 3.8.10-0ubuntu1~20.04.7
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - what-is-the-latest-python-version-that-is-installed-on-the-target-10
#cat/CODE #cpts
```
python3.8-minimal 3.8.10-0ubuntu1~20.04.7
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - find-the-wordpress-database-password
#cat/CODE #cpts
Subsequently, students need to print out the contents of the `wp-config.php` file in `/var/www/html` and use `grep` to filter out the database password:

```
cat /var/www/html/wp-config.php | grep "DB_PASSWORD"
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - use-the-privileged-group-rights-of-the-secaudit-user-to-locate-a-flag
#cat/CODE #cpts
Students will notice that the user is part of the `adm` group, which allows reading all of the files under the directory `/var/log/`, thus, students need to use `grep` recursively on the `/var/log/` directory searching f

```
grep -rw "flag" /var/log 2>/dev/null
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - use-the-privileged-group-rights-of-the-secaudit-user-to-locate-a-flag-2
#cat/CODE #cpts
```
:~$ grep -rw "flag" /var/log 2>/dev/null
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - follow-along-with-the-examples-in-this-section-to-escalate-privileges-
#cat/CODE #cpts
Discovering that the `mem_status.py` script can be run with elevated privileges, students need to take advantage of library hijacking. Students need to identify their permissions on the `psutil` library, which contains t

```
grep -r "def virtual_memory*" /usr/
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - follow-along-with-the-examples-in-this-section-to-escalate-privileges--2
#cat/CODE #cpts
Discovering that the `mem_status.py` script can be run with elevated privileges, students need to take advantage of library hijacking. Students need to identify their permissions on the `psutil` library, which contains t

```
ls -l /usr/local/lib/python3.8/dist-packages/psutil/__init__.py
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - follow-along-with-the-examples-in-this-section-to-escalate-privileges--3
#cat/CODE #cpts
```
:~$ grep -r "def virtual_memory*" /usr/
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - submit-the-contents-of-flag4txt
#cat/CODE #cpts
Using the same SSH connection established in the previous question -with the user being `barry`\-, students need to use `netstat` to list open ports, finding 8080 listening:

```
netstat -tulpn | grep LISTEN
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - submit-the-contents-of-flag4txt-2
#cat/CODE #cpts
```
:/home/htb-student$ netstat -tulpn | grep LISTEN
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - submit-the-contents-of-flag4txt-3
#cat/CODE #cpts
```
(No info could be
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/CODE #cpts
Subsequently, students need to know the IP address of the interface that is connected to the `172.16.0.0/16` network, which is named `ens192` on `DMZ01`:

```
ip a show ens192 | grep "inet" -m 1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/CODE #cpts
```
:~# ip a show ens192 | grep "inet" -m 1
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - fluffy
#cat/CODE #cpts
extrait du PDF Joplin: fluffy

```
echo "10.10.11.69 fluffy.htb dc01.fluffy.htb" | sudo tee -a /etc/hosts
```

## Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - Grep / Awk / Sed / cut - voleur
#cat/CODE #cpts
extrait du PDF Joplin: voleur

```
echo "10.10.11.76 DC.voleur.htb voleur.htb DC" | sudo tee -a /etc/hosts
```

