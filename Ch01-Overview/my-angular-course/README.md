# Chapter 1: Create a repository for your course work

## Objectives

* Practice with markdown files
* Practice with VSCode
* Install VS Code extensions
* Create new local repository used during class
* Commit changes
* Optionally create GitHub repository

## NOTES

* Please pay attention to detail. Follow each step carefully.
* Throughout the course the terms folder and directory are used interchangeable.
* You may see references to Enter key and Return key. These are the same intention, Enter is usually found on Windows and Return on Macs.

## Links to content below

[Part 1 - Markdown .md files in Edit & Preview Mode](#part-1---markdown-md-files-in-edit--preview-mode)

[Part 2 - The Course Files](#part-2---the-course-files)

[Part 3 - Tracking changes with Git in VSCode](#part-3---source-control-tracking)

[Part 4 - Install VSCode extensions](#part-4-install-vs-code-extensions)

[Part 5 - Create Local Git Repo](#part-5---create-new-mywebcourse-local-repository)

[Part 6 - Opening Multiple Instances of VScode](#part-6---opening-multiple-instances-of-vscode)

[Part 7 - Using VSCode to commit changes](#part-7---using-vscode-to-commit-changes)

[Part 8 - Use .gitignore to not track changes](#part-8---using-gitignore-to-ignore-changes)

[Part 9 - Optionally create GitHub remote repo](#part-9-optional--setup-github-remote-repository)

[Part 10 - View GitLens extension](#part-10---view-gitlens)

[Bonus - Explore VSCode](#bonus)

### **Part 1 - Markdown .md files in Edit & Preview Mode**

    We use markdown files in this class as they are used extensively in the industry with modern web projects.  They are plain text files that end in the extension `.md` and use special characters to indicate the meaning of text and how to display it when used on websites.
    
    On repository sites such as GitHub and Bitbucket a README.md in the root directory describes repositories and how to build and run dynamic projects. If you like to use Reddit you can use markdown to style your posts.
    
    The default mode of VS Code opens `.md` files in EDIT MODE where you see the special characters for formatting. VSCode also offers a PREVIEW MODE so you can more easily read the styled text.

    We will look at multiple ways to open markdown files in PREVIEW MODE in VSCode. You will use these methods for lab exercises and some demos. 

    
**Shortcut CTRL-SHIFT-V**

1. With this README.md in focus (click this text in the VSCode editor if the document has lost focus) you can open a new tab in PREVIEW MODE by hitting control-shift-V. This will open the preview in a new tab. You can then switch back and forth using the tabs. 
   
    **OPEN SPLIT SCREEN**

2. Open a Split screen in order to view both at the same time by clicking on this icon 
![Open Split Screen](screenshots/open-split-screen.png)

1. Drag the tab to the other window.
![Open In Preview](screenshots/dragtabs.png)

        You should now see the two files at the same time. With both Edit mode and Preview mode open in split panes, notice that if you scroll in one, the other scrolls as well.

        Remember this process to split the panes, it will be helpful when you want to see two files at the same time - such as lab instructions and the file you are editing.

    **VERTICAL MENU BUTTONS TOGGLE**

1. Give yourself more room to view code by hiding the leftmost pane. It should currently be the Explorer pane. Clicking the Explorer pane icon - pictured here with a blue circle and 1 will toggle this view. All of the icons in this vertical menu can be toggled to give you more room to work. Practice clicking to show and hide the menus.

    ![Vertical Pane](screenshots/vertical-pane.png)

     **USING GITHUB**

2. If you have been given a link to an online repository for this class, such as GitHub, you can use that link to navigate to the folder \Labs\Ch00-Intro in a browser. Try this now and see if you can find/see the formatted markdown.

   ![GitHub](screenshots/github.png)

    This is a good option if you have more than one monitor to use during class. If this is an option,you may want to open this now on your other monitor as you move forward in the directions.

    **MARKDOWN FORMATTING**

3. Make sure you can see both the Edit Mode in VSCode and the Preview Mode in VSCode or GitHub while you review the following:

    * Hash marks (#), are used for formatting headings.
        * A single # is heading "level 1" which is biggest, ## is "level 2", slightly smaller, and so on.
    * The asterisk is used to make a bullet.
        * Tabs are used for indentation of bullets.
    * Text can be highlighted using `backticks` around key words.
    * Code can be made **bold** using double asterisks.
    * Every item can be numbered as 1 in Edit Mode. When the markdown file is rendered: in preview mode or in browsers - the numbers will increment correctly.
        * This makes it easy to insert new items or re-order items, without needing to take the time to renumber.


    **OPEN PREVIEW TO SIDE**

4. Close all tabs so only the README.md is open in Edit Mode.
   
5. When a markdown file is the active file, there is a button that automatically opens Preview in the split pane.
![Preview button](screenshots/preview-button.png)

        Most everything in VSCode has a hover effect. If you forget what anything does, just hover over it.

    **OPENING FROM EXPLORER**
1. In VSCode, from the Explorer Pane, you can find the markdown file of interest, right click and choose **Open Preview**. Try this now with this README.md as shown.
![Open In Preview](screenshots/open-preview.png)

1. In VSCode, while viewing in Preview mode, if you double-click an area of the file, you will be taken back to the EDIT VIEW or "source" markdown file for editing.

    Notice that if you double click the  image shown above - it takes you to the edit mode version where the image is linked.

2.  For the rest of this lab exercise, view this file in Preview mode or on GitHub. 

### **Part 2 - The Course Files**

1. Ensure the Explorer view is visible, listing the files/directories. Recall to click the icon if the view is hidden. 

2. Understanding the Angular100-Labs repository
    * This repository contains the markdown files which re the instructions for the labs in this course. It is organized by chapter.  
    * There is a z-cheatsheets folder which contains help for VSCode, HTML, CSS      * If you make and save changes to any of these files, the VSCode source control icon (The Y looking icon in the vertical menu strip) will display a number for each file changed. 
        * You can always revert to the original files by clicking this source control icon, and discarding the changes from one or all files. 
    * Practice Bonus problems are available for CSS and JS.
    * The z_cheatsheets has shortcuts and links for what we will be discussing in class.


## Steps

1. We will be using Git in class as it is a helpful tool while working with Angular. Using the Angular CLI tool - we will create and modify many files at once. Sometimes, this may have been done mistakenly, and can be a mess to clean up! To make the process easier, and be able to UNDO - we will use a local Git repo to track our files.
   
2. Depending on your lab setup, the global config for git may or may have not been setup. You can verify this by typing this command into the command prompt.  

    ```bat
    git config --global user.name
    git config --global user.email
    ```

3. If there are values present, that is all you need for a local Git repo to be able to commit and discard your changes.  If you would like to hook up your work to a Remote Git repo - such as with GitHub, you can set your own personal identifiers.
   
   The actual values to not need to match anything such as your work or GitHub email. These are just idetifiers for when the code is pushed to a remote branch. These are not used for authentication.
   
4. To set up your personal git username and email idenitifers, locally using these commands - replacing **John Doe** in inside the quotes with your name and **johndoe@example.com** with your email.

   1. git config --global user.name "John Doe"
   2. git config --global user.email johndoe@example.com

5. Open a command prompt in windows and navigate to c:\

6. Navigate to C:\repos and issue this command

   ```bat
   mkdir my-angular-course
   ```

7. Change into this directory using `cd my-angular-course`

8. You will be using this directory to create an Angular project from scratch. If you wish to continue, the steps that follow will help you to setup a GitHub repository and link it to this local directory. You will need a valid GitHub account that you can login to. So if you have a phone, or other way to check your email you can set this up. Some students have created temporary emails using Google, Yahoo, etc and have used this to setup GitHub. You can always change the email on your account later when you have access to your email.


## Setting up GitHub so that you have a remote repository

1. Log into your Github account, click the + in the upper right and choose New repo

2.  Call it **my-angular-course**. Do not initialize - do not check any boxes. When it creates it will display some setup code which includes **…or create a new repository on the command line**

3.  Copy the multiple commands given by GitHub into your command prompt within the **my-angular-course** directory. It will look similar to the following: 

    (**DO NOT EXECUTE THESE COMMANDS - GET THE ONES FROM GITHUB**)

    ```bash
    echo "# test1234" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/SOME-URL
    git push -u origin master
    ```

4.  From the prompt, open in VSCode with code .

5.  Update the README with your name and the date. Save the file.

6.  In VSCode commit, your changes by clicking the third icon down which looks like a Y. In the source control: git menu, type in the message box - Added name and email. Click the checkmark to commit. This commits it to your local repository.

7.  In VSCode, look at the bottom left where it says "master" to the right of this notice the circular arrows. Click this icon, which will pull any code from the remote repo, and then push any changes to be committed.

8.  You will be prompted to input your username and password for Github.

9.  Once logged in successfully you should be able to check Github and see your changes.

10. Install windows git credential helper:

   git config --global credential.helper wincred

## Bonus

1. If done before others, check out the VSCode Interactive Playground
