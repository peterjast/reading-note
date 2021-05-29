# Custom Hooks

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Review, Research, and Discussion

### What does a component’s lifecycle refer to?

React components have a lifecycle consisting of three phases:

1. *mounting* - when a component is rendered to the DOM

1. *updating* - when a component is updated

1. *unmounting* - when a component is removed from the DOM.

### Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

You sometimes need to "wrap" functions in useCallback when called from within useEffect because it helps avoid regeneration of functions when a component re-renders, so when specifying a function as a dependency of useEffect, you would "wrap" functions in useCallback so that the function won't be recreated and useEffect won't be triggered every time the component renders.

### Why are functional components preferred over class components?

They're lightweight and easier to use and understand. You don't need to use the this keyword and they make React applications more performant.

### What is wrong with the following code?

```javascript
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

In the provided code, useEffect shouldn't be used inside of a for loop. There are two rules that need to be followed when usign React hooks. Hooks should only be called at the top level and you should only call them from React functions.

## Document the following Vocabulary Terms

### state hook

A react hook, useState, that lets you add state to functional components.

### effect hook

A react hook, useEffect, that allows you to express side effects after a component renders.

### reducer hook

A react hook that is an alternative to use State. The useReducer hook accepts a reducer of type (state, action) => newState, and returns current state with a dispatch method.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

useState, useEffect, useReducer

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

custom hooks, async hooks, useReducer hook

### What are you most excited about trying to implement or see how it works?

hooks and functional components

## Preparation Materials

### Authoring

[custom hooks - all you need to know](https://www.telerik.com/blogs/everything-you-need-to-create-a-custom-react-hook)

[async hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)

[useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)

[react custom hooks](https://reactjs.org/docs/hooks-custom.html)

### Hooks Lists/Collections

[use hooks](https://usehooks.com/)

[hooks list](https://github.com/rehooks/awesome-react-hooks)

[10 essential react hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)
