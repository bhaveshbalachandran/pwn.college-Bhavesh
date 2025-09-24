# Intro to commands 
this challenge expects to run a simple command called hello that will output the flag 
the challenge 

## My solve 
**Flag** 'pwn.college{cinwTt0x1qBDHc4aFEIrysBcgNu.QX3YjM1wiNyEZNZEZW}'

The challenge text explicitly says “invoke the hello command to get the flag.” 
the direct approach is to run the named command.
 first confirmed I had a working shell then executed hello .
Once the command printed text that matched the pattern, 
I copied it as the flag.

```bash
$ hello 
pwn.college{cinwTt0x1qBDHc4aFEIrysBcgNu.QX3YjM1wiNyEZNZEZW}
 
