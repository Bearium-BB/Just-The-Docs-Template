---
layout: default
title: Git Fundamentals
nav_order: 3
---


# Git Fundamentals
{: .no_toc }

Git is a free, open-source, distributed version control system (VCS) created by Linus Torvalds, the creator of the Linux OS. It helps you track changes to your source code over the life of a project, allowing you to create "save points" called commits, which you can return to later.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

## Configuring Git

Before you begin working on a project, you need to complete a one-time setup to let Git know who you are. This information will be attached to every commit you make. You can also turn on colorization to make the command line output easier to read.
Run the following commands in your terminal, replacing the placeholder text with your own information:

- Set your name: `git config --global user.name "Your Name"`
- Set your email: `git config --global user.email "your.email@example.com"`
- Enable helpful colorization: `git config --global color.ui auto`

These global settings only need to be configured once on your computer.


## Initializing a Repo

A repository (or repo) is the collection of files and directories that you are monitoring for changes with a version control tool. To start tracking a new project with Git, you must first initialize a repository from within the project's root folder.
- To initialize a new Git repo, use the command: `git init .`
- Git's default main branch is often named "master," but you can rename it to "main" using: `git branch -m main`



## Staging and Committing Files

The Git life cycle consists of three main stages: the Working Directory, the Staging Area, and the Git Commit.
1. Working Directory: This is the current state of your project's files on your computer.
2. Staging Files: Before you can save changes (commit), you must first add the new or modified files to a staging area. This lets you select which changes you want to include in the next commit.
    - To stage a specific file: `Git add readme.md`
    - To stage all new or modified files in the current directory: `git add .`
    - You can also use wildcards: `git add docs/textfiles/*.txt`

3. Committing Files: A commit is a snapshot of your entire repository compressed into a unique identifier called a SHA hash. You commit your staged changes with a descriptive message.
    - To commit with a short message: `git commit -m "Your explanation of the changes goes here."`
    - For more complex changes, you can add a title and a longer description: `git commit -m "Title" -m "Long description goes here .........."`
Writing good commit messages is crucial as they provide traceability, aid collaboration, and serve as documentation for your project's history. For example, a good message is "Enhance user experience by validating signup form fields," while a bad one is simply "fixing stuff".


## Status, Log, and Diff

Git provides several commands to view the state of your repository and its history.
- `git status`: Use this command to check the status of your repo for any changes or additions.
- `git log`: This command allows you to review all the commits made in the repository's history. Each log entry displays the commit hash (a unique 40-character SHA1 ID), the author, the date, and the commit message.
- `git diff`: This command is used to see the differences between the current files in your working directory and the last commit. You can also use it to compare specific files (git diff secret_plans.txt) or entire folders (git diff ./textfiles/plans).


## Using a Git Ignore File

You may have files in your project that you do not want to include in your repository, such as files with secrets (passwords, API keys), temporary files, or build files. You can tell Git to ignore these files by creating a .gitignore file in your project's root directory.
Here is an example of .gitignore syntax:

```
# Comments start with a '#'
# Ignore a specific file
Thumbs.db

# Use wildcards to ignore all .exe files
*.exe

# Create an exception to a wildcard rule
!special.exe

# Ignore all files in any folder named 'build'
build/

# Ignore all .pdf files in the doc/ folder and any sub-folders
doc/**/*.pdf
```


### Want to know more?

- [Git Guide](https://github.com/git-guides)
- [Git CheetSheet](https://training.github.com/downloads/github-git-cheat-sheet/)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Useful .gitignore templates for common languages and technologies](https://github.com/github/gitignore)
- [Atlassian git config tutorial](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)




