1. In your own words highlight the differences in functionality and purposes Client-Side and Server-Side code serves in a full-stack web application.

The client-side (browser) is to render web pages and all it's looks and styles.  The purpose of the server is to serve the code for those pages.  In terms of function, the client-side sends requests to the server, retrieves data from it, and interacts with local storage(cookies) while the server responds to requests, processes user input and interacts with permanent storage (database).  The browser has a window and document object, the server does not.  The client-side interfaces with HTML and the DOM where the server does not.  The client side uses AJAX to make HTTP requests where the server makes them directly.

2. What explains Nodes' rise in popularity and use? What does "Isomorphic JavaScript programming" mean? Provide some real-world examples not listed in this checkpoint of companies using Node.js.

Node's rise in use is due to the improved developer satisfaction and productivity, and increased application performance.  Coding in the same language frontend and backend eliminates handling and translating date and currency formatting, form validations, and routing logic written in a different language.

Isomorphic JavaScript programming allows developers to write and execute the same code in the client and server.  The client and server can now collaborate in a way that wasn't possible before and therefore address and improve upon some of the shortcomings each side previously had.  Another benefit is that there is less code to write for the developers and code redundancy can be avoided as the client and server can now share code.  Development times are reduced and testing is more efficient because developers no longer have to code the same functionality in two different programming languages for the client and server. Examples of companies using Node.js are NASA, Uber, PayPal, Trello and LinkedIn.

3. Draw a diagram of a full-stack web application and its key components.
![Link to Diagram](https://github.com/jchaoooo/WDT-Node-Module4/blob/master/1-full-stack-app-diagram.JPG)
