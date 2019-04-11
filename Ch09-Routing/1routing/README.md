# Chapter 9 Routing: Work with Routing

## Objectives

- Use Routing in your application
- Add the use of the bootstrap javascrpt file for navbar functionality

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

2. Create a component for album details

   ```console
   $ ng g component albums/album-details
   ```

3. Add Nav/Update **app.component.html**:

   - Remove Jumbtron -> Add Navbar
   - Remove app-album-list tags

   ```html
   <nav class="navbar navbar-expand-lg navbar-light bg-light">
     <a class="navbar-brand" routerLink="/">{{ title }}</a>
     <div class="navbar-nav">
       <a
         class="nav-item nav-link"
         routerLink="/albums"
         routerLinkActive="active"
         >Home</a
       >
     </div>
   </nav>
   ```

4. Update **angular.json** file to reference the Bootstrap navbar

   ```javascript
    "scripts": [
              "./node_modules/bootstrap/dist/js/bootstrap.min.js"
            ]
   ```

5. Define Routes in **app-routing.module.ts**:

   ```typescript
   const routes: Routes = [
     { path: "", redirectTo: "/albums", pathMatch: "full" },
     { path: "albums", component: AlbumListComponent },
     { path: "details", component: AlbumDetailsComponent }
   ];
   ```

6. Update the button on the card in **album-card.component.html**:

   - Remove (click) directive -> add the use of **routerLink**

   ```html
   <button class="btn btn-primary float-right" routerLink="/details">
     See Details
   </button>
   ```

7. Test your changes in the browser
   - Page will navigate to album-details component when "See Details" button is clicked on the cards
   - Page will navigate to /albums when clicking Home or app name in nav
