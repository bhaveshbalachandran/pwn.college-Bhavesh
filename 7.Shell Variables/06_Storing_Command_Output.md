## Challenge 6: storing_command_output

The challenge is about command substitution — running a command and placing its stdout directly into a shell variable. The task: run /challenge/run and store its output in a variable named PWN, then print that variable to reveal the flag.


## My Solve 
**Flag:**'pwn.college{MoLL3YApwVTvxCUFzJ4moItL9Hl.QX1cDN1wiNyEzNzEzW}'

```

hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{MoLL3YApwVTvxCUFzJ4moItL9Hl.QX1cDN1wiNyEzNzEzW}

```


## What I Learned


Use VAR=$(command) to capture a command’s stdout into the shell variable VAR.
Quote variable expansions when printing (echo "$VAR") to preserve exact whitespace and avoid word-splitting.


## Incorrect Tangents
   
N/A


## References

N/A

