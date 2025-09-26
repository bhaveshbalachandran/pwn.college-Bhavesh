## Challenge 10: hidden_files

The challenge is about hidden files — files whose names begin with '.' 
ls does not show dotfiles by default; 
you must use ls -a to reveal them. 
The flag for this level was hidden as a dot-prefixed 
file in the root directory '/'.

## My Solve 
**Flag:**'pwn.college{Ym2Zf8MoufEf8BN7g0JuAyzr6_G.QXwUDO0wiNyEzNzEzW}'

I listed the root directory, noticed nothing obvious, then listed with -a 
to reveal dotfiles and read the hidden file:
```

hacker@commands~hidden-files:/$ ls -a
.           .flag-392226508037  challenge  home   lib64   mnt  proc  sbin  tmp
..          bin                 dev        lib    libx32  nix  root  srv   usr
.dockerenv  boot                etc        lib32  media   opt  run   sys   var
hacker@commands~hidden-files:/$ cat /.flag-392226508037
pwn.college{Ym2Zf8MoufEf8BN7g0JuAyzr6_G.QXwUDO0wiNyEzNzEzW}
```


## What I Learned

Files beginning with '.' are hidden from normal ls output; 
use 'ls -a' to reveal them.
To read a hidden file, use its absolute path or include the dot when using 
relative paths.


## Incorrect tangents

N/A


## References 

N/A

