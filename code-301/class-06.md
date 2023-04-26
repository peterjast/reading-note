# **NODE.js**

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## An Intro to Node.js

Code samples from: [https://www.sitepoint.com/an-introduction-to-node-js/](https://www.sitepoint.com/an-introduction-to-node-js/)

### What is Node.js?

We can use Node.js to execute JavaScript on our computers.

Definitions:

From the [project homepage](https://nodejs.org/en/):

> Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

From [Stack Overflow](https://stackoverflow.com/tags/node.js/info):

> Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

* JavaScript runtime

* built on Google Chrome's v8 JavaScript Engine

* event-based

* non-blocking

* asynchronous

#### Google Chrome's V8 JavaScript Engine

* open-source JS engine that runs in Google Chrome and Chromium-based browsers

* responsible for compiling JavaScript to machine code

* Node took v8 engine and added a file system API, an HTTP library and OS related utility methods

### Installing Node.JS

* npm - node package manager

* You can use Node binaries for your system or install multiple versions using Node Version Manager

### "Hello, World"

1. Create a file hello.js

1. Inside this file:

```javascript
console.log("Hello, World!");
```

1. Use Node's console module

> node Hello.js

"Hello, World!" will be displayed

### Node.js Has Excellent Support for Modern JavaScript

* Supports ES6 and beyond
  
* No compatibility issues

Example:

```javascript
function upcase(strings, ...values) {
  return values.map(name => name[0].toUpperCase() + name.slice(1))
    .join(' ') + strings[2];
}

const person = {
  first: 'brendan',
  last: 'eich',
  age: 56,
  position: 'CEO of Brave Software',
};

const { first, last } = person;
const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];

console.log(
  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')
);
```

Run this file and you should see Brendan Eich is the creator of JavaScript! ┌(˘⌣˘)ʃ in the terminal.

### JavaScript Package Manager - npm

* npm -v checks version of node

* the world's largest software registry

* 1,000,000 packages of JS code

#### Installing Package Globally

> npm install -g jshint

This installs jshint package globally

#### Installing Package Locally

Creates and auto-populates package.json file:

> npm init -y

Install lodash package and save it as project dependency:

> npm install lodash --save

Create test.js and add:

```javascript
const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];
console.log(_.compact(arr));
```

Running node test.js will output [1, 2, 3] to the terminal

#### Working with the package.json

Specify dependencies in package.json. This will allow any dev to clone your project and use npm to install the packages needed to run it.

### What is Node.js Used For?

* installing build tools (npm)

* running build tools (node)

* automates the process of developing modern JS applications

#### Node.js Lets Us Run JavaScript on the Server

Execution Model:

1. Node apps pass async tasks to event loop along with a callback

1. event loop manages a thread pool and executes tasks efficiently

1. executes each callback as tasks complete

### Hello,Word - Server Version

```javascript
const http = require('http');

http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);

console.log('Server running on http://localhost:3000');
```

This will print to http://localhost:3000 when you run it

### Node.js Uses and Advantages

* Building applications that require real-time interaction or collaboration

* speed and scalability

* easily share code between server and client

* speaks JSON - most important data exhange format on the Web

* interacting with object databases

* It can be uses as a scripting language

## 6 Reasons for Pair Programming

1. Greater efficiency

1. Engaged Collaboration

1. Learning from Fellow Students

1. Social Skills

1. Job Interview Readiness

1. Work Environment Readiness

## Resources

[An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js)

[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

[Axios docs](https://www.npmjs.com/package/axios)

[MDN async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)