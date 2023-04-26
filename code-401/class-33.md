# Context API

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## Review, Research, and Discussion

### Describe use cases for useMemo() and useReducer()

* useMemo(): You’re noticing a component’s render is frustratingly slow, and you’re passing a calculation to an unknowable number of children, such as when rendering children using Array.map() or your app often becomes unresponsive because you’re fetching a large amount of data, and having to transform it into a usable format. [source](https://maxrozen.com/understanding-when-use-usememo)

* useReducer(): useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks. [source](https://reactjs.org/docs/hooks-reference.html#:~:text=useReducer%20is%20usually%20preferable%20to,dispatch%20down%20instead%20of%20callbacks.)

### Why do custom hooks need the use prefix?

React has established this as a naming convention, so it makes it obvious that it is a hook. This is a best practice that should be followed to enhance code readability.

### What do custom hooks usually do?

React hooks are used for reusable logic, which cleans up your code base and makes it easier to apply the same functionality between components.

### Using any list of custom hooks, research and name one that you think will be useful in your applications

I found some very useful custom hooks in the article [5 Useful and Modern Custom Hooks for your React App](https://dev.to/viclafouch/5-useful-and-modern-custom-hooks-for-your-react-app-3dl). One that I found particularly useful was useViewport. This hooks allows you to manage the viewport of a user's device. You can retrieve the width of the screen and whether it corresponds to a mobile device, tablet or desktop.

```javascript
// hooks/use-viewport.js
import { useState, useEffect } from 'react'

export const MOBILE = 'MOBILE'
export const TABLET = 'TABLET'
export const DESKTOP = 'DESKTOP'

const getDevice = width => {
  if (width < 768) return MOBILE
  else if (width < 992) return TABLET
  else return DESKTOP
}

export function useViewport() {
  const [viewport, setViewport] = useState({
    width: window.innerWidth,
    device: getDevice(window.innerWidth)
  })

  useEffect(() => {
    const handleResize = () =>
      setViewport({
        width: window.innerWidth,
        device: getDevice(window.innerWidth)
      })
    window.addEventListener('resize', handleResize)
    return () => {
      window.removeEventListener('resize', handleResize)
    }
  }, [])

  return { viewport }
}
```

### Describe how a hook that fetches API data might work

You could use axios, superagent or fetch to fetch API data and it's likely that you would want to use them with the useEffect hook in order to fetch data when a page loads or re-renders.

## Document the following Vocabulary Terms

### reducer

Can be used in place of useState and is useful when dealing with complex state logic. It can be used to manage state based on defined actions.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

custom hooks, useMemo, useReducer

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

custom hooks, reducer, redux

### What are you most excited about trying to implement or see how it works?

context api

## Preparation Materials

[context api](https://reactjs.org/docs/context.html)

[hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)

[react context links](https://github.com/diegohaz/awesome-react-context)
