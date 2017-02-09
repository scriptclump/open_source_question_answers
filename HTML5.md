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

**SGV**

SVG stands for Scalable Vector Graphics and it is a language for describing 2D-graphics and graphical applications in XML and the XML is then rendered by an SVG viewer.

**MathML**

The HTML syntax of HTML5 allows for MathML elements to be used inside a document using ```<math>...</math>``` tags.

**Web Storage**

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


