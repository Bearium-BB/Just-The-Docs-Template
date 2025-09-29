<!-- prettier-ignore-start -->

\# Creating Using and Merging Branches

{: .no\_toc }

This page introduces the concept of branching in Git. Branches are a fundamental feature that allows you to work on different features or bug fixes in isolation without affecting the main project timeline. We will cover how to create and switch between branches, how to merge your changes back into the main line of development, and what to do when Git cannot automatically merge changes, resulting in a merge conflict.





\## Table of Contents

{: .no\_toc }



1\. TOC

{:toc}





\## Introducing Branches

In Git, a branch can be thought of as an alternate timeline for your project. It is a lightweight, movable pointer to a set of commits. Branching allows developers to work on different features or fix bugs in an isolated environment without affecting the main project timeline. Once the work in a branch is complete, it can be merged back into the main line of development. This capability is essential for managing different aspects of development, like feature creation or bug fixing, separately.



\## Creating and Using Branches

Git provides simple commands for creating and navigating branches.

Command Prompts



\- To create a new branch: `git branch <branch-name>`

\- To switch to an existing branch: `git checkout <branch-name>`

\- To create a new branch and switch to it in a single command: `git checkout -b <branch-name>`



\## Merging Branches

While branching allows for isolated development, merging is the process that brings those developments back into the main project timeline. When you 

merge a branch, you are incorporating its changes into your current branch.

Command Prompts



Let's say you've been working on a branch named experimental and want to merge those commits back into your main branch. You would first switch to the main branch and then run the merge command.

\- First, switch to the branch you want to merge into: `git checkout <branch-name>`

\- Then, merge the other branch's changes into your current branch: `git merge  <feature-branch-name>`



\## Handling Merge Conflicts

A merge conflict occurs when Git is unable to automatically merge two branches. This typically happens when changes have been made to the same lines in the same file on both branches. When a conflict occurs, Git will alert you in the terminal and mark the conflicted areas within the affected file(s).

Git's Conflict Markers

Git uses special markers to show you where the conflicting changes are:

\- `<<<<<<< HEAD`: This indicates the start of the changes from your current branch (the HEAD branch).

\- `=======`: This separates the changes from your current branch and the other branch.

\- `>>>>>>> branch-name`: This marks the end of the changes from the other branch you are merging in.



\## Resolving a Merge Conflict

Resolving a merge conflict is a manual process where you decide which code to keep.

1\. Edit the file: Open the conflicted file and edit it to fix the changes. You must decide which version of the code to keep and be sure to remove the conflict markers (<<<<<<<, =======, >>>>>>>).

2\. Stage the file: Once you have resolved the conflict in the file, add it to the staging area.

4\. Commit the fix: Commit the resolved file to finalize the merge.



\## Further Resources

\- \[Git Guide] (https://github.com/git-guides) - Official git Learning Guides from the folks at GitHub.

\- \[Git CheetSheet] (https://training.github.com/downloads/github-git-cheat-sheet/)- The most popular git commands in one page.

\- \[Pro Git Book] (https://git-scm.com/book/en/v2) - Free ebook provides a deep dive into everything git.



<!-- prettier-ignore-end -->

