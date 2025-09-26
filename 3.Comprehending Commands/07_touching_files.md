## Challenge 7: touching_files

The challenge is about creating files with touch and using those files 
to satisfy a challenge requirement. 
In this level you must create two files, /tmp/pwn and /tmp/college, 
then run the challenge binary to get the flag.


## My Solve 
**Flag:**'pwn.college{4-Wr6qj2DMK3yzj6C6cafACRRmV.QXwMDO0wiNyEzNzEzW}'

I created the required files using touch, then ran the challenge binary. 
```

hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{4-Wr6qj2DMK3yzj6C6cafACRRmV.QXwMDO0wiNyEzNzEzW}
```

## What I Learned

touch filename creates a new, empty file if it does not already exist, 
or updates the file's timestamp if it does.
You can create multiple files at once: touch /tmp/pwn /tmp/college.
/tmp is a writable temporary directory on most Unix systems 
and is commonly used for transient files.


## Incorrect tangents

N/A


## References
N/A


