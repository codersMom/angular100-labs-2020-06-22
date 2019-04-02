create a model using ng g m album <--confirm this and put into a directory called albums
(might want to add a list of properties for them to add to the model, json data contains more complex model and missing elements)

```console
ng generate class <dir/file> [options]
foo@bar:~$ ng g class albums/album --type=model --skipTests=true
```
OR

```console
ng generate interface <dir/file> <type>
foo@bar:~$ ng g interface albums/album model
```

in appcompoennt, import he type Album
In AppComponent create a property called albumsArray
which is of type Album[]

Add an ngOnInit that contains setting of data and creation of an album.model.ts
in ngOnInit() set teh albumsArray an array of 3 albums
use data from music-info.json in this folder

price that is a decimal value
currency USD or EURO

use a console.log to print the data

in next section we will add to the screen
