# Chapter 1: Create repo and practice committing code

## Objectives

* Create new local repository used during class
* Commit changes
* Optionally create GitHub repository


## Table of Contents

[Part 1 - Create Your Own Local Git Repo](#part-1-create-your-own-repository-for-your-coursework)

[Part 2 - Opening Multiple Instances of VS Code](#part-2---opening-multiple-instances-of-vs-code)

[Part 3 - Using VS Code to commit changes](#part-3---using-vs-code-to-commit-changes)

[Part 4 - Use .gitignore to not track changes](#part-4---using-gitignore-to-ignore-changes)

[Part 5 - Optionally create GitHub remote repo](#part-5-optional--setup-github-remote-repository)

[Part 6 - BONUS View GitLens extension](#part-6---BONUS-view-gitlens)

[Bonus - Explore VS Code](#bonus)

   
### **Part 1: Create your own repository for your coursework**
[back to top](#table-of-contents)

You will create a repository called **my-angular-course**. It will be tracked by Git so that if you accidentally delete or change files you can recover them easily. (Later we will create a project inside called **my-angular-albums**.)

Additionally, and optionally, you will be able to connect your local repository to a remote GitHub repository. 

Git is an especially helpful tool while working with Angular. One reason for this is we will be using the Angular CLI tool to create and modify many files at once. 
    
Sometimes, you may accidentally run a command and modify a lot of files you did not mean to. It can be time consuming to clean this up! To make the process easier, and be able to UNDO - we will use a local Git repo to track our files.
   
1. Depending on your lab setup, the global config for git may or may have not been setup. You can verify this by typing these commands into a command prompt.  These are global settings so you can be in any directory.

    ![config global](screenshots/git-config-global-check.png)

2. If there are values present, that is all you need for a local Git repo to be able to commit (and more easily discard) your changes.  
    
    It is a good practice to match to the info you would use on a remote repository, such as  GitHub, but it is not required.

3. To set up your personal git username and email idenitifers, use these commands - replacing **John Doe** inside the quotes with your name and **johndoe@example.com** with your email. Again, these are global settings so you can be in any directory.

    ![config global](screenshots/git-config-global.png)

4. Execute the following commands to create a new folder for your work and to initialize a local Git repo. You may or may not see the warnings. Use cd \ to take you to c:\
   
    ![GitInit](screenshots/git-init.png)

5. Test that you can add to your local repo and commit by executing the following commands. If you cannot commit, check that you set your global setting correctly in the previous steps.

    ![add readme](screenshots/git-cli-add-readme.png)

### **Part 2 - Opening Multiple Instances of VS Code**
[back to top](#table-of-contents)

Quite often you will need to have multiple instances of VS Code open.
    
For example, you may be referring to a sample project and comparing to your own project. 

VS Code allows use of control+c and control+v and corresponding context menu options to copy and paste files and directories between projects.  

1. From the Command Prompt within your **my-angular-course** directory execute the command **code .** to open the project in VS Code. 

    ![add readme](screenshots/code-space-dot.png)


2. Search the Extensions Marketplace to find `Peacock` by John Papa. If you do not have it already installed click the install button.
   
   ![](screenshots/extensions-install-menu.png)

    This extension lets us easily provide a color to the top and left sidebars of each instance of VS Code we open. 
    
    In the real world this is helpful as you may have reference implementation projects open as well as your own work.

    In this course it will be helpful as we will have different VS Code instances for 
    
    * Angular100-labs 
    * Angular100-solutions
    * Angular100-demos
    * MyAngularCourse (you will create in next Part) 
    
3. To use the extension, hit control+shift+p to bring up the command pallette and start typing Peacock.
   
   ![](screenshots/peacock-search.png)
   
4. You should see a list of options, choose Vue green to identify the VS Code instance for your labs.

   ![](screenshots/peacock-favorites.png)











5. You should now have two instances of VS Code running. In your my-angular-course use Peacock to change the color to C# purple. 

   1. Control+shift+p for command palette
   2. start typing peacock 
   3. choose C# purple
   
   ![add readme](screenshots/my-course-purple.png)


#### Switch between instances using Windows Task Bar

1. Move your cursor to the VS Code icon in  the windows status bar.
   
2. You should see your two VS Code instances with their colors. Peacock makes switching easier.

 ![](screenshots/VSCode-multiple-instances.png)

3. Click the **Angular100-Labs** project (green). If you are not using a virtual machine you can use Alt+tab to switch.

4. In **Angular100-Labs** find the file license-agreement.txt from the same  directory as this README.md. Click to highlight the license-agreement.txt file and hit Control-C or right-click to choose copy.
   
5. Switch back to your **my-angular-course** project and paste the file by right-clicking below your files and choosing paste.

 ![](screenshots/right-click-paste.png)


  
### **Part 3 - Using VS Code to Commit Changes**
[back to top](#table-of-contents)

By adjusting the color and copying a file into your project, you might have noticed the source control icon now has a number on it. Here we will practice with change tracking in projects.

1.  In your README.md file add your name.

    ![](screenshots/readme-add-name.png)


2.  Click on the Source Control button to open the panel `Source Control`. In this panel, mouse over the README.md file; press the `+` button that appeared to stage the change. You can also stage the change by right clicking on the README.md and clicking `Stage Changes`. You should now see that `README.md` was added to `Staged Changes`

    ![](screenshots/git-vscode-stage-readme.png)

3.  Above `Staged Changes` you should see a text input field with the text **Message (press Ctrl+Enter to commit)**. Within this field enter a good commit message which describes the changes we staged in the previous step.

    ![](screenshots/vscode-commit.png)


4.  Click the check mark above the text message field to commit the changes made to README.md
   
### **Part 4 - Using .gitignore to ignore Changes**
[back to top](#table-of-contents)

Sometimes, you do not want Git to track certain files or directories. Git looks for a settings file called `.gitignore`. Any files or directories included in this file will not be tracked.

1. Create a file called `.gitignore` by viewing the explorer pane and hovering over the name of the project to reveal a menu. Choose the icon to create a new file and name it .gitignore.
   
   Notice there is an intentional period (.) proceeding the name of the file.

    ![](screenshots/vs_code_explorer_hover.png)

2. Open the .gitignore file and add this on the first line: .vscode
  ![](screenshots/source-control-ignore.png) 
  
1. Now, inside the .vscode directory, create a new file called `untracked.text` and inside add the text "This is a local file."
    * Save the file - and you should not see it being tracked by Git because the directory is in .gitignore


1.  Please mark your work as complete. With your name tent card if in a classroom or by using method for online training. (spreadsheet, status symbol, etc.) Then you can move on to the OPTIONAL part or Bonus below.


### **Part 5 OPTIONAL- Setup GitHub remote repository**
[back to top](#table-of-contents)

1. If you have access to GitHub you can follow the directions in this folder's file [optional-github.md](./optional-github.md)  file. If others are done with this exercise already you can return to do this on a break or at a later time. It can be completed at any time before the end of class. 

### **Part 6 - BONUS View GitLens** 
[back to top](#table-of-contents)

1.  On VS Code's left hand toolbar, click on the `GitLens` extension you installed earlier. This extension contains additional features.

    ![](screenshots/gitlens.png)

1.  Familiarize yourself with `GitLens'` panel. Notice how you can use it to access different repositories and their branches, remote, your stashes, etc. Also notice how you can navigate through it to see history of a file, a line, or compare files between different branches or between local and remote.


## Bonus
[back to top](#table-of-contents)

1. If done before others, explore the VS Code Interactive Playground
   
![](screenshots/interactive-playground.png)

