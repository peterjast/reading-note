# Hooks API

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Review, Research, and Discussion

### Why do we not need more .html pages in a multi-page React app?

Multi-page React apps are still technically single page applications. There is only one index.html file and then the pages of the application are rendered using react-router-dom.

### If we wanted a component to show up on every page, where would we put it and why?

* Outside the ```<BrowserRouter/>```

* Inside the ```<BrowserRouter />```, outside a ```<Route />```

* Inside a ```<Route />```

We would put it inside the ```<BrowserRouter />```, outside a ```<Route />``` because BrowserRouter wraps our entire application. If you want a component to show up on every page, such as a header or footer, but you want to render different content, you would want to put it outside of a route. Otherwise, you would have to include it inside of every route.

### What does props.children contain?

The special React component property, props.children can contain one element, multiple elements or no elements. It contains any child elements defined within a component and is used a s a generic template.

## Document the following Vocabulary Terms

### Composition

A development pattern based on the component model in React which allows reusability and state management through components and props.

### Children / Child Components

A child component is a component that is a specific part of a parent component. This relationship allows for data or props to be passed between the components.

### Hash Routing

Hash routing is meant to support legacy browsers and uses the hash portion of a URL to keep your UI in sync with the URL.

### Link Routing

Link routing matches a URL and then renders the specific components for that page.

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

Hash Routing, Link Routing, props.children

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

props.children, hooks, effects hook

### What are you most excited about trying to implement or see how it works?

hooks and functional components

## Preparation Materials

[making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)

[the state hook](https://reactjs.org/docs/hooks-state.html)

[hooks api](https://reactjs.org/docs/hooks-overview.html)

[hooks api reference](https://reactjs.org/docs/hooks-reference.html)

[effects hook](https://reactjs.org/docs/hooks-effect.html)
