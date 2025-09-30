## Challenge 8: reading_files

This level teaches a shell-native way to read a file into a variable without using cat (avoid the “Useless Use Of Cat”). The trick is to redirect the file into read, which reads from standard input.

## My Solve 
**Flag:**'pwn.college{gbcDMvYFriOxziY8MtqpzYcPq8d.QXwIDO0wiNyEzNzEzW}'

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{gbcDMvYFriOxziY8MtqpzYcPq8d.QXwIDO0wiNyEzNzEzW}

```


## What I Learned

Use read < file to read a file into a shell variable


## Incorrect Tangents
   
N/A


## References

N/A
