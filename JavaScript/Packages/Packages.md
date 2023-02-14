# JavaScript Packages

`npm install <NAME> --save-dev` installing package as dev dependency

`npm install <NAME>` installing new package 


## List of useful packages

`axios` browser - server communication

`json-server` development server for JS database

`express` backend server

`nodemon` development server

`morgan` middleware for logging

`cors` cors middleware for cross origin requests

`mongoose` mongoDB for node

`eslint` static code analyzer

`jest` testing library

`cross-env` env variables for windows users

`supertest` package to help us write our tests for testing the API.

## List of useful commands and settings

```json
{
  // package.json
  "scripts": {
    "server": "json-server -p3001 --watch db.json", // server for json database
  },
}
```

then run for example

`npm run <SCRIPT>`


`"proxy": "http://localhost:3001"` allows us to use proxy for development frontend