# AWS: Events

## Review, Research, and Discussion

### Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server

They are both ways you can implement an API. Within an Express Server you define your routes and write the logic for them. With AWS API Gateway, you set up your routes and then implement the functionality using lamda functions.

### List the AWS Database offerings and talk about the pros and cons of each

AWS database offerings include:

* RDS

* DynamoDB

* ElastiCache

* Neptune

* Amazon QLDB

* Amazon DocumentDB

* Amazon Keyspaces

* Amazon Timestream

They are each comparable to different db services. RDS is similar to oracle SQL, DynamoDB is similar to MongoDB, Aurora is MySQL, postrgeSQL compatible, etc. 

Pros: They are scalable, managed, secure, easy to work with, and scalable

Cons: The only major con I can see is the cost.

### What’s the difference between a FIFO and a standard queue?

A FIFO queue is first in first out and a standard queue provides at least once delivery and isn't neccessarily ordered.

### How can the server be assured a message was properly received?

Logging and using timestamps and checking whether it was delivered based on the response sent from the endpoint.

## Document the following Vocabulary Terms

### Serverless API

An API that lives in the cloud and is created using cloud services.

### Triggers

Essentially a connection between resources. When something happens to a resource, it triggers an action to be taken.

### Dynamo vs Mongo

Dynamo is like the AWS version of Mongo. Mongo is open source and uses JSON objects, whereas Dynamo uses tables. MongoDB is less restrictive of data types and size.

### Dynamoose vs Mongoose

Dynamoose is a modeling tool used for dynamo and mongoose is used for mongo.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

aurora, SQS, SNS

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

SQS, SNS, and I look forward to jumping back into React.

### What are you most excited about trying to implement or see how it works?

SQS and SNS