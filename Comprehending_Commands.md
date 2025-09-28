# Comprehending Commands

## cat: not the pet, but the command!
One of the most critical Linux commands is cat. cat is most often used for reading out files, like so:
```
hacker@dojo:~$ cat /challenge/DESCRIPTION.md
One of the most critical Linux commands is `cat`.
`cat` is most often used for reading out files, like so:
```
cat will concatenate (hence the name) multiple files if provided multiple arguments. For example:
```
hacker@dojo:~$ cat myfile
This is my file!
hacker@dojo:~$ cat yourfile
This is your file!
hacker@dojo:~$ cat myfile yourfile
This is my file!
This is your file!
hacker@dojo:~$ cat myfile yourfile myfile
This is my file!
This is your file!
This is my file!
```
Finally, if you give no arguments at all, cat will read from the terminal input and output it. We'll explore that in later challenges...

In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!

### Solve
**Flag:** `pwn.college{0lZbPGbpMXwwkjweW0M-qwS1AEi.QXxcTN0wCO4kjNzEzW}`

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{0lZbPGbpMXwwkjweW0M-qwS1AEi.QXxcTN0wCO4kjNzEzW}
```

### New Learnings
I learnt how to use the cat command and its working principle (to concatenate).

### References 
NA

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

## grepping for a needle in a haystack
Sometimes, the files that you might cat out are too big. Luckily, we have the grep command to search for the contents we need! We'll learn it in this challenge.

There are many ways to grep, and we'll learn one way here:
```
hacker@dojo:~$ grep SEARCH_STRING /path/to/file
```
Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!

HINT: The flag always starts with the text pwn.college.

### Solve
**Flag:** `pwn.college{gXl3oAGUsvVN7Quuys73nPfKn9E.QX3EDO0wCO4kjNzEzW}`

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{gXl3oAGUsvVN7Quuys73nPfKn9E.QX3EDO0wCO4kjNzEzW}
```

### New Learnings
I learnt how to search for a particular text from a big file by using the grep command.

### References 
NA

## comparing files
When looking for changes between similar files, eyeballing them might not be the most efficient approach! This is where the diff command becomes invaluable.

diff compares two files line by line and shows you exactly what's different between them. For example:
```
hacker@dojo:~$ cat file1
hello
world
hacker@dojo:~$ cat file2
hello
universe
hacker@dojo:~$ diff file1 file2
2c2
< world
---
> universe
```
The output tells us that line 2 changed (2c2), with world in the first file (<) being replaced by universe in the second file (>).

Sometimes, when new lines are added, you'll see something like:
```
hacker@dojo:~$ cat old
pwn
hacker@dojo:~$ cat new
pwn
college
hacker@dojo:~$ diff old new
1a2
> college
```
This tells us that after line 1 in the first file, the second file has an additional line (1a2 means "after line 1 of file1, add line 2 of file2").

Now for your challenge! There are two files in /challenge:

* /challenge/decoys_only.txt contains 100 fake flags
* /challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag

Use diff to find what's different between these files and get your flag!

### Solve
**Flag:** `pwn.college{0ay5OF9v7f-VrOgwIlnG58cV0xM.01MwMDOxwCO4kjNzEzW}`

For this challenge, I followed the instructions by first navigating to the /challenge directory with the cd command and then using the diff command to compare the two files provided to find the real flag.

```
hacker@commands~comparing-files:~$ cd /challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt
88a89
> pwn.college{0ay5OF9v7f-VrOgwIlnG58cV0xM.01MwMDOxwCO4kjNzEzW}
```

### New Learnings
I learnt how to use the diff command to compare files.

### References 
NA

## listing files
So far, we've told you which files to interact with. But directories can have lots of files (and other directories) inside them, and we won't always be here to tell you their names. You'll need to learn to list their contents using the ls command!

ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. Observe:
```
hacker@dojo:~$ ls /challenge
run
hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ ls /home/hacker
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$
```
In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.

### Solve
**Flag:** `pwn.college{helloworld}`

At first, I listed out the contents of /challenge to find two files, one was description.md and the other was the renamed run file. I first mistook the description.md to be the renamed file and used the cat command on it, but realised that it wasn't what I was supposed to do. Then I used the cat command for the other file and got another message. This then indicated which command I should invoke to get the flag.

```
hacker@commands~listing-files:~$ ls /challenge
25770-renamed-run-26838  DESCRIPTION.md
hacker@commands~listing-files:~$ cd /challenge/DESCRIPTION.md
bash: cd: /challenge/DESCRIPTION.md: Not a directory
hacker@commands~listing-files:~$ cat /challenge/25770-renamed-run-26838
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:~$ /opt/pwn.college/bash /challenge/25770-renamed-run-26838
Yahaha, you found me! Here is your flag:
pwn.college{YkJ2B6z3ZSPliKUhGJt53Q7q0pf.QX4IDO0wCO4kjNzEzW}
```

### New Learnings
learnt how to use the ls command and also incorporated the cat command learnt in the previous challenges

### References 
NA

## touching files
Of course, you can also create files! There are several ways to do this, but we'll look at a simple command here. You can create a new, blank file by touching it with the touch command:
```
hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ touch pwnfile
hacker@dojo:/tmp$ ls
pwnfile
hacker@dojo:/tmp$
```
It's that simple! In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag!

### Solve
**Flag:** `pwn.college{YZMA0frgwCZlFVvECeok-aLvI99.QXwMDO0wCO4kjNzEzW}`

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.4mK6TfTSUV
hacker@commands~touching-files:/tmp$ cd
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{YZMA0frgwCZlFVvECeok-aLvI99.QXwMDO0wCO4kjNzEzW}
```

### New Learnings
learnt how to create new files using the touch command

### References 
NA

## removing files
Files are all around you. Like candy wrappers, there'll eventually be too many of them. In this level, we'll learn to clean up!

In Linux, you remove files with the rm command, as so:
```
hacker@dojo:~$ touch PWN
hacker@dojo:~$ touch COLLEGE
hacker@dojo:~$ ls
COLLEGE     PWN
hacker@dojo:~$ rm PWN
hacker@dojo:~$ ls
COLLEGE
hacker@dojo:~$
```
Let's practice. This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag!

### Solve
**Flag:** `pwn.college{MenT7CUbqc6jP1FLmwR6ts7q-nM.QX2kDM1wCO4kjNzEzW}`

```
hacker@commands~removing-files:~$ ls
a  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{MenT7CUbqc6jP1FLmwR6ts7q-nM.QX2kDM1wCO4kjNzEzW}
```

### New Learnings
learnt how to delete a file in a directory using rm command.

### References 
NA

## moving files
You can also move files around with the mv command. The usage is simple:
```
hacker@dojo:~$ ls
my-file
hacker@dojo:~$ cat my-file
PWN!
hacker@dojo:~$ mv my-file your-file
hacker@dojo:~$ ls
your-file
hacker@dojo:~$ cat your-file
PWN!
hacker@dojo:~$
```
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

### Solve
**Flag:** `pwn.college{08Y_wSccTSCbWkLyMwjD314uhHv.0VOxEzNxwCO4kjNzEzW}`

```
hacker@commands~moving-files:~$ ls
a
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{08Y_wSccTSCbWkLyMwjD314uhHv.0VOxEzNxwCO4kjNzEzW}
```

### New Learnings
learnt how to move files using mv command.

### References 
NA

## hidden files
Interestingly, ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag, as so:
```
hacker@dojo:~$ touch pwn
hacker@dojo:~$ touch .college
hacker@dojo:~$ ls
pwn
hacker@dojo:~$ ls -a
.college	pwn
hacker@dojo:~$
```
Now, it's your turn! Go find the flag, hidden as a dot-prepended file in /.

### Solve
**Flag:** `pwn.college{0Bi92eHQjqAEbT4pdDF1M96yFf3.QXwUDO0wCO4kjNzEzW}`

```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-7486242329709  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-7486242329709
pwn.college{0Bi92eHQjqAEbT4pdDF1M96yFf3.QXwUDO0wCO4kjNzEzW}
```

### New Learnings
Learnt how to check for hidden files in the directory using the ls -a command

### References 
NA

## An Epic Filesystem Quest
With your knowledge of cd, ls, and cat, we're ready to play a little game!

We'll start it out in /. Normally:
```
hacker@dojo:~$ cd /
hacker@dojo:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  dev        flag  lib   lib64  media   opt  root  sbin  sys  usr
```
That's a lot of contents! One day, you will be quite familiar with them, but already, you might recognize the flag file and the challenge directory.

In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

0. Your first clue is in /. Head on over there.
1. Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
2. cat that file to read the clue!
3. Depending on what the clue says, head on over to the next directory (or don't!).
4. Follow the clues to the flag!
Good luck!

### Solve
**Flag:** `pwn.college{cm2DXVg2ypSj5AsDESf7bZSOtBq.QX5IDO0wCO4kjNzEzW}`

The overall process was tedious and maybe a few negative tangents along the way which is displayed in the code below but it was pretty self-explanatory. 

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
SPOILER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat SPOILER
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386$ ls -a
.  ..  .POINTER  __init__.py  __pycache__  ascii_shellcode.py  delta.py  xor.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386$ cat .POINTER
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/angr/analyses/decompiler/structuring
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386$ cd .
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib/encoders/i386$ cd ..
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib/encoders$ cd ..
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/pwnlib$ cd ..
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages$ cd .angr/analyses/decompiler/structuring
bash: cd: .angr/analyses/decompiler/structuring: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages$ cd angr/analyses/decompiler/structuring
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/analyses/decompiler/structuring$ ls
ALERT  __init__.py  __pycache__  dream.py  phoenix.py  recursive_structurer.py  structurer_base.py  structurer_nodes.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/analyses/decompiler/structuring$ cat ALERT
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl/cross-config-5.30.0
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/analyses/decompiler/structuring$ cd
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/lib/x86_64-linux-gnu/perl/cross-config-5.30.0
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/cross-config-5.30.0$ ls
Config.pm  Config_heavy.pl  README
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/cross-config-5.30.0$ cat README
Great sleuthing!
The next clue is in: /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Main/BoldItalic

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/cross-config-5.30.0$ cd /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Main/BoldItalic
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Main/BoldItalic$ ls -a
.  ..  .NUGGET  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Main/BoldItalic$ cat .NUGGET
Congratulations, you found the clue!
The next clue is in: /usr/lib/R/library/base/help

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Main/BoldItalic$ cd /usr/lib/R/library/base/help
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/base/help$ ls
AnIndex  DOSSIER  aliases.rds  base.rdb  base.rdx  paths.rds
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/base/help$ cd DOSSIER
bash: cd: DOSSIER: Not a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/base/help$ cd AnIndex
bash: cd: AnIndex: Not a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/base/help$ cat DOSSIER
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/base/help$ cd /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed$ la
bash: la: command not found
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed$ ls
HINT  LICENSE  stdlib  third_party
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed$ cat HINT
Yahaha, you found me!
The next clue is in: /usr/lib/jvm/java-17-openjdk-amd64/legal/jdk.security.auth

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/lib/jvm/java-17-openjdk-amd64/legal/jdk.security.auth
ASSEMBLY_EXCEPTION  WHISPER-TRAPPED
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/lib/jvm/java-17-openjdk-amd64/legal/jdk.security.auth/WHISPER-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/lib/x86_64-linux-gnu/lua/5.2

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/lib/x86_64-linux-gnu/lua/5.2
GIST-TRAPPED  lpeg.so  luv.so
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/lib/x86_64-linux-gnu/lua/5.2/GIST-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{cm2DXVg2ypSj5AsDESf7bZSOtBq.QX5IDO0wCO4kjNzEzW}
```

### New Learnings
learnt the extensive use of the ls, ls -a, cd and the cat commands in solving the quest.

### References 
NA



