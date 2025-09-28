## Challenge 2: matching_with ?

The challenge is about the single-character wildcard ?. Unlike *, which matches any string (including empty), ? matches exactly one character. The task: starting from your home directory, cd into /challenge but use ? in place of the letters c and l in the argument you pass to cd. Then run /challenge/run for the flag.


## My Solve
**Flag:**'pwn.college{gc_TjLMqI8LoU8s3yyenr5eT5h8.QXyIDO0wiNyEzNzEzW}'

I used a pattern where each ? stands for a single character. Replacing c and both l characters in challenge with ? gives the pattern /?ha??enge, which the shell expanded to /challenge before cd ran:

```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{gc_TjLMqI8LoU8s3yyenr5eT5h8.QXyIDO0wiNyEzNzEzW}

```

## What I Learned 

? matches exactly one character in shell globbing; multiple ?s match multiple single characters.
You can replace specific letters in a known name with ? to build concise patterns that still uniquely identify the target.
Use * when you want variable-length matches and ? when you need precise single-character substitution.


## Incorrect Tangents

N/A


## References

N/A
