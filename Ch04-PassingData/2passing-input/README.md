# Chapter 4 Passing Data: Using @Input in child components

## Objectives

- Overview in this lab, you will practice passing data to child components

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

1. Open the integrated terminal. Create an **AlbumCardComponent** by using this Angular CLI command. Note that g is short for generate, c is for component.

   ```
   ng g c albums/album-card
   ```

1. Find the first element (with all of its child elements) in **album-list.component.html** that has

   ```html
   <div class="card"></div>
   ```

1. Move this code (about 16 lines) to the newly created **album-card.component.html** file replacing its placeholder content.

1. Search and replace in **album-card.component.html** the **albumsArray[0]** references to instead be **album**.

1. In **album-card.component.ts**, declare a member variable in the top of the class decleration

   ```javascript
    @Input()
    album: Album;
   ```

1. You may have a red wavy line under **@Input** and **Album**; fix these if you do.

1. In **album-list.component.html** update it to look like this:

   ```html
   <div class="container">
     <div class="card-deck">
       <app-album-card [album]="albumsArray[0]"></app-album-card>
       <app-album-card [album]="albumsArray[1]"></app-album-card>
       <app-album-card [album]="albumsArray[2]"></app-album-card>
     </div>
   </div>
   ```

1. In **album-card.component.css** add a rule that the class for card should be:

   ```css
   .card {
     width: 275px;
     height: 500px;
     margin: 5px;
   }
   ```

1. In the browser you should see the 3 different albums.

1. Mark your work as complete
