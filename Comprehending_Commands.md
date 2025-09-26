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
