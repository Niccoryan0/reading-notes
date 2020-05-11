# Day 6 Readings

## Intro to Node.js
- Node.js is a runtime environment for JavaScript built off of Chrome's V8 Engine.
- The options for downloading it are to download binaries or a version manager, a version manager will download multiple version of Node and allow switching between them easily.
- Node already has excellent support for ES6 and beyond, so it's devoid of compatibility issues and allows use of the latest and most modern syntax.
- Node.js allows us to run JavaScript on the server, or back-end, and while it's not the first to attempt this, it is the first to get real traction. 
- As opposed to languages like Ruby and PHP, JavaScript will not block any code execution while I/O operations are taking place, it will instead register a callback function, finish the I/O operation, execute the callback and the continue on to the next event.
- Some downsides: since it's run on a single thread, blocking I/O calls should be avoided, and CPU intensive opersation should be handed off to a worker thread (new to Node.js v10.5), and errors need to be handled carefully. Additionally, some don't like the callback-based system, as some believe native Asynchoronous JS can be a nightmare(see: callbackhell.com) 
- One other slight downside (in some people's view) is how slim Node.js is out-of-box, requiring other libraries or frameworks to make building a web app easier, as opposed to frameworks like Rails or Laravel which are much more flushed out initially.
- Speed and scalability are big factors, but so is just the ability to write everything in one kind of code, and not need to switch for back-end work to a different language. It also speaks JSON, which is the largest data exchange format on the web, and MongoDB and other database's main method for data storage. 