
---
layout: default
title: Undoing In Git
nav_order: 4
---

# Undoing in Git
{: .no_toc }



This page provides a guide to undoing changes in Git, a crucial skill for effective version control. It covers four primary commands—checkout, reset, revert, and clean—detailing how each one works and the specific scenarios where they should be used. The goal is to help you understand the differences between these commands, especially their safety levels and impact on your project's history, so you can confidently manage and correct mistakes in your code base.




## Table of Contents
{: .no_toc }



1. TOC
{:toc}



## Undoing with Checkout

The git checkout command is considered the simplest way to perform a private "undo". Its primary function in this context is to discard uncommitted local changes in your working directory. You should use this command when you have modified files that you have not yet committed and want to restore them to their most recently committed state.

To discard changes in a specific file: `git checkout -- filename.txt`

For example, if you made unwanted changes to readme.md, you can run `git checkout readme.md` to restore it.

To discard changes in all files and folders in your working directory: `git checkout --` 

Warning: This action is described as slightly dangerous because any discarded changes cannot be recovered.



## Undoing with Reset

The git reset command is a powerful, but destructive, tool used to undo one or more commits in your local repository.

- Warning: This command is considered dangerous because it rewrites the project's history by moving the HEAD pointer to a previous commit. It should be used with caution and typically only on commits that have not been shared with others.

git reset has two primary modes:

- Hard Reset (--hard)
This command changes your working directory to match a specific commit. Any uncommitted changes are lost, and all files in the working directory and staging area are reset to the state of the specified commit. You can get the commits ID via the `git log` command.

Command: `git reset --hard [commit_id]`.

- Soft Reset (--soft)

This command also resets the HEAD pointer to a previous commit, but it keeps your changes in the working directory. It effectively undoes the commit while preserving your work, leaving the changes as uncommitted modifications.

 Command: `git reset --soft [commit_id]`.



## Undoing with Revert

The 'git revert' command is considered the safest way to undo changes, particularly for commits that have already been shared with others on a remote repository. It is known as the "public undo" because it transparently documents the reversal of a previous change.
How it works: Instead of deleting commits from the project history, git revert creates a new commit that contains the inverse of the changes from the specified commit. This preserves the integrity of the project's history, making it a safe choice for collaborative projects.

- To revert a single commit: `git revert [commit_id]`

- To revert multiple commits: `git revert --no-commit <oldest-commit>..<newest-commit>`



## Undoing with Clean

The `git clean` command is a helpful utility for cleaning up your working directory.

- Use Case: This command is used to discard all files that are not under version control (i.e., untracked files). This is useful for removing temporary or build files that you don't want to include in your repository.


## When to Use Different Strategies

Choosing the right "undo" strategy depends on whether the changes are local or have been shared with others.

- Use `git checkout` to discard local changes in your working directory that have not been committed.

- Use `git reset` to undo commits in your local repository that have not been pushed to a remote repository. Since it rewrites history, it is best for private cleanup.

- Use `git revert` to undo commits that have already been shared with others. It is the safest method for public commits because it creates a new commit to reverse the changes and does not alter existing history.

- Use `git clean` to remove untracked files from your working directory.





### Want to know more?

- [Git Guide](https://github.com/git-guides) Official git Learning Guides from the folks at GitHub.

- [The Git Week: A guide to Git revert, Reset and checkout](https://medium.com/@lorenzouriel/the-git-week-a-guide-to-git-revert-reset-and-checkout-da103b119b17)  Helpful article.

- [Pro Git Book](https://git-scm.com/book/en/v2) Free ebook provides a deep dive into everything git.





