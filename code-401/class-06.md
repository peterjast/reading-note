# Authentication

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Explain what a “Singleton” is (in Computer Science terms)

A simple design pattern where a class can only have one instantiation or one object instance of the class at any time.

## Explain how the Singleton pattern can be used with Node modules, specifically with classes

Node modules are cached after they are loaded, so required modules are used as singletons

## If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

I think I'd need to clarify a lot of ambiguity first. I'd need to know what type of data I'd be working with, what programming languages the applications use on either side of my middleware system, and what operating systems I need to account for.

## Document the following Vocabulary Terms

### Router Middleware

Router middleware is route level middelware that takes the request object sent on a a specific route and performs some pre-defined action with it.

### Dynamic Module Loading

Modules are loaded dynamically into memory at runtime, retrieving functions and variables, using them and then unloaded from memory.

### Singleton Pattern

A common and simple design pattern where classes are one allowed to have one instance object at any time.

### CRUD -> REST Method Matches

CREATE -> POST

READ -> GET

UPDATE -> PUT

DELETE -> DELETE

### Mock Testing

Allows your unit tests to make assertions about ineractions with other modules by replacing dependencies with objects that emulate the dependencies actually used by your application.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

Bcrypt Hashing Functions

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

Cryptographic hash algorithms, BCrypt speed, Key Stretching

### What are you most excited about trying to implement or see how it works?

Bcrypt and setting permissions for different users. I'd also like to develop my own cryptographic hash algorithm.

## Resources

[Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

[Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

[OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

[bcrypt docs](https://www.npmjs.com/package/bcrypt)
