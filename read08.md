## Routing
### Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing.

### You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function (See Using middleware for details).

### These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

### In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.


## Route paths
### Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

### The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.

### If you need to use the dollar character ($) in a path string, enclose it escaped within ([ and ]). For example, the path string for requests at “/data/$book”, would be “/data/([\$])book”.


## Express Router
### What exactly is the Express Router? It is a mini express application without all the bells and whistles of an express application, just the routing stuff. Let's take a look at exactly what this means. We'll go through each section of our site and use different features of the Router.

### Basic Routes express.Router()
### Let's call an instance of the Router for creating our frontend routes for our application. This will include the Home and About pages.
