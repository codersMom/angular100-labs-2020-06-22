# Chapter 5 Directives: styling methods

## Objectives

- Use ngStyle to conditional set a style on albums

## Steps

1. Open the album-card.component.html file and find the div with class="card"

    ```html
    <div class="card"></div>
    ```

1. Modify this element to have a style applied if the album is on sale.

   ```html
   <div
     class="card"
     [ngStyle]="{ 'background-color': album.onSale ? 'green' : '' }"
   >
     
   </div>
   ```

1. Mark your work as complete.
