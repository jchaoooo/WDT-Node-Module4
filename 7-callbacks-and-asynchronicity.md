Questions

1. What is the difference between readdirSync and readdir?

`readdirSync` is a synchronous and blocking method. This means that we must wait until the code is done execute before it continues the next JavaScript execution. `readdir` on the other hand is asychronous and non-blocking.  This means that as this method is executing we can continue to the next javascript execution as `readdir` runs in the background.

2. What is the event loop and how does it handle asynchronous requests?

The event loop is where JavaScript runtimes contain a message queue which stores a list of messages to be processed and their associated callback functions. These messages are queued in response to external events (such as a mouse being clicked or receiving the response to an HTTP request) given a callback function has been provided. If, for example a user were to click a button and no callback function was provided – no message would have been enqueued.  In a loop, the queue is polled for the next message and when a message is encountered, the callback for that message is executed.

An asynchronous request has a call back as an argument so it can be removed from the execution stack while the request completes unblocking the stack to execute other code while we wait.  Once the request has been returned the callback is triggered, the pending operation moves to the event queue and once it is its turn it will finally be moved back to the execution stack to run.

3. Given the following code, specify whether the program is asynchronous and non-blocking or synchronous and blocking or synchronous and non-blocking.

Synchronous and blocking
```
const fs = require('fs');
const file = fs.readFileSync('foo.txt');
console.log(file.toString());
```

4. Given the following code, specify whether the program is asynchronous and non-blocking or synchronous and blocking or synchronous and non-blocking.

Asynchronous and non-blocking
```
const fs = require('fs');
fs.readFile('foo.txt', (err, file) => {
 if (err) throw err;
 console.log(file.toString());
});
console.log("test");
```

5. In what order will the console.log statements execute in the code below?

The order would be C, A, B
```
const fs = require('fs');
fs.readFile('foo.txt', (err, file) => {
 if (err) throw err;
 console.log("A");
 console.log("B")
});
console.log("C");
```

6. setTimeout is a JavaScript function which calls a function after a set amount of milliseconds. Given the following code, explain in what sequence the functions will run and why.

The sequence of functions would first run greeting, but since greeting contains `setTimeout` it will wait 100 milliseconds until it executes.  The greeting function is asynchronous so it will countdown in the background and the next function can execute.  Therefore the hello function will run and console.log `hello` and by this time greeting is executed console.log `friend`.  The final output would be `hello friend`

```
function greeting() {
 setTimeout(() => {
   console.log("friend");
 }, 100);
}

function hello(){
 console.log("hello");
}

greeting();
hello();
```

7. Create a function which utilizes a callback. Make sure to add console.log statements to understand when your callback function is called.

```
function doSomething(callback) {
  console.log('doSomething called');
  callback('stuff', 'goes', 'here');
  console.log('doSomething finished');
}

function foo(a, b, c) {
  console.log('foo called')
  console.log(a + " " + b + " " + c);
  console.log('Callback to foo finsished');
}

doSomething(foo);
```
