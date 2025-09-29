## Challenge 9: filtering_with_grep -v

The challenge is about removing unwanted lines from a stream using grep -v (invert match). /challenge/run prints the real flag and many decoy lines that include the literal DECOY. Use grep -v 'DECOY' to remove those decoys and reveal the true flag.


## My Solve 
**Flag:**'pwn.college{MQ1QKcv4VQ_LUls12Nes9EZsS8h.0FOxEzNxwiNyEzNzEzW}'

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{MQ1QKcv4VQ_LUls12Nes9EZsS8h.0FOxEzNxwiNyEzNzEzW}

```

## What I Learned 

grep -v PATTERN prints lines that do not match PATTERN — useful to remove noisy or decoy lines.
Combining grep -v with a second grep for the desired pattern is a common, efficient pipeline: remove the junk, then pick the useful content.


## Incorrect Tangents
   
N/A


## References

N/A



