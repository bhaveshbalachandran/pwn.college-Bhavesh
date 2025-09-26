## Challenge 3: more_catting_practice

The challenge is about using absolute paths to read files with
cat when you are not allowed to change directories. The flag will be
placed somewhere in the filesystem in a “crazy” directory; you must
find its absolute path and cat it — you cannot rely on cd or on relative paths

## My Solve
**Flag:**'pwn.college{47bllCmxFhn0TPiTAtadBgczaUe.QXwITO0wiNyEzNzEzW}'

To solve this I searched the filesystem from '/' for the flag file
and then used its absolute path with cat to read it.
```
hacker@commands~more-catting-practice:~$ cat /usr/include/netpacket/flag
pwn.college{47bllCmxFhn0TPiTAtadBgczaUe.QXwITO0wiNyEzNzEzW}
```

## What I Learned

You can always pass an absolute path to cat and it will
read that file regardless of your current working directory.
When you cannot 'cd' use tools like 'find'
   

## Incorrect tangents
Trying 'cd'  is disallowed by the challenge
Typing cat f without knowing you’re in the directory
containing the file will fail

## References
N/A
