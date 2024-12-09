# Bash Scripting

## Command Line Interface

To control the OS of a machine we have two main mechanisum.

1. GUI - Graphical user Interface
2. CLI - Command line Interface
   It becomes very easy to control your whole os using GUI interfacing. But at a lot of situation you will expected to control the whole OS using CLI interface. When can this happen ? Let's say we hosted our backend application on a AWS cloud server, now these server are present in a very remote location, now if we have to interact with this server, then we need to control the OS of this server from our machione. And here CLI will only help us as we won't be having any GUI access to the server.

In CLI interface, we use softwares like iterm, terminal, CMD, power shell etc, which gives us an interface to write some commands that will be running directly in our OS.

## REPL Console

REPL stands for Read, Evaluate, Print, Loop. A repl console is a special type of console which understand a particular programming language and every time we run it, it will expect us to add one valid instruction to the console, it will then evaluate it's output, print the output and then go back to the same same where it is expecting an input form us.

## What is Shell?

A shell in the context of computing and operating systems like Linux, is an interface that allows you to access and interact services of your operating system. The primary function of shell is to accept commands from user and then execute them.

## What is Bash?

Bash is a type of scripting language that helps us to interact with a linux shell. Bash stands for Bourse Again Shell. Using Bash, we can write linux command in CLI softwares like Iterm and terminal, and also write end to end programmed scripts which can help us to automate a lot of things in our computer.

## What is a bash script?

We can say that at some point of time, we might have to execute multiple bash commands for achieving a complex task. For example: We want to monitor that if the disk usage of our machine goes beyond 90%, we should be mailed for this incident. If we are implementing this problem using bash script then we might need a lot of lines to work together in a single logical piece, that's where bash script will help.
Any bash script that we prepare will be having an extension of `.sh`
