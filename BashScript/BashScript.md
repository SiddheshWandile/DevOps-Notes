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

## How to write a bash script?

We can make a new file with an extension of `.sh` to make a bash script file. Any command that we were able to directly execute in the terminal can be added as a code in this file to eventually run it.

```bash
echo "Welcome to  shell scripting"
echo "We are writing our first bash script"
echo "Ending....."
ls
```

Let's say we save the above code in a new `script.sh` file. Now to run this file, we can use the following command.

```bash
sh script.sh
```

or

```bash
bash script.sh
```

with both of these command we can actually run the bash script and see output on our screen.

Now in your machine there can be more than one shell scripting language avilable, like bash, zsh etc. Sometimes the default scripting language is not bash, so that's why we have to seprately of the `sh` shell script.
If we don't want to mention which scripting language to use in order to run the file, and expect it to pick it form the code we can use shebang.

## Shebang in scripts

Shebang looks like this: `#!` This shebang is added on the top of the script and then we can mention that path of the scripting language we want to get execute by.

```bash
#!/bin/bash
echo "Welcome to shell scripting"
echo "We are writing our first bash script"
echo "Ending...."
```

Here we have added some bash code at the top of the file added `#!bin/bash`. So we passed the path of the interpreter which will be used to run the code. instead of picking the default one form system.
Because we have mentioned the interpreter, we can run the independently,

```bash
./script.sh
```

But this command will give you error. Why? Because the current script filr is not executable. When we say `bash script.sh` then bash interpreter is directly executable in the terminal. To make our file directly executable we can change it's permission.

```bash
chmod +x script.sh
```

And now, we can run the script independently

```bash
./script.sh
```

This command will start running the file, at the top because of shebang pick the interpreter as bash and then run the remaining code with bash.

## Variables in bash script

Sometimes we want to reuse a value at multiple places in our bash script, to do that we can create variable. Variable in bash script serve the same purpose as variable in any other language.
To create a variable, we just give variable name put an equals and then give it a value

```bash
threshold =  80
```

This command create a new variable threshold with value 80. Now if we want to use this variable at any place, we have to prepend a `$` before the variable name to acces it's value.

In this statement, `$threshold` helps us to access a the value of the variable threshold.
Now to add a varivable inside a bash script we can use the same syntax.

```bash
echo "Welcome to the program"
threshold = 80
echo "Value of the threshold set is $threshold"
```

The variable which we create in a termial, or in script will exist only in the same terminal session, once you close your terminal or move to a new terminal window, those variable won't be accessible.
Apart form variable created by us, there are some predesined variable as well like `$USER`, `$PATH` that are already present in every terminal session we create. These are ppredefined in linux and serve some specific purpose but if we want we can chnage their value.

if we want to see all the inbuild variable we can use the command

```bash
env
```

This will list all the exixting prebuild variable for us.
