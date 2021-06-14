# React Native

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Review, Research, and Discussion

### Compare and Contrast Redux Toolkit with Redux “Ducks”

* Redux Toolkit(RTK) is an opinionated toolset for efficient Redux development. RTK makes store setup, creating reducers and immutable state logic easier with included utilities. Common Redux addons are built-in and good defaults for store setup are provided. RTK allows you to work with immutable update logic and create slices of state. With RTK, you can do more with less code.

* Ducks bundle reducers, action types and actions into one file. When you organize them by type, going back and fourth between files can be repetitive and bothersome, which can be solved by modularizing them into a duck. A duck is a clean, clear and comprehensible file for optimized state management that contains all of the functionality in one place.

### What is the principle advantage of Redux Toolkit

The principle advantage of Redux Toolkit is efficiency. It provides various tools and addons to help developers with store setup, creating reducers, and even allows you to write mutative immutable update logic and automatically create slices of state. The utilities it provides out of the box speed up the development process and allow developers to write code more efficiently.

## Document the following Vocabulary Terms

### redux toolkit slices

Redux toolkit slices are objects containing automatically generated action creators and types based on initial state and reducers. A slice can be created using the createSlice function, which accepts inital state, an object containing reducer functions and a slice name. The createSlice function returns action creators and action types that correspond to the reducers and state in an object that contains a name property, reducer property, actions property and caseReducers property. A corresponding action creator is generated using createAction for each reducer function and is included in the actions property with the same function name.

```javascript
{
    name : string,
    reducer : ReducerFunction,
    actions : Record<string, ActionCreator>,
    caseReducers: Record<string, CaseReducer>
}
```

### namespace

In regards to Redux Toolkit and slices, a namespace is the name property of a slice, the object returned by the createSlice() function. Actions are generated with the namespace or the slice name that was passed as an argument as well as the name of the corresponding reducer function, which is the key in the reducers object that it was passed. The createSlice() function namespaces all actions goint with a slice, so the type for an action generated with the namespace of counter and a reducer named increment would be counter/increment

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

Redux Toolkit, Ducks, Slices

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

Redux Toolkit, Ducks, Slices

### What are you most excited about trying to implement or see how it works?

Ducks

## Preparation Materials

[Getting Started with React Native](https://facebook.github.io/react-native/docs/getting-started)

[React Native Basics](https://facebook.github.io/react-native/docs/tutorial)

[React Native](https://facebook.github.io/react-native/)

[Expo](https://expo.io/)

[Expo Snack](https://snack.expo.io/)

[Ejecting](https://docs.expo.io/versions/latest/expokit/eject)
