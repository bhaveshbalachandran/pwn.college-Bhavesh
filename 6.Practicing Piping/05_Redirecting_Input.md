## Challenge 5: redirecting_input

The challenge is about redirecting standard input into a program using <. The level requires you to create a file named PWN whose contents are the text COLLEGE
then run /challenge/run with its stdin redirected from that file so the program reads COLLEGE from stdin and prints the flag.


## My Solve 
**Flag:**'pwn.college{IKLJdwZh9I1xc_Pt1UHTxOLY49S.QXwcTN0wiNyEzNzEzW}'

```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{IKLJdwZh9I1xc_Pt1UHTxOLY49S.QXwcTN0wiNyEzNzEzW}
```

## What I Learned

< filename redirects stdin of a program so the program reads from filename as if the bytes had been typed into the terminal.


## Incorrect Tangents
   
N/A


## References

N/A
