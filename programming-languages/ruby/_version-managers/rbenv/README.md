# Ruby - Version Managers - [`rbenv`](https://rbenv.org/)

Created: Wednesday, March 18, 2026 | Last Updated: Wednesday, March 18, 2026

## Installation with [Homebrew](https://brew.sh/) for macOS

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

## List available Ruby versions

```shell
rbenv install -l
```

## install a version of Ruby

```shell
rbenv install [VERSION-NUMBER-HERE]
```

### Example

For example, to install Ruby 4.0.2:

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
