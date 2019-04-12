# Chapter 10 Forms: Reactive form - login

## Objectives

- Create a login form
- Update Display when user is logged in

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the solution files from the last exercise.

2) In **app.module.ts** in the @NgModule decorator of core to import **ReactiveFormsModule** to be able to create a template driven form. Make sure to import the module.

3) Create a component for logging in.

```command
  ng g c LoginComponent -it -is
```

4. Add method to get individual album by 'id'

   ```typescript
   getAlbumById(id: number): Observable<Album> {
     return this.http.get<Album>(this.url + "/" + id);
   }
   ```

5. Update route to accept id param

   ```typescript
   { path: "details/:id", component: AlbumDetailsComponent }
   ```

6. Update album-card html:

   - Add id as parameter in routerLink

   ```typescript
   { path: "details/:id", component: AlbumDetailsComponent }
   ```

7. Update **album details component**:

   - Add router and service dependencies
   - Add method to use parameter and get album
   - Add html to display album details on page
