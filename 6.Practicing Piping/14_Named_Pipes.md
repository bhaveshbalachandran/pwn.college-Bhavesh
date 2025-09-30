## Challenge 14: named_pipes

This challenge introduces FIFOs / named pipes. You create a persistent pipe with mkfifo, then one process writes into it and another reads from it. Writers/readers block until the other side opens the FIFO, which gives automatic synchronization (handy for coordinating two processes).
In this level you must create /tmp/flag_fifo and redirect stdout of /challenge/run into it so the challenge writes the flag into the FIFO — but because FIFOs block, you also need a reader  open on the other end to receive the flag.


## My Solve
**Flag:**'pwn.college{AXhhND1MBurzXqmP1E12pnjKFg5.01MzMDOxwiNyEzNzEzW}'

```
Terminal 1 

hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{AXhhND1MBurzXqmP1E12pnjKFg5.01MzMDOxwiNyEzNzEzW}

Terminal 2 

hacker@piping~named-pipes:~$ /challenge/run >/tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
```


## What I Learned 

FIFOs only executes a command when both read and write operations are acting on them 



## Incorrect Tangents
   
N/A


## References

N/A

