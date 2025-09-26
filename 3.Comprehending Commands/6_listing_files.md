## Challenge 6: listing_files

The challenge is about using ls to discover filenames in a directory when the names are not given to you. 
The '/challenge' directory contains the executable, but it was saved under a random name — list the directory to find it, then run it.

## My Solve
**Flag:**'pwn.college{cf-_h_UcmJdCbk6EsiPKSxh9T0G.QX4IDO0wiNyEzNzEzW}'

I listed the 'ls /challenge' directory to reveal the randomly-named executable, then ran it by absolute path:
```

hacker@commands~listing-files:~$ ls /challenge
11087-renamed-run-21680  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/11087-renamed-run-21680
Yahaha, you found me! Here is your flag:
pwn.college{cf-_h_UcmJdCbk6EsiPKSxh9T0G.QX4IDO0wiNyEzNzEzW}
```

## What I Learned 

ls /path lists the contents of the specified directory so you can discover filenames you weren’t told.
When filenames are randomized, start by listing the directory
Once you find the filename, invoke it by absolute path '/challenge/filename' to run it.


## Incorrect tangents
N/A


## References
N/A


