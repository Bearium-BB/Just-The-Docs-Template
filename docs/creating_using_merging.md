---
layout: default
title: Remote Repository
nav_order: 5
---

<!-- prettier-ignore-start -->

# Creating, Using and Merging Branches
{: .no_toc }

This page introduces the concept of branching in Git. Branches are a fundamental feature that allows you to work on different features or bug fixes in isolation without affecting the main project timeline. We will cover how to create and switch between branches, how to merge your changes back into the main line of development, and what to do when Git cannot automatically merge changes, resulting in a merge conflict.



## Table of Contents


1. TOC

{:toc}



## Introducing Branches

In Git, a branch can be thought of as an alternate timeline for your project. It is a lightweight, movable pointer to a set of commits. Branching allows developers to work on different features or fix bugs in an isolated environment without affecting the main project timeline. Once the work in a branch is complete, it can be merged back into the main line of development. This capability is essential for managing different aspects of development, like feature creation or bug fixing, separately.



## Creating and Using Branches

Git provides simple commands for creating and navigating branches.

Command Prompts


- To create a new branch: `git branch <branch-name>`

- To switch to an existing branch: `git checkout <branch-name>`

- To create a new branch and switch to it in a single command: `git checkout -b <branch-name>`



## Merging Branches

While branching allows for isolated development, merging is the process that brings those developments back into the main project timeline. When you 

merge a branch, you are incorporating its changes into your current branch.

Command Prompts

Let's say you've been working on a branch named experimental and want to merge those commits back into your main branch. You would first switch to the main branch and then run the merge command.

- First, switch to the branch you want to merge into: `git checkout <branch-name>`

- Then, merge the other branch's changes into your current branch: `git merge  <feature-branch-name>`


### Want to know more? 

- [Atlassian](https://www.atlassian.com/git/tutorials/using-branches/git-merge) - Merging Guide.

- [Git CheetSheet](https://training.github.com/downloads/github-git-cheat-sheet/)- The most popular git commands in one page.

- [Pro Git Book](https://git-scm.com/book/en/v2) - Free ebook provides a deep dive into everything git.



<!-- prettier-ignore-end -->

