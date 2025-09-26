## Challenge 9: moving_files

The challenge is about using mv to move files. 
You must move the /flag file into /tmp/hack-the-planet, then run the 
checker to confirm and get the flag.

## My Solve
**Flag:**'pwn.college{UKt6Z3WXG4Em9E3P_8RPr-i-ikO.0VOxEzNxwiNyEzNzEzW}'
```

hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{UKt6Z3WXG4Em9E3P_8RPr-i-ikO.0VOxEzNxwiNyEzNzEzW}
```

## What I Learned 

mv source target moves files or renames them. When target is a 
directory, the file is moved into that directory.
After moving the file to the required place, run the provided checker 
to validate the action and reveal the flag.


## Incorrect tangents
N/A


## References
N/A
