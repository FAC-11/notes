# Error handling in Node
This is a summary of what I took to be the most relevant points from the
[Joyent error
handling](https://www.joyent.com/node-js/production/design/errors) resource.

## Asynchronous error handling
Most errors in node are operational errors in asynchronous functions. For
these, you should take a callback as an additional argument and pass the error
to the callback (using the **error-first callback** approach - e.g. node `fs`
module). 

## Synchronous error handling
The next most common case is operational errors in synchronous functions, e.g.
`JSON.parse`, or **invalid user input**. For these you can either throw the error
or return it. Throwing the error is more common.

Synchronous and aysnchronous error handling methods **should not be combined**
within a function.

- **Operational error** are not an issue with the code but represent an issue
elsewhere - e.g. out of memory, network connection issue...
- **Programmer errors** are bugs in the code. Programmer errors should not be
handled, as they are bugs which should be fixed.

## Resources
[Joyent - Error
Handling](https://www.joyent.com/node-js/production/design/errors)
