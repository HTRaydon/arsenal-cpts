# SNMP

% snmp, cpts

## SNMP - SNMP - SNMP - SNMP - dangerous-settings
#cat/RECON #cpts
Enumération SNMP

```
snmpwalk -v 2c -c public <ip> 1.3.6.1.2.1.1.5.0
```

## SNMP - SNMP - SNMP - SNMP - dangerous-settings-2
#cat/RECON #cpts
```
snmpwalk -v 2c -c private <ip>
```

## SNMP - SNMP - SNMP - SNMP - dangerous-settings-3
#cat/RECON #cpts
Brute-force de communauté

```
onesixtyone -c dict.txt <ip>
```

