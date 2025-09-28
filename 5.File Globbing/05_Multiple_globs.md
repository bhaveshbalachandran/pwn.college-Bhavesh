## Challenge 5: multiple_globs

The challenge is about using multiple glob metacharacters in a single word. Bash allows more than one * in the same argument; for example *f*l* matches any pathname that contains an f followed later by an l. In this level you must cd into /challenge/files and run /challenge/run with a single short (3 characters or less) globbed word that contains two * and matches every filename that contains the letter p.

## My Solve
**Flag:**'pwn.college{8GiUSxhYeIY8iWTdbaHgnQhRKYL.0lM3kjNxwiNyEzNzEzW}'

I used the three‑character pattern *p* (two * characters with p between them). From /challenge/files the shell expands *p* into every filename that contains p, and I passed that expanded list as the single argument to /challenge/run:

```
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{8GiUSxhYeIY8iWTdbaHgnQhRKYL.0lM3kjNxwiNyEzNzEzW}
```

## What I Learned 

You can include multiple * wildcards in a single argument (e.g., *p*), and the shell will expand that one word into all matching filenames before the command runs.
*p* is three characters long and contains two * characters, satisfying the level’s constraints while matching any name that contains p.


## Incorrect Tangents
   
N/A


## References

N/A

