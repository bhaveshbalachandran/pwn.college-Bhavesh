## Challenge 7: exclusionary_globbing

The challenge is about using an inverted bracket glob ([!...] or [^...]) to select filenames that do not start with certain characters. You must pass a single globbed argument to /challenge/run that expands to all files in /challenge/files whose first character is not p, w, or n.

## My Solve 
**Flag:**'pwn.college{0FwGPtyocVplHBp1TfEFqZ2RfZf.QX2IDO0wiNyEzNzEzW}'

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0FwGPtyocVplHBp1TfEFqZ2RfZf.QX2IDO0wiNyEzNzEzW}
```

## What I Learned 

! or ^ list files that are not under by the  file globs.


## Incorrect Tangents
   
N/A


## References

N/A
