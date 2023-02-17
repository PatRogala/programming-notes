# Jest

Jest requires one to specify that the execution environment is Node. This can be done by adding the following to the end of package.json:

```json
{
 // package.json
 "jest": {
   "testEnvironment": "node"
 }
}
```

Tests example template:

```js
const reverse = require('../utils/for_testing').reverse

test('reverse of a', () => {
  const result = reverse('a')

  expect(result).toBe('a')
})

test('reverse of react', () => {
  const result = reverse('react')

  expect(result).toBe('tcaer')
})

test('reverse of releveler', () => {
  const result = reverse('releveler')

  expect(result).toBe('releveler')
})
```

We need to add config to eslint

```js
// eslintrc.js
module.exports = {
  'env': {
    'jest': true,
  },
  // ...
}
```

Running single file

`npm test -- tests/note_api.test.js`

Running single test

`npm test -- -t "a specific note is within the returned notes"`

Running tests with name including `notes`

`npm test -- -t 'notes'`