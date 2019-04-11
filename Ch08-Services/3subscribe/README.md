# Chapter 8 Services: 3 Using subscribe

## Objectives

- Instead of async pipe now use subscribe to get the data

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

2. In the **AlbumListComponent** change the data type of the albums from **albums: Observable<Album[]>**; back to an Album[].

   ```javascript
        albums: Album[];
   ```

3. Change the method that calls the service to subscribe to the call. Notice the first argument is the function to be called is the cal is a success aka "happy path", the second function is is there are errors.

   ```javascript
   getAlbums() {
       this.albumService.getAlbums()
       .subscribe(
           albums => this.albums = albums,
           error => console.log("Error: ", error));
   }
   ```

4. In the **album-list.component.html** remove the use of the async pipe

   ```html
   <app-album-card *ngFor="let album of albums | async"
   ```

5. Check that your app is working, and mark your work as complete.
