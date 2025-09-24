# Comprehending Commands

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
