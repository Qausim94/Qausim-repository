---
title: 02 Git and GitHub
permalink: /guide/git-and-github
---

# Git and GitHub Guide

## Introduction

Welcome to the Git and GitHub Guide! In this comprehensive guide, you will embark on a journey to master the essential concepts and commands of Git, the popular version control system, and GitHub, the widely used web-based hosting service for Git repositories.

Whether you are a beginner starting your programming journey or an experienced developer seeking to enhance your collaboration and version control skills, this guide is designed to provide you with a solid foundation in Git and GitHub.

Throughout the lessons, you will learn how to set up Git on your local machine, work with Git commands for local version control, collaborate with others using Git and GitHub, and explore the rich features offered by Git and GitHub for effective teamwork.

Each lesson is crafted with detailed explanations, practical examples, and hands-on assignments to ensure a thorough understanding of the topics covered. You will have the opportunity to put your knowledge into practice by executing commands, creating repositories, making commits, merging branches, and more.

By the end of this guide, you will possess the knowledge and skills necessary to confidently utilize Git and GitHub in your development workflow. You will be able to track changes, manage project history, collaborate with teammates, and leverage the power of distributed version control.

So, let's dive in and discover the world of Git and GitHub together. Get ready to enhance your development practices, streamline collaboration, and take your programming skills to the next level with this comprehensive Git and GitHub guide!

## Table of Contents

- [Lesson 1: Introduction to Git and GitHub](#lesson-1-introduction-to-git-and-gitHub)
- [Lesson 2: Creating Repositories in Git and GitHub](#lesson-2-creating-repositories-in-git-and-gitHub)
- [Lesson 3: Understanding Essential Git Commands](#lesson-3-understanding-essential-git-commands)
- [Lesson 4: Advanced Git Operations and Collaboration on GitHub](#lesson-4-advanced-git-operations-and-collaboration-on-gitHub)
- [Lesson 5: Git Bash and External Command Integration](#lesson-5-git-bash-and-external-command-integration)

## Lesson 1: Introduction to Git and GitHub

In this lesson, we'll introduce you to Git and GitHub, explain their benefits, and guide you through the setup process. By the end of this lesson, you'll have Git installed, a GitHub account created (if needed), and your local Git linked with GitHub using SSH.

### 1. What is Git and GitHub?

Git is a distributed version control system that allows developers to track changes in their code and collaborate with others effectively. It works at a local level, meaning you can make commits and manage version control on your local machine.

GitHub, on the other hand, is a web-based hosting service that provides a remote location for your Git repositories. It allows you to store and share your code with others, making it a valuable platform for collaboration and open-source projects. GitHub works at a remote level, enabling you to interact with repositories stored on its servers.

### 2. Installing Git and Creating a GitHub Account

#### Installing Git:

To get started, download and install Git on your machine. The installation process varies depending on your operating system. You can find detailed instructions and downloads in the official Git documentation: [Git Downloads](https://git-scm.com/downloads)

#### Creating a GitHub Account:

If you don't already have a GitHub account, visit the GitHub website ([GitHub.com](https://github.com/)) and sign up for a free account.

### 3. Linking Git with GitHub using SSH

To establish a secure connection between your local Git and GitHub, we'll use SSH (Secure Shell). SSH allows you to authenticate securely without the need for passwords.

#### Generating SSH Key:

If you don't have an SSH key yet, you'll need to generate one.

1. Open your terminal or Git Bash.
2. Use the following command to generate an SSH key:

   ```
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```

   Replace `"your_email@example.com"` with the email associated with your GitHub account.

3. Press Enter when prompted to save the key in the default location.
4. Set a passphrase (optional but recommended) to add extra security.

#### Adding SSH Key to GitHub:

Once you've generated your SSH key, you'll need to add it to your GitHub account.

1. Copy your public SSH key to the clipboard using the command:

   ```
   cat ~/.ssh/id_ed25519.pub | clip
   ```

   If you're using macOS or Linux, use `pbcopy` instead of `clip`.

2. Go to your GitHub account settings ([GitHub SSH Settings](https://github.com/settings/keys)) and click on "New SSH key."

3. Give your SSH key a title (e.g., "My Laptop SSH Key") and paste the key into the "Key" field.

4. Click "Add SSH key" to save.

### Assignment:

Verify that you've successfully linked your local Git with GitHub using SSH. To do this:

1. Open your terminal or Git Bash.
2. Enter the command:
   ```
   ssh -T git@github.com
   ```
   You should receive a message indicating that you've successfully authenticated.

Congratulations! You have installed Git, created a GitHub account, and linked your local Git with GitHub using SSH. In the next lesson, we'll explore different ways to create repositories in both Git and GitHub.

---

## Lesson 2: Creating Repositories in Git and GitHub

In this lesson, we'll learn how to create repositories both locally in Git and remotely on GitHub. We'll also cover using template repositories. By the end of this lesson, you'll be able to create new repositories with ease.

### 1. Creating a Repository in Git

To create a new repository locally in Git, follow these steps:

1. Open your terminal or Git Bash.
2. Navigate to the desired directory for your repository using the `cd` command.

#### a. Initialize a New Git Repo

To start a new Git repository, use the command:

```
git init
```

This will create a new, empty repository in the current directory.

#### b. Create and Add Files

Create files in the repository directory, and then use `git add` to stage them for the first commit.

```
touch index.html       # Create a new file
git add index.html     # Stage the file for commit
```

You can also add all files in the directory with:

```
git add .
```

#### c. Make the First Commit

After staging your changes, commit them with a descriptive message:

```
git commit -m "Initial commit"
```

### 2. Creating a Repository on GitHub

To create a new repository on GitHub, follow these steps:

1. Log in to your GitHub account.
2. Click on the "+" icon in the top-right corner and select "New repository." or go to [repo.new](https://repo.new) on your browser.

#### a. Repository Name and Description

Enter a name and description for your repository. Optionally, you can choose to make it public or private.

#### b. README, .gitignore, and License

GitHub provides the option to initialize your repository with a README, .gitignore, and license. Choose the appropriate settings for your project.

#### c. Create Repository

Click the "Create repository" button to create your repository on GitHub.

#### 3. Using Template Repositories

GitHub allows you to use template repositories as a starting point for new projects.

1. Open the template repository you want to use.
2. Click the "Use this template" button.
3. Provide a name for your new repository, and choose whether to make it public or private.
4. Click "Create repository" to generate your new repository using the template.

### Assignment:

1. Create a new repository locally using `git init`, add a file, and make the initial commit.
2. Create a new repository on GitHub with a README and .gitignore file.
3. Use a template repository to create a new repository on GitHub. Use can use thi repo as an example.
4. Write a summary of your understanding of the lesson.

In the next lesson, we'll dive deeper into Git commands, covering basic commands that are essential for version control.

---

## Lesson 3: Understanding Essential Git Commands

In this lesson, we'll dive deeper into essential Git commands, focusing on basic operations that are crucial for version control. You'll learn how to initialize a repository, clone an existing repository, stage changes, create commits, push to a remote repository, fetch and merge changes, work with branches, switch between branches, and view commit history.

### a. git init - Initialize a new Git repo

The `git init` command is used to initialize a new Git repository in the current directory.

```
git init
```

### b. git clone - Clone an existing repo to your local machine

The `git clone` command allows you to copy an existing repository from GitHub or any other remote source to your local machine.

```
git clone <repository-url>
```

### c. git add - Stage changes for commit

The `git add` command stages changes, preparing them to be committed to the repository.

```
git add <filename>     # Stage a specific file
git add .              # Stage all modified files in the current directory
```

### d. git commit - Create a new commit with staged changes

The `git commit` command creates a new commit with the changes staged for the commit.

```
git commit -m "Commit message"
```

### e. git push - Push commits to a remote repo

The `git push` command is used to push commits from your local repository to a remote repository, such as GitHub.

```
git push origin main    # Push commits to the remote repository "origin" and branch "main"
```

### f. git pull - Fetch & merge changes from a remote repo

The `git pull` command fetches changes from a remote repository and automatically merges them into your local branch.

```
git pull origin main    # Fetch and merge changes from the remote repository "origin" and branch "main"
```

### g. git branch - Create, list, or delete branches

The `git branch` command allows you to create new branches, list existing branches, and delete branches.

```
git branch <branch-name>   # Create a new branch
git branch                # List all branches in the repository
git branch -d <branch-name> # Delete a branch (use -D to force delete if not fully merged)
```

### h. git merge - Merge changes from one branch into another

The `git merge` command combines changes from one branch into another, bringing separate lines of development together.

```
git merge <branch-name>   # Merge changes from <branch-name> into the current branch
```

### i. git checkout - Switch between branches or restore files

The `git checkout` command is used to switch between branches or restore files to a previous version.

```
git checkout <branch-name>     # Switch to a different branch
git checkout <commit-hash>     # Restore files to a specific commit
```

### j. git log - View commit history

The `git log` command displays the commit history of your local repository, including commit hashes, authors, dates, and commit messages.

```
git log
```

### Assignment:

1. Create a new repository locally using `git init`, add a file, and make the initial commit.
2. Clone another repository from GitHub to your local machine using `git clone`.
3. Stage and commit changes to your local repository using `git add` and `git commit`.
4. Push your local commits to the GitHub repository using `git push`.
5. Fetch and merge changes from the GitHub repository to your local branch using `git pull`.
6. Create and switch between branches using `git branch` and `git checkout`.
7. Merge changes from one branch into another using `git merge`.
8. View the commit history of your repository using `git log`.
9. Write a summary of your understanding of the lesson.

Congratulations! You have now learned the essential Git commands, and you're well on your way to mastering Git and GitHub. In the next lesson, we'll explore more advanced Git operations and collaboration techniques.

---

## Lesson 4: Advanced Git Operations and Collaboration on GitHub

In this lesson, we'll explore more advanced Git operations and collaboration techniques on GitHub. You'll learn about more complex Git commands, resolving conflicts, working with remote branches, and collaborating with other developers on GitHub.

### a. git remote - Manage remote repositories

The `git remote` command allows you to manage remote repositories, such as GitHub. You can add, rename, or remove remotes.

```
git remote add <remote-name> <repository-url>   # Add a new remote repository
git remote -v                                 # List remote repositories with their URLs
git remote set-url <remote-name> <new-url>    # Change the URL of an existing remote
git remote remove <remote-name>              # Remove a remote repository
```

### b. git fetch - Fetch changes from a remote repo

The `git fetch` command fetches changes from a remote repository but doesn't automatically merge them.

```
git fetch origin    # Fetch changes from the remote repository "origin"
```

### c. git pull vs. git fetch and git merge - Update your branch with remote changes

You can use either `git pull` or `git fetch` followed by `git merge` to update your branch with remote changes.

```
git pull origin main   # Fetch and merge changes from "origin/main" into your current branch
# OR
git fetch origin       # Fetch changes from "origin"
git merge origin/main  # Merge fetched changes into your current branch
```

### d. git push with upstream - Set the default upstream branch

Use `git push -u <remote-name> <branch-name>` to push the current branch to a remote repository and set the default upstream branch.

```
git push -u origin feature   # Push "feature" branch to "origin" and set it as the default upstream
```

### e. git cherry-pick - Apply specific commits to a branch

The `git cherry-pick` command allows you to apply specific commits from one branch to another.

```
git cherry-pick <commit-hash>     # Apply a specific commit to the current branch
```

### f. git rebase - Reapply commits on top of another branch

`git rebase` allows you to reapply commits on top of another branch, leading to a linear commit history.

```
git rebase <branch-name>   # Reapply commits on top of <branch-name>
```

### g. Handling Merge Conflicts

Merge conflicts occur when Git can't automatically merge changes from different branches. To resolve conflicts, manually edit the conflicting files, and then commit the changes.

```
# Resolve conflicts in the conflicting files, then
git add <conflicting-file>    # Stage the resolved changes
git commit                   # Commit the resolved changes
```

### Assignment:

1. Add a remote connection to your local repository using `git remote add`.
2. Fetch changes from the remote repository using `git fetch`.
3. Update your local branch with remote changes using `git pull`.
4. Push your branch to the remote repository with the default upstream using `git push -u`.
5. Cherry-pick a specific commit from one branch to another using `git cherry-pick`.
6. Resolve a merge conflict between two branches.
7. Write a summary of your understanding of the lesson.

By the end of this lesson, you'll have a deeper understanding of advanced Git operations and collaboration on GitHub. In the next lesson, we'll explore integrating Git with external commands and using Git Bash effectively.

---

## Lesson 5: Git Bash and External Command Integration

In this lesson, we'll delve into using Git Bash effectively and integrating external commands, such as Node.js, Yarn, and more, with Git.

### a. Using Git Bash effectively

- Navigating directories:

  ```
  cd <directory>       # Change directory
  cd ..                # Move to the parent directory
  ls                   # List files and directories
  ```

- Creating and deleting directories:

  ```
  mkdir <directory>    # Create a new directory
  rmdir <directory>    # Delete an empty directory
  rm -rf <directory>   # Delete a directory and its contents
  ```

- Editing files with Nano:
  ```
  nano <filename>      # Open the file in the Nano text editor
  ```

### b. Integrating External Commands

- Using Node.js and NPM/Yarn:
  ```
  node <filename>      # Run a Node.js script
  npm install          # Install Node.js dependencies (npm)
  yarn install         # Install Node.js dependencies (Yarn)
  ```

### Assignment:

1. Navigate to a specific directory using Git Bash.
2. Create a new directory and a file within it using Git Bash commands.
3. Use Nano to edit the file and add some content.
4. Run a Node.js script using Git Bash.
5. Install Node.js dependencies using either NPM or Yarn with Git Bash.
6. Write a summary of your understanding of the lesson.

Congratulations! You have now completed the Git and GitHub guide, covering essential Git operations, collaboration techniques, and integrating external commands with Git Bash. You're now equipped with the knowledge and skills to efficiently use Git and GitHub in your development workflow.

---

## Conclusion

In this comprehensive guide, you've learned the fundamentals of Git and GitHub, from basic version control to advanced collaboration techniques. By setting up Git and GitHub, creating repositories, using essential Git commands, resolving conflicts, and integrating external commands, you're ready to take your development skills to the next level.

Keep practicing and exploring, as version control is an essential tool for developers to work efficiently, collaborate effectively, and maintain the integrity of their codebase. The more you use Git and GitHub, the more proficient you'll become in managing projects and contributing to open-source software.

Happy coding, and may your journey with Git and GitHub be fruitful! If you encounter challenges or have questions, remember to refer to the documentation and seek guidance from the vibrant developer community.

---

Thank you for joining this Git and GitHub guide. We hope you found it helpful in your learning journey. If you have any feedback or suggestions, feel free to share them, open an issue or issue a pull request. Happy coding!

## Further learning resources

1. [Git Basics](https://www.theodinproject.com/paths/foundations/courses/foundations#git-basics)
1. [Learn Git & GitHub](https://www.codecademy.com/learn/learn-the-command-line)
1. [About Git](https://docs.github.com/en/get-started/using-git/about-git)
