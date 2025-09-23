# Pondering Paths

## Position thy self
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{UkG1MA5ZnjH16wT5bVpIjLTDnPH.QX2QTN0wCO4kjNzEzW}`

Thought process: since I didnt know which directory exactly it would ask me to invoke the program from, i proceeded to first invoke it through the absolute path hoping it would give me a hint and consequently it did and provided the pathway through which i was supposed to invoke the directory and hence used that to get the flag.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/doc/fontconfig
hacker@paths~position-thy-self:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{UkG1MA5ZnjH16wT5bVpIjLTDnPH.QX2QTN0wCO4kjNzEzW}
```

### New Learnings
Since I closed my WSL terminal in between this challenge i faced a difficulty in relinking the ssh key back to pwn.college. I had to use eval $(ssh-agent) && ssh-add to reconnect again.
With respect to the challenge, I learnt how the terminal gives signals whether a certain directory can be invoked directly or through a certain specified pathway. I also learnt how to navigate through various paths using the cd command.
### References 
NA

