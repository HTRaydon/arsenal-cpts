# Proxychains

% proxychains, pivot, cpts

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - dynamic-port-forwarding
#cat/PIVOT #cpts
The -D argument requests the SSH server to enable dynamic port forwarding. Once we have this enabled, we will require a tool that can route any tool's packets over the port 9050. We can do this using the tool proxychains

```
tail -4 /etc/proxychains.conf
```

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - using-xfreerdp-with-proxychains
#cat/PIVOT #cpts
Dynamic Port Forwarding with SSH and SOCKS Tunneling

```
[13:02:42:481] [4829:4830]
```

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - submit-the-contents-of-the-flagtxt-file-on-the-administrator-desktop-o
#cat/PIVOT #cpts
Students also need to edit `/etc/proxchains.conf`, adding the socks5 proxy entry to the bottom of the config file:

```
sudo nano /etc/proxychains.conf
```

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/PIVOT #cpts
```
shell-session
```

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt-
#cat/PIVOT #cpts
From `Pwnbox`/`PMVPN`, students need to use the attained SSH private key (after assigning it the appropriate permissions) to connect to `172.16.9.25`, proxying the connection through `proxychains`:

```
chmod 600 ssmallsadmKey
```

## Proxychains - Proxychains - Proxychains - Proxychains - Proxychains - gain-access-to-the-mgmt01-host-and-submit-the-contents-of-the-flagtxt--2
#cat/PIVOT #cpts
```
└──╼ [★]$ proxychains ssh -i ssmallsadmKey ssmallsadm@172.16.9.25
```

