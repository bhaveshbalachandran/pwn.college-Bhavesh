## Challenge 7: help_for_builtins

The challenge is about shell builtins — commands implemented inside the shell itself — and using the shell's help builtin to read their documentation.


## My Solve 
**Flag:**'pwn.college{4TzZE-gvvSacPLYAzrLpkgYnpwQ.QX0ETO0wiNyEzNzEzW}'

I used the shell help builtin to read the documentation for the challenge builtin, discovered the secret option, and invoked the builtin with that option to print the flag:

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "4TzZE-gv".
hacker@man~help-for-builtins:~$ challenge --secret 4TzZE-gv
Correct! Here is your flag!
pwn.college{4TzZE-gvvSacPLYAzrLpkgYnpwQ.QX0ETO0wiNyEzNzEzW}

```

## What I Learned

Builtins are implemented inside the shell and are documented with the help builtin: help lists builtins and help <name> shows the usage for a specific builtin.


## Incorrect Tangents

N/A


## References

N/A
