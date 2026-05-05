---
layout: post
author:
  - Brittni Watkins
date: 2025-05-20
modified_date: 2026-05-05
title: "Create and Clone a GitHub Repository"
tags:
  - git
  - github
  - create a repository
  - new repository
  - clone a repository
toc: true
---

## Introduction

[GitHub](https://github.com/) is a developer platform that allows developers to create, store, manage and share their code, providing the distributed version control of Git.
Using Git and GitHub together, a developer can update their code, track changes, create issues, build deployment workflows, and review and accept changes to their code from developers around the world.

In this guide, we will walk through how to create a new GitHub repository and how to clone the repository to our local machine.

To complete this tutorial, you will need the following:

1. A [GitHub](https://github.com/) account
1. A Unix shell command line interface (CLI) installed on your computer. Additional information about installing a CLI can be found in the [Unix Shell Installation guide](../../unix/01_getting-started/01_installation).
1. Git installed on your computer. Additional information about installing Git can be found in the [Git Installation guide](../01_getting-started/01_installation).

## Local Repository vs. Remote Repository

Before we create a new repository, we need to understand the difference between a local repository and a remote repository, and how we use Git and GitHub together to maintain the two.

A local repository is code in a folder on your computer.
This is the code that we will be editing, saving, running, testing, and debugging during the development process.
You do not need a network connection to access this code, because all of the files are downloaded and saved on your computer.

A remote repository is code that resides on some remote server.
In this case, the code will be held on GitHub servers.
You can interact with this code via the GitHub website, and you can run, test, and debug the code using [GitHub Codespaces](https://docs.github.com/en/codespaces).
Accessing a remote repository always requires a network connection because accessing the code requires access to the GitHub website.

It is possible to have a local repository that does not have a corresponding remote repository on GitHub, and it is possible to have a remote repository on GitHub that does not have a corresponding local repository on your computer. 
For this tutorial, we will be creating a remote repository on the GitHub website, and cloning that remote repository so that we have a corresponding local repository on our computer.

After cloning the remote repository, changes to the local repository will not be synced automatically to the remote repository, nor vice versa.
Once a repository has been cloned, we must use Git to indicate which files and changes should be synced between the local and remote repositories.
Any interaction between our local repository and our remote repository will require a network connection and access to the GitHub website.

## GitHub Authentication

We always want to make sure that our code and all associated accounts are secure.
We also want to make sure that no one can make edits to our code without our express permission.
Setting up our GitHub authentication helps us ensure that no one can make a change to a GitHub remote repository using our GitHub credentials.

GitHub has multiple ways to authenticate your account, and the method you select will determine the type of URL you use to clone repositories from the GitHub website.

If you would like to authenticate to GitHub using an SSH key, you can follow the instructions on the [GitHub Docs - Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) page.
If you are using an SSH key to authenticate to GitHub, you will clone repositories using `SSH`.

If you would like to authenticate to GitHub using a person access token, you can follow the provided instructions on the [GitHub Docs - Managing your personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) page.
If you are using a personal access token or password to authenticate to GitHub, you will clone repositories using the `HTTPS` URL.

For additional information about GitHub Authentication, the following resources may be helpful:

[GitHub Docs - Authentication](https://docs.github.com/en/authentication).

## Create a New Repository

A full guide on how to create a GitHub repository can be found on the [GitHub Docs - Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) page.

After you are signed in to GitHub, you can create a new repository from any page by clicking the `+` symbol in the top-right section of your screen.
After you click the `+` symbol, select `New Repository` to begin creating a new repo.

You can also create a new repository using the `New` button on the left-hand side of your Home page, or using the `New` button at the top of your list of repositories.

On the repository creation page, select a name for your repository and an optional description.

Choose if you would like to have a `Public` or `Private` repository.

Select the checkbox next to `Add a README file` so that your repository is initialized with a `README.md` file.
Initializing our repo with a `README` file makes the cloning process much easier.

You do not need to add a `.gitignore` file.
I rarely choose a `.gitignore` template and prefer to add files to `.gitignore` as needed, but I encourage you to explore and experiment with the different templates that are available.

You do not need to select a license.
Choosing a license is a big part of code development for any open source project, but it's not necessary to choose one for our first repository.
You can learn more about open source software licenses on the [Open Source Initiative website](https://opensource.org/licenses).

## Clone a Repository

A full guide on how to clone a GitHub repository can be found on the [GitHub Docs - Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) page.

Choose the repository you would like to clone.

Under the `Code` tab of the repository, select the `<> Code` button.

Select the `Local` tab.

Choose the method you would like to use to clone the repository.
If you are using a personal access token or password to authenticate to GitHub, you will clone repositories using the `HTTPS` URL.
If you are using an SSH key to authenticate to GitHub, you will clone repositories using `SSH`.

Copy the address provided by GitHub.

Open a Unix shell CLI and navigate to the directory of your choice using the appropriate Unix shell commands.
Additional information about Unix shell commands can be found in the [Useful Unix Commands guide](../../unix/commands.md).

Type and execute the following command, using the repository URL copied from GitHub.
Follow any prompts needed to authenticate your account.

```shell
git clone REPOSITORY_URL_HERE
```

<br/>

> [!CAUTION]
> ***Do NOT clone repositories from unverified sources.***
> 
> ***Do NOT clone repositories from developers you do not trust.***

<br/>

Do you see a folder in your current directory with the same name as your GitHub repository?
If yes, congratulations! You have successfully cloned your repository.

## Resources and References

For additional information about GitHub and GitHub repositories, the following resources may be helpful:

[GitHub Docs](https://docs.github.com/en)
