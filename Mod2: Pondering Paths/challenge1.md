# Pondering Paths

## The Root
Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!

You can invoke a program by providing its path on the command line. In this case, you'll be giving the exact path, starting from /, so the path would be /pwn. This style of path, one that starts with the root directory, is referred to as an "absolute path".

Start the challenge, launch a terminal, invoke the pwn program using its absolute path, and Capture that Flag! Good luck!

### Solve
**Flag:** `pwn.college{oEGJ6W11c0HM93_EqsLWmXlwsDq.QX4cTO0wCO4kjNzEzW}`

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{oEGJ6W11c0HM93_EqsLWmXlwsDq.QX4cTO0wCO4kjNzEzW}
```

### New Learnings
Files need to be saved in directories to organise them and keep track of them. Some directories can be inside other directories. The file path in Linux is basically like a tree branching out. The root directory is denoted by / and contains all other files and directories. Giving an exact path of a file starting with / is called the absolute path.

### References 
NA

