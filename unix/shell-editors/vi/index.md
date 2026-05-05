---
layout: post
author:
  - Brittni Watkins
date: 2025-06-10
modified_date: 2026-05-05
title: "vi"
tags:
  - unix
  - shell
  - scripting
  - bash
  - z shell
  - vi
toc: true
---

## Introduction

`vi` is a screen-oriented text editor originally created for the Unix operating system.
In this guide, we will cover the basics of using `vi` to edit files in a Unix shell.
This guide is not an exhaustive list of `vi` commands and features.

All `vi` commands will be executed using a command line interface (CLI) application running a Unix shell instance, such as `bash` or `zsh`.

## Opening a File in `vi`

The `vi` command opens the specified file in the `vi` text editor.
If the file does not exist, it will be created when you save your changes.

```shell
vi FILEPATH_HERE
```
<br/>

The provided file path can be an absolute path or a relative path.
Additional information about file paths can be found in the
[Unix Paths guide](../../paths).

## Insert Mode

When you open a file in `vi`, the file opens in command mode by default.
To edit the file, you will need to switch to insert mode.

To switch to insert mode from command mode, press the `i` key on your keyboard.
You can now type and edit the file as needed.

To return to command mode from insert mode, press the `ESCAPE` key on your keyboard.
You will need to return to command mode to save your changes or exit `vi`.

## Command Mode

In command mode, you cannot type or edit the file directly.
Instead, you will use various commands and keystrokes to manipulate the file.
In command mode, you can perform actions such as saving the file, exiting `vi`, deleting lines, copying lines, and more.

### Commands

#### Save Your File (Write)

The `:w` command saves the changes you have made to the file without exiting `vi`.

```
:w
```
<br/>

To execute this command, type `:w` while in command mode, then press `ENTER`.

#### Exit `vi` (Quit)

The `:q` command exits `vi` without saving any changes you have made to the file.

```
:q
```
<br/>

To execute this command, type `:q` while in command mode, then press `ENTER`.

#### Save and Exit (Write and Quit)

The `:wq` command saves the changes you have made to the file and then exits `vi`.

```
:wq
```
<br/>

To execute this command, type `:wq` while in command mode, then press `ENTER`.

## Resources and References

For additional information about `vi`, the following resources may be helpful:

[Wikipedia - vi (text editor)](https://en.wikipedia.org/wiki/Vi_(text_editor))

[Red Hat - An introduction to the vi editor](https://www.redhat.com/en/blog/introduction-vi-editor)

[GeeksforGeeks - vi Editor in Linux](https://www.geeksforgeeks.org/linux-unix/vi-editor-unix/)

[Tutorials Point - Unix/Linux - The vi Editor Tutorial](https://www.tutorialspoint.com/unix/unix-vi-editor.htm)
