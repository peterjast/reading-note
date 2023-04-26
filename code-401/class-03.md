# Express REST API

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Name 3 real world use cases where you’d want to change the request with custom middleware

1. parsing cookies

1. Dealing with sessions

1. authentication

1. parsing data

## True or false: The route handler is middleware?

True

## In what ways can a middleware function end the process and send data to the browser?

You could have conditions met where your middleware function sends data and ends the process. You could have error handling that sends an error message to the browser and ends the process. You could configure your middlewear by exporting a function that returns different middleware implementations based on the input params.

## At what point in the request lifecycle can you “inject” middleware?

Using node-dependency-injection-express-middleware, you can retrieve the container from the request and inject middleware.

## What can cause express to error with “Request headers sent twice, cannot start a second response”

I think this could happen due to a timing error of an asynchronous response in an express route. Also, it would seem that the function didn't end the life cycle after sending the first response, so I would take a look at that and see what needs to be fixed.

## Document the following Vocabulary Terms

### Middleware

> a function that has access to the request object, response object and next middlewear function
> can execute any code, make changes to request and response objects, end the request-response cycle, call next middleware function in stack

### Request Object

> has props for request query, params, body, HTTP headers and represents the HTTP request - properties communicate to server what resource the client wants to interact with

### Response Object

> HTTP response sent back to client from server - after the request is receieved, the server searches for the requested resource - server sends a status code and if it was successful, the requested resource

### Application Middleware

> using the app.use() and app.METHOD() functions, you can bind application-level middlewear to an instance of the app object - METHOD is the HTTP method of the request the middleware handles

### Routing Middleware

> Bound to an instance of express.Router(), but works the same as App middleware - using the router.use() and router.METHOD() functions - handles routing

### Test Driven Development

> Think about the functionality you need, write comprehensive tests before you start writing code, write code to pass your tests and refactor until it passes all tests and is clean and optimized

### Behavioral Testing

> Otherwise known as black box testing - tests the external behavior of software to see if it performs as expected

## Which 3 things had you heard about previously and now have better clarity on?

1. Middleware - I didn't know you could do soe much with it

1. express routing

1. test driven development

## Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1. Test Driven Development - I want to learn how to write tests

1. custom configurable express routing

1. request response cycle and middle wear

## Resources

[Review ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

[Using Express Routing](https://expressjs.com/en/guide/routing.html)

[Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)
