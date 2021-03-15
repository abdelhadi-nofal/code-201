# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

## INTRODUCING HTML5 STORAGE

What I will refer to as “HTML5 Storage” is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.” The naming situation is made even more complicated by some related, similarly-named, emerging standards that I’ll discuss later in this chapter.

So what is HTML5 Storage? Simply put, it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

Which browsers? Well, the latest version of pretty much every browser supports HTML5 Storage… even Internet Explorer!

From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object. Before you can use it, you should detect whether the browser supports it.

`function supports_html5_storage() {`

  `try {`

    `return 'localStorage' in window && window['localStorage'] !== null;`

  `} catch (e) {`

    `return false;`

  `}`

`}`

Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

`if (Modernizr.localstorage) {`

  `// window.localStorage is available!`

`} else {`

  `// no native support for HTML5 storage :(`

  `// maybe try dojox.storage or a third-party solution`

`}`


## USING HTML5 STORAGE

HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

`interface Storage {`

  `getter any getItem(in DOMString key);`

  `setter creator void setItem(in DOMString key, in any data);`

`};`


Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. For example, this snippet of code:

`var foo = localStorage.getItem("bar");`

`// ...`

`localStorage.setItem("bar", foo);`

…could be rewritten to use square bracket syntax instead:

`var foo = localStorage["bar"];`

`// ...`

`localStorage["bar"] = foo;`

There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

`interface Storage {`

  `deleter void removeItem(in DOMString key);`

  `void clear();`

`};`

Calling `removeItem()` with a non-existent key will do nothing.

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

`interface Storage {`

  `readonly attribute unsigned long length;`

  `getter DOMString key(in unsigned long index);`

`};`

If you call key() with an index that is not between 0–(length-1), the function will return null.

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

`if (window.addEventListener) {`

  `window.addEventListener("storage", handle_storage, false);`

`} else {`

  `window.attachEvent("onstorage", handle_storage);`

`};`


The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

`function handle_storage(e) {`

  `if (!e) { e = window.event; }`

`}`


At this point, the variable e will be a StorageEvent object, which has the following useful properties.

The storage event is not cancelable. From within the handle_storage callback function, there is no way to stop the change from occurring. It’s simply a way for the browser to tell you, “hey, this just happened. There’s nothing you can do about it now; I just wanted to let you know.”

## LIMITATIONS IN CURRENT BROWSERS

In talking about the history of local storage hacks using third-party plugins, I made a point of mentioning the limitations of each technique, such as storage limits. I just realized that I haven’t mentioned anything about the limitations of the now-standardized HTML5 Storage. I’ll give you the answers first, then explain them. The answers, in order of importance, are “5 megabytes,” “QUOTA_EXCEEDED_ERR,” and “no.”

“5 megabytes” is how much storage space each origin gets by default. This is surprisingly consistent across browsers, although it is phrased as no more than a suggestion in the HTML5 Storage specification. One thing to keep in mind is that you’re storing strings, not data in its original format. If you’re storing a lot of integers or floats, the difference in representation can really add up. Each digit in that float is being stored as a character, not in the usual representation of a floating point number.

“QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes. “No” is the answer to the next obvious question, “Can I ask the user for more storage space?” At time of writing (February 2011), no browser supports any mechanism for web developers to request more storage space. Some browsers (like Opera) allow the user to control each site’s storage quota, but it is purely a user-initiated action, not something that you as a web developer can build into your web application.

## HTML5 STORAGE IN ACTION
Let’s see HTML5 Storage in action. Recall the Halma game we constructed in the canvas chapter. There’s a small problem with the game: if you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.

How does it work? Every time a change occurs within the game, we call this function:

`function saveGameState() {`

    `if (!supportsLocalStorage()) { return false; }`

    `localStorage["halma.game.in.progress"] = gGameInProgress;`

    `for (var i = 0; i < kNumPieces; i++) {`

	`localStorage["halma.piece." + i + ".row"] = gPieces[i].row;`

	`localStorage["halma.piece." + i + ".column"] = gPieces[i].column;`

    `}`

    `localStorage["halma.selectedpiece"] = gSelectedPieceIndex;`

    `localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;`

    `localStorage["halma.movecount"] = gMoveCount;`

    `return true;`

`}`


As you can see, it uses the localStorage object to save whether there is a game in progress (gGameInProgress, a Boolean). If so, it iterates through the pieces (gPieces, a JavaScript Array) and saves the row and column number of each piece. Then it saves some additional game state, including which piece is selected (gSelectedPieceIndex, an integer), whether the piece is in the middle of a potentially long series of hops (gSelectedPieceHasMoved, a Boolean), and the total number of moves made so far (gMoveCount, an integer).

On page load, instead of automatically calling a newGame() function that would reset these variables to hard-coded values, we call a resumeGame() function instead. Using HTML5 Storage, the resumeGame() function checks whether a state about a game-in-progress is stored locally. If so, it restores those values using the localStorage object.

`function resumeGame() {`

    `if (!supportsLocalStorage()) { return false; }`

    `gGameInProgress = (localStorage["halma.game.in.progress"] == "true");`

    `if (!gGameInProgress) { return false; }`

    `gPieces = new Array(kNumPieces);`

    `for (var i = 0; i < kNumPieces; i++) {`

	`var row = parseInt(localStorage["halma.piece." + i + ".row"]);`

	`var column = parseInt(localStorage["halma.piece." + i + ".column"]);`

	`gPieces[i] = new Cell(row, column);`

    `}`

    `gNumPieces = kNumPieces;`

    `gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);`

    `gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";`

    `gMoveCount = parseInt(localStorage["halma.movecount"]);`

    `drawBoard();`

    `return true;`

`}`

The most important part of this function is the caveat that I mentioned earlier in this chapter, which I’ll repeat here: Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. For example, the flag for whether there is a game in progress (gGameInProgress) is a Boolean. In the saveGameState() function, we just stored it and didn’t worry about the datatype:

`localStorage["halma.game.in.progress"] = gGameInProgress;`

But in the resumeGame() function, we need to treat the value we got from the local storage area as a string and manually construct the proper Boolean value ourselves:

`gGameInProgress = (localStorage["halma.game.in.progress"] == "true");`

Similarly, the number of moves is stored in gMoveCount as an integer. In the saveGameState() function, we just stored it:

localStorage["halma.movecount"] = gMoveCount;
But in the resumeGame() function, we need to coerce the value to an integer, using the parseInt() function built into JavaScript:

`gMoveCount = parseInt(localStorage["halma.movecount"]);`








