## Configuring Git

<<<<<<< Updated upstream
Before you begin working on a project, you need to complete a one-time setup to let Git know who you are. This information will be attached to every commit you make. You can also turn on colorization to make the command line output easier to read.

Run the following commands in your terminal, replacing the placeholder text with your own information:

- Set your user name:

- Set your email address:

- Enable helpful colorization for UI output:

These global settings only need to be configured once on your computer.
=======
Before you begin using Git, you need to configure it with your name and email address. This information is included in the commits you create. You only need to do this configuration once.
- Set your name: `git config --global user.name "Your Name"`
- Set your email: `git config --global user.email "your.email@example.com"`
- Enable helpful colorization: `git config --global color.ui auto`
>>>>>>> Stashed changes



<<<<<<< Updated upstream


## Initializing a Repository

To start tracking a project with Git, you must first initialize a repository within the project's root folder. This creates the necessary infrastructure for version control.

1. Navigate to your project's root folder in the command line.

2. Run the init command:

4. By default, Git names the primary branch "master," but the new industry standard is "main". You can rename it with the following command:


=======
A repository (or repo) is the collection of files and directories that you are monitoring for changes with a version control tool. To start tracking a new project with Git, you must first initialize a repository from within the project's root folder.
- To initialize a new Git repo, use the command: `git init .`
- Git's default main branch is often named "master," but you can rename it to "main" using: `git branch -m main`
>>>>>>> Stashed changes



## Staging and Committing Files

<<<<<<< Updated upstream
Saving changes in Git is a two-step process that moves your work from the working directory to the staging area, and finally commits it permanently to the repository.

1. Stage Your Changes: First, you must add any new or changed files to the staging area. This tells Git which specific changes you want to include in your next save point.

- To stage a single file: git add readme.md

- To stage all new or modified files in the current directory: git add .

- You can also use wildcards and sub-folders: git add docs/textfiles/\*.txt

2. Commit Your Changes: After staging, you commit the changes, which creates a snapshot of your repository. Each commit must include a descriptive message explaining what you changed.

- For a short message: git commit -m "Your explanation of the changes goes here."

- For more complex changes, you can add a title and a longer description: git commit -m "Title" -m "Long description goes here..."

The best practice is to commit early and commit often to create a detailed and useful project history.

The Importance of Good Commit Messages

Writing high-quality commit messages is crucial. They contribute to:

- Traceability: Clarifying code history and making debugging easier.

- Collaboration: Helping teammates understand the purpose behind your changes.

- Documentation: Serving as a form of documentation for the source code.

- Change Management: Generating "Change Logs" for new software releases.

Bad Message Examples: "fixing stuff", "Final version.", "asdf" Good Message Example: "Prevent null reference crashes by adding pointer checks in the teleport code."


=======
The Git life cycle consists of three main stages: the Working Directory, the Staging Area, and the Git Commit.
1. Working Directory: This is the current state of your project's files on your computer.
2. Staging Files: Before you can save changes (commit), you must first add the new or modified files to a staging area. This lets you select which changes you want to include in the next commit.
    - To stage a specific file: git add readme.md
    - To stage all new or modified files in the current directory: `git add .`
    - You can also use wildcards: `git add docs/textfiles/*.txt`

3. Committing Files: A commit is a snapshot of your entire repository compressed into a unique identifier called a SHA hash. You commit your staged changes with a descriptive message.
    - To commit with a short message: git commit -m "Your explanation of the changes goes here."
    - For more complex changes, you can add a title and a longer description: `git commit -m "Title" -m "Long description goes here .........."`
Writing good commit messages is crucial as they provide traceability, aid collaboration, and serve as documentation for your project's history. For example, a good message is "Enhance user experience by validating signup form fields," while a bad one is simply "fixing stuff".


## Status, Log, and Diff

Git provides several commands to view the state of your repository and its history.
- `git status`: Use this command to check the status of your repo for any changes or additions.
- `git log`: This command allows you to review all the commits made in the repository's history. Each log entry displays the commit hash (a unique 40-character SHA1 ID), the author, the date, and the commit message.
- `git diff`: This command is used to see the differences between the current files in your working directory and the last commit. You can also use it to compare specific files (git diff secret_plans.txt) or entire folders (git diff ./textfiles/plans).
>>>>>>> Stashed changes



## Inspecting Your Repository: Status, Log, and Diff

Git provides several commands to check the state and history of your project.

- git status: Use this command at any time to see which files have been modified, which are new, and what is currently in the staging area.

- git log: To review the project's entire commit history, run git log. Each entry shows the unique commit hash, the author, the date, and the commit message.

- git diff: This command shows the exact differences between the files in your working directory and your last commit. You can use it to see all changes, or focus on a specific file or folder.

- To see all changes: git diff

- To see changes in a specific file: git diff secret\_plans.txt





## Ignoring Files with .gitignore

You should not track every file in your project directory. Files containing secrets (like passwords or API keys), temporary build files, or hidden OS files (Thumbs.db, .DS\_Store) should be excluded.

To ignore files, create a file named .gitignore in your project's root folder. Inside this file, you can list patterns for files and folders that Git should ignore.

Example .gitignore entries:

```
# Ignore a specific file by name. Comments start with a '#'

Thumbs.db



# Use wildcards to ignore all files with a .exe extension

*.exe



# Create an exception to a rule to track a specific file

!special.exe



# Ignore an entire folder named 'build'

build/
``` 
_You can find many useful .gitignore templates online for various programming languages and technologies._

