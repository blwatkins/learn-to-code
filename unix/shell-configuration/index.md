---
layout: post
author:
  - Brittni Watkins
date: 2025-05-21
modified_date: 2026-05-05
title: "Unix Shell Configuration"
tags:
  - unix
  - configuration
  - profile file
  - rc file
  - shell
  - bash
  - z shell
  - environment variables
toc: true
---

## Introduction

When a Unix shell is initialized, it reads and executes commands from a set of configuration files.
These files are used to set up the shell environment, including environment variables, aliases, and functions.
The specific files that are executed depend on the type of shell being used and whether the shell has registered a login operation.

## The Home Directory

Profile files and RC files should be located in the user's home directory.
To see the location of your home directory, execute one of the following commands in your preferred Unix shell command line interface (CLI).

```shell
echo $HOME
```

```shell
cd ~
pwd
```
<br/>

If a profile file or RC file does not exist, you can create it using the `touch` command.
For example, to create a `.bash_profile` file, execute the following command in your preferred Unix shell CLI.

```shell
touch ~/.bash_profile
```
<br/>

Additional information about Unix shell commands can be found in the [Unix Commands guide](../commands.md).

## Shell Profile Files

Shell profile files are executed when a user logs in to the shell.
On a personal computer, opening a new shell window will typically register as a login operation.

In [Bash shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), the profile file is typically called `.bash_profile`.

In [Z shell](https://en.wikipedia.org/wiki/Z_shell), the profile file is typically called `.zprofile`.

## Shell RC Files

RC files are executed when a new shell is started or initialized.
This includes opening a new shell window or executing a shell script (e.g. `bash` or `zsh`).

In [Bash shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), the RC file is typically called `.bashrc`.

In [Z shell](https://en.wikipedia.org/wiki/Z_shell), the profile file is typically called `.zshrc`.

## Editing Profile and RC Files

### Editing on macOS

You can edit profile and RC files on macOS using the `TextEdit` application.
You can open files in `TextEdit` from the command line using the `open` command.
For example, to open the `.bashrc` file, execute the following command in your preferred Unix shell CLI.

```shell
open ~/.bashrc
```

### Editing on Windows

You can edit profile and RC files on Windows using the `Notepad` application.
You can open files in `Notepad` from the command line using the `explorer` command.
For example, to open the `.bashrc` file, execute the following command in your preferred Unix shell CLI.

```shell
explorer ~/.bashrc
```

### Editing from the Command Line

You can edit profile and RC files directly from the command line using a wide range of command line text editors, including [`nano`](https://www.nano-editor.org/), [`vi`](https://en.wikipedia.org/wiki/Vi_(text_editor)), and [`vim`](https://www.vim.org/).
Additional information about `vi` can be found in the [vi guide](../shell-editors/vi.md).

For additional information about command line editors, the following resources may be helpful:

[Wikipedia - GNU nano](https://en.wikipedia.org/wiki/GNU_nano)

[Wikipedia - Vim (text editor)](https://en.wikipedia.org/wiki/Vim_(text_editor))

## Resources and References

For additional information about Unix shell configuration, the following resources may be helpful:

[Red Hat Blog - How to customize Linux user environments](https://www.redhat.com/en/blog/customize-user-environments)

[Red Hat Blog - Linux environment variable tips and tricks](https://www.redhat.com/en/blog/linux-environment-variables)

[GeeksforGeeks - bashrc vs. bash_profile: What Is the Difference?](https://www.geeksforgeeks.org/linux-unix/bashrc-vs-bash_profile-what-is-the-difference/)

[Tutorials Point - Shell Initialization Files and User Profiles in Linux](https://www.tutorialspoint.com/article/shell-initialization-files-and-user-profiles-in-linux)

[Tutorials Point - Difference Between .bashrc, .bash-profile, and .profile](https://www.tutorialspoint.com/article/difference-between-bashrc-bash-profile-and-profile)

[Tutorials Point - Unix / Linux - Environment](https://www.tutorialspoint.com/unix/unix-environment.htm)
