## Challenge 10: Duplicating_piped_data_with_tee

The challenge is about using tee to duplicate piped data so you can both forward a stream to a consumer and capture a copy for inspection. The level requires you to pipe /challenge/pwn into /challenge/college, but you must intercept (view/save) what /challenge/pwn emits so you can see what /challenge/college expects.


## My Solve 
**Flag:**'pwn.college{02fjuv-ywlDnqUQR3AoQXIQUxbO.QXxITO0wiNyEzNzEzW}'

```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee /tmp/pwn_output | /challenge/college
Processing...
WARNING: you are overwriting file /tmp/pwn_output with tee's output...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat /tmp/pwn_output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "02fjuv-y"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 02fjuv-y | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{02fjuv-ywlDnqUQR3AoQXIQUxbO.QXxITO0wiNyEzNzEzW}
```

## What I Learned

tee FILE duplicates the incoming stream: one copy goes to FILE, another to stdout so downstream commands still receive the data.


## Incorrect Tangents
   
N/A


## References

N/A

