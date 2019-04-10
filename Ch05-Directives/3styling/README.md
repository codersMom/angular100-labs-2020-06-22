# Chapter 5 Directives: styling methods

## Objectives

- Use different methods to affect formatting data

## Steps

1. Make it so that when an album is clicked it sends up an event to list - and changes the array
   for the album to toggle a property selected - from true to false.

1. Data doesn't have selected - so might need to update the data.

1. Write logic that if it is null or false to set to true,

1. Update album-card.component.html
   <app-album-card \*ngFor="let album of albums"
   [album]="album" (albumClicked)="getSelectedAlbum(\$event)"
   [album]="album" [ngStyle]="{'background-color': album.on_sale ? 'green' : ''}"
   [ngClass]="{ 'text-success bg-success': album == selectedAlbum }">
   </app-album-card>

1. Create an event that when
