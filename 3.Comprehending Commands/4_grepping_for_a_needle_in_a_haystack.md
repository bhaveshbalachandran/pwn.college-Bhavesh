## Challenge 4: grepping_for_a_needle_in_a_haystack

The challenge is about using grep to search large files for the flag. The file /challenge/data.txt contains a huge number of lines; 
the hint tells us the flag always starts with pwn.college, so we can grep that pattern to extract the flag quickly.


## My Solve
**Flag:**'pwn.college{cPJTI-hVBd0hDrP-ySuxQA_E_lP.QX3EDO0wiNyEzNzEzW}'
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{cPJTI-hVBd0hDrP-ySuxQA_E_lP.QX3EDO0wiNyEzNzEzW:}
```

## What I Learned
grep PATTERN file searches a file for lines containing PATTERN and 
prints matching lines.
Use a unique substring of the flag as the search term to reliably locate the flag.
grep is far faster and more practical than manually scanning very large files.


## Incorrect tangents
N/A


## References
N/A
