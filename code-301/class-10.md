# **In Memory Storage**

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Understanding the JavaScript Call Stack

Code samples from [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

* JS engine is found in hosting environment

* single-threaded interpreter

* heap and single call stack

* browser provides web APIS

  * DOM

  * AJAX

  * Timers

* call stack is used to invoke functions

* execute one at a time, from top to bottom

* call stack is synchronous

* Asynchronous JS:
  
  * callback
  
  * event loop

  * task queue

### Defining the Call Stack

> Call Stack - data structure that uses LIFO to store and manage calls (temporary storage)

Print stack trace error to demonstrate LIFO:

```javascript
function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();
```

### How the Call Stack Handles Function Calls

```javascript
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();

1. When secondFunction() gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. secondFunction() then calls firstFunction()which is pushed into the stack.
3. firstFunction() returns and prints “Hello from firstFunction” to the console.
4. firstFunction() is pop off the stack.
5. The execution order then move to secondFunction().
6. secondFunction() returns and print “The end from secondFunction” to the console.
7. secondFunction() is pop off the stack, clearing the memory.
```

### Stack Overflow

* When a recursive function has no exit point, a stack overflow occurs
  
* When the hosting environment exceeds its maximum stack call and throws a stack error

```javascript
function callMyself(){
  callMyself();
}

callMyself();
```

### Call Stack Summary

1. single-threaded

1. synchronous execution

1. a stack frame that occupies temporary memory is created when a function is called

1. LIFO

## JavaScript Error Messages && Debugging

Code samples from [JavaScript Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

### Types of Error Messages

* Reference Errors - occurs when you try to use a variable that is not yet defined

* Syntax Errors - when you use invalid syntax

* Range Errors - when you try to manipulate an object with length and give an invalid length

* Type Errors - when you try to use or access incompatible types

### Debugging

* use console.log()

* You can also use breakpoints and debugger code

* Node.js with VS Code has a debug tab where you can add configurations

### Handling Errors

* Use try, catch, finally

* You can even throw your own errors

### Tools to Avoid Runtime Errors

* Quokka

* eslint

* TypeScript

## Resources

[Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

[JavaScript Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
