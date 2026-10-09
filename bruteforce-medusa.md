# Medusa

% medusa, bruteforce, cpts

## Medusa - Medusa - Medusa - Medusa - Medusa - installation
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Medusa often comes pre-installed on popular penetration testing distributions. You can verify its presence by running:

```
medusa -h
```

## Medusa - Medusa - Medusa - Medusa - Medusa - installation-3
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Installing Medusa on a Linux system is straightforward.

```
sudo apt-get -y install medusa
```

## Medusa - Medusa - Medusa - Medusa - Medusa - command-syntax-and-parameter-table
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Medusa's command-line interface is straightforward. It allows users to specify hosts, users, passwords, and modules with various options to fine-tune the attack process.

```
medusa [target_options] [credential_options] -M module [module_options]
```

## Medusa - Medusa - Medusa - Medusa - Medusa - targeting-multiple-web-servers-with-basic-http-authentication
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
Suppose you have a list of web servers that use basic HTTP authentication. These servers' addresses are stored in `web_servers.txt`, and you also have lists of common usernames and passwords in `usernames.txt` and `passw

```
medusa -H web_servers.txt -U usernames.txt -P passwords.txt -M http -m GET
```

## Medusa - Medusa - Medusa - Medusa - Medusa - testing-for-empty-or-default-passwords
#cat/ATTACK/BRUTEFORCE-SPRAY #cpts
If you want to assess whether any accounts on a specific host (`10.0.0.5`) have empty or default passwords (where the password matches the username), you can use:

```
medusa -h 10.0.0.5 -U usernames.txt -e ns -M service_name
```

