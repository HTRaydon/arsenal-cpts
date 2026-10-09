# Jenkins

% jenkins, web, cpts

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - initial-enumeration
#cat/ATTACK #cpts
Let's assume our client provided us with the following scope:

```
cat scope_list
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - using-eyewitness
#cat/ATTACK #cpts
Let's run the default `--web` option to take screenshots using the Nmap XML output from the discovery scan as input.

```
eyewitness --web -x web_discovery.xml -d inlanefreight_eyewitness
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - script-console
#cat/ATTACK #cpts
The script console can be reached at the URL `http://jenkins.inlanefreight.local:8000/script`. This console allows a user to run Apache [Groovy](https://en.wikipedia.org/wiki/Apache_Groovy) scripts, which are an object-o

```
groovy
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - attack-the-jenkins-target-and-gain-remote-code-execution-submit-the-co-2
#cat/ATTACK #cpts
Now, students can click on "Run" in the `Jenkins` web page, and the reverse-shell session will be established:

```
shell-session
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - home-directory-contents
#cat/ATTACK #cpts
```
ls /home
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - passwd
#cat/ATTACK #cpts
```
cat /etc/passwd
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - existing-users
#cat/ATTACK #cpts
Occasionally, we will see password hashes directly in the `/etc/passwd` file. This file is readable by all users, and as with hashes in the `/etc/shadow` file, these can be subjected to an offline password cracking attac

```
cat /etc/passwd | cut -f1 -d:
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - existing-users-2
#cat/ATTACK #cpts
With Linux, several different hash algorithms can be used to make the passwords unrecognizable. Identifying them from the first hash blocks can help us to use and work with them later if needed. Here is a list of the mos

```
grep "sh$" /etc/passwd
```

## Jenkins - Jenkins - Jenkins - Jenkins - Jenkins - users-last-login
#cat/ATTACK #cpts
```
lastlog
```

