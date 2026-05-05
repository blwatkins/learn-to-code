---
layout: post
author:
  - Brittni Watkins
date: 2026-05-05
modified_date: 2026-05-05
title: "Unix Paths"
tags:
  - unix
  - paths
  - absolute paths
  - relative paths
  - shell
  - bash
  - z shell
toc: true
---

When specifying the location of files and folders on a computer system, it is important to know the difference between a relative path and an absolute path, and which is most appropriate for your code.

## Absolute Path

An absolute path is the path to a file or directory from the root directory of the computer.

On Unix-like systems, absolute paths begin with `/` (e.g. `/Users/username/`).

On Windows systems, absolute paths begin with the drive name (e.g. `C:/Users/username/`).

In a Unix shell, you print the absolute path of your working directory with the `pwd` command.
Additional information about Unix shell commands can be found in the [Unix Commands guide](../commands.md).

I rarely recommend using absolute paths.
The absolute path to a file on one machine will likely be very different from the path to the file on a different machine, which could lead to errors, crashes, and unexpected behaviors in your program.

## Relative Path

A relative path allows us to reference the location of a file or directory relative to the working directory.

Certain characters in relative paths can be use to indicate different directories relative to the working directory.

`..` is used to indicate the directory one level up from the working directory.

`.` is used to indicate the working directory.

`~` is used to indicate your `$HOME` directory.

If you do not know the location of your home directory, you can print it using the `echo` command in a Unix shell CLI.

```shell
echo $HOME
```

Additional information about Unix shell commands can be found in the [Unix Commands guide](../commands.md).

### `cd` with Relative Paths

In a Unix shell, you can use the `cd` command to change your working directory. Let's say we have three directories: <span style="color: red;">Level-0</span>/<span style="color: blue;">Level-1</span>/<span style="color: green;">Level-2</span>.

From <span style="color: red;">Level-0</span>, `cd Level-1` will take you to <span style="color: blue;">Level-1</span>.

From <span style="color: blue;">Level-1</span>, `cd ..` will take you to <span style="color: red;">Level-0</span>.

From <span style="color: blue;">Level-1</span>, `cd ./Level-2` will take you to <span style="color: green;">Level-2</span>.

From <span style="color: green;">Level-2</span>, `cd ../..` will take you to <span style="color: red;">Level-0</span>.

From <span style="color: red;">Level-0</span>, `cd Level-1/Level-2` will take you to <span style="color: green;">Level-2</span>.

From <span style="color: blue;">Level-1</span>, `cd .././Level-1/Level-2/..` will take you to <span style="color: blue;">Level-1</span>.

Additional information about Unix shell commands can be found in the [Unix Commands guide](../commands.md).

## Paths with Spaces

When executing commands in a Unix shell, if any folder in a directory path has a space character in its name, the path must be surrounded by quotes.

```shell
cd '../directory with spaces/sub-1'
```

```shell
ls './directory with spaces'
```

```shell
mkdir 'directory with spaces'
```

Additional information about Unix shell commands can be found in the [Unix Commands guide](../commands.md).
