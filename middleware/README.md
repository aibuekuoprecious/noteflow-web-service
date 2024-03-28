## Error Handler Middleware

This module defines an error handler middleware function for Express.js applications. It requires the `logEvents` function from the `logger` module to log errors. 

- When an error occurs, the middleware logs the error message, method, URL, and origin in a log file named `'errLog.log'`, and also logs the error stack to the console.
- It sets the HTTP status code of the response to either the existing status code or 500 (server error).
- Finally, it sends a JSON response containing the error message to the client.

This middleware function is then exported to be used in an Express.js application for handling errors.

## Logging Events

This module contains functions related to logging events in an Express.js application.

- `logEvents`: An asynchronous function that takes a message and a log file name as parameters. It formats the current date and time, generates a unique identifier using UUID, creates a log item combining the date, time, UUID, and message. Then, it checks if the logs directory exists and creates it if not. Finally, it appends the log item to the specified log file.
  
- `logger`: A middleware function that logs incoming requests. It calls `logEvents` with the request method, URL, and origin, and logs the request method and path to the console. It then calls `next()` to pass control to the next middleware function in the chain.

Both functions are exported to be used in my Express.js application for logging purposes.