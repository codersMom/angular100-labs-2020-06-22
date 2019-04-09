Create a component for album details

```console
$ ng g component albums/album-details
```

Add Nav/Update app.component.html:

- Remove Jumbtron -> Add Navbar
- Remove app-album-list tags

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" routerLink="/">{{ title }}</a>
  <div class="navbar-nav">
    <a class="nav-item nav-link" routerLink="/albums" routerLinkActive="active"
      >Home</a
    >
  </div>
</nav>
```

Update Routes (app-routing.module.ts):

```typescript
const routes: Routes = [
  { path: "", redirectTo: "/albums", pathMatch: "full" },
  { path: "albums", component: AlbumListComponent },
  { path: "details", component: AlbumDetailsComponent }
];
```

Update album-card.component.html:

- Remove click directive -> add router link

```html
<button class="btn btn-primary float-right" routerLink="/details">
  See Details
</button>
```

Results:

- Page will navigate to album-details component when "See Details" button is clicked on the cards
- Page will navigate to /albums when clicking Home or app name in nav

this.route.params snippet
gives pipe and tap
