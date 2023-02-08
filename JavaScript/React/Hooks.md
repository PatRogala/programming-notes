# Hooks in React

```js
import { useEffect } from 'react'
```

```js
  useEffect(() => {
    console.log('effect')
    axios
      .get('http://localhost:3001/notes')
      .then(response => {
        console.log('promise fulfilled')
        setNotes(response.data)
      })
  }, [])
```

useEffect does something when something changes
if second argument is empty array `[]` then useEffect will trigger at first load of page

By default, effects run after every completed render, but you can choose to fire it only when certain values have changed.
