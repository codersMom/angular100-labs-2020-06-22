# Chapter 4 Passing @Input to child components

## Objectives

- Overview in this lab, you will practice passing data to child components

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

2. Open the integrated terminal. Create an **AlbumCardComponent** by using this Angular CLI command. Note that g is short for generate, c is for component.

   ```
   ng g c albums/album-card
   ```

3. Find the first element (with all of its child elements) in **album-list.component.html** that has

   ```html
   <div class="card"></div>
   ```

4. Move this code (about 16 lines) to the newly created **album-card.component.html** file replacing its placeholder content.

5. Search and replace in **album-card.component.html** the **albumsArray[0]** references to be instead **albumInfo**.

6. Now declare a member variable in **album-card.component.ts** to be

   ```javascript
    @Input()
    albumInfo: Album;
   ```

7. In **album-list.component.html** update it to look like this:

   ```html

   ```

8. In **album-card.component.css** add a rule that the class for card should be:

   ```css
   .card {
     width: 275px;
     height: 500px;
     margin: 5px;
   }
   ```

9. In the browser you should see the 3 different albums.

10. Mark your work as complete
