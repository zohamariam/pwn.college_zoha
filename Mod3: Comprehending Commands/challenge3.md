# Comprehending Commands

## more catting practice
You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. 
In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you.
You must retrieve the flag by absolute path, wherever it is.

### Solve
**Flag:** `pwn.college{4iDt6h3lYorYa7Pjt5wSZLVDvfw.QXwITO0wCO4kjNzEzW}`

```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/lib/ipxe/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/lib/ipxe/flag
pwn.college{4iDt6h3lYorYa7Pjt5wSZLVDvfw.QXwITO0wCO4kjNzEzW}
```

### New Learnings
I learnt that I can use any sort of path as an argument to a command and hence found the flag by navigating into the file by using cat with the given path as the argument.

### References 
NA
