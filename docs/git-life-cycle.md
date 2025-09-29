---
layout: default
title: The Git Life Cycle
nav_order: 2
---


<!-- prettier-ignore-start -->
# **The Git Life Cycle**
{: .no_toc }

Learn what version control is, why it is important in software development, the different types that exist, and why you should add it to your proyects.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## What is it?

- [According to Git official web page:](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository).

- Each file in your working directory can be in one of two states: **tracked** or **untracked**.
- Tracked files are files that were in the last snapshot, as well as any newly staged files; they can be unmodified, modified, or staged. **In short, tracked files are files that Git knows about.**
- Untracked files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area. 
- When you first clone a repository, all of your files will be tracked and unmodified because Git just checked them out and you haven’t edited anything.

- As you edit files, Git sees them as modified, because you’ve changed them since your last commit. As you work, you selectively stage these modified files and then commit all those staged changes, and the cycle repeats.

## The Git Life Cycle -> Visual 

![Git's Life Cycle](https://git-scm.com/book/en/v2/images/lifecycle.png)

## Want to know more?

- [Here is the official page from where the information was taken](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository). You can read more about git's cycle, as well as get to know git commands to check the status of your files and how to track, stage and commit your files. 


