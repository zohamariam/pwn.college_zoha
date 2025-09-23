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
