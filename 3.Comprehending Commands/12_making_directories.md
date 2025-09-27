## Challenge 12: making_directories

The challenge is about creating directories with mkdir and placing files inside them. 
You must create /tmp/pwn and then create a file named college inside that directory. 
After that, run /challenge/run which will check your work and reveal the flag.

## My Solve 
**Flag:**'pwn.college{sgHQT8erBi07R93HKjrmbA4sKmx.QXxMDO0wiNyEzNzEzW}'
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{sgHQT8erBi07R93HKjrmbA4sKmx.QXxMDO0wiNyEzNzEzW}
```

## What I Learned

mkdir creates the directory and any missing parent directories.
touch creates an empty file.


## Incorrect Tangents

N/A


## References

N/A

