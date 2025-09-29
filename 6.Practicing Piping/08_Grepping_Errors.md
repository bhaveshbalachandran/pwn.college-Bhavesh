## Challenge 8: grepping_errors

This level teaches how to search (grep) text that a program writes to standard error (FD 2). Pipes (|) only connect stdout (FD 1) to the next command, so to grep stderr you first redirect stderr into stdout and then pipe the combined stream into grep.


## My Solve 
**Flag:**'pwn.college{kogdig0gKfzWSlCcJ1_LccK3V_j.QX1ATO0wiNyEzNzEzW}'

```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwns
pwn
pwning
pwn.college{kogdig0gKfzWSlCcJ1_LccK3V_j.QX1ATO0wiNyEzNzEzW}
pwned
```

## What I Learned 

2>&1 makes stderr (fd 2) go to the same place as stdout (fd 1), so subsequent | pipes will see the former.
|& is a bash (and some other shells) shorthand for 2>&1 |.


## Incorrect Tangents
   
N/A


## References

N/A

