## Challenge 5: printing_exported_variables

This level practices viewing exported (environment) variables. The env command lists all exported variables available to the current shell; use it (or printenv) to find the FLAG variable.


## My Solve 
**Flag:**'pwn.college{oquKC2g-seFoYSIWAQ9kzNI1tJR.QX4UTN0wiNyEzNzEzW}'

```

hacker@variables~printing-exported-variables:~$ env 
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=717b5a138abd14d580c661118299ec1ad4792fdf51500828d90b42969f811060
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{oquKC2g-seFoYSIWAQ9kzNI1tJR.QX4UTN0wiNyEzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env

```


## What I Learned 

env prints the environment (exported variables) available to the current shell


## Incorrect Tangents
   
N/A


## References

N/A
