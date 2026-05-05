---
layout: post
author:
  - Brittni Watkins
date: 2025-05-13
modified_date: 2026-05-05
title: "Git Installation"
tags:
  - git
  - version control
  - installation
toc: true
---

## Introduction

[Git](https://git-scm.com/) is a version control software that allows us to save and restore different versions of our files at various points.
It is a powerful tool that allows us to track changes, collaborate with others, and manage our codebase effectively.

We have a few options for installing Git, and those options change depending on the operating system you are using. 
In this tutorial, I will walk you through the installation process for Windows and macOS. 
If you are using Linux, you can find download instructions for your specific distribution on the [Git website](https://git-scm.com/downloads/linux).

## Installing Git for Windows

You can find the official Git installation instructions for Windows on the [Git website](https://git-scm.com/downloads/win).

### Step 1: Download Git Installer

Download Git from the [Git website](https://git-scm.com/downloads/win).

### Step 2: Install Git to Windows

Follow all instructions and prompts in the installation program. 
Be sure to opt-in to installing the GitBash application.

Windows does not come with a Unix shell command line interface (CLI) by default. 
Installing GitBash will allow us to navigate through our operating system using common Unix shell commands that we would use with macOS or Linux machines.

### Step 3: Confirm Windows Git Installation

Let's make sure the installation was successful.

Find and open the GitBash application. I recommend adding a shortcut to your Desktop or Start Menu, if one does not exist already.

Type and execute the following (hit `ENTER` or `RETURN` to execute the command):

```shell
git --version
```
<br/>

Do you see a version number? If yes, congratulations! You have successfully installed Git!


## Installing Git for macOS

You can find the official Git installation instructions for macOS on the [Git website](https://git-scm.com/downloads/mac). 
This guide will walk through the steps to install Git using [Homebrew](https://brew.sh/).

### Step 1: Install Homebrew

[Homebrew](https://brew.sh/) is a popular package manager used for managing software and package dependencies on macOS.

Find and open the Terminal application on your computer, then follow the steps on the [Homebrew website](https://brew.sh/) to install Homebrew.

### Step 2: Confirm Homebrew Installation

Let's make sure the Homebrew installation was successful.

Find and open the Terminal application.
I recommend adding a shortcut to your Desktop or Dock, if one does not exist already.

Type and execute the following (hit `ENTER` or `RETURN` to execute the command):

```shell
brew --version
```
<br/>

Do you see a version number? If yes, congratulations! You have successfully installed Homebrew!

### Step 3: Install Git with Homebrew

In the Terminal application, type and execute the following:

```shell
brew install git
```

### Step 4: Confirm macOS Git Installation

Let's make sure the Git installation was successful.

In the Terminal application, type and execute the following:

```shell
git --version
```
<br/>

Do you see a version number? If yes, congratulations! You have successfully installed Git!

## First Time Git Setup

Git must have a configured username and email to associate with each commit made in your repositories.
This configuration can either be set individually in each repository on your machine, or it can be set globally for every repository on your computer.
The following instructions will walk through the global configuration.

If you are only using Git locally, the username and email that you set is inconsequential.
However, if you are using a Git hosting service, such as [GitHub](https://github.com/) or [GitLab](https://about.gitlab.com/) your username and email should match those being used in the hosting service.
<br/>

> [!CAUTION]
> The name and email you set in your configuration will be accessible to anyone who clones your repository or any repository you contribute to.
> If you have a GitHub account, and would like to keep your email address private, you can configure your git email address to be the `noreply` email address provided by GitHub.
> Instructions on how to find your `noreply` email on GitHub are available in the [GitHub Docs: Setting your commit email address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)
<br/>

To set your Git configuration variables, open the Unix shell of your choice.
On macOS, this will likely be the Terminal application.
On Windows, this will likely be the GitBash application.

Type and execute the following commands:

```shell
git config --global user.name USER_NAME_HERE
```

```shell
git config --global user.email USER_EMAIL_HERE
```
<br/>

You can double-check that the variables have been set with the following command:

```shell
git config --global --list
```
<br/>

For additional information about first time Git setup, the following resources may be helpful:

[Pro Git Book: First-Time Git Setup](https://git-scm.com/book/ms/v2/Getting-Started-First-Time-Git-Setup)

[GitHub Docs: Setting your commit email address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)

## Successful Git Installation and Set Up

I believe Git is successfully installed and configured when you are able to do the following:

1. Clone a remote GitHub repository
1. Commit a change to a local repository and push it up to a remote repository
1. Commit a change to a remote repository and pull it down to a local repository

Additional information about cloning a remote GitHub repository can be found in the [Create and Clone a GitHub Repository guide](./github/create-and-clone-repo.md).
