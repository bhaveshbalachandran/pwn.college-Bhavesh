## Challenge 4: exporting_variables

This level teaches the difference between a shell-local variable and an exported (environment) variable. You must run /challenge/run with PWN exported and set to COLLEGE, while COLLEGE should be set to PWN but not exported (so the child process does not see COLLEGE).


## My Solve 
**Flag:**'pwn.college{khReCA1ON1cfJ91oTTbWtluq--Q.QXyYTN0wiNyEzNzEzW}'

```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!

```


## What I Learned 

NAME=value assigns a shell-local variable
export NAME=value


## Incorrect Tangents
   
N/A


## References

N/A

