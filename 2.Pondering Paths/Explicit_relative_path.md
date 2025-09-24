Challenge 7 : Explicit_Relative_Paths
The challenge is about using the '.' (current directory) entry inside relative paths. 
It demonstrates that '.' can be inserted anywhere in a path without changing 
what it refers to, and that './challenge/./run' is equivalent to 'challenge/run' 
when your current working directory is '/'.

## My Solve 
**Flag:**'pwn.college{sWO7npfriZmKBViRvid5oAbWikJ.QXwUTN0wiNyEzNzEzW}'

I changed my working directory to the filesystem root and execute the 'run' program using
a relative path that explicitly includes '.' components.
```

hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sWO7npfriZmKBViRvid5oAbWikJ.QXwUTN0wiNyEzNzEzW}

## What I Learned 
'.' refers to the current directory and can be used anywhere in a path without 
changing the target.
Paths like 'challenge/run', './challenge/run', and './challenge/./run' are 
equivalent when cwd is '/'.
Using '.' explicitly can help clarify that a path is relative) 

## Incorrect tangents
N/A

## References
N/A

