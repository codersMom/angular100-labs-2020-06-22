# Chapter 8 Services: 3 Using subscribe

## Objectives

- Instead of async pipe now use subscribe to get the data

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

1. In the **AlbumListComponent** change the data type of the albums from **albums: Observable<Album[]>** back to a **Album[]**

        ```typescript
        albumsArray: Album[];
        ```

   It's good to remove any imports not in use, such as Observable from rxjs.

1. Change the method that calls the service to subscribe to the call. Notice the first argument of .subscribe( is to be called on success aka "happy path" and the second fuction will be called if there are any errors.

   ```typescript
   getAlbums() {
       this.albumService.getAlbums()
       .subscribe(
           albums => this.albumsArray = albums,
           error => console.log("Error: ", error));
   }
   ```

1. In the **album-list.component.html** remove the use of the async pipe

   ```html
   <app-album-card 
        *ngFor="let album of albums"
   ```

1. Check that your app is working, and mark your work as complete.
