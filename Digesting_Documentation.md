# Digesting Documentation

## Learning From Documentation
The typical need you'll have for documentation is just to figure out how to use all these dang programs, and a specific case of that is figuring out what arguments to specify on the command line. This module will mostly dig into that concept, as a proxy for figuring out how to use the programs in general. Through the rest of the module, you'll go through various ways of asking the environment for help for the programs, but first, we'll dig into the concept of reading documentation.

The correct usage of programs depends, in a large part, on the proper specification of arguments to them. Recall the -a of ls -a in the hidden files challenge of the Basic Commands module: that -a was an argument that told ls to list out hidden files as well as non-hidden files. Because we wanted to list out hidden files, invoking ls with the -a argument was the correct way to use it in our scenario.

The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag. Let's pretend that this is its documentation:

`Welcome to the documentation for /challenge/challenge! To properly run this program, you will need to pass it the argument of --giveflag. Good luck!`

Given that knowledge, go get the flag!

### Solve
**Flag:** `pwn.college{0n1K49U936ONuXzQgoRYdu581lg.QX0ITO0wCO4kjNzEzW}`

At first I thought the argument was supposed to be /challenge/challenge, but it was the other way around, and hence I retrieved the flag.

```
hacker@man~learning-from-documentation:~$ --giveflag /challenge/challenge
bash: --giveflag: command not found
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0n1K49U936ONuXzQgoRYdu581lg.QX0ITO0wCO4kjNzEzW}
```

### New Learnings
learnt how to read and process a given documentation of invoking certain files using given arguments and commands.

### References 
NA



