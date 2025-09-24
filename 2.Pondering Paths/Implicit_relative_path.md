Challenge 8 : Implicit_relative_path

The challenge is about explicitly running a program that lives in the current 
directory by using '.' (the current-directory marker). 
It intentionally does not search '.' for naked commands (for safety), 
so you must tell the shell you mean “the program in this directory” by using './'.

## My Solve 
**Flag:**'pwn.college{cK7svNfa9QyHEANRI_zrHFdwXrn.QXxUTN0wiNyEzNzEzW}'

I changed my working directory to '/challenge' and then explicitly invoked the 'run'
program in the current directory using './run'
```

hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{cK7svNfa9QyHEANRI_zrHFdwXrn.QXxUTN0wiNyEzNzEzW}

## What I Learned 
By default, the shell does not look in the current directory for commands 
when you type a “naked” name 'run' — this is a safety feature.
To execute a program that lives in the current directory you must explicitly 
reference it, './run'.
'.' in a path refers to the current directory and is the correct way to tell 
the shell “execute this file here.”

## Incorrect tangents 
N/A

## References
N/A



