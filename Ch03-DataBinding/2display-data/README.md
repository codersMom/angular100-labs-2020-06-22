# Chapter 3 DataBinding: Display data in the template

## Objectives

- Display data to the screen using interpolation

## Steps

1. In the app.component.html file refer to each of the three albums by using
   albumsArray[0]
   albumsArray[1]
   albumsArray[2]

and accessing the properties

for each album use this bootstrap styling and structure

```html
<div class="container">
  <div class="card-deck">
    <div class="card">
      <div class="card-body text-center">
        <h4 class="card-title">{{albumsArray[0].artist}}</h4>
        <ul>
          <li>{{albumsArray[0].album_name}}</li>
          <li>{{albumsArray[0].genre}}</li>
          <li>{{albumsArray[0].price}} {{albumsArray[0].currency}}</li>
        </ul>
      </div>
    </div>
    <div class="card">
      <div class="card-body text-center">
        <h4 class="card-title">{{albumsArray[1].artist}}</h4>
        <ul>
          <li>{{albumsArray[1].album_name}}</li>
          <li>{{albumsArray[1].genre}}</li>
          <li>{{albumsArray[1].price}} {{albumsArray[1].currency}}</li>
        </ul>
      </div>
    </div>
    <div class="card">
      <div class="card-body text-center">
        <h4 class="card-title">{{albumsArray[2].artist}}</h4>
        <ul>
          <li>{{albumsArray[2].album_name}}</li>
          <li>{{albumsArray[2].genre}}</li>
          <li>{{albumsArray[2].price}} {{albumsArray[2].currency}}</li>
        </ul>
      </div>
    </div>
  </div>
</div>
```

1. Load the app you should now see three albums on the screen.
