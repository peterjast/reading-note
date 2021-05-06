# Event Driven Architecture

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Review, Research, and Discussion

### What’s the difference between a FIFO and a standard queue?

Standard queues deliver the message at least once and FIFO queues deliver the message exactly once.

### How can the server be assured a message was properly received?

You could set up your client to send back a response when it recieves a message.

### What classic design pattern is best represented by event driven programming?

The Observer pattern

### How do you test an event driven system?

Integrate logging into the event system and then write unit tests utilizing the spy method.

## Document the following Vocabulary Terms

### FIFO Queue

A first in first out queue - the first value in the queue is the first value out of the queue - similar to standard queues but support ordering and exactly-once processing

### Pub/Sub

A messaging pattern where publishers send messages and suscribers recieve the messages of the publishers they subscribe to

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

SNS, SQS, Credit Card Transactions, Lamda functions

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

AWS Lambda, SQS, SNS

### What are you most excited about trying to implement or see how it works?

I'm looking forward to using different AWS tools.

## Resources

[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)
