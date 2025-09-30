## Challenge 11: process_substitution_for_input

The challenge is about process substitution — using <(command) to present a running command’s stdout as a file-like argument — and using it to compare outputs of two commands with diff without creating any temporary files on disk.


## My Solve 
**Flag:**'pwn.college{AcXb2QrEZ-FuKKlWFjPxCEws5dK.0lNwMDOxwiNyEzNzEzW}'

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
65a66
> pwn.college{AcXb2QrEZ-FuKKlWFjPxCEws5dK.0lNwMDOxwiNyEzNzEzW}
```

## What I Learned

<(givenfile) is a placeholder for the output of the given file 


## Incorrect Tangents
   
N/A


## References

N/A


