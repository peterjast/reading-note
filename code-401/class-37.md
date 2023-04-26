# Redux - Combined Reducers

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Review, Research, and Discussion

### Why choose Redux instead of the Context API for global state?

It is ideal for larger applications and dealing with frequent state updates because it only re-renders updated components.

### What is the purpose of a reducer?

The purpose of a reducer is to evaluate the type of an action and return a new copy of state with any applicable changes.

### What does an action contain?

An action contains an object literal with a type and payload.

### Why do we need to copy the state in a reducer?

We need to copy the state in a reducer because in Redux, state is immutable and read-only.

## Document the following Vocabulary Terms

### immutable state

A state that is essentially read-only and can't be changed.

### time travel in redux

Time travel allows you to step forward and backwards through changes made to state. This allows you to manage your application's lifecycle and see exactly what changes occur each time an event occurs in your application.

### action creator

Action creators are essentially contructor functions for actions, which are object's with a type and payload.

### reducer

Reducers are pure functions that evaluate a type of action and return a new copy of state.

### dispatch

Action creators are dispatched to components, which allows components to trigger state changes.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

cookies, authorization, access control

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

material ui, redux, secure payments

### What are you most excited about trying to implement or see how it works?

payments

## Preparation Materials

[Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)

[Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)

[Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)
