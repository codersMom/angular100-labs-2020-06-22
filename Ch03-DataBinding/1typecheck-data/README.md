# Chapter 3: Add data that is type checked to the project

## Objectives

- Add data to the project
- Define an interface to indicate the type of the data

## Steps

1.  You may have already started seeing messages from TSLint about quotes single versus double. In tslint.json add this entry to ignore quotes: "quotemark": false

2.  Another helpful extension is prettier. If not already installed install it. Create a file with the name **.prettierrc**
    in the root of your directory. Use JSON formatting to add these rules:

    ```javascript
    {
        "trailingComma": "es5",
        "tabWidth": 4,
        "semi": true,
        "singleQuote": true
    }
    ```

3.  Data is added VIA the **XXX.component.ts** type files. We will start by modifying the file **app.component.ts**. Open this file and after the line with **title = "My Angular Albums";**
    and a property called

    ```javascript
    albumsArray: any;
    ```

    The use of any indicates that albumsArray can be of any type. We are using it not to demonstrate that there are no restrictions with any.

4.  Modify the line with the class export to include implements OnInit like this:

    ```javascript
    export class AppComponent implements OnInit {
    ```

5.  We will be exploring this in more detail, it indicates that you intend to implement a method called **ngOnInit()** which is defined in the OnInit interface. This method is called when the component is loaded by Angular.

6.  You must import **OnInit**. If you have extensions installed this may have already been done for you - if not, modify the top of **app.component.ts** which imports from Angular core to look like this:

    ```javascript
    import { Component, OnInit } from "@angular/core";
    ```

7.  You may see errors that you need to now implement OnInit. Do this by adding this function in the class after the property definitions - but before the closing brace } for the class.

    ```javascript
    ngOnInit(): void {    }
    ```

8.  Inside of this function is where you should initialize the **albumsArray** property you created. For now you can hard-code 3 items from an array such as shown next. In the future we will get these from a server.

    ```javascript
    ngOnInit(): void {
    this.albumsArray = [
      {
        id: "1",
        artist: "Tremonti",
        album_name: "Dust",
        on_sale: "true",
        price: 11.99,
        currency: "USD",
        year: 2016,
        release_date: "April 29, 2016",
        "recording_location": "Studio Barbarosa, Orlando, FL",
        genre: "Pop/Rock",
        duration: "43:18:00",
        URL: "https://www.allmusic.com/album/dust-mw0002918360"
      },
      {
        id: 2,
        artist: "Bon Jovi",
        album_name: "7800 Fahrerenheit",
        on_sale: false,
        price: 7,
        year: 1985,
        currency: "USD",
        release_date: "April 20, 1985",
        "recording_location": "Warehouse, Philadelphia, PA",
        genre: "Pop/Rock",
        duration: "47:15:00",
        URL: "https://www.allmusic.com/album/7800%C2%B0-fahrenheit-mw0000189199"
      },
      {
        id: 3,
        artist: "The Beatles",
        album_name: "The White Album",
        on_sale: true,
        currency: "GBP",
        price: 24,
        year: 1968,
        release_date: "November 22, 1968",
        "recording_location": "",
        genre: "Pop/Rock",
        duration: "1:33:43",
        URL:
          "https://www.allmusic.com/album/the-beatles-white-album-mw0000418113"
      }
    ];
    ```

9.  In the **ngOnInit()** use a console.log to print the data `console.log(this.albumsArray);` and make sure it displays in the console of the browser.

10. You may notice that there are some purposeful issues with this array data. The first item has id as a string value and the other as a number. Lets define an interface to do type checking against this data.

11. Open a terminal in VSCode for the project, and use Angular CLI to create a model file for an **album** within a folder called **albums** using this:

```
ng g interface albums\album --type=model
```

12. Notice the creation of the directory albums and the naming of the file **album.model.ts** the type fag was used to name the file with the type. Look inside this file and notice it is rather bare bones but exports an interface.

13. Complete the interface so that it looks like this:

```javascript
export interface Album {
  id: number;
  artist: string;
  album_name: string;
  genre: string;
  price: number;
  currency: string;
  on_sale: boolean;
  year: number;
  release_date: string;
  recording_location: string;
  duration: string;
  url: string;
}
```

14. In **app.component.ts**, import the type Album

```javascript
import { Album } from "./albums/album.model";
```

15. Now make the property of albumsArray be of type Album[]

```javascript
albumsArray: Album[];
```

16. You should now get errors about the data not quite matching up. Fix the hard-coded array items to update the id and on_sale. For currency and tracks, data may not exists so add a question mark so data looks something like this:

```javascript
export interface Album {
 id: number;
 artist: string;
 album_name: string;
 genre: string;
 price: number;
 currency?: string;
```

17. Make the necessary changes so the code compiles and runs in the browser.
