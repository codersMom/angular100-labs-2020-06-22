# Chapter 4 Passing Data: Add more components

## Objectives

- Overview in this lab, you will practice creating a hierarchy of components, moving HTML template from AppComponent

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

2. Open the integrated terminal. Create an **AlbumListComponent** by using this Angular CLI command. Note that g is short for generate, c is for component.

   ```
   ng g c albums/album-list --flat
   ```

   Here we are specifying to create album-list inside of a directory called albums. The --flat indicates to start at the root directory. If the command given was **ng g c some-name** there would be a directory created called **some-name** and inside would be the **some-name** component files.

3. Examine the updates made to the **app.module** class decorator. You can see the changes easily if you click on the Y shaped Source Control icon in VSCode and click the changed **app.module.ts** file.

4. From the **app.component.html** file, move the entire element that starts with `<div class="container">` to the new **album-list.component.html** file.

5. You may notice an error because of the need for albumsArray to be in the **album-list.component.ts** file. In that file, include the declaration of **albumsArray** in the class:

   ```javascript
   albumsArray: Album[];
   ```

6. To make this compile you must import Album into the AlbumListComponent file.

   ```javascript
   import { Album } from "../album.model";
   ```

7. Move the **ngOnInit()** from app.component.ts into the album-list.component.ts file.

8. Update **app.component.html** so that it only has this code:

   ```html
   <div style="text-align:center;">
     <h1 class="jumbotron my-5 mx-5">Welcome to {{ title }}!</h1>
   </div>

   <app-album-list></app-album-list>

   <router-outlet></router-outlet>
   ```

   Note the reference to the selector of AlbumListComponent.

9. Mark your work as complete.
