# `gh clone`

`gh clone` is a [`gh` extension](https://docs.github.com/en/github-cli/github-cli/using-github-cli-extensions) to clone a repository, in my preferred [repository structure](#usage--repository-structure)

## Installation

```shell
$ gh extension install AaronMoat/gh-clone
```

## Usage & Repository Structure

I like to have a root directory for all repositories, then a sub-directory for each owner:

```shell
$ cd /users/me
$ gh clone some-owner/some-repo
First run. Enter the location where you want to clone repositories: /users/me/code
Cloning into '/users/me/code/some-owner/some-repo'...
...
Cloned to /users/me/code/some-owner/some-repo
```

It will infer the owner from the current directory if not provided:

```shell
$ cd /users/me/code/some-owner
$ gh clone some-other-repo
Cloning into some-other-repo
Cloned to /users/me/code/some-owner/some-other-repo
```

Otherwise, if you're not in an inferrable location, the inferred owner will be yourself:

```shell
$ cd /users/me
$ gh clone some-repo
Cloning into some-repo
Cloned to /users/me/code/MyGitHubUsername/some-repo
```

There is no support for specifying owner syntaxes like `git@...`, `https://...`, or `git://...`.
