# Chapter 4 Passing Data: Add more components

## Objectives

- Overview in this lab, you will practice creating a hierarchy of components

## Steps

1. Create AlbumList
   ng g c albums/album-list --flat

1. Examine the updates made to the app.module class decorator. Use the git tool if need be to see the changes.

1. Move working with array code from app.component to the newly generated component class.

1. In app.component.html refer to the new albumlist selector.

1. Create AlbumCard
   ng g c albums/album-card --flat

1. In album list hard-code 3 album cards

```html
<app-album-card></app-album-card>
<app-album-card></app-album-card>
<app-album-card></app-album-card>
```

1. In album card just have the structure used by cards
   can copy array[0] data to the card component ts file

1. Have a property called albumData. Use this in album card html to display data.

1. In later section we will pass the data to the card so each will be unique.
