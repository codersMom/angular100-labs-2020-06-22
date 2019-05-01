# Chapter 5 Directives: ngFor

## Objectives

- Copy more data into the project and use ngFor to display all albums

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

1. In this folder's README there is a file called **albums.data.ts**. Open and examine this file and copy it to your project's app/albums folder. (src/app/albums)

1. Replace the content of **album.model.ts** with the following to add in the Album properties that were not present before, and to add in Track.

   ```javascript
   export interface Album {
     id: number;
     artist: string;
     album_name: string;
     genre: string;
     price: number;
     currency?: string;
     on_sale: boolean;
     year: number;
     release_date: string;
     recording_location: string;
     duration: string;
     url: string;
     tracks: Track[];
   }

   export interface Track {
     id: number;
     track_number: number;
     title: string;
     length: string;
   }
   ```

1. Now, in **album-list.component.ts** - import this JSON file using an import.

   ```javascript
   import { ALBUMS } from "../albums.data";
   ```

1. Modify **album-list.component.ts** so that the ngOnInit() is simply:

   ```javascript
   ngOnInit(): void {
    this.albumsArray = this.albumsArray = ALBUMS;
   }
   ```

1. In **album-list.component.html**, modify the inclusion of the three cards, to be a single card reference that uses an \*ngFor:

   ```html
   <app-album-card
     *ngFor="let album of albumsArray"
     [album]="album"
     (albumClicked)="parentFunctionHandler($event)"
   ></app-album-card>
   ```

    Make sure to keep the above still contained in the following two <divs>

    ```html
    <div class="container">
      <div class="card-deck">
    ```

1. Now in the browser you should now see all of the albums. Now that we have more data - resize the browser to see the responsiveness from using Bootstrap. Can you point out what part of your code is has Bootsrtap implement this functionality?

1. Once this is working, mark your work as complete.
