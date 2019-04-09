# Chapter 8 Services: Use a service to return data for use in component

## Objectives

- Define a service, which returns hard-coded data
- Use dependency injection to inject service to component
- Call the service to get the data

## Steps

1. Generate a service which returns albums

```
ng g s albums/shared/album
```

1. update album list component to be dependency injected via the constructor.

   1. import the service
   2. Add it as an argument to the constructor

2. In ngOnInit() call the service using this.service.getAlbums() and set it to your albumArray property

3. Check that your code still works
