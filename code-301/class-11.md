# **Authentication**

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## What us OAuth?

* OAuth allows is widely accepted and lets websites and services share assets among users

* open authorization framework

* single sign-on (SSO) - one of the challeneges for personal computer networks

* access among multiple computers

* OAuth allows users to use password, phone digital certificate, biometric identity, two-factor authentication, multi-factor authentication SSO solution

### OAuth defintion

* open standard authorization protocol

* framework describing how servers and services safely allow authentication to their assets without sharing intitial single logon credential

* secure, third-party, user-agent, delegated authorization

* OAuth 2.0 is a framework

### How OAuth Works

1. website connects to second website using OAuth on behalf of user

1. second site generates token and secret unique to transaction and parties involved

1. gives token and secret to client software

1. software presents token and secret to authorization provider

1. client may be asked to authentication, then asked to approve authorization transaction

1. user approves transaction

1. user given access token

1. user gives access token to first website

1. use sees completed transaction

* OAuth isn't first authentication systen for users, but is widely adopted and works across the web

### OAuth 2.0

* no internet-wide authentication standards

* drastic changes from 1.0 to 2.0

* 2.0 is less sercure and more complex

* token expiration

* not compatible with version 1

* doesn't define or support encryption, signature, client verification or client binding

* TLS(transport layer security) can provide protections, but its up to devs to require its use

## Authentication and Authorization Flows

* Auth0 uses OpenID Connect Protocol (OIDC) and OAuth2.0 Authorization Framework for authentication and authorization to access protected resources

* Auth0 easily supports different flows in apps and APIs

* **Authentication** and **authorization** are fundamentally different functions

* **Authentication** verifies who a user is

* **Authorization** verifies what user has access to

* access to resources is protected by authentication and authorization

### **AUTHENTICATION**

* is user who they claim to be?

* makes user validate credentials

* done before authorization

* transmits info throguh ID Token

* governed by OIDC(OpenID Connect) protocol

### **AUTHORIZATION**

* what can a user access?

* uses policies and rules to verify if access is allowed

* done after authentication

* transmits info through Access Token

* governed by the OAuth 2.0 framwork

### Authorization Code Flow

* regular web apps are server-side

* source code is not publicly exposed

* authorization code flow - exchanges Authorization Code for a token

[Authorization Code Flow](https://auth0.com/docs/flows/authorization-code-flow)

[Add Login Using the Authorization Code Flow](https://auth0.com/docs/flows/add-login-auth-code-flow)

[Call API Using the Authorization Code Flow](https://auth0.com/docs/flows/call-your-api-using-the-authorization-code-flow)

![auth-sequence](https://images.ctfassets.net/cdy7uua7fh8z/2nbNztohyR7uMcZmnUt0VU/2c017d2a2a2cdd80f097554d33ff72dd/auth-sequence-auth-code.png)

### Authorization Code Flow with Proof Key for Code Exchange (PKCE)

* single-page apps have special challenges

[Authorization Code Flow with PKCE](https://auth0.com/docs/flows/authorization-code-flow-with-proof-key-for-code-exchange-pkce)

[Add Login Using the Authorization Code Flow with PKCE](https://auth0.com/docs/flows/add-login-using-the-authorization-code-flow-with-pkce)

[Call API Using the Authorization Code Flow PKCE](https://auth0.com/docs/flows/call-your-api-using-the-authorization-code-flow-with-pkce)

### Implicit Flow with Form Post

* intended for public clients or applications unable to stoe client secrets

[Implicit Flow with Form Post](https://auth0.com/docs/flows/implicit-flow-with-form-post)

[Add Login Using the Implicit Flow with Form Post](https://auth0.com/docs/flows/add-login-using-the-implicit-flow-with-form-post)

[Authenticate SPAs with Cookies](https://auth0.com/docs/sessions/cookies/spa-authenticate-with-cookies)

## Resources

[What is OAuth? How the Open Authorization Framework Works](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

[Auth0 Docs - Authentication and Authorization Flows](https://auth0.com/docs/flows)

### Additional Resources

[Auth0 React SDK for Single Page Apps](https://auth0.com/docs/libraries/auth0-react)
