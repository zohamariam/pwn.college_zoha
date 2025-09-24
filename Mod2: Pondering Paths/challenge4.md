# Pondering Paths

## Position elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{EXZhzD56nvOsEweZXnQDO1nWylY.QX3QTN0wCO4kjNzEzW}`

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/run$ cd /
hacker@paths~position-elsewhere:/$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EXZhzD56nvOsEweZXnQDO1nWylY.QX3QTN0wCO4kjNzEzW}
```

### New Learnings
I learnt how to navigate to the root directory using cd command

### References 
NA

