# Pondering Paths

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
