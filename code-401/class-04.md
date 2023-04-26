# Data Modeling

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Name 3 advantages to Test Driven Development

1. High Quality Code

1. Better Design Architecture

1. Reliable solution and better documentation

## In what case would you need to use beforeEach() or afterEach() in a test suite?

You should use beforeEach() and afterEach() when you need to repeat the same setup for many tests. If several tests use the same logic, using beforeEach() and afterEach() will save you some time.

## What is one downside of Test Driven Development

The tests are difficult to write and understand.

## What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

**ES6 Classes** are like a blueprint that define a type of object and can be instantiated at runtime. Classes inherit from a parent class using the extends keyword and can have new properties and methods. The child class is still a type definition.

**Prototypes** are object instances and their children are object instances that delegate any properties to the parent any properties not implemented on the child.

## Why REST?

Writing code for REST services and implementations is much easier than working with SOAP APIs. REST also supports various data formats, while SOAP only supports XML. Over 70% of public APIs are REST APIs. REST has superior performance. Its faster, easier to use, and uses less bandwidth.

## Document the following Vocabulary Terms

### functional programming

A programming paradigm that focuses on building software using only functions.

### object-oriented programming (OOP)

A programming paradigm that focuses on building software using objects and how they interact and relate to one another. OOP stands on 4 fundamental pillars, encapsulation, abstraction, polymorphism and inheritance. Encapsulation is when an object and its properties and methods are bundled into a single unit. Abstraction is hiding implementation details and only making necessary information accessible. Inheritance is when a child inherits properties or methods from a parent. Polymorphism means the ability to take on many forms. A child can inherit properties and methods from a parent, but still have its own properties and methods.

### class

A class is a type definition and essentially a blueprint for an object, thus classes can be instantiated at runtime. Using the extends keyword, a child class can inherit properties or methods from a parent class and have its own properties and methods as well.

### super

The super keyword allows a child to inherit properties and methods from a parent and to access and call functions on the parent. Both classes and object literals can use super in any method.

### this

The this keyword refers to the object it belongs to. If this occurs inside of an object's method, then it will refer to that object. If this occurs inside of a global method, then this will refer to the global object, which is usually the browser window.

### Test Driven Development (TDD)

Test Driven Development is design process for developing software. First, you should take time to think about what functionality you need to test for and then you write your tests. After your tests are written, you write code to pass all of your tests and refactor your code.

### Jest

A JavaScript testing framework. It is maintained by Facebook for the purpose of supporting large web applications and focusing on simplicity.

### Continuous Integration (CI)

The process of continuously integrating code into a shared repository and having each integration require verification by an automated build and automated tests.

### REST

Representational state transfer is an architectural pattern:

> Client Server -> Stateless -> Cacheable -> Layered System -> Uniform Interface

1. It is very fast, easy to use, doesn't need a lot of bandwidth, and supports plain text XML, HTML, JSON

1. It uses uniform service locators to access the device's components and can make use of SOAP

1. REST services and implementation are much easier to code than SOAP.

### Which 3 things had you heard about previously and now have better clarity on?

1. Test Driven Design

1. Jest

1. Continuous Integration and Delivery

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1. writing tests

1. nosql modeling techniques

1. Continous Integration and Delivery

### What are you most excited about trying to implement or see how it works?

Test driven development and continuous integration and delivery.

## Resources

[sql vs nosql](hhttps://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

[nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

[nosql modeling techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

### Additional Resources

[mongoose API](https://mongoosejs.com/docs/api.html#Model)
