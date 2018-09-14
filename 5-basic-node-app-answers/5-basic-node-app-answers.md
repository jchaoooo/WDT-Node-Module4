Exercises

Create a file called basic_node_app_answers.txt and put your answers in the file.

1. What is a Node module?

2. What is the main difference between exports and module.exports?

3. Why is using exports recommended?

Programming Questions

Before you begin, make sure you have greeting.js and main.js in the following states:
```
greeting.js
exports.greetingEnglish = function(){
 console.log("Hello");
}

exports.greetingJapanese = function(){
 console.log("Konichiwa");
}
```
```
main.js
const greetings = require("./greeting.js");

// "Hello"
greetings.greetingEnglish();

// "Konichiwa"
greetings.greetingJapanese();
```

4. Add two more functions, greetingSpanish and greetingIcelandic, in greeting.js.

5. Utilize the two functions in main.js just like greetingEnglish and greetingJapanese.

6. Create another Node module and import it into main.js. Your Node module should have at least two functions within it. Then, call a function from your Node module in main.js.

Submit basic_node_app_answers.txt and your three .js files.
