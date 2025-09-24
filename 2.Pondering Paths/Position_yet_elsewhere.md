Challenge 5 : Navigate_and_Run

The challenge is about navigating the filesystem using the cd command
and executing a program from a specific directory.

## My Solvw 
**Flag:** 'pwn.college{cqt_F5X1TOErhzDlzTQZSwpWLuP.QX4QTN0wiNyEzNzEzW}'

As instructed in the challenge,I first changed my current working directory to the 
location required by the program and then invoked the 'run' using its absolute path:
```

hacker@paths~position-yet-elsewhere:~$ cd /etc
hacker@paths~position-yet-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{cqt_F5X1TOErhzDlzTQZSwpWLuP.QX4QTN0wiNyEzNzEzW}

## What I Learned

This challenge taught me How to navigate directories using the cd command.
How the current working directory affects program execution.
and that programs require execution from a specific directory, even if their 
absolute path is known.

## Incorrect tangents
N/A


## References
N/A



