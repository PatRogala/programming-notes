## Component helper functions

Let's expand our Hello component so that it guesses the year of birth of the person being greeted:

```js
const Hello = (props) => {
  const bornYear = () => {
    const yearNow = new Date().getFullYear()
    return yearNow - props.age
  }

  return (
    <div>
      <p>
        Hello {props.name}, you are {props.age} years old
      </p>
      <p>So you were probably born in {bornYear()}</p>
    </div>
  )
}
```

If we examine our current code closely, we'll notice that the helper function is defined inside of another function that defines the behavior of our component. In Java programming, defining a function inside another one is complex and cumbersome, so not all that common. In JavaScript, however, defining functions within functions is a commonly-used technique.

## Destructuring
Before we move forward, we will take a look at a small but useful feature of the JavaScript language that was added in the ES6 specification, that allows us to destructure values from objects and arrays upon assignment.


Since props is an object
```js
props = {
  name: 'Arto Hellas',
  age: 35,
}
```

Destructuring makes the assignment of variables even easier since we can use it to extract and gather the values of an object's properties into separate variables:
```js
const { name, age } = props
```

```js
const Hello = (props) => {
  const { name, age } = props
  ...
}

// Into

const Hello = ({ name, age }) => {...}
```

## Stateful component
Next, let's add state to our application's App component with the help of React's state hook.

```js
import { useState } from 'react'

const App = () => {
  const [ counter, setCounter ] = useState(0)

  setTimeout(
    () => setCounter(counter + 1),
    1000
  )

  return (
    <div>{counter}</div>
  )
}

export default App
```

In the first row, the file imports the useState function
```js
import { useState } from 'react'

const [ counter, setCounter ] = useState(0)
//      name,    function                default
```


## Event handling
In React, registering an event handler function to the click event happens like this:

```js
const App = () => {
  const [ counter, setCounter ] = useState(0)

  const handleClick = () => {
    console.log('clicked')
  }

  return (
    <div>
      <div>{counter}</div>
      <button onClick={handleClick}>
        plus
      </button>
    </div>
  )
}

// shorter
<button onClick={() => setCounter(counter + 1)}>
  plus
</button>
```

## Complex state
```js
{ ...clicks, right: clicks.right + 1 }
```
creates a copy of the clicks object where the value of the right property is increased by one.
```js
const handleLeftClick = () =>
  setClicks({ ...clicks, left: clicks.left + 1 })

const handleRightClick = () =>
  setClicks({ ...clicks, right: clicks.right + 1 })
```

Conditional Rendering
```js
const History = (props) => {
  if (props.allClicks.length === 0) {
    return (
      <div>
        the app is used by pressing the buttons
      </div>
    )
  }
  return (
    <div>
      button press history: {props.allClicks.join(' ')}
    </div>
  )
}
```