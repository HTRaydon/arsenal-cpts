# Smbmap

% smbmap, smb, cpts

## Smbmap - Smbmap - Smbmap - Smbmap - smbmap
#cat/RECON #cpts
SMBMap is great for enumerating SMB shares from a Linux attack host. It can be used to gather a listing of shares, permissions, and share contents if accessible. Once access is obtained, it can be used to download and up

```
smbmap -u forend -p Klmcargo2 -d INLANEFREIGHT.LOCAL -H 172.16.5.5
```

## Smbmap - Smbmap - Smbmap - Smbmap - recursive-list-of-all-directories
#cat/RECON #cpts
```
smbmap -u forend -p Klmcargo2 -d INLANEFREIGHT.LOCAL -H 172.16.5.5 -R 'Department Shares' --dir-only
```

## Smbmap - Smbmap - Smbmap - Smbmap - recursive-list-of-all-directories-2
#cat/RECON #cpts
```
.\Department Shares\*
```

## Smbmap - Smbmap - Smbmap - Smbmap - file-share
#cat/RECON #cpts
`Smbmap` is another tool that helps us enumerate network shares and access associated permissions. An advantage of `smbmap` is that it provides a list of permissions for each shared folder. Attacking SMB

```
smbmap -H 10.129.14.128
```

## Smbmap - Smbmap - Smbmap - Smbmap - file-share-2
#cat/RECON #cpts
Using `smbmap` with the `-r` or `-R` (recursive) option, one can browse the directories: Attacking SMB

```
smbmap -H 10.129.14.128 -r notes
```

## Smbmap - Smbmap - Smbmap - Smbmap - file-share-3
#cat/RECON #cpts
Using `smbmap` with the `-r` or `-R` (recursive) option, one can browse the directories: Attacking SMB

```
.\notes\*
```

## Smbmap - Smbmap - Smbmap - Smbmap - file-share-4
#cat/RECON #cpts
From the above example, the permissions are set to `READ` and `WRITE`, which one can use to upload and download the files. Attacking SMB

```
smbmap -H 10.129.14.128 --download "notes\note.txt"
```

## Smbmap - Smbmap - Smbmap - Smbmap - file-share-5
#cat/RECON #cpts
Attacking SMB

```
smbmap -H 10.129.14.128 --upload test.txt "notes\test.txt"
```

