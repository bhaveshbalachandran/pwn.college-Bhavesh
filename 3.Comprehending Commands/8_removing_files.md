## Challenge 8: removing_files

The challenge is about removing files with rm. 
The level creates a delete_me file in your home directory; 
you must delete it and then run '/challenge/check' which verifies the 
deletion and prints the flag.

## My Solve 
**Flag:**'pwn.college{0KsW63ZDtnzKtxD1eqlVy0RKoL5.QX2kDM1wiNyEzNzEzW}'

I removed the delete_me file from my home directory and then ran the 
checker to confirm it was gone:
```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{0KsW63ZDtnzKtxD1eqlVy0RKoL5.QX2kDM1wiNyEzNzEzW}
```

## What I Learned

rm FILENAME deletes a file

## Incorrect tangents
N/A


## References
N/A

