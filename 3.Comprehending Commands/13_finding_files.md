## Challenge 13: finding_files

The challenge is about using the find command to locate files anywhere on the filesystem. The flag file is named flag and is hidden somewhere under /. Some other flag files exist, and many locations are permission‑restricted (ignore the permission errors). Use find to locate the correct file and cat it.


## My Solve 
**Flag:**'pwn.college{A79V_bTCHFR9NyQcn4nn-NuvPFn.QXyMDO0wiNyEzNzEzW}'

```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/doc/gcc-9-aarch64-linux-gnu-base/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/flag
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls 
__init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cat flag.py
"""Describes a way to submit a key to a key server.
"""
from __future__ import absolute_import
from __future__ import division

import os

from pwnlib.args import args
from pwnlib.log import getLogger
from pwnlib.tubes.remote import remote

env_server  = args.get('FLAG_HOST', 'flag-submission-server').strip()
env_port    = args.get('FLAG_PORT', '31337').strip()
env_file    = args.get('FLAG_FILE', '/does/not/exist').strip()
env_exploit_name = args.get('EXPLOIT_NAME', 'unnamed-exploit').strip()
env_target_host  = args.get('TARGET_HOST', 'unknown-target').strip()
env_team_name    = args.get('TEAM_NAME', 'unknown-team').strip()

log = getLogger(__name__)

def submit_flag(flag,
                exploit=env_exploit_name,
                target=env_target_host,
                server=env_server,
                port=env_port,
                team=env_team_name):
    """
    Submits a flag to the game server

    Arguments:
        flag(str): The flag to submit.
        exploit(str): Exploit identifier, optional
        target(str): Target identifier, optional
        server(str): Flag server host name, optional
        port(int): Flag server port, optional
        team(str): Team identifier, optional

    Optional arguments are inferred from the environment,
    or omitted if none is set.

    Returns:
        A string indicating the status of the key submission,
        or an error code.

    Doctest:

        >>> l = listen()
        >>> _ = submit_flag('flag', server='localhost', port=l.lport)
        >>> c = l.wait_for_connection()
        >>> c.recvall().split()
        [b'flag', b'unnamed-exploit', b'unknown-target', b'unknown-team']
    """
    flag = flag.strip()

    log.success("Flag: %r" % flag)

    data = "\n".join([flag,
                      exploit,
                      target,
                      team,
                      '']).encode('ascii')

    if os.path.exists(env_file):
        write(env_file, data)
        return

    try:
        with remote(server, int(port)) as r:
            r.send(data)
            return r.recvall(timeout=1)
    except Exception:
        log.warn("Could not submit flag %r to %s:%s", flag, server, port)
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd /nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag$ grep pwn flag.py
from pwnlib.args import args
from pwnlib.log import getLogger
from pwnlib.tubes.remote import remote
hacker@commands~finding-files:~$ cat /usr/share/doc/gcc-9-aarch64-linux-gnu-base/flag
pwn.college{A79V_bTCHFR9NyQcn4nn-NuvPFn.QXyMDO0wiNyEzNzEzW}
```


## What I Learned

find / -type f -name flag -print searches from the root for regular files named flag.
here can be multiple files with the same name; verify each candidate with cat (or file/head) to find the real flag.


## Incorrect Tangents

N/A


## References

N/A
