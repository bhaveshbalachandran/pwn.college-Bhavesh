## Challenge 4: matching_paths_with []

The challenge is about using bracket globs ([...]) to expand entire absolute paths. 
Globbing is performed per pathname component, so you can write a single argument that expands into several absolute file paths.


## My Solve
**Flag:**'pwn.college{Aoc5g5ch21Tdqd5eqTQ_cIuebIf.QX0IDO0wiNyEzNzEzW}'

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Aoc5g5ch21Tdqd5eqTQ_cIuebIf.QX0IDO0wiNyEzNzEzW}
```

## What I Learned

Bracket globs [...] can be used inside absolute paths '/challenge/files/file_[bash]' to expand into multiple full pathnames.
Globbing happens before the command runs, so the program receives separate arguments for each matched file path.


## Incorrect Tangents
   
N/A


## References

N/A

