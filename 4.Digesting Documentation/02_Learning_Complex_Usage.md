## Challenge 2: learning_complex_usage

The challenge is about commands whose arguments themselves take arguments. 
The documentation for /challenge/challenge explained that it supports a --printfile option whose 
argument is the path of the file to print. Use that to print the flag.


## My Solve
**Flag:**'pwn.college{0fLT5TrftgDYizX_ujpO75itfkX.QX1ITO0wiNyEzNzEzW}'

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /home/hacker/not-the-flag
Correct argument! Here is the /home/hacker/not-the-flag file:
pwn.college{0fLT5TrftgDYizX_ujpO75itfkX.QX1ITO0wiNyEzNzEzW}
```

## What I Learned

Some command-line options accept their own arguments read the docs carefully to know which options do.
Quoting is important when the argument contains spaces or shell-special characters.


## Incorrect Tangents

N/A


## References

N/A
