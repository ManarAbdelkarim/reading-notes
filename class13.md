# `THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS`

For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files.

## COOKIES:
![](https://yourpcfriend.com/wp-content/uploads/2019/05/cookie.gif)

Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

- Cookies are included with every HTTP request, thereby:

    -  slowing down your web application by needlessly transmitting the same data over and over

    -  sending data unencrypted over the internet (unless your entire web application is served over SSL)

- Cookies are limited to about 4 KB of data — enough to slow down your application , but not enough to be terribly useful

### GOOD LOCAL STORAGE HAS:
- a lot of storage space

- on the client
- that persists beyond a page refresh
- and isn’t transmitted to the server

## A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5:
- userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure.

- Flash 6 “Flash cookies.” it allows Flash objects to store up to 100 KB of data per domain.

-  Flash 8, accessing LSOs from JavaScript became an order of magnitude easier and faster.

- Brad rewrote AMASS and integrated it into the popular Dojo Toolkit under the moniker dojox.storage

![dojo](https://dojotoolkit.org/blog/wp-content/uploads/2011/11/dgrid1-1024x481.png)

- In 2007, Google launched Gears, an open source browser plugin aimed at providing additional capabilities in browsers.Gears provides an API to an embedded SQL database based on SQLite.

- Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox.

## INTRODUCING HTML5 STORAGE

### what is HTML5 Storage?
it’s a way for web pages to store named key/value pairs locally, within the client web browser.Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.the latest version of pretty much every browser supports HTML5 Storage… even Internet Explorer!

![](https://scriptverse.academy/img/tutorials/html5-localstorage.png)

## USING HTML5 STORAGE

- HTML5 Storage is based on named key/value pairs.

- The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. 

### setItem() & getItem() & removeItem():
- Calling setItem() with a named key that already exists will silently overwrite the previous value. 

- Calling getItem() with a non-existent key will return null rather than throw an exception.

- Calling removeItem() deletes the value,  with a non-existent key will do nothing.

## TRACKING CHANGES TO THE HTML5 STORAGE AREA
The storage event is supported everywhere the localStorage object is supported,
 
          if (window.addEventListener) {
          window.addEventListener("storage", handle_storage, false);
          } else {
          window.attachEvent("onstorage", handle_storage);
          };

### STORAGEEVENT OBJECT:

![](https://image.slidesharecdn.com/html5localstorage-140511235722-phpapp01/95/html5-local-storage-12-638.jpg?cb=1399852926)

## LIMITATIONS IN CURRENT BROWSERS

1. “5 megabytes” is how much storage space each origin gets by default.

2. “QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes.

3. browser doesn't support any mechanism for web developers to request more storage space.

