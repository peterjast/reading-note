# **Introduction to React and Components**

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## React Tutorial

Code samples are from this article: [https://reactjs.org/tutorial/tutorial.html](https://reactjs.org/tutorial/tutorial.html)

### Getting Started

Using integrated toolchains when creating a new React app helps with the following:

* Scaling to many files
* The use of npm third-party libraries
* Detecting mistakes
* Being able to live-edit CSS and JS
* Optimal output for production

#### Recommended Toolchains

* Use **Create React App** to create a new single-page app
* Use **Next.js** to build server-rendered websites with Node.js
* Use **Gatsby** to build static content-oriented websites
* Try using more flexible toolchains to build component libraries or integrate with an existing code base

> npx create-react-app  *creates new project*
>
> npm start *compiles source code and runs app on local host*
>
> npm run build *creates optimized build of your app*

### What is React?

"*React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex Uis from small isolated pieced of code called components.*" - from the React tutorial found [here](https://reactjs.org/tutorial/tutorial.html)

#### React.Component subclasses

Use components to tell React what to display on the screen. React efficiently updates and re-renders components when data changes.

```javascript
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

// Example usage: <ShoppingList name="Mark" />
```

ShoppingList is a **React component class**, or **React component type**.

A component takes in *props* as parameters. A heirarchy of views to display via the *render* method is returned.

The *render* method returns a **React element**, a description of what to render.

**JSX** is a special syntax that makes these structures easier to write. Example:

```javascript
return React.createElement('div', {className: 'shopping-list'},
    React.createElement('h1', /* ... h1 children ... */),
    React.createElement('ul', /* ... ul children ... */)
);
```

### Passing Data Through Props

```javascript
class Board extends React.Component {
  renderSquare(i) {
    return <Square value={i} />;
  }
}
```

```javascript
class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {this.props.value}
      </button>
    );
  }
}
```

## React Docs - Hello World

Code Sample from [https://reactjs.org/docs/hello-world.html](https://reactjs.org/docs/hello-world.html)

```javascript
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

## React Docs - Introducing JSX

Code Samples from [https://reactjs.org/docs/introducing-jsx.html](https://reactjs.org/docs/introducing-jsx.html)

```javascript
const element = <h1>Hello, world!</h1>;
```

This tag syntax is JSX, a syntax extension to JavaScript used with React to desribe the display of the UI.

JSX produces **React elements** and is helpful as a visual aid for working with UI in JavaScript.

### Embedding Expressions in JSX

```javascript
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

Use curly braces to embed valid JavaScript expressions.

```javascript
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

### JSX is an Expression Too

JSX expressions evaluate to JavaScript objects after compilation, so you can use JSX inside conditionals, loops, variable assignments, arguments, and return it from a function.

```javascript
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```

### Specifying Attributes with JSX

Using quotes and string literals:

```javascript
const element = <div tabIndex="0"></div>;
```

Using an embedded JavaScript expression:

```javascript
const element = <img src={user.avatarUrl}></img>;
```

**Important:** *React DOM uses camelCase: className, tabIndex, etc.*

### Specifying Children with JSX

You can close empty tags immediately:

```javascript
const element = <img src={user.avatarUrl} />;
```

JSX tags can contain children:

```javascript
const element = (
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you here.</h2>
  </div>
);
```

### JSX Prevents Injection Attacks

React DOM escapes JSX embedded values before rendering, so anything not explicitly written in your code can never be injected. Before being rendered, everything is converted to a string, which helps prevent injection attacks and makes embedding user input in JSX safe.

```javascript
const title = response.potentiallyMaliciousInput;
// This is safe:
const element = <h1>{title}</h1>;
```

### JSX Represents Objects

JSX is compiled down to React.createElement() calls, so these two examples create identical objects.

```javascript
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```

```javascript
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

React.createElement() creates an object called a **React element**, a desription of what you want to be displayed. React uses these objects to construct and update the DOM.

```javascript
// Note: this structure is simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```

## React Docs - Rendering Elements

Code Samples from: [https://reactjs.org/docs/introducing-jsx.html](https://reactjs.org/docs/introducing-jsx.html)

**React elements** are the smallest building blocks of your application and describes what you want displayed.

```javascript
const element = <h1>Hello, world</h1>;
```

### Rendering an Element into the DOM

Pass a react element and root DOM node to ReactDOM.render() to render the element.

```javascript
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

### Updating the Rendered Element

**React elements** are *immutable*.

```javascript
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```

## React Docs - Components and Props

Code Samples from: [https://reactjs.org/docs/components-and-props.html](https://reactjs.org/docs/components-and-props.html)

Use components to split UI into reusable pieces. Like JavaScript functions, components accept inputs called **props** and return React elements.

### Function and Class Components

Define components using a JavaScript function or an ES6 class.

Function Component:

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

Class Component:

```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

### Rendering a Component

When an elements represents a user-defined component, React passes JSX attributes and childre to this component as a **props** object.

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;
ReactDOM.render(
  element,
  document.getElementById('root')
);
```

### Composing Components

Components can be referred to in the output of other components, which allows the same component abstraction for any level of the view heirarchy.

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

### Extracting Components

Split components into smaller components

```javascript
function Comment(props) {
  return (
    <div className="Comment">
      <div className="UserInfo">
        <img className="Avatar"
          src={props.author.avatarUrl}
          alt={props.author.name}
        />
        <div className="UserInfo-name">
          {props.author.name}
        </div>
      </div>
      <div className="Comment-text">
        {props.text}
      </div>
      <div className="Comment-date">
        {formatDate(props.date)}
      </div>
    </div>
  );
}
```

Extracting an Avatar component and a UserInfo Component

```javascript
function Avatar(props) {
  return (
    <img className="Avatar"
      src={props.user.avatarUrl}
      alt={props.user.name}
    />
  );
}

function UserInfo(props) {
  return (
    <div className="UserInfo">
      <Avatar user={props.user} />
      <div className="UserInfo-name">
        {props.user.name}
      </div>
    </div>
  );
}

function Comment(props) {
  return (
    <div className="Comment">
      <UserInfo user={props.author} />
      <div className="Comment-text">
        {props.text}
      </div>
      <div className="Comment-date">
        {formatDate(props.date)}
      </div>
    </div>
  );
}
```

Having a lot of reusable components pays off in large apps. If it is used several times or complex, it should be extracted to a separate component.

**Props are Read-Only and all components must act like pure functions with respect to their props.**

## Resources

[React Tutorial through 'Passing Data Through Props](https://reactjs.org/tutorial/tutorial.html)

[React Docs - hello world](https://reactjs.org/docs/hello-world.html)

[React Docs - introducing JSX](https://reactjs.org/docs/introducing-jsx.html)

[React Docs - rendering elements](https://reactjs.org/docs/rendering-elements.html)

[React Docs - Components and props](https://reactjs.org/docs/components-and-props.html)
