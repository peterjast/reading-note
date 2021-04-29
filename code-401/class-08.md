# Access Control (ACL)

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## When is Basic Authorization used vs. Bearer Authorization?

* Use basic to access API directly with username and password

* Bearer is more secure and requires two calls, one to get a token and one to get the data - bearer is preferred because of the extra security

## What does the JSON Web Token package do?

* allows you to use JSON Web Tokens to securely transfer data between two parties as JSON objects

## What considerations should we make when creating and storing a SECRET?

* a secret should be secure

* secrets should be encrypted

* secret should be visually different from id

## Document the following Vocabulary Terms

### encryption

* cryptographically turns data into a secret code that cannot easily be deciphered

### token

* a token is a thing that represents an object

### bearer

* a type of token used for authentication - represents the user

### secret

* a secret ket or passcode used to login or create a login/token

### JSON Web Token

JSON web tokens are used to securely transmit data between parties as JSON objects

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

RBAC, JWT, ACL

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

RBAC, ACL, cookies, sessions, extra layers of encryption for JWTs, securing JWTs

### What are you most excited about trying to implement or see how it works?

sessions, extra layers of encryption with JWTs, best practices related to auth, JWT, RBAC, ACL

## Resources

[RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

[5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

[wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)