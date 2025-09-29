## Challenge 4: redirecting_errors

The challenge is about redirecting both stdout and stderr to separate files using file descriptor numbers. You must capture the flaginto myflag.
and capture the program’s instructions into instructions. Because you redirect both streams, nothing should appear on the terminal — the flag will be in myflag and the human-readable messages will be in instructions.


## My Solve 
**Flag:**'pwn.college{QG8WzJdHzIz4R9WuYQun3bycisY.QX3YTN0wiNyEzNzEzW}'

```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{QG8WzJdHzIz4R9WuYQun3bycisY.QX3YTN0wiNyEzNzEzW}

```

## What I Learned

File descriptors: 0 = stdin, 1 = stdout, 2 = stderr.
> (or 1>) redirects stdout; 2> redirects stderr. You can redirect both at once: cmd > out 2> err.
Programs often print machine-readable output to stdout and human-facing messages to stderr; redirecting them separately lets you capture each stream for different purposes.


## Incorrect Tangents
   
N/A


## References

N/A


