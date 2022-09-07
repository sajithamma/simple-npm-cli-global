# How to write a NPM CLI package like decentraland npm (dcl)

## Use node to create a global command line interface (CLI)

```bash

npm install -g <your-package-name>

```

## First Step: Edit package.json
### Add "bin" parameter and point to a javascript file, eg: command.js

```javascript

{
  "name": "mycommand",
  "version": "1.0.0",
  "description": "",
  "main": "cli.js",
  "bin": {
    "mycommand": "cli.js"
  },
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}

```

## cli.js file should look like this

```javascript

#!/usr/bin/env node

console.log('hello');


```