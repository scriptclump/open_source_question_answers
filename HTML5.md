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