## Challenge 4: searching_mannuals

The challenge is about using the man pager’s built-in search to quickly find the option in a manual page that will print the flag.

## My Solve 
**Flag:**'pwn.college{wQRTfEHZ1UulLQWnY0AQAzLCztD.QX1EDO0wiNyEzNzEzW}'

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --mkk
Initializing...
Correct usage! Your flag: pwn.college{wQRTfEHZ1UulLQWnY0AQAzLCztD.QX1EDO0wiNyEzNzEzW}
```

## What I Learned
 
The man pager supports incremental searching: type /pattern to search forward and ?pattern to search backward.
After a search, use n to jump to the next match and N to go to the previous match — this is much faster than manual scrolling for long pages.


## Incorrect Tangents

N/A


## References

N/A
