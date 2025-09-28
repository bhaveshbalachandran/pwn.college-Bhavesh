## Challenge 8: tab_completion

The challenge demonstrates using the shell’s tab completion to complete a filename you are unable (or discouraged) to type fully. The file /challenge/pwncollege is present but typing it directly fails; pressing <Tab> lets the shell expand the partial name into the correct full filename so you can cat it.

## My Solve
**Flag:**'pwn.college{UGmk2zyRFdieSFjmpUtUL7sxTFd.0FN0EzNxwiNyEzNzEzW}'

I listed /challenge to confirm the entry and then used tab-completion to expand the partial name before running cat:

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0FwGPtyocVplHBp1TfEFqZ2RfZf.QX2IDO0wiNyEzNzEzW}
```

## What I Learned

Tab can be used to complete the file path 


## Incorrect Tangents
   
N/A


## References

N/A

