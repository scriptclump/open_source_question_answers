# HTML:5

HTML is not a programming language, but rather a mark up language.

**New Features**

- New Semantic Elements ( ```<header></header> <footer></footer> <section></section>``` )
- Form 2.0 ( ```<input>``` )
- Persistent Local Storage (without resorting to third-party plugins.)
- WebSocket  (bidirectional communication technology for web applications.)
- Server-Sent Events ( HTML5 introduces events which flow from web server to the web browsers and they are called Server-Sent Events (SSE).)
- Canvas (two-dimensional drawing surface)
- Audio & Video (without resorting to third-party plugins)
- Geolocation (visitors can choose to share their physical location with your web application)
- Microdata (lets you create your own vocabularies beyond HTML5 and extend your web pages with custom semantics)
- Drag and drop

**Attributes while including a file**

Attributes are not required in ```<script></script>```, ```<link>``` tag like type="text/javascript", type="text/css"

**New Tags in HTML5:**

- ```<section></section>```
- ```<header></header>```
- ```<nav></nav>```
- ```<article></article>```
- ```<aisde></aisde>```
- ```<footer></footer>```
- ```<dialog></dialog>```
- ```<figure></figure>```

**Introduction of custom data attribute**

A custom data attribute starts with **data-** and would be named based on your requirement.

**Introduction of new input types**

- datetime
- datetime-local
- date
- month
- week
- time
- number
- range
- email
- url

* Also introduce the ```<output></output>``` tag.

**Introduction of new attributes**

- placeholder
- autofocus
- required

## SGV

SVG stands for Scalable Vector Graphics and it is a language for describing 2D-graphics and graphical applications in XML and the XML is then rendered by an SVG viewer.

## MathML

The HTML syntax of HTML5 allows for MathML elements to be used inside a document using ```<math>...</math>``` tags.

## Web Storage

HTML5 introduces the web storage which will overcome the drawbacks of the cookie. Coookie has following drawbacks.

- Cookies are included with every HTTP request, thereby slowing down your web application by transmitting the same data.
- Cookies are limited to about 4 KB of data . Not enough to store required data.
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet.

Two types of storage introduce in HTML5.

- Session Storage
- Local Storage

Assigning:

```localStorage.VARIABLE_NAME = 1```

```sessionStorage.VARIABLE_NAME = 1```

Deleting:

```localStorage.clear()``` This will remove all localstorage variable

```localStorage.remove('key')``` This will remove a particular key


## Web SQL

The Web SQL Database API isn't actually part of the HTML5 specification but it is a separate specification which introduces a set of APIs to manipulate client-side databases using SQL.

Following are the core methods of Web SQL.

- openDatabase - Create, use the database
- transaction - Will allow to commit and rollback
- executeSql - execute the SQL query

Complete example:

```
<!DOCTYPE HTML>
<html>
   <head>
      <script type="text/javascript">
		 // Creates, use database
         var db = openDatabase('mydb', '1.0', 'Test DB', 2 * 1024 * 1024);
         var msg;

		 // Creates table and insert data
         db.transaction(function (tx) {
            tx.executeSql('CREATE TABLE IF NOT EXISTS LOGS (id unique, log)');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (1, "foobar")');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (2, "logmsg")');
            msg = '<p>Log message created and row inserted.</p>';
            document.querySelector('#status').innerHTML =  msg;
         });

		 // Selects from database
         db.transaction(function (tx) {
            tx.executeSql('SELECT * FROM LOGS', [], function (tx, results) {
               var len = results.rows.length, i;
               msg = "<p>Found rows: " + len + "</p>";
               document.querySelector('#status').innerHTML +=  msg;

               for (i = 0; i < len; i++){
                  msg = "<p><b>" + results.rows.item(i).log + "</b></p>";
                  document.querySelector('#status').innerHTML +=  msg;
               }
            }, null);
         });
      </script>
   </head>
   <body>
      <div id="status" name="status">Status Message</div>
   </body>
</html>
```


## Server-Sent Events

HTML5, WHATWG Web Applications 1.0 introduces events which flow from web server to the web browsers and they are called Server-Sent Events (SSE). Using SSE you can push DOM events continously from your web server to the visitor's browser.

The event streaming approach opens a persistent connection to the server, sending data to the client when new information is available, eliminating the need for continuous polling.

**Server Side Script for SSE**

Server side script should send Content-type header and type should be ```text/event-stream``` like this

```
print "Content-Type: text/event-stream\n\n";
```

Server side script would send an Event: tag followed by event name. Event name should be terminated by a new line character

```
print "Event: server-time\n";
```

Server side script would send event data using Data: tag which would be followed by integer of string value terminated by a new line character.

***Perl Example***

```
#!/usr/bin/perl

print "Content-Type: text/event-stream\n\n";

while(true){
   print "Event: server-time\n";
   $time = localtime();
   print "Data: $time\n";
   sleep(5);
}
```

***Handle Server-Sent Events example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <script type="text/javascript">
         document.getElementsByTagName("eventsource")[0].addEventListener("server-time", eventHandler, false);
         function eventHandler(event){
            // Alert time sent by the server
            document.querySelector('#ticker').innerHTML = event.data;
         }
      </script>
   </head>
   <body>
      <div id="sse">
         <eventsource src="/cgi-bin/ticker.cgi" />
      </div>
      <div id="ticker" name="ticker">
         [TIME]
      </div>
   </body>
</html>
```


## Web Sockets

A WebSocket is a standard bidirectional TCP socket between the client and the server. The socket starts out as a HTTP connection and then "Upgrades" to a TCP socket after a HTTP handshake. After the handshake, either side can send data.

***WebSocket Attributes***

Socket.readyState readonly attribute readyState represents the state of the connection.

- 0 = connection has not yet been established
- 1 = connection is established and communication is possible
- 2 = connection is going through the closing handshake
- 3 = connection has been closed or could not be opened.

Socket.readyState

The readonly attribute bufferedAmount represents the number of bytes of UTF-8 text that have been queued using send() method.

***WebSocket Events***

- Socket.onopen = occurs when socket connection is established.
- Socket.onmessage = occurs when client receives data from server.
- Socket.onerror = occurs when there is any error in communication.
- Socket.onclose = occurs when connection is closed.

***WebSocket Methods***

- Socket.send() = send(data) method transmits data using the connection.
- Socket.close() = The close() method would be used to terminate any existing connection.

***WebSocket Example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <script type="text/javascript">
         function WebSocketTest(){
            if ("WebSocket" in window){
               alert("WebSocket is supported by your Browser!");
               // Let us open a web socket
               var ws = new WebSocket("ws://localhost:9998/echo");
               ws.onopen = function(){
                  // Web Socket is connected, send data using send()
                  ws.send("Message to send");
                  alert("Message is sent...");
               };

               ws.onmessage = function (evt){
                  var received_msg = evt.data;
                  alert("Message is received...");
               };

               ws.onclose = function(){
                  // websocket is closed.
                  alert("Connection is closed...");
               };
            }else{
               // The browser doesn't support WebSocket
               alert("WebSocket NOT supported by your Browser!");
            }
         }
      </script>
   </head>
   <body>
      <div id="sse">
         <a href="javascript:WebSocketTest()">Run WebSocket</a>
      </div>
   </body>
</html>
```

## Canvas

```<canvas>``` gives you an easy and powerful way to draw graphics using JavaScript.

***Canvas example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <style>
         #mycanvas{border:1px solid red;}
      </style>
      <script type="text/javascript">
         var canvas  = document.getElementById("mycanvas");
         if (canvas.getContext){
            var ctx = canvas.getContext('2d');
            // drawing code here
         }else {
            // canvas-unsupported code here
         }
      </script>
   </head>
   <body>
      <canvas id="mycanvas" width="100" height="100"></canvas>
   </body>
</html>
```

## Audio and  Video

The HTML5 ```<audio>``` and ```<video>``` tags make it simple to add media to a website without need for flash.

***Example***

```
<!DOCTYPE HTML>
<html>
   <body>
      <video  width="300" height="200" controls autoplay>
         <source src="/html5/foo.ogg" type="video/ogg" />
         <source src="/html5/foo.mp4" type="video/mp4" />
         Your browser does not support the video element.
      </video><br />
      <audio controls autoplay>
         <source src="/html5/audio.ogg" type="audio/ogg" />
         <source src="/html5/audio.wav" type="audio/wav" />
         Your browser does not support the audio element.
      </audio>
   </body>
</html>
```

## Geolocation

HTML5 Geolocation API lets you share your location with web sites. The geolocation APIs work with a new property of the global navigator object.

***Geolocation Methods***

- getCurrentPosition() = retrieves the current geographic location of the user
- watchPosition() = retrieves periodic updates about the current geographic location of the device.
- clearWatch() = cancels an ongoing watchPosition call.


***Location properties***

- coords
- coords.latitude
- coords.longitude
- coords.altitude
- coords.accuracy
- coords.altitudeAccuracy
- coords.heading
- coords.speed
- timestamp

***Handling Errors***

- 0  UNKNOWN_ERROR = The method failed to retrieve the location of the device due to an unknown error.
- 1  PERMISSION_DENIED = The method failed to retrieve the location of the device because the application does not have permission to use the Location Service.
- 2  POSITION_UNAVAILABLE = The location of the device could not be determined.
- 3  TIMEOUT  = The method was unable to retrieve the location information within the specified maximum timeout interval.

***Example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <script type="text/javascript">
         function showLocation(position) {
            var latitude = position.coords.latitude;
            var longitude = position.coords.longitude;
            alert("Latitude : " + latitude + " Longitude: " + longitude);
         }
         function errorHandler(err) {
            if(err.code == 1) {
               alert("Error: Access is denied!");
            } else if( err.code == 2) {
               alert("Error: Position is unavailable!");
            }
         }
         function getLocation(){
            if(navigator.geolocation){
               // timeout at 60000 milliseconds (60 seconds)
               var options = {timeout:60000};
               navigator.geolocation.getCurrentPosition(showLocation, errorHandler, options);
            }else{
               alert("Sorry, browser does not support geolocation!");
            }
         }
      </script>
   </head>
   <body>
      <form>
         <input type="button" onclick="getLocation();" value="Get Location"/>
      </form>
   </body>
</html>
```

## Microdata

Coming Soon...

## Drag and Drop

HTML 5 came up with a Drag and Drop (DnD) API that brings native DnD support to the browser making it much easier to code up.


***Drag and Drop Events***

- dragenter
- dragover
- dragleave
- drag
- drop
- dragend

Drag and drop events accept Event object which has a readonly attribute called dataTransfer. The DataTransfer object holds data about the drag and drop operation.

***DataTransfer attributes***

- dataTransfer.dropEffect ```[ = value ] (none, copy, link, and move.)```
- dataTransfer.effectAllowed ```[ = value ] (none, copy, copyLink, copyMove, link, linkMove, move, all and uninitialized.)```
- dataTransfer.types
- dataTransfer.clearData( [ format ] )
- dataTransfer.setData(format, data)
- data = dataTransfer.getData(format)
- dataTransfer.files
- dataTransfer.setDragImage(element, x, y)
- dataTransfer.addElement(element)

***Example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <style type="text/css">
         #boxA, #boxB {
            float:left;padding:10px;margin:10px;-moz-user-select:none;
         }
         #boxA { background-color: #6633FF; width:75px; height:75px;  }
         #boxB { background-color: #FF6699; width:150px; height:150px; }
      </style>
      <script type="text/javascript">
         function dragStart(ev) {
            ev.dataTransfer.effectAllowed='move';
            ev.dataTransfer.setData("Text", ev.target.getAttribute('id'));
            ev.dataTransfer.setDragImage(ev.target,0,0);
            return true;
         }
         function dragEnter(ev) {
            event.preventDefault();
            return true;
         }
         function dragOver(ev) {
            return false;
         }
         function dragDrop(ev) {
            var src = ev.dataTransfer.getData("Text");
            ev.target.appendChild(document.getElementById(src));
            ev.stopPropagation();
            return false;
         }
      </script>
   </head>
   <body>
      <center>
         <h2>Drag and drop HTML5 demo</h2>
         <div>Try to move the purple box into the pink box.</div>
         <div id="boxA" draggable="true"
            ondragstart="return dragStart(ev)">
            <p>Drag Me</p>
         </div>
         <div id="boxB" ondragenter="return dragEnter(ev)"
            ondrop="return dragDrop(ev)"
            ondragover="return dragOver(ev)">Dustbin
         </div>
      </center>
   </body>
</html>
```

## Web Workers

JavaScript was designed to run in a single-threaded environment, meaning multiple scripts cannot run at the same time. Web Workers are background scripts that are not interrupted by scripts that respond to clicks or other user interactions, and allows long tasks to be executed without yielding to keep the page responsive.

Web Worker it cannot access the web page's window object (window.document), which means that Web Workers don't have direct access to the web page and the DOM API. Although Web Workers cannot block the browser UI, they can still consume CPU cycles and make the system less responsive.


***Web Workers methods***

- postMessage() = communication between web worker and its parent page is done using the postMessage()
- onmessage() = Message passed by Web Worker is accessed using onmessage event in the main page.
- terminate() = Web Workers don't stop by themselves but the page that started them can stop them by calling terminate() method.

***Example***

```
<!DOCTYPE HTML>
<html>
   <head>
      <title>Big for loop</title>
      <script>
         if (Modernizr.webworkers) {
            var worker = new Worker('bigLoop.js');
            worker.onmessage = function (event) {
               alert("Completed " + event.data + "iterations" );
            };
            worker.onerror = function (event) {
               console.log(event.message, event);
            };
         } else{
            alert("Sorry!! you do not have web workers support." );
         }

         function sayHello(){
               alert("Hello sir...." );
         }
      </script>
   </head>
   <body>
      <input type="button" onclick="sayHello();" value="Say Hello"/>
   </body>
</html>
```

## Indexeddb

The indexeddb is a new HTML5 concept to store the data inside user's browser. indexeddb is more power than local storage and useful for applications that requires to store large amount of the data. Web SQL database is a deprecated local storage specification.

***Features****

- it stores key-pair values
- it is not a relational database
- IndexedDB API is mostly asynchronous
- it is not a structured query language
- it has supported to access the data from same domain

```
<!DOCTYPE html>
<html>
   <head>
      <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
      <script type="text/javascript">
         //prefixes of implementation that we want to test
         window.indexedDB = window.indexedDB || window.mozIndexedDB || window.webkitIndexedDB || window.msIndexedDB;
         //prefixes of window.IDB objects
         window.IDBTransaction = window.IDBTransaction || window.webkitIDBTransaction || window.msIDBTransaction;
         window.IDBKeyRange = window.IDBKeyRange || window.webkitIDBKeyRange || window.msIDBKeyRange
         if (!window.indexedDB) {
            window.alert("Your browser doesn't support a stable version of IndexedDB.")
         }
         const employeeData = [
            { id: "00-01", name: "gopal", age: 35, email: "gopal@tutorialspoint.com" },
            { id: "00-02", name: "prasad", age: 32, email: "prasad@tutorialspoint.com" }
         ];
         var db;
         var request = window.indexedDB.open("newDatabase", 1);
         request.onerror = function(event) {
            console.log("error: ");
         };
         request.onsuccess = function(event) {
            db = request.result;
            console.log("success: "+ db);
         };
         request.onupgradeneeded = function(event) {
            var db = event.target.result;
            var objectStore = db.createObjectStore("employee", {keyPath: "id"});
            for (var i in employeeData) {
               objectStore.add(employeeData[i]);
            }
         }
         function read() {
            var transaction = db.transaction(["employee"]);
            var objectStore = transaction.objectStore("employee");
            var request = objectStore.get("00-03");
            request.onerror = function(event) {
               alert("Unable to retrieve daa from database!");
            };
            request.onsuccess = function(event) {
               // Do something with the request.result!
               if(request.result) {
                  alert("Name: " + request.result.name + ", Age: " + request.result.age + ", Email: " + request.result.email);
               } else {
                  alert("Kenny couldn't be found in your database!");
               }
            };
         }
         function readAll() {
            var objectStore = db.transaction("employee").objectStore("employee");
            objectStore.openCursor().onsuccess = function(event) {
               var cursor = event.target.result;
               if (cursor) {
                  alert("Name for id " + cursor.key + " is " + cursor.value.name + ", Age: " + cursor.value.age + ", Email: " + cursor.value.email);
                  cursor.continue();
               }else {
                  alert("No more entries!");
               }
            };
         }
         function add() {
            var request = db.transaction(["employee"], "readwrite")
            .objectStore("employee")
            .add({ id: "00-03", name: "Kenny", age: 19, email: "kenny@planet.org" });
            request.onsuccess = function(event) {
               alert("Kenny has been added to your database.");
            };
            request.onerror = function(event) {
               alert("Unable to add data\r\nKenny is aready exist in your database! ");
            }
         }
         function remove() {
            var request = db.transaction(["employee"], "readwrite")
            .objectStore("employee")
            .delete("00-03");
            request.onsuccess = function(event) {
               alert("Kenny's entry has been removed from your database.");
            };
         }
      </script>
   </head>
   <body>
      <button onclick="read()">Read </button>
      <button onclick="readAll()">Read all </button>
      <button onclick="add()">Add data </button>
      <button onclick="remove()">Delete data </button>
   </body>
</html>
```

## Web Messaging

Web Messaging is the way for documents to separates browsing context to share the data without Dom. It overrides the cross domain communication problem in different domains, protocols or ports.

## Web CORS

Cross-origin resource sharing (CORS) is a mechanism to allows the restricted resources from another domain in web browser.

For suppose, if you click on HTML5- video player in html5 demo sections. it will ask camera permission. if user allow the permission then only it will open the camera or else it doesn't open the camera for web applications.

## Web RTC

Cross-origin resource sharing (CORS) is a mechanism to allows the restricted resources from another domain in web browser.

For suppose, if you click on HTML5- video player in html5 demo sections. it will ask camera permission. if user allow the permission then only it will open the camera or else it doesn't open the camera for web applications.