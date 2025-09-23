# Hello Hackers

## Intro to Arguments
Let's try something more complicated: a command with arguments, which is what we call additional data passed to the command. When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments. Observe:
```
hacker@dojo:~$ echo Hello
Hello
hacker@dojo:~$
```
In this case, the command was echo, and the argument was Hello. echo is a simple command that "echoes" all of its arguments back out onto the terminal, like you see in the session above.

Let's look at echo with multiple arguments:
```
hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
hacker@dojo:~$
```
In this case, the command was echo, and Hello and Hackers! were the two arguments to echo. Simple!

In this challenge, to get the flag, you must run the hello command (NOT the echo command) with a single argument of hackers. Try it now!

### Solve
**Flag:** `pwn.college{Yq2E8owjKxLfiSad8w7YrHHTk08.QX4YjM1wCO4kjNzEzW}`
```
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{Yq2E8owjKxLfiSad8w7YrHHTk08.QX4YjM1wCO4kjNzEzW}
```
### New Learnings
Learnt the concept of arguments, wherein the first word in the command line is always the command and the subsequent words are the arguments which are additional data to pass the commands.
Understood how the echo command works and used the 'hello' command with the 'hackers' argument to obtain the flag.

### References 
NA
