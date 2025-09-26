

# Challenge 4 : Position_elsewhere 

The challenge is about navigating the filesystem using the cd command 
and executing a program from a specific directory

## My Solve 
**Flag:** 'pwn.college{UNB2-SbacGQIlgtkr6J7oIxMwMK.QX3QTN0wiNyEzNzEzW}'

As instructed in the challenge, I first changed my current working directory
to the location required by the program and then invoked the 'run' using its 
absolute path
```

hacker@paths~position-elsewhere:~$ cd /var
hacker@paths~position-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{UNB2-SbacGQIlgtkr6J7oIxMwMK.QX3QTN0wiNyEzNzEzW}
```

## What I Learned

This challenge taught me How to navigate directories using the cd command 
how the current working directory affects program execution 
and that programs require execution from a specific directory even 
if you know their absolute path

## Incorrect tangents 
N/A

## References
N/A 
