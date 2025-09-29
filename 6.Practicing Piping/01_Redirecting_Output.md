## Challenge 1: redirecting_output

The challenge is about redirecting standard output into a file using >. You must write the exact text PWN (uppercase) into a file named COLLEGE (uppercase) using output redirection.

## My Solve 
**Flag:**'pwn.college{MUr1ACi7I6wWSgv067AY2flCYO8.QX0YTN0wiNyEzNzEzW}'

I used echo with output redirection to create the file COLLEGE containing PWN, verified its contents, and then ran the challenge.

```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{MUr1ACi7I6wWSgv067AY2flCYO8.QX0YTN0wiNyEzNzEzW}

```

## What I Learned

'>' redirects a program’s standard output to a file, creating or overwriting it.
echo is a simple way to emit strings. 


## Incorrect Tangents
   
N/A


## References

N/A

