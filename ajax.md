Ajax is a client-side script that communicates with server without refresh the complete page. You can also say "the method of exchanging data with a server, and updating parts of a web page without reloading the entire page". Ajax is used in all web-technology like PHP, ASP, Java and Mobile Technology etc.


**What is Ajax?**

AJAX (Asynchronous JavaScript and XML) is a client-side script which is used to get the data from Server.

AJAX stands for Asynchronous JavaScript and XML. It is a group of related technologies to display data asynchronously.

Ajax is abbreviated as Asynchronous Javascript and XML. It is new technique used to create better, faster and more interactive web systems or applications. Ajax uses asynchronous data transfer between the Browser and the web server.

This technique is used to make internet faster and user friendly. It is not a programming language.

**Why Ajax is used?**

Ajax is used to get the data from server without refreshing the current page.

**When we can use Ajax? Give Few Examples?**

Ajax can be used to get the data from Server when you don't want to refresh the page. See Below Scenario:

In Registration Page, check the username is available OR NOT.

In Registration page, check email address is already taken OR NOT.

In Product Listing page, when user click on "Next" under pagination, you won't want to show the next page data without refreshing the page.

**What files need to install to use Ajax in Website?**

Initially, no files required to use the ajax in your website.
But to manage your ajax call in better way, you can use JS library like JQuery.

**What js library are available to use the Ajax?**

Following are few JS library which are used for Ajax

- JQuery
- MooTools
- Prototype
- YUI Library
- Backbone js

**What Browsers support Ajax?**

Today, All the Browser support ajax. Following are minium version of browser which support Ajax.

- Internet Explorer 5.0 and up,
- Opera 7.6 and up,
- Netscape 7.1 and up,
- Firefox 1.0 and up,
- Safari 1.2 and up,

**What is XMLHttpRequest?**

XMLHttpRequest is an API available to web browser scripting languages (i.e. JavaScript).
It is used to send HTTP/HTTPS requests to a web server and load the server's response into the script.

**How we can send data to server using Ajax?**

We can use GET OR POST Method to send data.

**What is Asynchronous in Ajax?**

We can set the Asynchronous value as true OR false.
Async=true
Ajax request execute independently, Its response can come earlier than other request which is execute later .
Async=true
Ajax request does not execute independently, Its response can comes when earlier request finished.

**What do the different readystates in XMLHttpRequest?**

Following are different stats(0-4) of ready state in XMLHttpRequest
0 Ajax Request not initialized
1 Ajax Request's server connection established
2 Ajax Request received
3 Ajax Request processing
4 request finished and response is ready.

**Can I send Ajax Request to another domain?**

No, you can't do this.

**What are advantage of AJax?**

- Its faster as it load only required content.
- More user friendly.
- One page application possible due to Ajax.
- Reduce the loading of page.

**What are disadvantage of Ajax?**

It does not crawl to search Engine.

**Define JSON?**

JSON is JavaScript Object Notation.

**What type of response we can get in Ajax Response?**

- text data
- html data
- JSON data
- XML data

**Describe how to handle concurrent AJAX requests?**

JavaScipt Closures can be used for handling concurrent requests.

**How do you know that an AJAX request has completed?**

If readyState's value is 4 means its completed.


**What are the advantages of AJAX?**

- Quick Response
- Bandwidth utilization
- User is not blocked until data is retrieved from the server.

**What are the disadvantages of AJAX?**

- Dependent on JavaScript
- Security issues
- Debugging is difficult

**What are the real web applications of AJAX currently running in the market?**

- Twitter
- Facebook
- Gmail
- Javatpoint
- Youtube etc.

**What are the security issues with AJAX?**

- AJAX source code is readable
- Attackers can insert script into the system

**What is the difference between synchronous and asynchronous requests?**

Synchronous request blocks the user until response is retrieved whereas asynchronous doesn't block the user.

**What are the technologies used by AJAX?**

- HTML/XHTML and CSS
- DOM
- XML
- XMLHttpRequest
- JavaScript

**What does XMLHttpRequest?**

- sends data in the background
- receives data
- updates data without reloading the page


**What are the properties of XMLHttpRequest?**

The important properties of XMLHttpRequest object are given below.

- onReadyStateChange
- readyState
- responseText
- responseXML

**What are the important methods of XMLHttpRequest?**

- open()
- send()
- setRequestHeader()

**What is JSON in AJAX?**

JSON stands for JavaScript Object Notation. It is easy to understand and data exchange is fast than XML. It supports array.

**What are the tools for debugging AJAX applications?**

There are two most widely used tools for debugging AJAX applications.

- Firebug for Mozilla Firefox
- Fiddler for IE (Internet Explorer)

**What are the types of post back in AJAX?**

There are two types of post back in AJAX.

- Synchronous Postback
- Asynchronous Postback

**What are the different ready states of a request in AJAX?**

There are 5 ready states of a request in AJAX.

- 0 means UNOPENED
- 1 means OPENED
- 2 means HEADERS_RECEIVED
- 3 means LOADING
- 4 means DONE


**What are the common AJAX frameworks?**

- Dojo Toolkit
- YUI
- Google Web Toolkit (GWT)
- Spry
- MooTools
- Prototype

**How can you test the AJAX code?**

JsUnit is the open source unit testing framework for client side JavaScript. It is a part of JUnit.

**What is the difference between JavaScript and AJAX?**

JavaScript makes a request to the server and waits for the response. It consumes more bandwidth as it reloads the page.

AJAX sends a request to the server and doesn't wait for the response. It doesn't reload the page so consumes less bandwidth.


----------------------------------


**What are Ajax applications?**

Browser based applications and platform independent applications are used by Ajax.

**How many types of triggers are present in update panel?**

There are two types of triggers used in update panel:

- PostBackTrigger – This works as full postback and it cannot work asynchronously
- AsyncPostBackTrigger – Partial post back asynchronously

**What are all the controls of Ajax?**

Following are the controls of Ajax:

- ScriptManager
- ScriptManagerProxy
- UpdatePanel
- UpdateProgress
- Timer

**What is the name of the DLL that contains Ajax control tool kit?**

Ajaxcontroltoolkit.dll is the DLL used for Ajax control tool kit and it can be downloaded from the internet. It can be added in the tool box or copied directly in the bin folder.


**What role of #&& in querystring?**

hashsign is treated as fragment delimiter to delimit the history state and && precedes is used to check on the information in the query string.

**How to control the duration of an Ajax request?**

AsyncPostBackTimeout property is used to control the duration of Ajax request. Deafult value of this property is 90 seconds.

Example –

```
<asp:ScriptManager runat=”server” id=”sample” AsyncPostBackTimeout=”40”/>
```


**What are the advantages of Ajax?**

Following are the advantages of Ajax:

- Bandwidth utilization – It saves memory when the data is fetched from the same page.
- More interactive
- Speeder retrieval of data

**What are the disadvantages of Ajax?**

Following are the disadvantages of Ajax:

- AJAX is dependent on Javascript. If there is some Javascript problem with the browser or in the OS, Ajax will not support
- Ajax can be problematic in Search engines as it uses Javascript for most of its parts.
- Source code written in AJAX is easily human readable. There will be some security issues in Ajax.
- Debugging is difficult
- Increases size of the requests
- Slow and unreliable network connection.
- Problem with browser back button when using AJAX enabled pages.

**What is update panel?**

Update panel  is a server control used to update the specified portion of a web page. Script Manager needs to be used whenever update panel is used. Using update panel, user cannot handle outside controls.

**Which are the two methods used for cross domain Ajax calls?**

There are two methods used to transfer data between the two more more security domains:

- CORS – Cross Origin Resource Sharing and it works with the HTTP web browsers
- JSONP – JSON with Padding which works with the HTTP GET and on legacy browsers

**What are all the technologies used by Ajax?**

AJAX uses following technologies:

- JavaScript
- XMLHttpRequest
- Document Object Model (DOM)
- Extensible HTML (XHTML)
- Cascading Style Sheets (CSS)

**What are all the features of Ajax?**

Following are the features of Ajax and they are as follows:

- Live data binding
- Client-side template rendering
- Declarative instantiation of client components
- Observer pattern on JavaScript objects and arrays
- Invoking ADO.NET data services and data contexts
- DataView control

**What is JSON in Ajax?**

JSON is abbreviated as JavaScript Object Notation.

JSON is a safe and reliable data interchange format in JavaScript, which is easy to understand for both users and machines.

**What are the difference between AJAX and Javascript?**

The differences between AJAX and JavaScript are as follows:

AJAX sends request to the server and does not wait for the response. It performs other operations on the page during that time  JavaScript make a request to the server and waits for response
AJAX does not require the page to refresh for downloading the whole page    JavaScript manages and controls a Web page after being downloaded
AJAX minimizes the overload on the server since the script needs to request once    JavaScript posts a request that updates the script every time

**What are the components of the ASP.NET AJAX architecture?**

There are two components of AJAX Architecture:

- AJAX client architecture
- AJAX server architecture

**What are the extender controls?**

The extender controls uses a block of JavaScript code to add new and enhanced capabilities to ASP.NET.

**What is AJAX Control Extender Toolkit?**

AJAX Control Toolkit is one of the extenders that are used to extend or add the functionalities of the ASP.NET controls. The extenders use a block of JavaScript code to add new and enhanced capabilities to the ASP.NET controls.

AJAX Control Extender Toolkit is a free download from site.

**Where AJAX cannot be used?**

Users cannot use AJAX if

- If Page need to show in a search engine
- If browser does not support JavaScript
- If user wants to create secure application

**What are the pre-requisites to execute AJAX applications on a server?**

AJAX is a built-in functionality of .NET Framework 4.0 and AJAX application can be executed by just installing Microsoft Visual Studio 2010. To use extenders in your applications, you are required to install AJAX Control Toolkit and copy the AjaxControlToolkit.dll file to the Bin directory of your application.

**What is AJAX Framework?**

ASP.NET AJAX is a free framework to implement Ajax in asp.net web applications. It is used to quickly creating efficient and interactive Web applications that work across all browsers.

**How can you find out that an AJAX request has been completed?**

ReadyState property is used to check whether AJAX request has been completed. If the property is equal to four, then the request has been completed and data is available.

**Is javascript knowledge is required to do Ajax?**

Yes, if you plan to develop new AJAX functionality for your web application.

**What are all the browsers support AJAX?**

Following browsers support AJAX:

- Internet Explorer 5.0 and above
- Opera 7.6 and above
- Netscape 7.1 and above
- Safari 1.2 and above

**How can you test the Ajax code?**

JSUnit is the client side javascript code used as part of JUnit. JSUnit has been used for Ajax code.

**Is Ajax said to be a technology platform or is it an architectural style?**

Ajax supports both technology and as architectural style.

**How can AJAX applications be debugged?**

Two tools are used for debugging:

- Fiddler for IE
- Firebug for Mozilla.

**How can we cancel the XMLHttpRequest in AJAX?**

Abort() method can be called to cancel the XMLHttpRequest in Ajax.

**Is AJAX code cross browser compatible?**

No, it is supporting cross browser compatible. If the browsers supports native XMLHttpRequest JavaScript object, then this can be used.

**What is the name of object used for AJAX request?**

XmlHttpRequest object is used for Ajax requests.

**What is prerequisite for Update Panel in Ajax?**

Script Manager is pre-requisite to use Update Panel controls.

**How many update panel can be used per page?**

There are no restrictions on the number of update panels per page.

**What is Script Manager?**

Script Manager helps manage the client side script of AJAX. Script Manager acts as a mediator as AJAX depends on JavaScript. Every page that uses AJAX has a Script Manager to enable AJAX libraries.

**How Ajax objects can be created?**

Following syntax can be used to create Ajax objects:

```
Var sample = New ajaxObject(‘path of the page’)
```

**What are the protocols used by Ajax?**

- HTTP’s GET or POST
- XMLHttpRequest for placing a request with the web server
- Uses JSON to communicate between the client and server
- UED or URL encoded data

**What are all the security issues of Ajax?**

Security issues that can be encountered

- When Ajax calls are sent through plain text and it may lead to know the database details
- Inserting scripts can also be possible and attackers can easily penetrate into the system

**How can we handle concurrent requests?**

Javascript functions should be written to handle concurrent requests and call back function can be passed as a parameter. Those parameters are passed to AjaxInteraction(URL, callback) object.

**Define the role of the Update Panel?**

Update Panel is used to add functionality to the existing ASP.NET applications. By using partial page rendering, it can be used to update the content. Refresh can be made for the partial page instead of whole page.

**an we use nested update panel in Ajax?**

Yes, we can use nested update panel in Ajax. Update panels can be nested to have more control over the Page Refresh.

**What are the types of post back in Ajax?**

There are two types of post backs:

- Synchronous Postback
- Asynchronous Postback

**How can we handle exception handling in Ajax?**

ErrorTemplate which is the child tag of Script Manager is used to handle exception handling in Ajax.

**What are the components of the ASP.NET Ajax Client Library?**

Following components are used in Ajax client library:

- Component Layer
- Core Services Layer
- Browser Compatibility Layer

**What are the controls of the Script Management group?**

The controls of script Management group are:

- ScriptManager
- ScriptManagerProxy

**What are all the different data types that JSON supports?**

JSON supports following data types:

- String
- Number
- Boolean
- Array
- Object
- Null

**What are the goals of Ajax?**

The basic goals of ASP.NET Ajax are:

- Reduced web server hits
- Reduced Network load
- Interactive user interface
- Platform and architecture neutrality
- Support for both synchronous and asynchronous communication
- Provide a server- and client-side framework

**What is the difference between proxied and proxyless calls in AJAX?**

- Proxied calls are made through stub objects which can be called from PHP classes on the JavaScript side in AJAX.

- Proxyless calls are made using utility JavaScript functions like HTML_AJAX.replace() and HTML_AJAX.append() in AJAX.

**How many types of ready states in Ajax?**

There are four ready states in Ajax:

- Initialization
- Request
- Process
- Ready

**What is the difference between RegisterClientScriptBlock, RegisterClientScriptInclude and RegisterClientScriptResource?**

Following are the functions:

- RegisterClientScriptBlock – The script is specified as a string parameter.
- RegisterClientScriptInclude – By setting the source attribute to a URL that point to a script file.
- RegisterClientScriptResource – specifies Resource name in an assembly. The source attribute is automatically populated with a URL by a call to an HTTP handler that retrieves the named script from the assembly.

**Which request is better, Get or Post?**

AJAX requests should use an HTTP GET request where the data does not change for a given URL requested.

An HTTP POST should be used when state is updated on the server. This is highly recommended for a consistent web application architecture.

**What are the limitations of Ajax?**

An Ajax Web Application tends to confuse end users if the network bandwidth is slow and there is no full postback running.
