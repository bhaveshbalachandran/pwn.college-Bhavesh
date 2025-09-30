## Challenge 13: Split-piping_stderr_and_stdout

The challenge is to send one program’s stdout into one consumer and its stderr into a different consumer, without mixing the two streams. The pipe operator (|) only connects stdout to the next command, and 2>&1 merges stderr into stdout (which mixes them). The clean solution is to use output process substitution (>(command)) to give the producer two writeable “files” — one for stdout and one for stderr — each hooked to a separate consumer.

## My Solve 
**Flag:**'pwn.college{wGkD0xg1oS61_wnGdws_6TsET_R.QXxQDM2wiNyEzNzEzW}'

```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{wGkD0xg1oS61_wnGdws_6TsET_R.QXxQDM2wiNyEzNzEzW}
```

## What I Learned

Process substitutions are expanded by the shell before launching the pipeline; the shell launches the consumer processes and supplies file-like paths for the producer to write to.


## Incorrect Tangents
   
N/A


## References

N/A


