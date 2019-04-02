Create AlbumList
ng g c albums/album-list --flat

Move workign wit array code from appcomponent to there

In appcomponent refer to albumlist

Create AlbumCard
ng g c albums/album-card --flat

in album list hard-code 3 album cards
<app-album-card></app-album-card>
<app-album-card></app-album-card>
<app-album-card></app-album-card>

in album card just have teh structure used by cards
can copy array[0] data to the card component ts file

have in a property called albumData
hard-code for now,

get t to work and shoud see 3 cards but all fo the same data

in later section we will pass the data to the card
