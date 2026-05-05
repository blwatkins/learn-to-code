---
layout: post
author:
  - Brittni Watkins
date: 2025-05-14
modified_date: 2026-05-05
title: "Useful Unix Commands"
tags:
  - unix
  - commands
  - command line
  - shell
  - bash
  - z shell
toc: true
---

## Introduction

A Unix shell provides a text-based user interface, known as a command line interface (CLI), for Unix-like operating systems.
The shell is both an interactive command language and a scripting language, and it is used by the operating system to control the execution of the system using shell scripts.

This guide will walk you through some Unix shell commands that will be useful to know as you progress on your coding journey.
This guide is not an exhaustive list.

## How to Execute a Unix Shell Command

A Unix shell command can be executed through a CLI application running a Unix shell instance, or it can be executed as part of a Unix shell script.

Once you have opened a CLI application, type the command into the console and press `ENTER` or `RETURN` to execute it.
Some commands will print text as a part of their execution, and some will not.
An error message will usually be printed if something has gone wrong during the program execution or if the command and its arguments were not structured properly.
Additional information about CLI applications can be found in the [Unix Installation guide](./01_getting-started/01_installation).

Additional information about creating, writing, and executing shell scripts can be found in the [Unix Shell Scripts guide](./shell-scripts).

## Unix Shell Shortcuts

Use the `TAB` key to autocomplete file, directory, and command names.

Use the `UP` arrow key to scroll through previous commands.

Use the `DOWN` arrow key to scroll forward through previous commands.

## Commands

### `pwd`

**Print Working Directory / Present Working Directory**

The [`pwd`](https://explainshell.com/explain/1/pwd) command prints the absolute file path of your current location in the shell.
Your current location will correspond to some folder in your computer's file system.

```shell
pwd
```

### `whoami`

**Print Your Username**

The [`whoami`](https://explainshell.com/explain/1/whoami) command prints your username.
This command can be used to check your username when you are connected to a remote server.

```shell
whoami
```

### `date`

**Print the Current Date and Time**

The [`date`](https://explainshell.com/explain/1/date) command prints the current date and time.

```shell
date
```

### `echo`

**Print Something**

The [`echo`](https://explainshell.com/explain/1/echo) command will print the given string.

```shell
echo STRING_HERE
```
<br/>

> [!TIP]
> Fun fact: Want to make your computer beep? Try the following:
> `echo -e "\a"`
<br/>

When given an environment variable name, such as `$HOME` or `$PATH`, the `echo` command will print the value of the given variable.

```shell
echo $VARIABLE_NAME_HERE
```
<br/>

For additional information about environment variables, the following resources may be helpful:

[Red Hat Blog - Linux environment variable tips and tricks](https://www.redhat.com/en/blog/linux-environment-variables)

#### `echo` Examples

```shell
echo "Hello, World!"
```

```shell
echo $HOME
```

### `clear`

**Clear the Shell Window**

The [`clear`](https://explainshell.com/explain/1/clear) command clears the shell window.

```shell
clear
```

### `ls`

**List the Directory Contents**

The [`ls`](https://explainshell.com/explain/1/ls) command prints all the visible files and folders in our working directory.

```shell
ls
```
<br/>

When we add the `-l` flag to the `ls` command, the visible files and folders will be printed in a long list format.

```shell
ls -l
```
<br/>

When we add the `-a` flag to the `ls` command, the command will list all the files and folders in our working directory, including hidden files and folders.

Hidden files and folders will always have a name that begins with `.` (e.g. `.bash_profile`).

```shell
ls -a
```
<br/>

When we add both the `-a` and `-l` flags to the `ls` command, the command will list all files in our working directory, including hidden files, in a long list format.

```shell
ls -al
```
<br/>

We can use the `ls` command to print the contents of a different directory by providing the absolute or relative path to the directory.

```shell
ls DIRECTORY_PATH_HERE
```
<br/>

Additional information about paths can be found in the [Unix Paths guide](./paths).

### `cd`

**Change the Working Directory**

The [`cd`](https://explainshell.com/explain/1posix/cd) command will change the working directory to the directory with the given absolute or relative path.

```shell
cd DIRECTORY_PATH_HERE
```
<br/>

Additional information about paths can be found in the [Unix Paths guide](./paths).

### `touch`

**Create a File**

The [`touch`](https://explainshell.com/explain/1/touch) command creates a file.

```shell
touch FILENAME_HERE
```
<br/>

When executing the `touch` command, the filename argument can also be a relative or absolute path to the file you are creating.

```shell
touch FILE_PATH_HERE
```
<br/>

Additional information about paths can be found in the [Unix Paths guide](./paths).

#### `touch` Examples

```shell
touch my-text-file.txt
```

```shell
touch ./my-directory/MyJavaClass.java
```

### `mkdir`

**Create a Directory (Folder)**

The [`mkdir`](https://explainshell.com/explain/1/mkdir) command creates a folder, also known as a directory.
The directory path argument can be an absolute path or a relative path.

```shell
mkdir DIRECTORY_PATH_HERE
```
<br/>

Additional information about paths can be found in the [Unix Paths guide](./paths).

### `chmod`

**Change File Permissions**

The [`chmod`](https://explainshell.com/explain/1/chmod) command updates the permissions of the given file using the given permissions.

```shell
chmod PERMISSIONS_HERE FILE_PATH_HERE
```
<br/>

Permissions can be provided in symbolic mode or octal mode.

#### `chmod` Examples

```shell
chmod 444 my-text-file.txt
```

```shell
chmod ugo+w my-text-file.txt
```

### `export`

**Set the Value of an Environment Variable**

The [`export`](https://explainshell.com/explain/1posix/export) command will set the given variable to the given value. When executed in a Unix shell, this change will only be active for the current shell session.

```shell
export VARIABLE_NAME_HERE=VARIABLE_VALUE_HERE
```
<br/>

If an environment variable needs to have some value in every shell session, it is recommended to set that variable in the appropriate shell profile file or shell RC file.
Additional information about shell profile files and RC files can be found in the [Unix Shell Configuration guide](./shell-configuration).

To confirm the variable has been set properly, you can print its value using the [`echo`](#echo) command.

```shell
echo $VARIABLE_NAME_HERE
```

#### `export` Examples

```shell
export SOME_VARIABLE="some value"
echo $SOME_VARIABLE
```

### `which`

**Print the Path of this Command**

The [`which`](https://explainshell.com/explain/1/which) command prints the absolute path to the location of the given command, provided as an argument.

```shell
which COMMAND_NAME_HERE
```
<br/>

When we add the `-a` flag to the `which` command, the command will print all paths to the given command.
A command may have multiple paths if there are multiple versions of the command installed on the machine.

```shell
which -a COMMAND_NAME_HERE
```
<br/>

The `which -a` commands give you all locations of the given command.
The `which` command tells you which one will be used when you execute that command.

#### `which` Examples

```shell
which ruby
```

```shell
which python
```

```shell
which -a ruby
```

```shell
which -a python
```

### `bash`

**Start a Bash Shell Instance**

The [`bash`](https://explainshell.com/explain/1/bash) command initializes an instance of the [Bash shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) inside the current shell instance.

```shell
bash
```

### `zsh`

**Start a Z Shell Instance**

The [`zsh`](https://explainshell.com/explain/1/zsh) command initializes an instance of the [Z shell](https://en.wikipedia.org/wiki/Z_shell) inside of the current shell instance.

```shell
zsh
```

### `exit`

**Exit the Current Shell Instance**

The [`exit`](https://explainshell.com/explain/1posix/exit) command can be used to exit the current shell instance.

```shell
exit
```

## Resources and References

For additional information about Unix shell commands, the following resources may be helpful:

[explainshell](https://explainshell.com/)

[GeeksforGeeks - Essential Unix Commands](https://www.geeksforgeeks.org/linux-unix/essential-linuxunix-commands/)

[freeCodeCamp - The Linux Command Handbook – Learn Linux Commands for Beginners](https://www.freecodecamp.org/news/the-linux-commands-handbook/)

[Tutorials Point - Linux Commands Reference](https://www.tutorialspoint.com/unix_commands/index.htm)

[SitePoint - 15 Little-Known Unix Commands](https://www.sitepoint.com/15-little-known-unix-commands/)

[Red Hat Blog - Linux file permissions explained](https://www.redhat.com/en/blog/linux-file-permissions-explained)

[W3Schools - What is Command Line Interface (CLI)?](https://www.w3schools.com/whatis/whatis_cli.asp)

[AWS - What is a CLI?](https://aws.amazon.com/what-is/cli/)

[Wikipedia - Unix shell](https://en.wikipedia.org/wiki/Unix_shell)
