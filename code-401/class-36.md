# Application State with Redux

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Review, Research, and Discussion

### What are the advantages of storing tokens in “Cookies” vs “Local Storage”

One main advantage is that cookies are not accessible via javascript which makes it less vulnerable to cross site scripting attacks. Another advantage is that they are sent in every HTTP request.

### Explain 3rd party cookies

Third party cookies are set by a website that you are not currently on. Cookies that were stored via a site that you previously visited can be accessed by the site you are currently on.

### How do pixel tags work?

Pixel tags are single pixel images added to a web page that are served from an ad server's and used to access the cookie and record information about the visitor and their behavior on a site.

## Document the following Vocabulary Terms

### cookies

a small piece of data stored to a user's browser, which can be accessed an re-used later on for various reasons such as sending request's to a server

### authorization

authorization checks the credentials of a user and grants or denies access to resources

### access control

controlling what routes or actions a user has access to

### conditional rendering

rendering different UI components based on certain conditions being met

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

cookies, authorization, access control

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

auth and access control in react, pixel tags, cookies and redux

### What are you most excited about trying to implement or see how it works?

react cookies

## Preparation Materials

[Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

[worlds easiest guide to redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)

[testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

[Redux Docs](https://redux.js.org/)
