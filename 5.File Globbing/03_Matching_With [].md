## Challenge 3: matching_with []

The challenge is about bracket globs ([...]) — a single-character wildcard that matches one character from a specified set. The task was to change into /challenge/files and run /challenge/run with a single argument that expands (via bracket-globbing) into file_b, file_a, file_s, and file_h.


## My Solve 
**Flag:**'pwn.college{AKiMfSZePpCRXVPCqeL1zHkmC6T.QXzIDO0wiNyEzNzEzW}'

From the /challenge/files directory I invoked the challenge with a bracket pattern that matches the four required filenames (b,a,s,h):

```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{AKiMfSZePpCRXVPCqeL1zHkmC6T.QXzIDO0wiNyEzNzEzW}

```

## What I Learned

[...] matches exactly one character from the set inside the brackets. file_[bash] matches file_b, file_a, file_s, and file_h.
If you quote the pattern ('file_[absh]'), the shell will not expand it; quoting is useful when you want the literal pattern rather than expansion.



## Incorrect Tangents
   
N/A


## References

N/A
