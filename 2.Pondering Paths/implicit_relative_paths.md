
# Challenge 6: Implicit_relative_paths,from /

The The challenge is about understanding relative paths and how the current working
 directory (cwd) affects them. The level required running the 'run' program using a
relative path while my cwd was /. A hint indicated the relative path begins with 
the letter c.

## My Solve 
**Flag:**'pwn.college{4NA7_jxRcplDwR6cRW__4Itm5qn.QX5QTN0wiNyEzNzEzW}'

I changed my working directory to the filesystem root '/' and ececuted the 'run' program
using a relative path that begins with 'c' (challenge/run where the cwd is '/')
```

hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4NA7_jxRcplDwR6cRW__4Itm5qn.QX5QTN0wiNyEzNzEzW}

## What I Learned 

A relative path does not start with '/' and is interpreted relative to the current
working directory.
From '/', the relative path challenge/run points to /challenge/run.
Using relative vs absolute paths changes how you refer to 
files — absolute paths (starting with /) ignore cwd, relative paths depend on cwd
And .. refers to the parent directory when composing relative paths.


## Incorrect tangents
N/A

## References
M/A
