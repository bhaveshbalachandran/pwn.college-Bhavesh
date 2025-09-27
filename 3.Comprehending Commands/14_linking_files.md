## Challenge 14: linking_files

The challenge is about using symbolic links to make one pathname resolve to another. The level gives you a program /challenge/catflag 
that will read /home/hacker/not-the-flag — but the real flag lives at /flag. 
Create a symlink named /home/hacker/not-the-flag that points to /flag, and the program will read the flag through the symlink.


## My Solve

**Flag:**'pwn.college{Mf0Lq4VsFm-8QNvNtPVwdn-yaz_.QX5ETN1wiNyEzNzEzW}'

```
hacker@commands~linking-files:~$ ls -l /home/hacker/not-the-flag
file /home/hacker/not-the-flag
lrwxrwxrwx 1 hacker hacker 5 Sep 27 22:20 /home/hacker/not-the-flag -> /flag
/home/hacker/not-the-flag: symbolic link to /flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Mf0Lq4VsFm-8QNvNtPVwdn-yaz_.QX5ETN1wiNyEzNzEzW}
```

## What I Learned

ln -s <original> <linkname> creates a symbolic link named <linkname> 
that points to <original>.
Accessing a symlink transparently resolves to the target file (so programs reading /home/hacker/not-the-flag will actually read /flag).


## Incorrect Tangents

N/A


## References

N/A
