## Challenge 2: redirecting_more_output

This level practices redirecting standard output from arbitrary programs into files. The challenge program /challenge/run prints status and prompts on stderr but prints the actual flag on stdout — so you must redirect stdout into a file named myflag to capture the flag, then read that file.

## My Solve
**Flag:**'pwn.college{ELmLZJeF_zVyswpzXiLAGfSSrns.QX1YTN0wiNyEzNzEzW}'

```

hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{ELmLZJeF_zVyswpzXiLAGfSSrns.QX1YTN0wiNyEzNzEzW}

```

## What I Learned

> redirects outputs as well.


## Incorrect Tangents

N/A


## References

N/A


