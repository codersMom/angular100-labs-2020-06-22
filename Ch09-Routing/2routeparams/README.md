# Chapter 9 Routing: Work with Route parameters

## Objectives

- Start a server and use HttpClient and asyncPipe to display it in the browser

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.
   Update AlbumService:

   5. Create a component for album details

   ```console
   $ ng g component albums/album-details
   ```

16) Update the button on the card in **album-card.component.html**:

- Remove (click) directive -> add the use of **routerLink**

```html
<button class="btn btn-primary float-right" routerLink="/details">
  See Details
</button>
```

1. Add method to get individual album by 'id'

   ```typescript
   getAlbumById(id: number): Observable<Album> {
     return this.http.get<Album>(this.url + "/" + id);
   }
   ```

1. Update route to accept id param

   ```typescript
   { path: "details/:id", component: AlbumDetailsComponent }
   ```

1. Update album-card html:

   - Add id as parameter in routerLink

   ```typescript
   { path: "details/:id", component: AlbumDetailsComponent }
   ```

1. Update **album details component**:

   - Add router and service dependencies
   - Add method to use parameter and get album
   - Add html to display album details on page
