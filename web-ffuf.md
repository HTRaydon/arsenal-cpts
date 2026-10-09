# Ffuf

% ffuf, web, fuzzing, cpts

## Ffuf - Ffuf - Ffuf - Ffuf - subdomain-discovery
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -u http://pov.htb -H "Host: FUZZ.pov.htb" -ac
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u "http://<target>/FUZZ"
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-2
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/web-extensions.txt:FUZZ -u "http://<target>/indexFUZZ"
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-3
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u "http://<target>/FUZZ.php"
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-4
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u "http://<target>/FUZZ" -recursion -recursion-depth 1 -e .php -v
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-5
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/DNS/subdomains-top1million-5000.txt:FUZZ -u https://FUZZ.<target>/
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-6
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/DNS/subdomains-top1million-5000.txt:FUZZ -u http://<target>/ -H "Host: FUZZ.<target>"
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-7
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/burp-parameter-names.txt:FUZZ -u "http://<target>/admin/admin.php?FUZZ=key" -fs xxx
```

## Ffuf - Ffuf - Ffuf - Ffuf - ffuf-8
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /opt/my-resources/SecLists/Discovery/Web-Content/burp-parameter-names.txt:FUZZ -u "http://<target>/admin/admin.php" -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' -fs xxx
```

## Ffuf - Ffuf - Ffuf - Ffuf - custom-wordlist
#cat/ATTACK/INJECTION #cpts
```
for i in $(seq 1 1000); do echo $i >> ids.txt; done
```

## Ffuf - Ffuf - Ffuf - Ffuf - fuzzing-for-php-files
#cat/ATTACK/INJECTION #cpts
The first step would be to fuzz for different available PHP pages with a tool like `ffuf` or `gobuster`, as covered in the [Attacking Web Applications with Ffuf](https://academy.hackthebox.com/app/module/54) module:

```
ffuf -w /opt/useful/seclists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u http://<ip>:<port>/FUZZ.php
```

## Ffuf - Ffuf - Ffuf - Ffuf - fuzzing-parameters
#cat/ATTACK/INJECTION #cpts
The HTML forms users can use on the web application front-end tend to be properly tested and well secured against different web attacks. However, in many cases, the page may have other exposed parameters that are not lin

```
ffuf -w /opt/useful/seclists/Discovery/Web-Content/burp-parameter-names.txt:FUZZ -u 'http://<ip>:<port>/index.php?FUZZ=value' -fs 2287
```

## Ffuf - Ffuf - Ffuf - Ffuf - lfi-wordlists
#cat/ATTACK/INJECTION #cpts
So far in this module, we have been manually crafting our LFI payloads to test for LFI vulnerabilities. This is because manual testing is more reliable and can find LFI vulnerabilities that may not be identified otherwis

```
ffuf -w /opt/useful/seclists/Fuzzing/LFI/LFI-Jhaddix.txt:FUZZ -u 'http://<ip>:<port>/index.php?language=FUZZ' -fs 2287
```

## Ffuf - Ffuf - Ffuf - Ffuf - server-webroot
#cat/ATTACK/INJECTION #cpts
We may need to know the full server webroot path to complete our exploitation in some cases. For example, if we wanted to locate a file we uploaded, but we cannot reach its `/uploads` directory through relative paths (e.

```
ffuf -w /opt/useful/seclists/Discovery/Web-Content/default-web-root-directory-linux.txt:FUZZ -u 'http://<ip>:<port>/index.php?language=../../../../FUZZ/index.php' -fs 2287
```

## Ffuf - Ffuf - Ffuf - Ffuf - server-logsconfigurations
#cat/ATTACK/INJECTION #cpts
As we have seen in the previous section, we need to be able to identify the correct logs directory to be able to perform the log poisoning attacks we discussed. Furthermore, as we just discussed, we may also need to read

```
ffuf -w ./LFI-WordList-Linux:FUZZ -u 'http://<ip>:<port>/index.php?language=../../../../FUZZ' -fs 2287
```

## Ffuf - Ffuf - Ffuf - Ffuf - fuzzing-extentions---cmd
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /usr/share/dirb/wordlists/common.txt -u http://10.129.204.227:8080/cgi/FUZZ.cmd
```

## Ffuf - Ffuf - Ffuf - Ffuf - fuzzing-extentions---bat
#cat/ATTACK/INJECTION #cpts
```
ffuf -w /usr/share/dirb/wordlists/common.txt -u http://10.129.204.227:8080/cgi/FUZZ.bat
```

## Ffuf - Ffuf - Ffuf - Ffuf - after-running-the-url-encoded-whoami-payload-what-user-is-tomcat-runni
#cat/ATTACK/INJECTION #cpts
Confirming that the target is indeed running Tomcat on port 8080, students need to fuzz for CGI scripts using `ffuf`, finding `welcome.bat`:

```
ffuf -w /usr/share/dirb/wordlists/common.txt -u http://STMIP:8080/cgi/FUZZ.bat
```

## Ffuf - Ffuf - Ffuf - Ffuf - after-running-the-url-encoded-whoami-payload-what-user-is-tomcat-runni-2
#cat/ATTACK/INJECTION #cpts
```
└──╼ [★]$ ffuf -w /usr/share/dirb/wordlists/common.txt -u http://10.129.205.30:8080/cgi/FUZZ.bat
```

## Ffuf - Ffuf - Ffuf - Ffuf - perform-vhost-discovery-what-additional-vhost-exists
#cat/ATTACK/INJECTION #cpts
Thereafter, students need to filter it out using the `-fs` option of `ffuf`; the additional VHost that exists is `monitoring`:

```
ffuf -w /opt/useful/SecLists/Discovery/DNS/namelist.txt:FUZZ -u http://STMIP/ -H 'Host:FUZZ.inlanefreight.local'
```

## Ffuf - Ffuf - Ffuf - Ffuf - perform-vhost-discovery-what-additional-vhost-exists-2
#cat/ATTACK/INJECTION #cpts
```
└──╼ [★]$ ffuf -s -w /opt/useful/SecLists/Discovery/DNS/namelist.txt:FUZZ -u http://10.129.203.114/ -H 'Host: FUZZ.inlanefreight.local' -fs 15157
```

## Ffuf - Ffuf - Ffuf - Ffuf - freelancer
#cat/ATTACK/INJECTION #cpts
extrait du PDF Joplin: freelancer

```
ffuf -u http://freelancer.htb/FUZZ -w ~/wordlists/SecLists/Discovery/Web- Content/common.txt -t 10 ________________________________________________ about [
```

## Ffuf - Ffuf - Ffuf - Ffuf - freelancer-2
#cat/ATTACK/INJECTION #cpts
extrait du PDF Joplin: freelancer

```
ffuf -u 'http://freelancer.htb/accounts/profile/visit/FUZZ/' -X GET -H 'Cookie: sessionid=huzgt9mzuwxby81ljky4iqp3i73vlgbk; csrftoken=8154bDPG3IHLsRuh4c4RAjRRZ4LgCh3m' -w ~/wordlists/SecLists/Fuzzing/all_ports.txt ________________________________________________ 2 [
```

