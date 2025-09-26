

# Challenge 3 : Position_thy_self

The challenge is about navigating using the cd command and executing the 
program from a specific directory 

## My solve
**Flag:**'pwn.college{0fUwecxgsJFtX-MlTVFFCyXN5Xs.QX2QTN0wiNyEzNzEzW}'

As instructed in the challenge, I first changed my current working directory
to the location required by the program and then invoked the run 
binary using its absolute path 
```

hacker@paths~position-thy-self:/challenge$ cd /usr/share/zoneinfo/posix/Asia
hacker@paths~position-thy-self:/usr/share/zoneinfo/posix/Asia$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0fUwecxgsJFtX-MlTVFFCyXN5Xs.QX2QTN0wiNyEzNzEzW}
```

## What I Learned
This challenge taugh me how to navigate directories using the cd command
the concept of current working directory and how it affects program execution
and some programs require execution from a specific directory even if the 
binary's absolute path is known

## Incorrect tangents
Attempting to run /challenge/run from a different directory initially
gave an error because the program checks the current working directory.

## References
N/A
