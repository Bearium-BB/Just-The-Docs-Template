---
layout: default
title: Remote Repository
nav_order: 10
---

# Collaborative Coding with Git and GitHub 
{: .no_toc }

With Git and GitHub, multiple developers can work on the same project without stepping on each other's toes.

**Key concepts include:**

- **Forking:** Creating a personal copy of another user's repository.  
- **Cloning:** Downloading a repository to your local machine.  
- **Committing:** Saving changes to the local repository.  
- **Pushing:** Sending committed changes to a remote repository.  
- **Pull Request:** Proposing changes to a repository that can be reviewed and potentially merged.  

## Table of Contents
{: .no_toc }

1. TOC
{:toc}
---

# Overview of Git Workflows

Git workflows are methods or procedures that dictate how developers interact with the Git system to achieve effective team collaboration.  

There are several popular workflows used by teams:

- Centralized Workflow  
- Feature Branch Workflow  
- Forking Workflow  

---

## Centralized Workflow

- All developers work directly on a single branch, often `main` or `master`.  
- Simple and similar to Subversion-style workflows.  
- Not as powerful or flexible as other workflows.  
- Suitable for small teams and projects.  
- Merging can be problematic.  

### Steps in Centralized Workflow

1. **Initialization:** One team member creates the repository with an online remote.  
2. **Cloning:** Each team member creates a local copy by *cloning* the remote.  
3. **Working Locally:** Developers work on the project, committing to their local repo.  
4. **Resolving Conflicts:** Before sharing changes, developers must pull outstanding changes from the remote and resolve merge conflicts if required.  
5. **Pushing to Remote:** Developers push their changes to the central repository.  
6. **Synchronizing Team:** Others can pull from the central repo to incorporate the latest changes locally.  

---

## Feature Branch Workflow

- All feature development or bug fixes are done in dedicated branches.  
- Isolates new development from the main branch.  
- Makes it easy to discard experimental changes.  
- Facilitates code review via pull requests.  

> Note: This workflow is sometimes called **GitHub Flow**.  

### Steps in Feature Branch Workflow

- Works like the Centralized Workflow, except:  
  - **Branching:** New features or fixes are developed locally in a short-lived branch.  
  - **Resolving Conflicts:** Remote commits by other developers can be pulled into the local feature branch, with conflicts resolved if required.  
  - **Pushing to Remote:** Completed branches are pushed to the remote.  
  - **Requesting a Remote Merge:** A pull request is created on the Git hosting service (e.g., GitHub).  
  - **Reviewing:** Team members review the pull request before merging into the main branch.  

> Pull requests can be sent back unmerged if rework is necessary.  

---

## Forking Workflow

- Often used for open-source projects.  
- Each developer gets their own **local repository** and a **server-side copy** of the project.  
- Developers push to their own server-side repositories.  
- Changes are shared via pull requests from personal public repositories.  
- The project maintainer decides what is merged into the official repository.  

### Steps in Forking Workflow

- Works like the Feature Branch workflow, except:  
  - **Forking:** Each team member creates a fork of the project on the hosting service.  
  - **Cloning:** Team members clone their forked repo locally.  
  - **Adding an Upstream:** Team members configure a secondary remote called `upstream` that points to the official repo.  
  - **Resolving Conflicts:** Remote commits from `upstream` can be pulled into the local feature branch, with conflicts resolved as required.  
  - **Pushing to Remote:** Local feature branches are pushed to the forked remote.  
  - **Requesting a Remote Merge:** Pull requests are created to request merges from the forked repo to the official `upstream` repo.  

---

## Pull Requests in More Detail

Pull requests are a mechanism to propose changes to a repository and facilitate discussion about them.  

Project maintainers and contributors can:  

- Review the changes  
- Comment on them  
- Suggest modifications  
- Approve or close the request  

> Pull requests are not part of Git itself. They are a feature provided by Git hosting solutions like GitHub.  

---

## References

- Centralized Workflow [craftquest.io/guides/git/git-workflows/centralized-workflow](https://craftquest.io/guides/git/git-workflows/centralized-workflow)
- Feature Branch [articles.mergify.com/feature-branch-a-quick-walk-through-git-workflow/](https://articles.mergify.com/feature-branch-a-quick-walk-through-git-workflow/)
- Forking Workflow [gitprotect.io/blog/git-forking-workflow/](https://gitprotect.io/blog/git-forking-workflow/)
