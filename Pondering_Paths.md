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


## Program and absolute paths
Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn, in the / directory. If you invoke the challenge correctly, it will give you the flag. Good luck!

### Solve
**Flag:** `pwn.college{UvXnaUyOoF-y3Ds-Cqpn9cfWaMT.QX1QTN0wCO4kjNzEzW}`

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{UvXnaUyOoF-y3Ds-Cqpn9cfWaMT.QX1QTN0wCO4kjNzEzW}
```

### New Learnings
determining the absolute path of the given program by navigating through the given directories starting by the root /

### References 
NA


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

## Position yet elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{QI5mBzASJfCInOPqzPZbcQxh2G8.QX4QTN0wCO4kjNzEzW}`

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{QI5mBzASJfCInOPqzPZbcQxh2G8.QX4QTN0wCO4kjNzEzW}
```

### New Learnings
I learnt how to invoke the given absolute path by navigating to the /tmp directory using cd command

### References 
NA

## implicit relative paths, from /
Now you're familiar with the concept of referring to absolute paths and changing directories. If you put in absolute paths everywhere, then it really doesn't matter what directory you are in, as you likely found out in the previous three challenges.

However, the current working directory does matter for relative paths.

* A relative path is any path that does not start at root (i.e., it does not start with /).
* A relative path is interpreted relative to your current working directory (cwd).
* Your cwd is the directory that your prompt is currently located at.
This means how you specify a particular file, depends on where the terminal prompt is located.

Imagine we want to access some file located at /tmp/a/b/my_file.

* If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
* If my cwd is /tmp, then a relative path to the file is a/b/my_file.
* If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.

  Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c 😊

### Solve
**Flag:** `pwn.college{s1baK9fmrN18zaAN6vTAn3p32zU.QX5QTN0wCO4kjNzEzW}`

Thought process: First, I navigated to the / directory using cd and then used the ls command to check which files are present in the current working directory to cross-check whether there are more relative paths that begin with c

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{s1baK9fmrN18zaAN6vTAn3p32zU.QX5QTN0wCO4kjNzEzW}
```

### New Learnings
I learnt how to invoke a relative path from a current working directory.

### References 
NA

## explicit relative paths, from /
Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:

* /challenge
* /challenge/.
* /challenge/./././././././././
* /./././challenge/././

The following relative paths are also all identical to each other:
* challenge
* ./challenge
* ./././challenge
* challenge/.

Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths. Get ready!

### Solve
**Flag:** `pwn.college{4LtT2-LSdlqD_0sf0U8Mf_lHrAo.QXwUTN0wCO4kjNzEzW}`

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4LtT2-LSdlqD_0sf0U8Mf_lHrAo.QXwUTN0wCO4kjNzEzW}
```

### New Learnings
Learnt to use . in invoking relative paths from a current working directory.

### References 
NA

## implicit relative path
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. Here, things get slightly tricky.

Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:
```
hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ run
```
This will not invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! 
As a result, the above commands will yield the following error:
```
bash: run: command not found
```
We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. 
The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!

### Solve
**Flag:** `pwn.college{YyUFvktiqnAeW4rFX8jJHMFxeF7.QXxUTN0wCO4kjNzEzW}`

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YyUFvktiqnAeW4rFX8jJHMFxeF7.QXxUTN0wCO4kjNzEzW}
```

### New Learnings
Learnt the explicit use of . to avoid getting error by using naked path.

### References 
NA

## home sweet home
Every user has a home directory, typically under /home in the filesystem. In the dojo, you are the hacker user, and your home directory is /home/hacker. The home directory is typically where users store most of their personal files.
As you make your way through pwn.college, this is where you'll store most of your solutions.

Typically, your shell session will start with your home directory as your current working directory. Consider the initial prompt:
```
hacker@dojo:~$
```
The ~ in this prompt is the current working directory, with ~ being shorthand for /home/hacker. Bash provides and uses this shorthand because, again, most of your time will be spent in your home directory. 
Thus, whenever bash sees ~ provided as the start of an argument in a way consistent with a path, it will expand it to your home directory. Consider:
```
hacker@dojo:~$ echo LOOK: ~
LOOK: /home/hacker
hacker@dojo:~$ cd /
hacker@dojo:/$ cd ~
hacker@dojo:~$ cd ~/asdf
hacker@dojo:~/asdf$ cd ~/asdf
hacker@dojo:~/asdf$ cd ~
hacker@dojo:~$ cd /home/hacker/asdf
hacker@dojo:~/asdf$
```
Note that the expansion of ~ is an absolute path, and only the leading ~ is expanded. This means, for example, that ~/~ will be expanded to /home/hacker/~ rather than /home/hacker/home/hacker.

Fun fact: cd will use your home directory as the default destination:
```
hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ cd
hacker@dojo:~$
```
Now it's your turn to play! In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

1. Your argument must be an absolute path.
2. The path must be inside your home directory.
3. Before expansion, your argument must be three characters or less.
Again, you must specify your path as an argument to /challenge/run as so:
```
hacker@dojo:~$ /challenge/run YOUR_PATH_HERE
```
### Solve
**Flag:** `pwn.college{sM363hQiHlBXXOMyv29x7ea0K_q.QXzMDO0wCO4kjNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```
hacker@paths~home-sweet-home:~$ cd
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{sM363hQiHlBXXOMyv29x7ea0K_q.QXzMDO0wCO4kjNzEzW}
```

### New Learnings
learnt how to use an absolute path as an argument using less than three characters to obtain the flag.

### References 
NA
