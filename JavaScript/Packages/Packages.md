# JavaScript Packages

`npm install <NAME> --save-dev` installing package as dev dependency

`npm install <NAME>` installing new package 


## List of useful packages

`axios` browser - server communication

`json-server` development server for JS database

`express` backend server

`nodemon` development server

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