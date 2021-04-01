---
date: "2021-04-01"
tags: ["pty", "cli", "tutorial"]
title: "Understanding and Creating Pseudo-Terminals (PTY)"
---

| This content was written based on the Chapter 6 of the **Hands-On System Programming with Go** book written by Alex Guerrieri. 

Pseudo-terminals, or pseudo-teletypes, are applications that run under a terminal. Many programs are build as pseudo-terminal because it enables interactive use from inside a terminal without needing any graphical interface.

As Software Engineers, we use many applications that are build as a pseudo-terminal. One of them is the SSH Client. SSH means Secure Shell, and shell is a computer program which exposes an operating system's services generally as a command-line interface. 

**PTY** are the initials of pseudo-teletype and is the formal way to call a pseudo-terminal. This name is inherited from TTY, which means teletype and is the name for typewriters. Typewriters are electromechanical systems connected to a computer, capable of sending information to the device to print it. TTY is also the name of a special device used by deaf or speech-impaired people to communicate through the telephone. In this device, typed messages go back and forth instead of talking and listening to each other. In this case, a TTY is required at both ends. 

In order to be considered a PTY, an application need to be capable of:
* accepting input from the user;
* sending input to the console and receiving back the output;
* showing the received output to the user.
