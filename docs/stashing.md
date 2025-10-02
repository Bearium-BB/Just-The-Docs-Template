---
layout: default
title: Stashing
nav_order: 7
---
# Stashing
{:.no_toc}

Git stash allows you to temporarily put aside changes that you don't want to commit yet.  
Think of it like a **magic toy box**: you can quickly clean your room (stash your changes), and later bring everything back to how it was.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

## When to Stash?

You may want to use `git stash` when:
- You want to switch branches, but you're in the middle of something and don't want to commit yet.  
- You need to pull changes, but you have uncommitted work.  


## Stashing in Action

```
git stash
```

This command stashes your changes, leaving you with a clean working directory.  

**Remember:** It's only temporary storage. Don't forget about your stashed changes!


## The Stash Stack

Think of `git stash` as creating a stack of saved changes.  
- You can stash multiple sets of changes.  
- Git stores them in a **LIFO (Last In, First Out)** order.  


## Restoring Stashed Changes

To restore stashed changes, use:

- `git stash pop` - Re-applies the changes and removes them from the stash
- `git stash apply` - Re-applies the changes but keeps them in the stash


## Other Helpful Stash Commands

- `git stash list` : Review all your stashes
- `git stash drop` : Remove the most recent stash
- `git stash branch <branchname>` : Create a new branch from the most recent stash
- `git stash clear` : Remove all stashes
- `git stash pop 'stash@{n}'` : Pop a specific stash seen in `git stash list`.

## Want to know more?

- [Git Documentation: git-stash (Official Manual)](https://git-scm.com/docs/git-stash)
- [Git Stash - Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)  