1. What is npm and what does it do?

npm stands for Node.js Package Manager.  It puts modules in place so that node can find them and manages dependency conflicts intelligently.  It is configurable to support a wide variety of use cases.  It is commonly used to publish, discover, install and develop node programs.

2. What kind of information does package.json hold?

- name: the name of the module
- version: denotes the current version of the module
- description: human-readable description about the module
- keywords: a collection of keywords that can help identify a package, related modules and software and concepts
- main: direction to the entry point to the module
- license: the license of the module
- repository: an array that defines where the source code for the module lives
- scripts: takes an object with as many key/value pairs as desired to be used to run commands
- dependencies: tells us what dependencies the other modules that this module uses

3. Google another Node package. Using the demo directory run npm install <theNameOfThePackage> --save. Check the contents of your package.json file to make sure that the dependencies list the name of the Node package.

```npm install lodash --save
{
  "name": "demo",
  "version": "1.0.0",
  "description": "Demo for node.js setup.",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "demo"
  ],
  "author": "Jessica",
  "license": "ISC",
  "dependencies": {
    "express": "^4.16.3",
    "lodash": "^4.17.10"
  }
}
```
