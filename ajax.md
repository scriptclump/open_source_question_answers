Ajax is a client-side script that communicates with server without refresh the complete page. You can also say "the method of exchanging data with a server, and updating parts of a web page without reloading the entire page". Ajax is used in all web-technology like PHP, ASP, Java and Mobile Technology etc.


**Question: What is Ajax?**
AJAX (Asynchronous JavaScript and XML) is a client-side script which is used to get the data from Server.

**Question: Why Ajax is used?**
Ajax is used to get the data from server without refreshing the current page.

**Question: When we can use Ajax? Give Few Examples?**
Ajax can be used to get the data from Server when you don't want to refresh the page. See Below Scenario:

    In Registration Page, check the username is available OR NOT.
    In Registration page, check email address is already taken OR NOT.
    In Product Listing page, when user click on "Next" under pagination, you won't want to show the next page data without refreshing the page.

**Question: What files need to install to use Ajax in Website?**
Initially, no files required to use the ajax in your website.
But to manage your ajax call in better way, you can use JS library which world used to use.

**Question: What js library are available to use the Ajax?**
Following are few JS library which are used for Ajax

    JQuery
    MooTools
    Prototype
    YUI Library
    Backbone js

**Question: What Browsers support Ajax?**
Today, All the Browser support ajax. Following are minium version of browser which support Ajax.

    Internet Explorer 5.0 and up,
    Opera 7.6 and up,
    Netscape 7.1 and up,
    Firefox 1.0 and up,
    Safari 1.2 and up,

**Question: What is XMLHttpRequest?**

XMLHttpRequest is an API available to web browser scripting languages (i.e. JavaScript).
It is used to send HTTP/HTTPS requests to a web server and load the server's response into the script.

**Question: How we can send data to server using Ajax?**

We can use GET OR POST Method to send data.

**Question: What is Asynchronous in Ajax?**

We can set the Asynchronous value as true OR false.
Async=true
Ajax request execute independently, Its response can come earlier than other request which is execute later .
Async=true
Ajax request does not execute independently, Its response can comes when earlier request finished.

**Question: What do the different readystates in XMLHttpRequest?**

Following are different stats(0-4) of ready state in XMLHttpRequest
0 Ajax Request not initialized
1 Ajax Request's server connection established
2 Ajax Request received
3 Ajax Request processing
4 request finished and response is ready.

**Question: Can I send Ajax Request to another domain?**

No, you can't do this.

**Question: What are advantage of AJax?**

    Its faster as it load only required content.
    More user friendly.
    One page application possible due to Ajax.
    Reduce the loading of page.

**Question: What are disadvantage of Ajax?**

It does not crawl to search Engine.

**Question: Define JSON?**

JSON is JavaScript Object Notation.

**Question: What type of response we can get in Ajax Response?**

    text data
    html data
    JSON data
    XML data

**Question: Describe how to handle concurrent AJAX requests?**
JavaScipt Closures can be used for handling concurrent requests.

**Question: How do you know that an AJAX request has completed?**
If readyState's value is 4 means its completed.