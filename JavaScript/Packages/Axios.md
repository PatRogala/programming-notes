# Axios

It allows for easy browser - server communication

```js
import axios from 'axios'

const promise = axios.get('http://localhost:3001/notes')
console.log(promise)

const promise2 = axios.get('http://localhost:3001/foobar')
console.log(promise2)
```

A Promise is an object representing the eventual completion or failure of an asynchronous operation.

The promise is pending: It means that the final value (one of the following two) is not available yet.

The promise is fulfilled: It means that the operation has been completed and the final value is available, which generally is a successful operation. This state is sometimes also called resolved.

The promise is rejected: It means that an error prevented the final value from being determined, which generally represents a failed operation.

```js
const promise = axios.get('http://localhost:3001/notes')

promise.then(response => {
  console.log(response)
})
```