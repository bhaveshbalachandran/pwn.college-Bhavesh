## Challenge 1: matching_with *

The challenge is about shell globbing with * (wildcard) and using it to change directories. The * matches any part of a filename (except a leading . or /), and the shell expands the pattern 
before the command runs. 
The level asks you, starting from your home directory, to cd into /challenge while passing at most four characters as the argument to cd.


## My Solve 
**Flag:**'pwn.college{8vZ9-Yoj1SOUQO3pziL6oTw6gaP.QXxIDO0wiNyEzNzEzW}'

```
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8vZ9-Yoj1SOUQO3pziL6oTw6gaP.QXxIDO0wiNyEzNzEzW}
hacker@globbing~matching-with-:/challenge$ 
```

## What I Learned 

* is a filename wildcard: the shell expands patterns like /c* into matching filesystem names before running the command.
The argument you type can be very short; the shell will expand it to the full pathname if a match exists.


## Incorrect Tangents

N/A


## References

N/A

