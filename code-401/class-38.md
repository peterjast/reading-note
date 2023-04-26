# Redux - Asynchronous Actions

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Review, Research, and Discussion

### How granular should your reducers be?

They should be as granular as possible in order to enhance UI performance. You should make as few components render on state change as possible.

### Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

I think this could be a pro or a con. Ideally, you want the fewest possible components to render on state change; however, there are definitely situations where this could be very helpful.

### Name a strategy for preventing the above

You could use redux-ignore or reduxr-scoped-reduce to ensure only specified reducers listen to an action. You should use very specific names for your actions.

## Document the following Vocabulary Terms

### store

A store is an object that holds the global state of your application.

### combined reducers

The combineReducers helper function combines multiple reducers into one function, which can be passed to createStore and allows you to easily access them throughout your application.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

redux, thunk, combined reducers

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

material ui, redux thunk, secure payments

### What are you most excited about trying to implement or see how it works?

secure payments

## Preparation Materials

[Async Actions](https://redux.js.org/advanced/asyncactions)

[Thunk Middleware](https://github.com/reduxjs/redux-thunk)

[Redux Thunk](https://alligator.io/redux/redux-thunk/)
