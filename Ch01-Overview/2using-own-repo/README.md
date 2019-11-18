# Chapter 1: Setup and Practice with VS Code 

## Objectives

* Practice with VS Code
* Practice with markdown files
* Install VS Code extensions
  

## NOTES

* Please pay attention to detail. Follow each step carefully.
* Throughout the course the terms folder and directory are used interchangeable.
* You may see references to Enter key and Return key. These are the same intention, Enter is usually found on Windows and Return on Macs.
* You must save changes to your files to see the effects take place. Control+S is the FASTEST. You can also use File | Save but this wastes seconds - adding up to minutes, etc...

## Links to content below

[Part 1 - Navigating the course on Github](#part-1---navigating-the-course-on-github)


[Part 2 - Opening files in VS Code and changing default settings](#part-2---opening-files-in-vs-code-and-changing-default-settings)

[Part 3 - Markdown .md files in Edit & Preview Mode](#part-3---opening-markdown-md-files-in-edit--preview-mode)

[Part 4 - The Angular100-Labs project](#part-4---the-angular100-labs-project)

[Bonus - Explore VS Code](#bonus)

   
### **Part 1 - Navigating the course on Github**

1. Throughout the course you can use the browser to navigate to the course Git repository Angular100-Labs (specific for your class). https://github.com/JudyLipinski/angular100-labs


    ![GitHub](screenshots/github.png)

    This is a good option if you are using a virtual machine for class and have more than one monitor. If this your situation, you may want to open this now on your other monitor as you move forward in the directions.

2. Bookmark this page for easier access later.  In Chrome can hit the star in the upper right hand side and choose Bookmarks bar. 
   ![Bookmark star in chrome](screenshots/1bookmarks-star.png)
   
3. If you do not see the bookmarks bar, hit control+shift+B to make it appear.
   ![Bookmark bar in chrome](screenshots/1-bookmarks-bar.png)


### **Part 2 - Opening files in VS Code and changing default settings**  
[back to top](#links-to-content-below)



**Install and use VS Code Peacock extension**
[back to top](#links-to-content-below)

    The extensions pane allows you to search for, install, disable and remove extensions easily.

1. Look on the left side bar menu of VS Code and click on the `Extensions` icon or use the shortcut (Ctrl + Shift + X). 

    ![extensions](screenshots/extensions.png)


2. Type into the Extensions Marketplace search field to find `Peacock` by John Papa. If you do not have it already installed click the install button.
   
   ![](screenshots/extensions-install-menu.png)

    This extension lets us provide a color to the top and left sidebars of each instance of VS Code we open. 
    
    In the real world this is helpful as you may have reference implementation projects open as well as your own work.

    In this course it will be helpful as we will have different VS Code instances for 
    
    * Angular100-labs 
    * Angular100-solutions
    * Angular100-demos
    * MyAngularCourse (you will create in next Part) 
    
1. To use the extension, hit control+shift+p to bring up the command pallette and start typing Peacock.
   
   ![](screenshots/peacock-search.png)
   
2. You should see a list of options, choose Vue green to identify the VS Code instance for your labs.

   ![](screenshots/peacock-favorites.png)


**OPENING FILES IN VS CODE**

1. If you are viewing these instructions on Github now, make sure you also have VS Code open to the ANGULAR100-LABS project. One way of opening this is to navigate in 

![](2-win-explorer-context-vscode.png)
   
2. By default, in VS Code when you single click files in the Explorer pane they open in a preview mode. This is indicated by italics in the tab. If you open another file it replaces the previous file. Try single clicking the file **license-agreement.txt**.

    ![italics](screenshots/1-italics.png)

3.   Now single click the file **optional-github.md** and it will replace the **license-agreement.txt** file. 
    
        ![optional](screenshots/1-optional-italics.png)
       
4.   If you double click on the tab it will become solid and opening another file will not replace its contents.

        ![](screenshots/1-optional-solid.png)

5. To make single clicking not open in preview mode, you can change VS Code settings. First click the gear icon to open the settings menu.

    ![Change Enable Preview](screenshots/1-gear-icon.png)


6. Then in the search field start typing open. Click the editor manager under Workbench, and deselect the checkbox for Enable Preview.

    ![Change Enable Preview](screenshots/1-enable-preview.png)

7. Now single click the file **really-long-file.txt** and it should open in its own tab and not be in italics.
   
   ![wrap text](screenshots/1-long-file.png)
   
   **Toggle text wrapping**
8. If VSCode is not wrapping, you will just see one line of text and need to scroll to the right to see the contents. Use the View menu or shortcut of Alt-Z to toggle the word wrap.

    ![wrap text](screenshots/1-alt-z.png)

9.  Notice the line number isn't incrementing it is still just one line - but easier to read.
   
   ![wrap text](screenshots/1-wrap-contents.png)

### **Part 3 - Opening Markdown .md files in Edit & Preview Mode**
[back to top](#links-to-content-below)


    We use markdown files in this class for lab directions as they are used extensively in the industry with modern web projects.  
    
    These plain text files end in the extension .md and are used to describe Angular projects.
    
    Special characters are used to indicate the meaning of text and how to display it when used on websites.
    
    On repository sites such as GitHub and Bitbucket a README.md in the root directory describes repositories and how to build and run dynamic projects. If you like to use Reddit you can use markdown to style your posts.
    
    The default mode of VS Code opens .md files in EDIT MODE where you see the special characters for formatting. VS Code also offers a PREVIEW MODE so you can more easily read the styled text.

    We will look at multiple ways to open markdown files in PREVIEW MODE in VS Code. You will use these methods for lab exercises and some demos. 


**OPENING PREVIEW USING CTRL-SHIFT-V**

1. If it isnt already, open this README.md in VS Code and make sure that it has focus. (click this text in the VS Code editor if the document has lost focus).
   
2.  You can open a new tab in PREVIEW MODE by hitting control-shift-V. This will open the preview in a new tab. You can then switch back and forth using the tabs. 
   
   ![](screenshots/2-control-shift-v.png)
   

   **OPENING A SPLIT SCREEN**

3. Open a Split screen in order to view both at the same time by clicking on this icon 
    ![Open Split Screen](screenshots/open-split-screen.png)

4. Drag the tab to the other window.
    ![Open In Preview](screenshots/dragtabs.png)

    You should now see the two files at the same time. With both Edit mode and Preview mode open in split panes, notice that if you scroll in one, the other scrolls as well.

    Remember this process to split the panes, it will be helpful when you want to see two files at the same time - such as lab instructions and the file you are editing.

    **VERTICAL MENU BUTTONS TOGGLE**

5. Give yourself more room to view code by hiding the leftmost pane. It should currently be the Explorer pane. Clicking the Explorer pane icon - pictured here with a blue circle and 1 will toggle this view. All of the icons in this vertical menu can be toggled to give you more room to work. Practice clicking to show and hide the menus.

    ![Vertical Pane](screenshots/vertical-pane.png)


    **MARKDOWN FORMATTING**

7. Make sure you can see both the Edit Mode in VS Code and the Preview Mode in VS Code or GitHub while you review the following:

    * Hash marks (#), are used for formatting headings.
        * A single # is heading "level 1" which is biggest, ## is "level 2", slightly smaller, and so on.
    * The asterisk is used to make a bullet.
        * Tabs are used for indentation of bullets.
    * Text can be highlighted using `backticks` around key words.
    * Code can be made **bold** using double asterisks.
    * Every item can be numbered as 1 in Edit Mode. When the markdown file is rendered: in preview mode or in browsers - the numbers will increment correctly.
        * This makes it easy to insert new items or re-order items, without needing to take the time to renumber.

    **OPEN PREVIEW TO SIDE**

8. Close all tabs in VS Code so that only the README.md is open in Edit Mode.
   
9.  When a markdown file is the active file, there is a button that automatically opens Preview in the split pane.
![Preview button](screenshots/preview-button.png)

        Most everything in VS Code has a hover effect. If you forget what anything does, just hover over it.

    **OPENING FROM EXPLORER**
1. In VS Code, from the Explorer Pane, you can find the markdown file of interest, right click and choose **Open Preview**. Try this now with this README.md as shown.
![Open In Preview](screenshots/open-preview.png)

1. In VS Code, while viewing in Preview mode, if you double-click an area of the file, you will be taken back to the EDIT VIEW or "source" markdown file for editing.

    Notice that if you double click the  image shown above - it takes you to the edit mode version where the image is linked.

2.  For the rest of this lab exercise, view this file in Preview mode or on GitHub. 

### **Part 4 - The Angular100-Labs project**
[back to top](#links-to-content-below)

1. Make sure you have VS Code open and can see the Angular100-Labs repository. Ensure the Explorer pane is visible, listing the files/directories. Recall to click the icon if the view is hidden. 

![](screenshots/3-angular100-labs-layout.png)


2. Understanding the Angular100-Labs repository
    * This repository contains the markdown files which are the instructions for the labs in this course. It is organized by chapter.  
    * There is a z-cheatsheets folder which contains help for VS Code, HTML, CSS       
    * Practice Bonus problems are available if you complete the regular exercises before others

1. There is no reason to make changes to these files, unless you wish to experiement with them. If you do make and save changes to any of these files, the VS Code source control icon (The Y looking icon in the vertical menu strip) will display a number for each file changed. 
   
    This prevents you from pulling additional bonus materials that may be added during the course.

    You can revert back to the original files by clicking this source control icon, hovering over the CHANGES menu and discarding all of the changes.

    ![](screenshots/discard-changes-ng.png)


## Bonus
[back to top](#links-to-content-below)

1. If done before others, explore the VS Code Interactive Playground
   
![](screenshots/interactive-playground.png)
