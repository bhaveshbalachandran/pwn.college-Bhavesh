## Challenge 12: Writing_to_multiple_programs

The challenge demonstrates writing the same stream of data as input to multiple commands by combining tee and output process substitution (>(...)). The goal here was to run /challenge/hack and deliver its output simultaneously as stdin to both /challenge/the and /challenge/planet, so that one (or both) of those consumers prints the flag.

## My Solve
**Flag:**'pwn.college{U6R4I05qfYf-EP1YPgjnZc74CBH.QXwgDN1wiNyEzNzEzW}'

```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
346920498216027306
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{U6R4I05qfYf-EP1YPgjnZc74CBH.QXwgDN1wiNyEzNzEzW}
```

## What I Learned

<(command) redirects output of the given 
command 
>(command) redirects input to given command


## Incorrect Tangents
   
N/A


## References

N/A
