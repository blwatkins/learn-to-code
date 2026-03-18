---
layout: post
author: Brittni Watkins
date: 2026-03-18 18:00:00 -0000
modified_date: 2026-03-18
title: "Ruby - Version Managers - rbenv"
---

# Ruby - Version Managers - [`rbenv`](https://rbenv.org/)

## Installation with [Homebrew](https://brew.sh/) for MacOS

```shell
xcode-select --install
brew install openssl@3 readline libyaml gmp autoconf rust
brew install rbenv ruby-build
rbenv init
```

## `.ruby-version`

Can be used to specify required Ruby version for a project

## Print the Current Version

```shell
rbenv --version
```

## list latest stable versions of ruby

```shell
rbenv install -l
```

## install a version of Ruby

```shell
rbenv install [VERSION-NUMBER-HERE]
```

### Example

As of March 2026, the latest stable version of Ruby is 4.0.2.

```shell
rbenv install 4.0.2
```

## Set a Ruby version for a directory

```shell
rbenv local [VERSION-NUMBER-HERE]
```

## Set a default Ruby version

```shell
rbenv global [VERSION-NUMBER-HERE]
```
