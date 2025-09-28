## Challenge 5: searching_for_mannuals

The challenge is about discovering a manpage that has been placed under a randomized name in the man database.


## My Solve
**Flag:**'pwn.college{w-R3TYOPbVu-YwhBN0feYgP2YC5.QX2EDO0wiNyEzNzEzW}'

I used the manpage for man to learn how to search the man database, found 'wbuwhfegwi' for the challenge, 
and then ran /challenge/challenge with the discovered option and obtained the flag 


```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
wbuwhfegwi (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man wbuwhfegwi
hacker@man~searching-for-manuals:~$ /challenge/challenge --wbuwhf 302
Correct usage! Your flag: pwn.college{w-R3TYOPbVu-YwhBN0feYgP2YC5.QX2EDO0wiNyEzNzEzW}
```

## What I Learned

man man is the authoritative place to learn advanced man usage; it documents tools like -k to search the man database.
'man -k (keyword)' searches the manpage short descriptions and returns matching entries even if the filenames are randomized.


## Incorrect Tangents

N/A


## References

N/A

