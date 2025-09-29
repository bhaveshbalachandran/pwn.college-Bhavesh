## Challenge 7: grepping_live_output

The challenge is about piping live program output into grep so you can search a stream without first writing it to disk. The | operator connects stdout of the left-hand command to stdin of the right-hand command, so you can run /challenge/run and immediately filter its output for the flag.


## My Solve 
**Flag:**'pwn.college{gqc3Yidxvx0yeP3ZqDfgY4fVAdj.QX5EDO0wiNyEzNzEzW}'

```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{gqc3Yidxvx0yeP3ZqDfgY4fVAdj.QX5EDO0wiNyEzNzEzW}
pwns
pwned
pwn
pwning
```

## What I Learned

The pipe | feeds stdout of one command into stdin of another, enabling streaming workflows


## Incorrect Tangents
   
N/A


## References

N/A




