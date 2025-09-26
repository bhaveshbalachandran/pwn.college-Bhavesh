##Challenge 11 : Catting_Absolute_Paths

The challenge shows that cat accepts absolute paths and that some
files can be read directly

## My Solve
**Flag:**'pwn.college{cnSiM63l16CTO5Ff6sVyNXi8uGw.QX5ETO0wiNyEzNzEzW}'

I read the flag by specifying its absolute path to cat:
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{cnSiM63l16CTO5Ff6sVyNXi8uGw.QX5ETO0wiNyEzNzEzW}
```

##What I Learned
cat accepts absolute paths as arguments.
Absolute paths refer to the same file regardless of your current
working directory.


##Incorrect tangents
N/A



##References
N/A
