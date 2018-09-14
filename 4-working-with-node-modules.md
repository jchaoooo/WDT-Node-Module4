Questions
1. How do you import a module?

To import a module you can either manually add the module as a dependency to the package.json, then run `npm install` or run `npm install --module-name save`.  Then to use the module you would need to require it on the top of your file `const module-name = require('module-name')`;

2. What JavaScript statement do you use to export a module?

A simple javascript statement to export a module would be `module.exports = 'insert what you want exported'`


Online Research Questions

1. Are there other ways to export a module?

There are different types of modules that can be exported, here are a few:
- Export a simple string  `module.exports = 'Hello world'`
- Export an object `module.exports.SimpleMessage = 'Hello world'`
- Attach a function to exports object `module.exports = function(msg) {console.log(msg); }`

2. What are ES6 modules and how do they differ from the module we created in this checkpoint?

Javascript has had modules for a long time.  However they were implemented using libraries not built into the language.  ES6 is the first time Javascript has built-in modules.  ES6 modules are stored in files.  There is exactly one module per file and one file per module.  Everything inside an ES6 module is private by default, and runs in strict mode.  Public variables, functions and classes are exposed using `export`. `import` is then used to pull items from a module into another script or module.

As you can see the module created in this checkpoint is not an ES6 module since we are using `module.exports` and `require` for exporting and importing.


Code Challenge

Create a Github repository called Terminal Command and add the code from this checkpoint. Implement the touch and mkdir commands to the terminal-commands module:

[link to repository here](https://github.com/jchaoooo/terminal-commands)

```
terminal-commands.js
const fs = require('fs');

module.exports.ls = () => {
  fs.readdir('./', (err, files)=>{
    const filesToString = files.reduce((acc, file) => {
      return `${acc} ${file} `;
    }, '');
    console.log(filesToString);
  });
};

module.exports.touch = () => {
  fs.writeFile('terminal-commands.js', (err) => {
    if (err) throw err;
    console.log('File Created');
  })
};

module.exports.mkdir = () => {
  fs.mkdir('./terminal-commands', function(err) => {
    if (err) throw err;
    console.log('Directory Created');
  })
};
```
