# Hello Hackers
 ## Intro To Commands
  In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:  
  ```
  hacker@dojo:~$ whoami  
hacker  
hacker@dojo:~$  
```
Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.  

In this level, invoke the hello command to get the flag! Keep in mind: commands in Linux are case sensitive: hello is different from HELLO.  
  ### Solve
  **Flag:** `pwn.college{sEEYCOvXWC4L_-mw3W375278GCs.QX3YjM1wCO4kjNzEzW}`
  ```
 hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{sEEYCOvXWC4L_-mw3W375278GCs.QX3YjM1wCO4kjNzEzW}
```
### New Learnings
I learnt how to install a WSL to connect pwn.college using ssh keys. This challenge was pretty self explanatory in the description and gave insight on the process of getting the flag to complete the task. All in all, a good start to understand what a command is and how it works.  
### References
none

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

## Command History
You're going to type a lot of commands, and typing everything from scratch can be annoying. Luckily, the shell saves a history of every command you invoke.

You can scroll through those saved commands with the up/down arrow keys, and we'll practice that in this challenge. This challenge will inject the flag into your history. Bring up a terminal, hit the up arrow, and grab it! In other challenges, the history will contain the log of the commands you've run, so if you need to run a similar command again, you can use the arrow keys to scroll through and find it!

### Solve
**Flag:** `pwn.college{wbclMv1md_8ML27vsj2v9z_tZ4B.0lNzEzNxwCO4kjNzEzW}`

```
hacker@hello~command-history:~$ the flag is pwn.college{wbclMv1md_8ML27vsj2v9z_tZ4B.0lNzEzNxwCO4kjNzEzW}
```

### New Learnings
History of every command invoked can be obtained by scrolling with the help of up/down arrow keys. This will be helpful in other challenges that require a lot of commands to be written.

### References 
NA

