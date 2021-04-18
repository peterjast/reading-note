# Express

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## What’s the difference between PUT and PATCH?

Put uses request URI to provide a modified version of a resource and replace it - sets all new attributes

Patch is a partial update and gives instructions for how to modify resource

## 3 services or tools that allow you to “mock” an API for development like json-server

1. JSONPlaceholder

1. soap-ui

1. Reqres

1. Beeceptor

1. Fake Rest

1. Mocky

1. api-now

## Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

For Swagger, you define a range of response codes using range definitions 1XX, 2XX, 3XX, 4XX, 5XX; however you should specify the conditions for error responses that are more likely to occur. When defined explicitly, each response status requires a description. 200 for successful operations, 400 for bad requests, 401 for missing or invalid authorization, 404 for not found, 5xx for unexpected error. I think Swagger seems more complex than APIDoc.js, but more practical for larger applications.

For APIDoc.js, 400 for bad request/invalid username, 401 for not authorized/NoAccessRight, 200 for success, 404 for not found. APIDoc.js seems simple and easy to use, but it doesn't seem like it would work for larger projects as well as Swagger.

## Compare and contrast SOAP and ReST

### SOAP

1. Simple Object Access Protocol

1. Protocol

1. Uses service interfaces to expose functionality to client apps

1. Needs more bandwidth

1. Only works with XML

1. Can't use REST

1. Asynchronous processing and subsequent invocation

1. Large file size

### REST

1. Representational State Transfer

1. Architectural Pattern | Client Server -> Stateless -> Cacheable -> Layered System -> Uniform Interface

1. uses uniform service locators to acces the hardware device's components

1. Doesn't need a lot of bandwidth

1. Works with plain text XML, HTML, JSON

1. Can make use of SOAP

1. Way easier coding REST services and implementation

1. Lack of Security

1. Lack of state

## Document the following Vocabulary Terms

### Web Server

* stores and delivers content for websites using HTTP and other protocols to respone to client requests

* node web server applications have to create web server object

* web servers can be created easily using node

### Express

> Express provides methods to specify what function is called for a particular HTTP verb (GET, POST, SET, etc.) and URL pattern ("Route"),
>
> and methods to specify what template ("view") engine is used, where template files are located, and what template to use to render a
>
> response. You can use Express middleware to add support for cookies, sessions, and users, getting POST/GET parameters, etc. You can use
>
> any database mechanism supported by Node (Express does not define any database-related behavior).

* most popular node web framework

* underlying library for other node web frameworks

* write handlers for requests with different HTTP verbs at URL paths(routes)

* integrate view rendering engines to generate responses by inserting data into templates

* set common web application settings like port for connecting, location of templates for response

* add middleware within request handling pipeline: cookies, sessions, user logins, URL parameters, POST data, security headers,

* unopinionated

### Routing

* Routing determines how an app responds to client request to a particular endpoint, a URI or Path and specific HTTP request method

* routes can have more than one handler function

* handlers for requests with different HTTP verbs at URL paths(routes)

```javascript
app.get('/', (req, res) => {
  res.send('Hello World!')
});

app.all('/secret', function(req, res, next) {
  console.log('Accessing the secret section ...');
  next(); // pass control to the next handler
});

//  Routes allow you to match particular patterns of characters in a URL, and extract some values from the URL and pass them as parameters to the route handler (as attributes of the request object passed as a parameter)
```

Routing methods: checkout(), copy(), delete(), get(), head(), lock(), merge(), mkactivity(), mkcol(), move(), m-search(), notify(), options(), patch(), post(), purge(), put(), report(), search(), subscribe(), trace(), unlock(), unsubscribe()

app.all() - used for loading middleware functions at a path for all request methods

* In express, grouping route handlers with same route prefix can be achieved using express.Router

```javascript
// wiki.js - Wiki route module

const express = require('express');
const router = express.Router();

// Home page route
router.get('/', function(req, res) {
  res.send('Wiki home page');
});

// About page route
router.get('/about', function(req, res) {
  res.send('About this wiki');
});

module.exports = router;
```

require route module then call use() on express ass to add Router to middleware handling path - routes will be accessible from /wiki/ and /wiki/about/

```javascript
const wiki = require('./wiki.js');
// ...
app.use('/wiki', wiki);
```

* adding routes to Router object is just like adding routes to app object

```javascript
const express = require('express');
const app = express();

// An example middleware function
let a_middleware_function = function(req, res, next) {
  // ... perform some operations
  next(); // Call next() so Express will call the next middleware function in the chain.
}

// Function added with use() for all routes and verbs
app.use(a_middleware_function);

// Function added with use() for a specific route
app.use('/someroute', a_middleware_function);

// A middleware function added for a specific HTTP verb and route
app.get('/', a_middleware_function);

app.listen(3000);
```

### WRRC

* Web Request Response Cycle

* client accesses service from server - clients are generally web browsers but can also be API's making requests to another server or the command line

* HTTP request specifies resource client wants to interact with through the URL sent with request - GET, PUT, POST, DELETE

* HTTP response is sent by server to client in response to HTTP request - contains status code and resource if request was successful - Also include message body - HTML body generally - if client is an API or command line, could be json or xml - also contains header with metadata

* once request is recieved, server searches for and returns requested info - querying a DB, loading info into an HTML page, returning HTML text to user in body of HTTP response

## Which 3 things had you heard about previously and now have better clarity on?

1. HTTP status codes

1. express routing

1. the difference between a framework like express, a runtime environment like node, and a library like React

## Which 3 things are you hoping to learn more about in the upcoming lecture/demo?**

1. Writing tests

1. Test Driven Development

1. Continuous integration and delivery

## What are you most excited about trying to implement or see how it works?**

I want to make an API, use swagger for my documentation, also try some new routing methods.

## Resources

[An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

[What is NPM?](https://docs.npmjs.com/getting-started/what-is-npm)

[What is TDD?](https://www.agilealliance.org/glossary/tdd/)

[CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)

### Additional Resources

[nodeJS Docs](https://nodejs.org/en/docs/)

[npm docs](https://docs.npmjs.com/)

[express docs](https://expressjs.com/en/4x/api.html)

[http status codes](https://www.restapitutorial.com/httpstatuscodes.html)

[supertest](https://github.com/visionmedia/supertest)