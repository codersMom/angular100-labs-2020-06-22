in the app.component.html file
refer to the three albums by using
albumsArray[0]
albumsArray[1]
albumsArray[2]

and accessing the properties

for each album use this bootstrap styling and structure
(do it based on the React album project, hard code three of them - then copy the code into here that they shoudl use. or i can copy later )

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
