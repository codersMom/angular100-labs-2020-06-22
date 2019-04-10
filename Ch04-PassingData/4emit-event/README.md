# Chapter 4 Passing Data: Emit Event

## Objectives

- Respond to a click event of a button by raising an alert to PARENT component

## Steps

1. In **album-card.component.ts** create a member variable which is an EventEmitter.

   ```javascript
    @Output()
    albumClicked: EventEmitter<Album> = new EventEmitter<Album>();
   ```

2. Modify the showAlbum function to be:

   ```javascript
    showAlbum() {
        this.albumClicked.emit(this.album);
    }
   ```

3. In **album-list.component.html**, modify the child components to look like this - which indicate the parent wants to listen for albumClicked events, and when they occur to call parentFunctionHandler

   ```html
   <app-album-card
     [album]="albums[0]"
     (albumClicked)="parentFunctionHandler($event)"
   ></app-album-card>
   <app-album-card
     [album]="albums[1]"
     (albumClicked)="parentFunctionHandler($event)"
   ></app-album-card>
   <app-album-card
     [album]="albums[2]"
     (albumClicked)="parentFunctionHandler($event)"
   ></app-album-card>
   ```

4. In **album-list.component.ts**, add the parentFunctionHandler function

   ```javascript
   parentFunctionHandler(album) {
       alert('Album ' + album.album_name + ' was sent from the album card component');
   }
   ```

5. Now in the browser when you click - an alert should be raised with the message from the parent.

6. Once this is working, mark your work as complete.

## Bonus

1. After the jumbotron, display on the screen the id and name of the last clicked album.
