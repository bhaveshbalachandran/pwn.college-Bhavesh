## Challenge 5: comparing_files

The challenge is about using diff to find the single real flag hidden among many decoys. 
Two files are provided:
/challenge/decoys_only.txt — 100 fake flags
/challenge/decoys_and_real.txt — the same 100 fake flags plus the one real flag
Use diff to compare the files line-by-line and see what was added.


## My Solve 
**Flag:**'pwn.college{ASE-0KANQVyaM6pgkY94Pxe9Enr.01MwMDOxwiNyEzNzEzW}'

I compared the two files and inspected the diff
```

hacker@commands~comparing-files:/challenge$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
61a62
pwn.college{ASE-0KANQVyaM6pgkY94Pxe9Enr.01MwMDOxwiNyEzNzEzW}
```

## Incorrect tangents
N/A


## References
N/A


