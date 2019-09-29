These instructions will help you to setup a remote repository in GitHub that you can push your code to.

### **Part 1 - Add a remote link from your local repo to GitHub**

1. Navigate to https://GitHub.com/ and sign into an existing account of yours or sign up for a new account.

2. After logging into GitHub, create a new GitHub repository called `MyWebCourse` by clicking Repositories in the menu and the green new button.

    ![New Repo](screenshots/repositories-new.png)


3. In the menu that appears, choose private and skip the steps to initialize with a readme.
    ![New Repo Wizard](screenshots/new-repo-wizard.png)

    Leave the checkbox for `Initialize this repository with a README` unchecked and click the green button to `Create Repository`

4. You will be given instructions for the remote repo. You only need the last two lines. Yours will be slightly different than what is shown because it will be for your repo. Copy these lines and paste them into the command prompt in your MyWebCourse directory.
![](screenshots/git-add-origin.png)

![](screenshots/git-add-remote.png)

### **Part 2 PUSHING CHANGES TO GITHUB**

    Now you can push your repo to GitHub. The changes you have committed locally will appear in GitHub.
   
    On projects with others involved, always PULL before you PUSH. 
    
1. Click on the `...` button found on top of VS Code's source control panel and choose **Push**.
   ![](screenshots/source-control-dots.png)

   ![](screenshots/source-control-push.png)


2.  VS Code will prompt you to enter your GitHub credentials to push the changes, please do so now. If you navigate to GitHub, you should see the README.md is updated with your changes.

3. To push commited changes, you can also click on the `Synchronize Changes` button found in blue on the bottom left of VS Code. This button will pull changes and then push commits made to the current branch we are on.    ![](screenshots/source-control-sync-button.png)

4.  VS Code will continue to ask for your GitHub username and password every time it talks to GitHub. You can use a credential helper shown in the Windows example below:

    On Windows, running the following in the command line will store your credentials:

    ```
    $ git config --global credential.helper manager
    ```
