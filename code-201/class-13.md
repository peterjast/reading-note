# **The Past, Present & Future of Local Storage for Web Applications**

* Native client applications have the advantage when it comes to persistent local storage

* Cookies can be used for persistent local storage of small amounts of data

## The Downsides of Cookies

* Cookies slow down your web application

* Cookies send unencrypted data over the internet

* Cookies are limited to 4KB of data

* Ideally, we want to be able to store lots of data on the client and have it persist beyond page refresh and not be transmitted to the server

## HTML5 Storage

* web storage, local storage, DOM storage

* store key/value pairs locally within the client web browser

* data persists but is never transmitted to remote web server

* Most recent versions of browsers support HTML5 storage

### Checking for HTML5 Storage

> function supports_html5_storage() {
>
> try {
>
> return 'localStorage' in window && window['localStorage'] !== null;
>
> } catch (e) {
>
>     return false;
>
> }
>
> }

#### Using Modernizr

> if (Modernizr.localstorage) {
>
> // window.localStorage is available!
>
> } else {
>
> // no native support for HTML5 storage :(

### Using HTML5 Storage

* Stored in named key/value pairs

* Data is stored as strings

* Use functions like parseInt() or parseFloat() to coerce retrieved data

> interface Storage {
>
> getter any getItem(in DOMString key);
>
> setter creator void setItem(in DOMString key, in any data);
>
> };

* Calling setItem() will overwrite pervious value if it already exists

* Calling getItem() will return null if doesn't exist

* You can treat localStorage object as an associateive array

> var foo = localStorage.getItem("bar");
>
> // ...
>
> localStorage.setItem("bar", foo);

#### Square Bracket Syntax

> var foo = localStorage["bar"];
>
> // ...
>
> localStorage["bar"] = foo;

#### removing values

> interface Storage {
>
> deleter void removeItem(in DOMString key);
>
> void clear();
>
> };

#### Get Total Amount of Values Stored

> interface Storage {
>
> readonly attribute unsigned long length;
>
> getter DOMString key(in unsigned long index);
>
> };

### Tracking Changes

* Event is fired on the window object whenever setItem(), removeItem() or clear() is called and a change is made

* You can track these changes by adding an event listener to the window

> if (window.addEventListener) {
>
> window.addEventListener("storage", handle_storage, false);
>
> } else {
>
> window.attachEvent("onstorage", handle_storage);
>
> };

* callback function will be called with StorageEvent object

> function handle_storage(e) {
>
> if (!e) { e = window.event; }
>
> }

### Limitiations

* Each origin gets 5 megabytes by default

* "QUOTA_EXCEEDED_ERR" exception thrown if you exceed storage quota

### HTML5 Storage In Action

> function saveGameState() {
>
> if (!supportsLocalStorage()) { return false; }
>
> localStorage["halma.game.in.progress"] = gGameInProgress;
>
> for (var i = 0; i < kNumPieces; i++) {
>
> localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
>
> localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
>
> }
>
> localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
>
> localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
>
> localStorage["halma.movecount"] = gMoveCount;
>
> return true;
>
> }
>
> function resumeGame() {
>
> if (!supportsLocalStorage()) { return false; }
>
> gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
>
> if (!gGameInProgress) { return false; }
>
> gPieces = new Array(kNumPieces);
>
> for (var i = 0; i < kNumPieces; i++) {
>
> var row = parseInt(localStorage["halma.piece." + i + ".row"]);
>
> var column = parseInt(localStorage["halma.piece." + i + ".column"]);
>
> gPieces[i] = new Cell(row, column);
>
> }
>
> gNumPieces = kNumPieces;
>
> gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
>
> gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
>
> gMoveCount = parseInt(localStorage["halma.movecount"]);
>
> drawBoard();
>
> return true;
>
> }

*All code snippets are from the following article. Please refer to this article for more information and additional resources*

[http://diveinto.html5doctor.com/storage.html](http://diveinto.html5doctor.com/storage.html)

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)
