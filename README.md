# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Node.js Express.js applications: unhandled promise rejections in asynchronous route handlers.

The `bug.js` file contains the buggy code.  The application starts a server, but if the asynchronous operation (`someAsyncOperation`) fails, the error is silently swallowed.  The console shows the error, but the application doesn't gracefully handle the failure, and it doesn't respond to the client request.

The `bugSolution.js` file provides a corrected version that handles the promise rejection appropriately and sends a proper error response to the client.