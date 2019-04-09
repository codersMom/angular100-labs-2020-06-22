Update AlbumService:
- Add method to get individual album by 'id'

```typescript
getAlbumById(id: number): Observable<Album> {
  return this.http.get<Album>(this.url + "/" + id);
}
```

Update route to accept id param

```typescript
{ path: "details/:id", component: AlbumDetailsComponent }
```

Update album-card html:
- Add id as parameter in routerLink

Update album details component:
- Add router and service dependencies
- Add method to use parameter and get album
- Add html to display album details on page
