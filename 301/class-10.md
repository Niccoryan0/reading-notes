# Day 10 Readings


## The Call Stack defined on MDN
- The Call Stack is a mechanism which can keep track of an interpreter's place in a script that calls multiple functions, keeping track of the currently running function and any internal functions for it.
### Straight from the docs:
- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

## Understanding the JavaScript Call Stack
- Async programming uses the call stack very regularly. When we have a callback function, event loop and task queue, the call stack acts upon the callback function after the event loop pushes it to the stack.
- A call stack uses LIFO (Last In, First Out) principles to store and manage function calls. It is single threaded, so i tcan only handle on responsibility at a time, it executes synchronously (hence it's use in asynch programming), a function call creates a "stack frame" in temporary memory.

## JavaScript error messages
- Reference Errors
: Using a variable not yet declared, or using const and let sometimes due to weird hoisting quirks. This is why JS devs frequently declare all variable at the top and assign them later on.
- Syntax Errors
: Literally just syntax, something is written incorrectly and the only real fix is just fixing the syntax.
- Range Errors
: Manipulating an object with some length property and giving an invalid length will throw this error. 
- Type Errors
: Types being accessed or manipulared are incompatible, commonly pops up when trying to access properties of an object that aren't defined.
- Debugging involves console.log() ing variables to confim their values, or by using Chrome or an IDE's developer tools, such as adding breaks or debuggers.
- Handling errors involves using try and catch to "gracefully fallback to a sefault state in case of an error".
- Tools to avoid errors: quokka to evaluate code as you type, and eslint to make a style guide is being consistently followed, additionally there is TypeSctipt, a more structured way to write JavaScript that helps to avoid errors.