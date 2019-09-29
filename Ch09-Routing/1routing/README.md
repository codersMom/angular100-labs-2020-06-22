# Chapter 9 Routing: Lab 1 Add Routing to your application

## Objectives

- Use Routing in your application
- Add the use of the bootstrap javascript file for navbar functionality

## Overview

You will create two new components: Welcome and About. You will setup routing so that both of these views are reachable. If anyone goes to the main page they will be routed to Welcome. Finally you will update the nav bar so that clicking on the links will load up the correct "pages"

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the last solution's src directory over your src directory.

1. We are going to use Bootstrap to style the navbar and make it be responsive, which requires **bootstrap.min.js**, **jquery** and **popper**. We have already installed Bootstrap, so **bootstrap.min.js** is available, but we need to install jquery and popper.

   ```bat
    npm i popper.js jquery -S
   ```

1. Update **angular.json** in order to refer to the .js files. Find the **scripts** property and add these items to the array:

   ```javascript
    "scripts": [
        "node_modules/jquery/dist/jquery.min.js",
        "node_modules/popper.js/dist/umd/popper.min.js",
        "node_modules/bootstrap/dist/js/bootstrap.min.js"
      ]
   ```

1. Because **angular.json** was updated you need to restart the server for changes to be picked up. Do that now by stopping and restarting the server.

1. Let's create the **Welcome** "page" for our application. Use the -is flag to make the component have inline styling. (alternatively you could use --inline-style)

   ```bat
   ng g c welcome -is
   ```

1. Modify the **welcome.component.html** template to display the following:

   ```html
      <div class="container">
        <div class="jumbotron my-5 mx-5 ">
          <h1 class="display-4">Welcome to {{ title }}!</h1>
          <p class="lead">The course project to practice Angular</p>
          <button
              type="button"
              routerLink="/albums"
              class="btn btn-primary text-center mt-3 mx-auto"
            >
              View Albums
            </button>
        </div>
      </div>
   ```

1. Create the title property within **welcome.component.ts** and set it equal to **My Angular Albums**.

1. We cannot reach this component yet.

1. Update **app.component.html** to simply be:

   ```html
       <router-outlet></router-outlet>
   ```

1. Now we will add paths to be loaded beneath the `<router-outlet>` element.

   Add 3 object elements to the Routes array in **app-routing.module.ts**:

   ```typescript
   const routes: Routes = [
     { path: "", redirectTo: "/welcome", pathMatch: "full" },
     { path: "welcome", component: WelcomeComponent },
     { path: "albums", component: AlbumListComponent }
   ];
   ```

1. Import the **WelcomeComponent** and **AlbumListComponent**.

   Remember that the convention is to have all @angular imports first, then a blank line, then all of the files we create and modify.

1. Open the browser for testing. Load the following URL and you should see the Welcome page.

    ```http://localhost:3333/```
  
1. Manually type in the following URL and you should see the albums. If not fix your errors.

    ```http://localhost:3333/albums```

1. Let's create a navbar component to click links to change page views.

    ```bat
    ng g c navbar -is
    ```

1. Update **app.component.html** to simply be:

     ```html
        <app-navbar></app-navbar>
        <router-outlet></router-outlet>
     ```

1. In **navbar.component.ts** create this title property

    ```typescript
     title: string = "My Albums Project";
    ```

1. Use this content for the new **navbar.component.html**. Note the use of **routerLink**

    ```html
    <nav class="navbar navbar-expand-lg navbar-light bg-light">

      <a class="navbar-brand" href="#">Angular100-Demos</a>

      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav"
        aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNav">
        <div class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" [routerLink]="['/welcome']" routerLinkActive="router-link-active">Home</a></li>
          <li class="nav-item">
            <a class="nav-link" [routerLink]="['/albums']" routerLinkActive="router-link-active">View Albums</a></li>
          <li class="nav-item"><a class="nav-link" [routerLink]="['/about']"
            routerLinkActive="router-link-active">About</a></li>
        </div>
      </div>
    </nav>
    ```

1. Copy the image **album.gif** from this README.md folder into your projects assets folder for its use in the navbar.

1. Test your changes in the browser and ensure you have no errors. You should see the navbar with image. If you click the links they should work. Clicking the nav brand "My Albums Project" should bring back the album page.

4. Modify the **About** template to use a button to routerLink to albums.

    ```html
    <div class="jumbotron text-center">
      <h1 class="display-4">Welcome to {{ title }}!</h1>
      <button
        type="button"
        routerLink="/albums"
        class="btn btn-primary text-center mt-3 mx-auto"
      >
        View Albums
      </button>
    </div>
    ```

5. Try adding a non-existing URL in the browser bar such as the following and view the browser devtools console to see the error generated.

    ```http://localhost:3333/abc```

6. Generate a new component to be used for any bad urls.

    ```bat
    ng g c Notfound -it -is
    ```

7. Update the **Notfound** template to have this content

    ```html
    <h1>Error 404</h1>
    <p>Page not found</p>
    ```

8. Update routes to add a wildcard path with asterix. This must go at the end of your path objects. It will be the match if no other url matches.

    ```typescript
      const routes: Routes = [
        { path: "", redirectTo: "/about", pathMatch: "full" },
        { path: "about", component: AboutComponent },
        { path: "albums", component: AlbumListComponent },
        { path: "**", component: NotfoundComponent, pathMatch: "full" }
      ];
    ```

    Make sure to import **NotfoundComponent**

9. Try adding a non-existing URL in the browser bar such as:

    ```http://localhost:xxxx/abc```

10. This should now load the 404 Error page and still include the nav bar.

11. Mark your work as complete.
