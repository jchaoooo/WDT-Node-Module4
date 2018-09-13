QUESTIONS

1. Why is the fs core module important for Node development?

The `fs` module provides an API for interacting with the file system.  It provides basic file system functionality needed by developers and apps.  For instance the ability to read files, create files, update files, delete files and rename files.

2. What is the difference between sync and non-sync methods in the fs module?

Synchronous means that the code runs in sequential order waiting for each line of code to finish executing before starting the next.  This is why sync code is called "blocking".  The execution of subsequent lines of code will be blocked from running until the current operation is complete.  Asynchronous on the other hand is the opposite.  The code does not wait for the current line to execute before moving on to run the next line.  Thus, asynchronous is called "non-blocking" because it does not block subsequent lines from running waiting for the current operation to finish.

3. Why are modules used?

Modules are the node equivalent of libraries in the front-end.  IT helps us deal with the complexity of large software programs and systems by decomposition into smaller pieces.  Modules and libraries are also used to save time by leveraging the effort of other developers.  We dont waste time reinventing the wheel when a perfectly fine solution already exists.  Instead of including everything upfront with a large program full of features and code we never need, using a library/module approach allows us to include the items we truly require/want.

4. Why are libraries such as fs used in Node programming?

Many of the node libraries are used to help bridge the gap between operation of javascript client-side in the browser and what we need to have it do in a server environment.

CODE PRACTICE

1. Create a Github repo called simple-http-node-server. Create an HTTP server on port 3000 with a request handler that creates a file named hello-world.txt. You will be using the fs module to do this. Write the content: "Hello to this great world" to the hello-world.txt file. Please submit your finished code in your submission.

```
const http = require('http');
const port = 3000;
const fs = require('fs')

const requestHandler = (request, respond) => {
    fs.writeFile('hello-world.txt', 'Hello to this great world!', 'utf8', (err)) => {
      if(err) throw err;
      console.log('success')
    });
    response.end('Handling a request on port ${port}')
};

const server = http.createServer(requestHandler);

server.listen(port, (err) => {
  if(err) {
    return console.log('You have an error: ${err}');
  }

  console.log('server is listening on port ${port}');
  });
  ```
