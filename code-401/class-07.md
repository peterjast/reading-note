# Bearer Authorization

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Write the following steps in the correct order

1. Register your application to get a client_id and client_secret

1. Ask the client if they want to sign in via a third party

1. Make a request to a third-party API endpoint

1. Redirect to a third party authentication endpoint

1. Make a request to the access token endpoint

1. Receive access token

1. Receive authorization code

## What can you do with an authorization code?

An authorization code allows you to send information, such as a request for an access token, to a secure resource.

## What can you do with an access token?

Access tokens are used to make API requests on behalf of a user

## What’s a benefit of using OAuth instead of your own basic authentication?

OAuth contains authorization requests, access tokens and refresh tokens and widely accepted as the standard for modern web applications. It is well documented and easy to implement.

## Document the following Vocabulary Terms

### Client ID

unique identifier

### Client Secret

Used to authenticate client and is only known by the server and client

### Authentication Endpoint

used to request access tokens or authorization

### Access Token Endpoint

used to get an access token or refresh token

### API Endpoint

the connection used to communicate with an API

### Authorization Code

allows you to send information, such as a request for an access token, to a secure resource

### Access Token

used for token-based authentication

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

bearer authentication, jwt, access tokens

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

sessions, extra layers of encryption for JWTs, securing JWTs

### What are you most excited about trying to implement or see how it works?

sessions and extra layers of encryption with JWTs

## Resources

[JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

[Intro to JWT](https://jwt.io/introduction/)

[Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

[jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)
