# Package.json

We can create a new initial project using `npm init`

This will create our `package.json` file

```json
// package.json
{
  "name": "backend",
  "version": "0.0.1",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Matti Luukkainen",
  "license": "MIT"
}
```

we can add our new `"scripts"` to enchance work

```json
"start": "node index.js", // starting server in prod mode
"dev": "nodemon index.js", // server in dev mode
"lint": "eslint .", // check eslint for errors
"test": "jest --verbose" // run tests for app
```