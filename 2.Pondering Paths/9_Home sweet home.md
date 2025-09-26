
# Challenge 9 : Home_sweet_home     

The challenge is about understanding the home directory (~) 
and how to use absolute paths inside it. 
In this level, '/challenge/run' writes the flag to a file specified as an argument. 
The argument must:  
Be an absolute path.
Reside inside the home directory (/home/hacker).
Be three characters or less before expansion.

## My Solve
**Flag:**'pwn.college{gKF-Q0uwjQNwtDKgGMWWwiTGKG6.QXzMDO0wiNyEzNzEzW}'

I ran the program specifying a short absolute path inside my home directory. 
```

hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{gKF-Q0uwjQNwtDKgGMWWwiTGKG6.QXzMDO0wiNyEzNzEzW}
```

## What I Learned
'~' expands to your home directory in paths.
Absolute paths starting with '/' inside your home directory can be used to save files.
Bash path expansion only applies to the leading ~,.
Short paths (≤3 characters) can be used as arguments, and the program writes output
files to that location.
Using cat confirmed that the flag was correctly written to the file.


## Incorrect tangents
Paths longer than three characters before expansion were rejected by the program.
Providing a relative path would not satisfy the requirement for an absolute path

## References
N/A
