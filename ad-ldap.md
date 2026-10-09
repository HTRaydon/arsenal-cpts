# LDAP enumeration

% ldap, ldapsearch, cpts

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - enumerating-the-password-policy---from-linux---ldap-anonymous-bind
#cat/RECON #cpts
[LDAP anonymous binds ](https://docs.microsoft.com/en-us/troubleshoot/windows-server/identity/anonymous-ldap-operations-active-directory-disabled)allow unauthenticated attackers to retrieve information from the domain, s

```
ldapsearch -h 172.16.5.5 -x -b "DC=INLANEFREIGHT,DC=LOCAL" -s sub "*" | grep -m 1 -B 10 pwdHistoryLength
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - ldapsearch
#cat/RECON #cpts
```
ldapsearch -h 172.16.5.5 -x -b "DC=INLANEFREIGHT,DC=LOCAL" -s sub "(&(objectclass=user))" | grep sAMAccountName: | cut -f2 -d" "
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - windapsearch
#cat/RECON #cpts
```
./windapsearch.py --dc-ip 172.16.5.5 -u "" -U
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - windapsearch-2
#cat/RECON #cpts
[Windapsearch](https://github.com/ropnop/windapsearch) is another handy Python script we can use to enumerate users, groups, and computers from a Windows domain by utilizing LDAP queries. It is present in our attack host

```
windapsearch.py -h
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - domain-admins
#cat/RECON #cpts
```
python3 windapsearch.py --dc-ip 172.16.5.5 -u forend@inlanefreight.local -p Klmcargo2 --da
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - privileged-users
#cat/RECON #cpts
```
python3 windapsearch.py --dc-ip 172.16.5.5 -u forend@inlanefreight.local -p Klmcargo2 -PU
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - ldapsearch-2
#cat/RECON #cpts
For example, `ldapsearch` is a command-line utility used to search for information stored in a directory using the LDAP protocol. It is commonly used to query and retrieve data from an LDAP directory service.

```
ldapsearch -H ldap://ldap.example.com:389 -D "cn=admin,dc=example,dc=com" -w secret123 -b "ou=people,dc=example,dc=com" "(mail=john.doe@example.com)"
```

## LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - LDAP enumeration - ldapsearch-3
#cat/RECON #cpts
This command can be broken down as follows: - Connect to the server `ldap.example.com` on port `389`. - Bind (authenticate) as `cn=admin,dc=example,dc=com` with password `secret123`. - Search under the base DN `ou=people

```
ldap
```

