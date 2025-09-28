## Challenge 6: helping_programs

The challenge is about discovering quick program documentation using the common --help flags. 
Some programs do not ship a manpage, but will print usage information when invoked with --help, -h, or other help-style options.


## My Solve 
**Flag:**'pwn.college{QUhgUkTp8j11MjEzp_JlLB2OMTZ.QX3IDO0wiNyEzNzEzW}'

```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give
                        you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 811
hacker@man~helpful-programs:~$ /challenge/challenge -g 811
Correct usage! Your flag: pwn.college{QUhgUkTp8j11MjEzp_JlLB2OMTZ.QX3IDO0wiNyEzNzEzW}
```

## What I Learned

Many programs support a quick help option; the most common is --help, but -h, help, or -? are also used.
Using --help is safe and non-destructive — it’s a good first step before trying unknown options.

## Incorrect Tangents

N/A


## References

N/A
