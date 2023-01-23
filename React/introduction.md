# Introduction to React

Creating new application
```
npx create-react-app part1
```

The application runs as follows
```
npm start
```

Simple code of index.js
```js
// src/index.js

import React from 'react'
import ReactDOM from 'react-dom/client'

import App from './App'

ReactDOM.createRoot(document.getElementById('root')).render(<App />)
```

Simple code of App component
```js
// src/App.js

const App = () => (
  <div>
    <p>Hello world</p>
  </div>
)

export default App
```

## Component

Defining component
```js
const App = () => (
  <div>
    <p>Hello world</p>
  </div>
)
```

Creating dynamic component
```js
const App = () => {
  const now = new Date()
  const a = 10
  const b = 20
  console.log(now, a+b)

  return (
    <div>
      <p>Hello world, it is {now.toString()}</p>
      <p>
        {a} plus {b} is {a + b}
      </p>
    </div>
  )
}
```
Any JavaScript code within the curly braces is evaluated and the result of this evaluation is embedded into the defined place in the HTML produced by the component.

## JSX

The layout of React components is mostly written using JSX
Under the hood, JSX returned by React components is compiled into JavaScript.
The compilation is handled by Babel. Projects created with create-react-app are configured to compile automatically
JSX is "XML-like", which means that every tag needs to be closed

```js
// bad
<br>

// good
<br />
```

## Multiple components

We can create multiple components and use them together
```js
const Hello = () => {
  return (
    <div>
      <p>Hello world</p>
    </div>
  )
}

const App = () => {
  return (
    <div>
      <h1>Greetings</h1>
      <Hello />
    </div>
  )
}
```

## props: passing data to components
```js
const Hello = (props) => {
  return (
    <div>
      <p>Hello {props.name}</p>
    </div>
  )
}
```
Now the function defining the component has a parameter props. As an argument, the parameter receives an object, which has fields corresponding to all the "props" the user of the component defines.

We define props as:
```js
const App = () => {
  return (
    <div>
      <h1>Greetings</h1>
      <Hello name='George' />
      <Hello name='Daisy' />
    </div>
  )
}
```

Also, keep in mind that React component names must be capitalized. If you try defining a component as follows:
