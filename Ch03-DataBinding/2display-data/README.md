# Chapter 3 DataBinding: Display data in the template

## Objectives

- Display data to the screen using interpolation
- In the app.component.html file you will refer to each of the three albums by using their array index and accessing the properties - later we will use a directive.
  albumsArray[0]
  albumsArray[1]
  albumsArray[2]

## Steps

1. Create a structure for displaying a number of albums as cards.

   ```html
   <div class="container">
     <div class="card-deck">
       <div class="card"></div>
       <div class="card"></div>
       <div class="card"></div>
     </div>
   </div>
   ```

1. Inside of each div with class="card" create an img reference (3 times)

   ```html
   <img
     class="card-img-top cover"
     src=""
     alt=""
     style="border: 1px solid grey"
   />
   ```

1. Copy the img folder from this README folder into your projects **/src/assets** directory. We will use this for albums. Where the album id is 1 the image is 1.jpg.

1. For the **src** paths of each card, use backticks to set each path to the corresponding image, example:

   ```
     assets/img/{{ albumsArray[0].id }}.jpg
   ```

1. For the **alt** content for each, use Album Cover for XXX where XXX is the name of the album.

1. Immediately after the `<img>` for each card, add a card body like this, updating it for the 2nd and 3rd card:

   ```html
   <div class="card-body">
     <h4 class="card-title">{{ albumsArray[0].artist }}</h4>
     <ul style="list-style: none;">
       <li>{{ albumsArray[0].album_name }}</li>
       <li>Released: {{ albumsArray[0].year }}</li>
       <li>{{ albumsArray[0].price }} {{ albumsArray[0].currency }}</li>
     </ul>
   </div>
   ```

1. Load the app you should now see three albums on the screen.

1. Mark your work as complete. (Name tent card, electronic status, etc.)
