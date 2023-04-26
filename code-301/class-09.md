# **Functional Programming**

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Concepts of Functional Programming in JavaScript

Code samples from [Concepts of Functional Programming in JavaScript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

* avoids changing state and mutable data

* style of building stucture of computer programs

* treats computation as evaluation of mathematical functions

### Pure Functions

* return same result if given same arguments

* no observable side effects

```javascript
let PI = 3.14;

const calculateArea = (radius, pi) => radius * radius * pi;

calculateArea(10, PI); // returns 314.0
```

Not pure:

* Reading files

* Random number generation

### Pure Function Benefits

* code is easier to test

### Immutability

* can't be changed

### Referential Transparency

* pure function will always have same output with same input

> pure functions + immutable data = referential transparency

### Functions as first-class entities

* treated as values and used as data

* refer to it from constants and variables

* pass it as a parameter to other functions

* return it as result from other functions

### Higher-order functions

* takes one or more functions as arguments

* returns a function as result

  * filter

  * map
  
  * reduce

## Refactoring Javascript for Performance and Readability

Code samples from [Refactoring Javascript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

```javascript
// Unrefactored code

const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;
}

function getLong(shortURL) {
  for (let i = 0; i < URLstore.length; i++) {
    if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
}

// Refactored code

const URLstore = new Map(); // Change this to a Map

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  // Place the short URL into the Map as the key with the long URL as the value
  URLstore.set(rndName, URL);
  return rndName;
}

function getLong(shortURL) {
  // Leave the function early to avoid an unnecessary else statement
  if (URLstore.has(shortURL) === false) {
    throw 'Not in URLstore!';
  }
  return URLstore.get(shortURL); // Get the long URL out of the Map
}
```

## Resources

[Concepts of Functional Programming in JavaScript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

[Refactoring Javascript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)
