---
title: 01 Basic Command Line
permalink: /guide/01-basic-command-line
---

# Basic Command Line Guide with Git Bash

Welcome to the Basic Command Line Guide with Git Bash! This guide will introduce you to essential command line operations using Git Bash, a terminal emulator for Windows.

Table of Contents

- [Lesson 1: Getting Started](#lesson-1-getting-started)
- [Lesson 2: Navigating Directories](#lesson-2-navigating-directories)
- [Lesson 3: Creating and Deleting](#lesson-3-creating-and-deleting)
- [Lesson 4: Editing Files](#lesson-4-editing-files)
- [Lesson 5: External Commands](#lesson-5-external-commands)

## Lesson 1: Getting Started

To begin, let's familiarize ourselves with the command line interface.

1. Launch Git Bash[^1].
1. Command Prompt: Once Git Bash is open, you'll see a terminal window with a command prompt that looks like `$`. This is where you can enter commands and interact with the command line interface.

[^1]: Git Bash can be downloaded from the official Git website: [Git Bash](https://git-scm.com/downloads).

### Assignment 1:

1. Download git from the official Git website
1. Download VS Code
1. Download Node

## Lesson 2: Navigating Directories

In this lesson, we'll learn how to navigate through directories.

1. `pwd` (print working directory): Use this command to know your current directory, displaying the full path of the directory you are currently in.
   Example: `pwd`

1. `ls` (list): Use this command to list the contents of the current directory, including files and subdirectories.
   Example: `ls`

1. `cd` (change directory): Use this command to change to a different directory.
   Example: `cd Documents`

1. `cd ..`: Use this command to move up one level in the directory hierarchy, to the parent directory.
   Example: `cd ..`

1. `cd` or `cd ~`: Use either of these commands to move directly to your home directory.
   Example: `cd` or `cd ~`

### Assignment 2:

1. Open Git Bash and navigate to your "Desktop" directory using `cd`.
1. List the contents of the "Desktop" directory using `ls`.
1. Move up one level in the directory hierarchy using `cd ..`.
1. Check your current directory using `pwd`.

## Lesson 3: Creating and Deleting

In this lesson, we'll learn how to create and delete directories and files.

1. `mkdir` (make directory): Use this command followed by the directory name to create a new directory.
   Example: `mkdir myfolder`

1. `touch`: Use this command followed by the file name to create a new file.
   Example: `touch myfile.txt`

1. `mv` (move): Use this command followed by the old name and new name to rename a file or directory.
   Example: `mv myfile.txt newfile.txt`

1. `rm` (remove): Use this command followed by the file name to delete a file.
   Example: `rm myfile.txt`

1. `rmdir` (remove directory): Use this command followed by the directory name to delete an empty directory.
   Example: `rmdir myfolder`

1. `rm -r` (remove recursively): Use this command followed by the directory name to delete a directory and its contents.
   Example: `rm -r myfolder`

### Assignment 3:

1. Create a directory named "myproject".
1. Move into the "myproject" directory.
1. Create a file named "index.html".
1. Rename the file "index.html" to "home.html".
1. Delete the file "home.html".
1. Delete the "myproject" directory.

## Lesson 4: Editing Files

In this lesson, we'll learn how to edit files using command line tools.

1. `cat` (concatenate): Use this command followed by the file name to view the contents of a file.
   Example: `cat myfile.txt`

1. `nano`: Use this command followed by the file name to edit a file using the nano text editor.
   Example: `nano myfile.txt`

1. Inside the nano editor:
   - Use the arrow keys to navigate.
   - Edit the file as needed.
   - Press `Ctrl + X` to exit.
   - Press `Y` to save the changes.
   - Press `Enter` to confirm the file name.

### Assignment 4:

1. Create a file named "message.txt".
1. Use the nano editor to add the following content: "Hello, Command Line!"
1. Save and exit the nano editor.
1. View the contents of the file "message.txt" using `cat`.

## Lesson 5: External Commands

In this lesson, we'll learn how to use external commands like Git, Node.js, and Yarn. Note that this is introductory and you will learn more about them in detail later.

1. Git:
   Git is a widely used version control system that allows you to track changes in your files and collaborate with others on projects. It's especially popular for managing source code repositories.

   - Check the Git version: The `git --version` command displays the version of Git installed on your system.
     Example: `git --version`

   - Clone a repository: The `git clone` command allows you to create a copy of a Git repository from a remote source. The example below will create a folder with all the content of the repository.
     Example: `git clone <repository-url>`, where <repository-url> is a repo url, e.g. `https://github.com/bolah2009/command-line-guide.git`

     Resources:

     - Git documentation: [Git Documentation](https://git-scm.com/doc)

1. Node.js:
   Node.js is a JavaScript runtime built on the V8 JavaScript engine. It allows you to run JavaScript code outside of a web browser, making it a powerful tool for server-side and command line applications.

   - Check the Node.js version: The `node --version` command displays the version of Node.js installed on your system.
     Example: `node --version`

   - Run a JavaScript file: The `node` command allows you to execute JavaScript files.
     Example: `node script.js`

     Sample code for `script.js`, you will need to create a file named `script.js`, open it and add the below code for the above command to work:

     ```javascript
     console.log('Hello, Command Line!');
     ```

     Resources:

     - Node.js website: [Node.js](https://nodejs.org)
     - Node.js documentation: [Node.js Documentation](https://nodejs.org/docs/latest/api/)

1. Yarn:
   Yarn is a package manager for JavaScript that offers faster and more reliable dependency management for your projects. It's commonly used in conjunction with Node.js and npm (Node Package Manager) to manage project dependencies efficiently. Before working with yarn, you will need to download it using the command `npm install --global yarn`. See [`yarn` installation guide](https://classic.yarnpkg.com/lang/en/docs/install) for more information.

   - Check the Yarn version: The `yarn --version` command displays the version of Yarn installed on your system.
     Example: `yarn --version`

   - Install project dependencies: The `yarn install` command installs the dependencies specified in a project's `package.json` file. Change your directory to the new folder created by the `git clone` command above, then run the below command to install the dependencies to the repo.
     Example: `yarn install`

     Resources:

     - Yarn website: [Yarn](https://yarnpkg.com)
     - Yarn documentation: [Yarn Documentation](https://yarnpkg.com/getting-started)

### Assignment 5:

1. Check the version of Node.js installed on your system by running the `node --version` command.
1. Create a JavaScript file named "script.js" and add the following code to it:
   ```javascript
   console.log('Hello, Command Line!');
   ```
1. Run the JavaScript file using the Node.js runtime by executing the `node` command followed by the file name.
   Example: `node script.js`
1. Check the version of Git installed on your system by running the `git --version` command.
1. Clone a Git repository of your choice by using the `git clone` command followed by the repository URL.
   Example: `git clone https://github.com/bolah2009/html-css-template.git`
1. Check the version of Yarn installed on your system by running the `yarn --version` command.
1. Install project dependencies for the above-cloned project by navigating to the project directory and running the `yarn install` command.

## Further learning resources

1. [Command Line Basics](https://www.theodinproject.com/lessons/foundations-command-line-basics)
1. [Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line)
1. [Learn Bash Scripting](https://www.codecademy.com/learn/bash-scripting)
