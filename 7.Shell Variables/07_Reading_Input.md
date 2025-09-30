## Challenge 7: reading_input

This level teaches how to read input from the user into a shell variable using the read builtin. Your goal is to set the variable PWN to the value COLLEGE using read.


## My Solve 
**Flag:**'pwn.college{o3ISw8xA_V1X9a1I9DZ4HaPeAUR.QX4cTN0wiNyEzNzEzW}'

```
hacker@variables~reading-input:~$ read -p "Enter: " PWN
Enter: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{o3ISw8xA_V1X9a1I9DZ4HaPeAUR.QX4cTN0wiNyEzNzEzW}

```


## What I Learned 


read VAR reads from stdin into VAR. Use -p to present a prompt interactively.


## Incorrect Tangents
   
N/A


## References

N/A


