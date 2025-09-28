## Challenge 9: multiple_options_for_tab_completion

The challenge explores what happens when tab-completion has more than one possible match. Different shells/configurations handle this differently (bash usually completes up to the common prefix and a second TAB lists candidates; other shells may cycle). The level places many files starting with pwncollege under /challenge/files; you must use tab completion from a sensible prefix to reach the flag file and cat it.


## My Solve
**Flag:**'pwn.college{A9H6ZBxcb4PUg56b7UQThElq6cV.0lN0EzNxwiNyEzNzEzW}'

```
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-
pwncollege-family      pwncollege-flamingo    pwncollege-hacking
pwncollege-flag        pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag
pwn.college{A9H6ZBxcb4PUg56b7UQThElq6cV.0lN0EzNxwiNyEzNzEzW}
```

## What I Learned 

if there are multiple files that match the text they are all displayed together
Pressing TAB twice in bash is a quick way to see all completion candidates so you can choose a longer prefix.


## Incorrect Tangents
   
N/A


## References

N/A
