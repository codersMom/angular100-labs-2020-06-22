# Chapter 10 Forms: Template Driven - Edit Album

## Objectives

- Use template form to edit an album

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the src directory from the solution files from the last exercise.

2. Follow the steps, noting that you can copy the content from included files in the lab. Either by navigating to this folder on GitHub (right-click to open in new tab) and click on the file to get content, or from a local angular100-labs folder.

    Online folder of files:
    https://github.com/JudyLipinski/angular100-labs/tree/master/Ch10-Forms/1template
   
3. Modify the AlbumService to include the use of HttpClient's put. We will use this to save the data changes. You can copy the content from **code-for-album-service.txt**

    ![](../screenshots/1-new-album-servce-methods.png)


6. Modify your **album-details.component.html** file so that you pass the album as a query parameter to the Edit component. This is possible through the following notation - passing an object with the property **albumToEdit** and the value is the object as a JSON string using the pipe operator.

     ![](../screenshots/1-pass-query-params.png)


7. From the same directory as this README - copy the file content for album-edit component and html to replace yours.
   ![](../screenshots/1-copy-edit-files.png)

8. In VS Code editor, view the contents of the **album-edit.component.ts** file - noting the following:
   *  What is dependency injected into the constructor, and why?
   *  note the use of queryParamMap in ngOnInit() to get access to the query param that was sent
   *  we only are sending one so we get that string and parse it to get back to the object
   *  editAlbum will be called passing the album object that is modified in the form

9.  In VS Code editor, view the contents of the **album-edit.component.html** file - noting the following:
   * how is the template variable #form used to describe form state?
   * where is two way data binding being used?
   * what happens when the form is submitted? 

10. Try to load the new content for the edit page. You should be able to click on the details page button, but get an error in the console. Can you make out what it means?

11. You need to import the **FormsModule** into your Albums feature module just as you did the CommonModule to make the directives for forms available.
   
   Note: Providers made available at root are available to features because of the way injectors work. Modules which give us access to directives such as FormsModule or CommonModule must be imported into the feature modules where you need them.

  ![](../screenshots/1-add-import-to-feature-import.png)

12. Make sure you also import the FormsModule so that your code compiles. When changing modules, it can be good to start and restart your server as modules may have already been loaded into memory.
   
13. Now try reaching the Edit page. 

14. Notice the state of the form as reflected in the pills. Remove the name of the artist and see the state change. Can you see which code is causing this?
    
16. Notice the button cannot be submitted until the form is valid.

15. Now change the name of the artist and hit submit.

16. You should be routed to the list of albums and see your changes as well as in the json file that json-server is using.

## Bonus

1.  Create a button to add an album which calls a new service in album using http.put
   
2.  Create a remove button on the details page that when clicked calls a method you create which uses a service to delete the item.
