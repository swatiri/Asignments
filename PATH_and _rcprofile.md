## What is PATH?

PATH is an environmental variable in Linux and other Unix-like operating systems that tells the shell which directories to search for executable files (i.e., ready-to-run programs) in response to commands typed in by a user. 

When typing commands in the Linux terminal, you’re generally calling a program to do a certain job, eg ls, cd, rm, mkdir, etc. All these programs are located somewhere in the file system,  for bash to know where these file are , the environment variables come into play, especially the PATH variable. This variable is responsible for telling bash where to look for those programs.

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
2. Display Directory Information
3. High-Performance Simple Prompt


How to Open A bash.rc and Save a File

The syntax you should use is practically the same as creating a temporary alias, except this time, you also have to save it in a file. So:

Step 1: Open a .bashrc file in a sample bash

```
vim ~/.bashrc
```
Step 2: Find a place in the file where you intend to keep the Aliases. For instance, you may want to add them at the end of the file.

Step 3: Save the file. This file will automatically load in your next session.

Note: the unalias command will use for removing an alias.

unalias alias_name

unalias -a [remove all alias]

## How to Edit .bashrc files

You may want to add your own commands in any terminal text editor. To do so, you can edit bashrc. We will use a nano editor in the following examples.

Step 1: To edit bashrc through nano, type the following command in Terminal:
```
nano ~/.bashrc

```
Note: If it is the first time you are editing your .bashrc file, you might find that it is empty.

Bring in your mind that next time you launch the terminal, any changes you make to .bashrc will apply. If you want to make use of them immediately, run the command below:

```
source ~/.bashrc

```





