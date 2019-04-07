# Chapter 1: Create a repository for your course work

## Objectives

- Create a local project to be used during the course
- Use github to create a new remote repository

## Overview

In this lab you will use create a Github repository and push code to your repository.

## Steps

1. Set up your git username and email locally using these commands - replacing John Doe with your name and johndoe@example.com with your email.

   1. git config --global user.name "John Doe"
   2. git config --global user.email johndoe@example.com

1. Open a command prompt in windows and navigate to c:\

1. Navigate to C:\ and issue this command

   ```bash
   mkdir my-angular-course
   ```

1. Change into this directory using `cd my-angular-course`

1. Log into your Github account, click the + in the upper right and choose New repo

1. Call it **my-angular-course**. Do not initialize - do not check any boxes. When it creates it will display some setup code which includes **…or create a new repository on the command line**

1. Copy the commands given by Github which will look something similar to the following into your command prompt within the **my-angular-albums**

   ```bash
   echo "# test1234" >> README.md
   git init
   git add README.md
   git commit -m "first commit"
   git remote add origin https://github.com/JudyLipinski/test1234.git
   git push -u origin master
   ```

1. From the prompt, open in VSCode with code .

1. Update the README with your name and the date. Save the file.

1. In VSCode commit, your changes by clicking the third icon down which looks like a Y. In the source control: git menu, type in the message box - Added name and email. Click the checkmark to commit. This commits it to your local repository.

1. In VSCode, look at the bottom left where it says "master" to the right of this notice the circular arrows. Click this icon, which will pull any code from the remote repo, and then push any changes to be committed.

1. You will be prompted to input your username and password for Github.

1. Once logged in successfully you should be able to check Github and see your changes.

1. Install windows git credential helper:

   git config --global credential.helper wincred

   https://help.github.com/en/articles/caching-your-github-password-in-git
