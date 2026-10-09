# Gobuster

% gobuster, web, fuzzing, dns, cpts

## Gobuster - Gobuster - Gobuster - Gobuster - dns-subdomain-enum
#cat/RECON #cpts
```
gobuster dns -d <url> -w <wordlist>
```

## Gobuster - Gobuster - Gobuster - Gobuster - dns-vhost-enum
#cat/RECON #cpts
```
gobuster vhost -u http://<ip> -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-110000.txt --append-domain
```

## Gobuster - Gobuster - Gobuster - Gobuster - directory-enum
#cat/RECON #cpts
```
gobuster dir -u <url> -w <wordlist>
```

## Gobuster - Gobuster - Gobuster - Gobuster - subdomain-discovery
#cat/RECON #cpts
```
gobuster vhost -u "" -w `fzf-wordlists` --append-domain
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumeration
#cat/RECON #cpts
After fingerprinting the Tomcat instance, unless it has a known vulnerability, we'll typically want to look for the `/manager` and the `/host-manager` pages. We can attempt to locate these with a tool such as `Gobuster`

```
gobuster dir -u http://web01.inlanefreight.local:8180/ -w /usr/share/dirbuster/wordlists/directory-list-2.3-small.txt
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumeration-2
#cat/RECON #cpts
After fingerprinting the Tomcat instance, unless it has a known vulnerability, we'll typically want to look for the `/manager` and the `/host-manager` pages. We can attempt to locate these with a tool such as `Gobuster`

```
Gobuster v3.0.1
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumeration---gobuster
#cat/RECON #cpts
We can hunt for CGI scripts using a tool such as `Gobuster`. Here we find one, `access.cgi`.

```
gobuster dir -u http://10.129.204.231/cgi-bin/ -w /usr/share/wordlists/dirb/small.txt -x cgi
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumeration---gobuster-2
#cat/RECON #cpts
We can hunt for CGI scripts using a tool such as `Gobuster`. Here we find one, `access.cgi`.

```
Gobuster v3.1.0
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumeration---gobuster-3
#cat/RECON #cpts
Next, we can cURL the script and notice that nothing is output to us, so perhaps it is a defunct script but still worth exploring further.

```
curl -i http://10.129.204.231/cgi-bin/access.cgi
```

## Gobuster - Gobuster - Gobuster - Gobuster - gobuster-enumeration
#cat/RECON #cpts
Once you have created the custom wordlist, you can use `gobuster` to enumerate all items in the target. GoBuster is an open-source directory and file brute-forcing tool written in the Go programming language. It is desig

```
gobuster dir -u http://10.129.204.231/ -w /tmp/list.txt -x .aspx,.asp
```

## Gobuster - Gobuster - Gobuster - Gobuster - gobuster-enumeration-2
#cat/RECON #cpts
Once you have created the custom wordlist, you can use `gobuster` to enumerate all items in the target. GoBuster is an open-source directory and file brute-forcing tool written in the Go programming language. It is desig

```
Gobuster v3.5
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the
#cat/RECON #cpts
After spawning the target machine, students need to first fuzz for CGI scripts hosted on the target, finding `access.cgi`:

```
gobuster dir -u http://STMIP/cgi-bin/ -w /usr/share/wordlists/dirb/small.txt -x cgi
```

## Gobuster - Gobuster - Gobuster - Gobuster - enumerate-the-host-exploit-the-shellshock-vulnerability-and-submit-the-2
#cat/RECON #cpts
```
└──╼ [★]$ gobuster dir -u http://10.129.205.27/cgi-bin/ -w /usr/share/wordlists/dirb/small.txt -x cgi
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified
#cat/RECON #cpts
After spawning the target machine, students need to clone \[IIS Short Name Scanner\](https://academy.hackthebox.com/app/module/113/section/git clone https://github.com/irsdl/IIS-ShortName-Scanner.git) to `Pwnbox`:

```
git clone https://github.com/irsdl/IIS-ShortName-Scanner.git
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-2
#cat/RECON #cpts
```
shell-session
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-3
#cat/RECON #cpts
Then, students need to download and install Java:

```
wget https://download.oracle.com/java/20/latest/jdk-20_linux-x64_bin.deb
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-4
#cat/RECON #cpts
Then, students need to download and install Java:

```
sudo apt install ./jdk-20_linux-x64_bin.deb
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-5
#cat/RECON #cpts
```
(Reading database ... 473878 files and directories currently installed.)
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-6
#cat/RECON #cpts
Additionally, the proper symbolic links must be set:

```
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-20/bin/java 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-7
#cat/RECON #cpts
Additionally, the proper symbolic links must be set:

```
sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-20/bin/javac 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-8
#cat/RECON #cpts
Additionally, the proper symbolic links must be set:

```
sudo update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk-20/bin/jar 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-9
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-20/bin/java 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-10
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-20/bin/javac 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-11
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk-20/bin/jar 1
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-12
#cat/RECON #cpts
Students need to also need to configure the default JDK 20:

```
sudo update-alternatives --config java
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-13
#cat/RECON #cpts
Students need to also need to configure the default JDK 20:

```
sudo update-alternatives --config javac
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-14
#cat/RECON #cpts
Students need to also need to configure the default JDK 20:

```
sudo update-alternatives --config jar
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-15
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --config java
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-16
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --config javac
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-17
#cat/RECON #cpts
```
└──╼ [★]$ sudo update-alternatives --config jar
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-18
#cat/RECON #cpts
The Java version can then be confirmed:

```
java -version
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-19
#cat/RECON #cpts
Now, students need to run the `IIS Shortname Scanner` tool against the target, selecting "No" when asked to use a proxy :

```
cd IIS-ShortName-Scanner/release/
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-20
#cat/RECON #cpts
The tool discovers two directories and three files. However, the remaining filename still needs to be bruteforced. Therefore, students need to generate a wordlist:

```
egrep -r ^transf /usr/share/wordlists/ | sed 's/^[^:]*://' > /tmp/list.txt
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-21
#cat/RECON #cpts
```
└──╼ [★]$ egrep -r ^transf /usr/share/wordlists/ | sed 's/^[^:]*://' > /tmp/list.txt
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-22
#cat/RECON #cpts
Finally, students need to run Gobuster with the newly created wordlist to fuzz the filename, finding `transfer.aspx`:

```
gobuster dir -u http://STMIP/ -w /tmp/list.txt -x .aspx,.asp
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-full-aspx-filename-that-gobuster-identified-23
#cat/RECON #cpts
```
└──╼ [★]$ gobuster dir -u http://10.129.252.121/ -w /tmp/list.txt -x .aspx,.asp
```

## Gobuster - Gobuster - Gobuster - Gobuster - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t
#cat/RECON #cpts
From the previous questions, students know that the `Tomcat` application running on the target machine suffers from [CVE-2019-0232](https://github.com/advisories/GHSA-8vmx-qmch-mpqg), therefore, before utilizing `msfcons

```
gobuster dir -u http://STMIP:8080/cgi/ -w /opt/useful/SecLists/Discovery/Web-Content/burp-parameter-names.txt -x .bat -t 50 -k -q
```

## Gobuster - Gobuster - Gobuster - Gobuster - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t-2
#cat/RECON #cpts
```
└──╼ [★]$ gobuster dir -u http://10.129.201.89:8080/cgi/ -w /opt/useful/SecLists/Discovery/Web-Content/burp-parameter-names.txt -x .bat -t 50 -k -q
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-url-of-the-wordpress-instance
#cat/RECON #cpts
Subsequently, students need to perform vHost fuzzing, finding three vHosts, `monitoring.inlanefreight.local`, `blog.inlanefreight.local`, and `gitlab.inlanefreight.local`:

```
gobuster vhost -u inlanefreight.local -w /opt/useful/seclists/Discovery/DNS/subdomains-top1million-5000.txt -t 50 -k -q --append-domain
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-url-of-the-wordpress-instance-2
#cat/RECON #cpts
```
└──╼ [★]$ gobuster vhost -u inlanefreight.local -w /opt/useful/seclists/Discovery/DNS/subdomains-top1million-5000.txt -t 50 -k -q --append-domain
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-fqdn-of-the-third-vhost
#cat/RECON #cpts
From the vHost fuzzing performed using `Gobuster` on `inlanefreight.local` in the first question, students will know that the Fully Qualified Domain Name of the third vHost is `monitoring.inlanefreight.local`:

```
gobuster vhost -u inlanefreight.local -w /opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -t 50 -k -q
```

## Gobuster - Gobuster - Gobuster - Gobuster - what-is-the-fqdn-of-the-third-vhost-2
#cat/RECON #cpts
```
└──╼ [★]$ gobuster vhost -u inlanefreight.local -w /opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -t 50 -k -q
```

## Gobuster - Gobuster - Gobuster - Gobuster - analysis
#cat/RECON #cpts
extrait du PDF Joplin: analysis

```
../employees/login.php [07:45:58] 200 - 13KB - /dashboard/404.html [07:46:03] 200 - 35B - /dashboard/tickets.php [07:46:12] 200 - 35B - /dashboard/emergency.php employees The suspected login functionality is discovered in /employees/login.php . Attempting common attacks that are relevant to login forms, such as SQL Injection or authentication bypasses yields no results, so we can proceed with enumerating the /users endpoint for a possible attack vector. users The only endpoint in the /users subdirectory seems to be list.php . Visiting the endpoint: dirsearch -w /usr/share/wordlists/SecLists/Di
```

