# Socket.io

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## What is the benefit of transforming data into packets?

* packets are basic units of communication over TCP/IP networks

* data is transformed into smaller pieces

* sending smaller units of data helps with the transmission of data

## UDP is often referred to as a connectionless protocol. Why is this?

UDP doesn't establish a connection before sending data.

## Can a socket server application have multiple socket connections?

Yes, a socker server application can have many socket connections

## Can a socket connection application be connected to multiple socket servers?

Yes, a socket connection application can be connected to multiple socket servers.

## Can an application be both a socket server and a socket connection?

Yes, an application can be both a socket server and a socket connection.

## Document the following Vocabulary Terms

### Observer Pattern

A software design pattern where an object has dependents called observers that are notified about events that happen to the object

### Listener

listeners wait for an event to happen on an object

### Event Handler

a function that is triggered by some event

### Event Driven Programming

programming paradigm based on events as opposed to objects

### Event Loop

design pattern that executes and reacts to events by monitorying the call stack and callback queue

### Event Queue

A queue containing the operations that should be sent for execution

### Call Stack

The call stack contains the order that an interpreter needs to perform called functions

### Emit/Raise/Trigger

used to trigger an event

### Subscribe

to listen to or keep track of a certain event

### database

An organized collection used to systematically store persistant data

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

event driven programming, web sockets, TCP

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

Event queues, databases, Triggers

### What are you most excited about trying to implement or see how it works?

Event driven programming, event loop, socket.io

## Resources

[OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)

[TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)

[Web Sockets](https://en.wikipedia.org/wiki/WebSocket)

[Socket.io](https://www.tutorialspoint.com/socket.io/)

[Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

[Socket.io Documentation](https://socket.io/docs/)

[Socket.io Server API](https://socket.io/docs/server-api)

[Socket.io Client API](https://socket.io/docs/client-api)

[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)
