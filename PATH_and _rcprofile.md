## What is PATH?

PATH is an environmental variable in Linux and other Unix-like operating systems that tells the shell which directories to search for executable files (i.e., ready-to-run programs) in response to commands typed in by a user. 

When typing commands in the Linux terminal, you’re generally calling a program to do a certain job, eg ls, cd, rm, mkdir, etc. All these programs are located somewhere in the file system,  for bash to know where these file are , the environment variables come into play, especially the PATH variable. This variable is responsible for telling bash where to look for those programs. Let’s check out how PATH works and how to view/modify PATH. -->

## Setting  your PATH
Let's say you wrote a little shell script called hello.sh and it is located in a directory called /place/with/the/file. This script provides some useful function to all of the files in your current directory, that you'd like to be able to execute no matter what directory you're in.

Simply add /place/with/the/file to the $PATH variable with the following command:
```
export PATH=$PATH:/place/with/the/file
```

You should now be able to execute the script anywhere on your system by just typing in its name, without having to include the full path as you type it.

## View your PATH

Sometimes, you may wish to install programs into other locations on your computer, but be able to execute them easily without specifying their exact location. You can do this easily by adding a directory to your $PATH. To see what's in your $PATH right now, type this into a terminal

```
echo $PATH

```
### What is Bashrc File

the .bashrc File is a shell script that initializes a shell session. You can put all commands in this file (those commands you can type in the command prompt). Every time you need to initiate the .bashrc File from the beginning, you can start it by pressing Ctrl+Alt+T; or do it by opening a new terminal tab.

#### What Can You Do With Linux Bashrc?
1. Change the Color on bash Command





