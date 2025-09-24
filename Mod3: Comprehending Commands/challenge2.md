# Comprehending Commands

## catting absolute paths
In the last level, you did cat flag to read the flag out of your home directory! You can, of course, specify cat's arguments as absolute paths:
```
hacker@dojo:~$ cat /challenge/DESCRIPTION.md
In the last level, you did `cat flag` to read the flag out of your home directory!
You can, of course, specify `cat`'s arguments as absolute paths:
...
```
In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.

FUN FACT: /flag is where the flag always lives in pwn.college, but unlike in this challenge, you typically can't access that file directly.

### Solve
**Flag:** `pwn.college{g97YbPw4XxPZjH5dXjI9vkDlF-j.QX5ETO0wCO4kjNzEzW}`

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{g97YbPw4XxPZjH5dXjI9vkDlF-j.QX5ETO0wCO4kjNzEzW}
```

### New Learnings
I learnt that we can read a file using cat and absolute path of the file as the argument.

### References 
NA
