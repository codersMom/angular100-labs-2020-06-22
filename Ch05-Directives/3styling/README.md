# Chapter 5 Directives: styling methods

## Objectives

- Use ngStyle to conditional set a style on albums

## Steps

1. Open the album-card.component.html file and find the

```html
<div class="card"></div>
```

<div
  class="card">
  [ngStyle]="{ 'background-color': album.on_sale ? 'green' : '' }"
>
1. Add the use of
   ```html
   <app-album-card
     *ngFor="let album of albums"
     [album]="album"
     (albumClicked)="getSelectedAlbum($event)"
     [ngStyle]="{'background-color': album.on_sale ? 'green' : ''}"
   >
   </app-album-card>
   ```
2. Create an event that when
