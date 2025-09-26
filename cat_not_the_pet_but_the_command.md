#Challenge 1 : Cat_not_the_pet_but_the_command!

The challenge is about using the cat utility to read files. 
The level copies the flag into a file in your home directory; 
to do  is simply read it with cat.

## My Solve
**Flag:**'pwn.college{kyAsIzYvup1HDopgiUg6FL63P-4.QXxcTN0wiNyEzNzEzW}'

I listed my home directory, saw the files, and used cat to read the flag file.
and the final successful reads:
```

hacker@commands~cat-not-the-pet-but-the-command:~$ ls
Desktop  f  flag
hacker@commands~cat-not-the-pet-but-the-command:~$ cat f
pwn.college{gKF-Q0uwjQNwtDKgGMWWwiTGKG6.QXzMDO0wiNyEzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{kyAsIzYvup1HDopgiUg6FL63P-4.QXxcTN0wiNyEzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$ 
```

## What I Learned
cat prints file contents to stdout and can concatenate multiple files.
If a filename is mistyped cat will report No such file or directory.
cat with no arguments reads from standard input it is.
Useful for quick checks: ls to confirm filenames, file to check file type, 
and cat to view contents.

## Incorrect tangents
Trying cat f failed because the file is named flag not f. 
Always confirm the exact filename.

## References 
N/A.


