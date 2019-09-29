# Chapter 1: Create a repository for your course work

## Objectives

* Practice with markdown files
* Practice with VS Code
* Install VS Code extensions
* Create new local repository used during class
* Commit changes
* Optionally create GitHub repository

## NOTES

* Please pay attention to detail. Follow each step carefully.
* Throughout the course the terms folder and directory are used interchangeable.
* You may see references to Enter key and Return key. These are the same intention, Enter is usually found on Windows and Return on Macs.

## Links to content below

[Part 1 - Markdown .md files in Edit & Preview Mode](#part-1---opening-markdown-md-files-in-edit--preview-mode)

[Part 2 - The Course Files](#part-2---the-course-files)

[Part 3 - More on Install VS Code extensions](#part-3-install-vs-code-extensions)

[Part 4 - Create Your Own Local Git Repo](#part-4-create-your-own-repository-for-your-coursework)

[Part 6 - Opening Multiple Instances of VS Code](#part-6---opening-multiple-instances-of-VS Code)

[Part 7 - Using VS Code to commit changes](#part-7---using-VS Code-to-commit-changes)

[Part 8 - Use .gitignore to not track changes](#part-8---using-gitignore-to-ignore-changes)

[Part 9 - Optionally create GitHub remote repo](#part-9-optional--setup-github-remote-repository)

[Part 10 - View GitLens extension](#part-10---view-gitlens)

[Bonus - Explore VS Code](#bonus)

### **Part 1 - Opening Markdown .md files in Edit & Preview Mode**

    We use markdown files in this class as they are used extensively in the industry with modern web projects.  They are plain text files that end in the extension `.md` and use special characters to indicate the meaning of text and how to display it when used on websites.
    
    On repository sites such as GitHub and Bitbucket a README.md in the root directory describes repositories and how to build and run dynamic projects. If you like to use Reddit you can use markdown to style your posts.
    
    The default mode of VS Code opens `.md` files in EDIT MODE where you see the special characters for formatting. VS Code also offers a PREVIEW MODE so you can more easily read the styled text.

    We will look at multiple ways to open markdown files in PREVIEW MODE in VS Code. You will use these methods for lab exercises and some demos. 

    
**Shortcut CTRL-SHIFT-V**

1. With this README.md in focus (click this text in the VS Code editor if the document has lost focus) you can open a new tab in PREVIEW MODE by hitting control-shift-V. This will open the preview in a new tab. You can then switch back and forth using the tabs. 
   
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

2. If you have been given a link to an online repository for this class, such as GitHub, https://github.com/JudyLipinski/angular100-labs you can use that link to navigate to this readme.md in a browser. Try this now and see if you can find/see the formatted markdown.

   ![GitHub](screenshots/github.png)

    This is a good option if you are using a virtual machine for class and have more than one monitor. If this your situation, you may want to open this now on your other monitor as you move forward in the directions.

    **MARKDOWN FORMATTING**

3. Make sure you can see both the Edit Mode in VS Code and the Preview Mode in VS Code or GitHub while you review the following:

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

        Most everything in VS Code has a hover effect. If you forget what anything does, just hover over it.

    **OPENING FROM EXPLORER**
1. In VS Code, from the Explorer Pane, you can find the markdown file of interest, right click and choose **Open Preview**. Try this now with this README.md as shown.
![Open In Preview](screenshots/open-preview.png)

1. In VS Code, while viewing in Preview mode, if you double-click an area of the file, you will be taken back to the EDIT VIEW or "source" markdown file for editing.

    Notice that if you double click the  image shown above - it takes you to the edit mode version where the image is linked.

2.  For the rest of this lab exercise, view this file in Preview mode or on GitHub. 

### **Part 2 - The Course Files**

1. Make sure you have VS Code open and can see the Angular100-Labs repository. Ensure the Explorer pane is visible, listing the files/directories. Recall to click the icon if the view is hidden. 

![](screenshots/3-angular100-labs-layout.png)



2. Understanding the Angular100-Labs repository
    * This repository contains the markdown files which re the instructions for the labs in this course. It is organized by chapter.  
    * There is a z-cheatsheets folder which contains help for VS Code, HTML, CSS       
    * Practice Bonus problems are available if you complete the regular exercises before others

1. If you make and save changes to any of these files, the VS Code source control icon (The Y looking icon in the vertical menu strip) will display a number for each file changed. 

    You can always revert to the original files by clicking this source control icon, hovering over the CHANGES menu and discarding all of the changes.

    ![](screenshots/discard-changes-ng.png)


### **Part 3: Install VS Code extensions**

    The extensions pane allows you to search for, install, disable and remove extensions easily.

1. Look on the left side bar menu of VS Code and click on the `Extensions` icon or use the shortcut (Ctrl + Shift + X). 

    ![extensions](screenshots/extensions.png)


2. Type into the Extensions Marketplace search field to find `Peacock` by John Papa. If you do not have it already installed click the install button.
   
   ![](screenshots/extensions-install-menu.png)

    This extension lets us provide a color to the top and left sidebars of each instance of VS Code we open. 
    
    In the real world this is helpful as you may have reference implementation projects open as well as your own work.

    In this course it will be helpful as we will have different VS Code instances for 
    
    * Angular100-labs repo
    * Angular100-solutions
    * Angular100-demos
    * MyAngularCourse (you will create in next Part) 
    

### **Part 4: Create your own repository for your coursework**

You will create a repository called my-angular-albums. It will be tracked by Git so that if you accidentally delete or change files you can recover them easily. 

Additionally, and optionally, you will be able to connect your local repository to a remote GitHub repository. 

Git is an especially helpful tool while working with Angular. One reason for this is we will be using the Angular CLI tool to create and modify many files at once. 
    
Sometimes, you may accidentally run a command and modify a lot of files you did not mean to. It can be time consuming to clean this up! To make the process easier, and be able to UNDO - we will use a local Git repo to track our files.
   
1. Depending on your lab setup, the global config for git may or may have not been setup. You can verify this by typing these commands into a command prompt.  These are global settings so you can be in any directory.

    ![config global](screenshots/git-config-global-check.png)

2. If there are values present, that is all you need for a local Git repo to be able to commit (and more easily discard) your changes.  

    To set these values you can use the following commands using your information. 
    
    It is a good practice to match to the info you would use on a remote repository, such as  GitHub, but it is not required.

3. To set up your personal git username and email idenitifers, use these commands - replacing **John Doe** inside the quotes with your name and **johndoe@example.com** with your email. Again, these are global settings so you can be in any directory.

    ![config global](screenshots/git-config-global.png)

4. Execute the following commands. These steps will create a new folder called MyWebCourse and place it under local source control. You may or may not see the warnings as pictured.
   
![GitInit](screenshots/git-init.png)

### **Part 6 - Opening Multiple Instances of VS Code**

    Quite often you will need to have multiple instances of VS Code open. For example, you may be referring to a sample project and comparing to your own project. In this class, you may wish to have open the Labs and your project.

    There are multiple options to do this including:
       * Running multiple instances of VS Code 
       * Putting projects in the same folder and opening that folder in VS Code
       * Creating a workspace 

    Whichever method you use, You can use control+c and control+v to copy and paste files and directories between projects.  


#### Multiple Instances, switch using Windows Task Bar
   ![](screenshots/VSCode-multiple-instances.png)

1. From the Command Prompt within `MyWebCourse` directory execute the command `code .` to open the project in VS Code. You should now have two instances of VS Code running.
   
2. In the modern web project find the file license-agreement.txt from the same  directory as this README.md. Highlight the license-agreement.txt file and hit Control-C or right-click to choose copy.
   
3. In your MyWebCourse project paste the file using Control-V or right-click and choosing paste.

   Here you can see more than one instance open. You can use the windows status bar to switch between projects by clicking the icon and choosing the one you want. If you are not using a virtual machine you can use Alt+tab to switch.

### **Part 7 - Using VS Code to Commit Changes**

    By copying a file into your project, you might have noticed the source control icon now has a number on it. Here we will practice with change tracking in projects.
   
1.  Delete the file license-agreement.txt. This will decrease the count of files being tracked as having changed.
   
2.  If not already open in VS Code, open this chapters README.md file in Edit Mode.

3.  Edit the README.md file to include your name

4.  Save the file, and notice the `Source Control` button on the left hand toolbar. It should now have a blue circle on it containing the number 1. This number indicates the number of files that have been changed locally.

5.  Click on the Source Control button to open the panel `Source Control`. In this panel, mouse over the README.md file; press the `+` button that appeared to stage the change. You can also stage the change by right clicking on the README.md and clicking `Stage Changes`. You should now see that `README.md` was added to `Staged Changes`

    ![](screenshots/source-control-stage-changes.png)

6.  Above `Staged Changes` you should see a text input field with the text `Message (press Ctrl+Enter to commit)`. Within this field enter a good commit message which describes the changes we staged in the previous step.

7.  Click the check mark above the text message field to commit the changes made to README.md

### **Part 8 - Using .gitignore to ignore Changes**

    Sometimes, you do not want Git to track certain files or directories. Git looks for a settings file called `.gitignore`. Any files or directories included in this file will not be tracked.
    
    In Modern Web projects for example, we end up with node_modules directories which should not be tracked.

1. Add a file called `.gitignore` - notice there is an intentional period (.) proceeding the name of the file.

    You can add a new file in VS Code by using the Explorer pane add button.
    ![](screenshots/VS Code-new-file.png)

1. Open the .gitignore file and add this on the first line: untracked.text
  ![](screenshots/source-control-ignore.png) 
  
1. Now create a new file called `untracked.text` and inside add the text "This is a local file."
    * Save the file - and you should not see it being tracked by Git.

1.  Please mark your work as complete. With your name tent card if in a classroom or by using method for online training. (spreadsheet, status symbol, etc.) Then you can move on to the OPTIONAL part or Bonus below.

### **Part 9 OPTIONAL- Setup GitHub remote repository**

1. If you have access to GitHub you can follow the directions in this folder's file [optional-github.md](./optional-github.md)  file. If others are done with this exercise already you can return to do this on a break or at a later time. It can be completed at any time before the end of class. 

### **Part 10 - View GitLens** 
1.  On VS Code's left hand toolbar, click on the `GitLens` extension you installed earlier. This extension contains additional features.

    ![](screenshots/gitlens.png)

1.  Familiarize yourself with `GitLens'` panel. Notice how you can use it to access different repositories and their branches, remote, your stashes, etc. Also notice how you can navigate through it to see history of a file, a line, or compare files between different branches or between local and remote.




## Bonus

1. If done before others, check out the VS Code Interactive Playground
2. 
You will be using this directory inthe next chapter to create an Angular project from scratch. If you wish to continue, the steps that follow will help you to setup a GitHub repository and link it to this local directory. You will need a valid GitHub account that you can login to. So if you have a phone, or other way to check your email you can set this up. Some students have created temporary emails using Google, Yahoo, etc and have used this to setup GitHub. You can always change the email on your account later when you have access to your email.