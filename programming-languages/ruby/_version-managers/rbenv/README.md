# Ruby - Version Managers - [`rbenv`](https://rbenv.org/)

## Installation with [Homebrew](https://brew.sh/) for MacOS

```shell
xcode-select --install
brew install openssl@3 readline libyaml gmp autoconf rust
brew install rbenv ruby-build
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

```shell
rbenv install 4.0.1
```

## Set a Ruby version for a directory

```shell
rbenv local [VERSION-NUMBER-HERE]
```

## Set a default Ruby version

```shell
rbenv global [VERSION-NUMBER-HERE]
```
