## Challenge 6: grepping_stored_results

This level combines redirection and searching: you must capture a large program output into a file and then grep that file for the flag.

## My Solve 
**Flag:**'pwn.college{QRWdjc_pn63gHsbkRng17tV1OkD.QX4EDO0wiNyEzNzEzW}'

```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwns
pwn
pwned
pwning
pwn.college{QRWdjc_pn63gHsbkRng17tV1OkD.QX4EDO0wiNyEzNzEzW}
```

## What I Learned 

Redirecting stdout (> file) is handy to capture large program outputs for later analysis without flooding your terminal.


## Incorrect Tangents
   
N/A


## References

N/A

