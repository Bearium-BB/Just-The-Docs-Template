---
layout: default
title: Remote Repository
nav_order: 9
---
# remote repository
# Collaborative Coding with Git and GitHub 
{: .no_toc }


## What is a remote repository
A remote repository is a repository connected to the internet, allowing people to collaborate easily and providing backups. There are tools for this, such as GitHub and GitLab, which host your Git repositories on their servers. These platforms let other people collaborate with you and provide an easy way to back up your code.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

## Linking Your Local Repo to GitHub

Let's say you've created a new repo on GitHub called `My-Lovely-Repo` and you've already initialized this project's local Git repository.  

From the command line (within your project folder) add GitHub as a remote:

```bash
git remote add origin git@github.com:<username>/My-Lovely-Repo.git
```

This should be all one line with `<username>` replaced by your actual username.  

You can check if a remote has been added to a repo:

```bash
git remote -v
```

---

## Simplest GitHub Workflow

If you don't have a local copy of a GitHub repo, you can clone it:

```bash
git clone git@github.com:<username>/<repo-name>.git
```

When you want to push the latest state of your repo to GitHub:

```bash
git push origin <branch-name>
```

When you want to grab the latest commits from GitHub:

```bash
git pull origin <branch-name>
```

---

## Step 1: Create a GitHub Account
1. Go to [GitHub.com](https://github.com).
2. Click on **Sign Up**.
3. Fill out the required information to create your account.
4. Apply for the **GitHub Education Student Benefits**.

---

## Step 2: SSH Keys for Authentication (Optional)

Generate a public/private key pair from the Git Bash terminal:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

- Press Enter to accept the default save path, and make note of this path.  
- It's good practice to secure your keys with a passphrase. Just don't forget it.  
- Navigate to the save path, open the `id_ed25519.pub` file, and copy-paste its contents into GitHub.  

Test your key from the terminal:

```bash
ssh -T git@github.com
```

(Type **yes** when prompted.)

---

## Step 3: Create a New Repository on GitHub
1. Once logged into GitHub, click on the **"+"** icon on the top right corner of the page and select **New repository**.
2. Give your repository a name. You can also add a description (optional).
3. Ensure the repo is set to **public**.
4. Click on **Create repository**.

---

## Step 4: Connect your Local Repository to GitHub
1. Open Git Bash (terminal application).
2. Navigate to the local repository folder from the previous activities.
3. Use:

   ```bash
   git remote add origin <your-repository-url>
   ```

   to set the new GitHub repository as your `origin` remote repository.  

   > You can find your repository URL on the web page for your repo on GitHub.  
   > Example:  
   > - HTTPS: `https://github.com/<username>/<repo-name>.git`  
   > - SSH: `git@github.com:<username>/<repo-name>.git`

---

## Step 5: Push Local Changes to GitHub

Push your local commits to the remote repository:

```bash
git push -u origin main
```

- The `-u` option sets the remote repository as the upstream repository for the current branch.  
- Subsequent pushes can now be done with:

```bash
git push
```

Reload the main page of your repository on GitHub to confirm that your local files are now there.

---

## Step 6: Making Changes and Committing Them on GitHub
1. On GitHub, navigate to one of your files and click on the **pencil** icon to edit it.
2. Make some changes in the file.
3. Below the editor, write a commit message describing your changes.
4. Click on **Commit changes**.

---

## Step 7: Pull Remote Commits
Back in your local repository, use:

```bash
git pull origin main
```

to fetch the commit you made on GitHub and merge it into your local branch.  

Try to trigger a merge conflict by committing changes to the **same line** locally and remotely, and then pulling.  

- Locally resolve the merge conflict that you triggered.  
- Commit the resolved state of the repo.  
- Push the resolved state to GitHub.  
