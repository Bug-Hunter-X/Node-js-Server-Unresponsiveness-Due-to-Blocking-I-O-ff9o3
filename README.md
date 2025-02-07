# Node.js Server Unresponsiveness Due to Blocking I/O

This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by blocking I/O operations.  The `server.js` file contains code that simulates a long-running task within the request handler, effectively blocking the event loop and preventing the server from responding to other requests.

The solution, provided in `serverSolution.js`, showcases how to handle such scenarios using asynchronous patterns (e.g., `setTimeout`, `process.nextTick`, or Promises).  This prevents blocking the event loop and keeps the server responsive.

## How to reproduce

1. Clone this repository.
2. Run `server.js` using Node.js.  You'll notice that sending multiple requests to the server will cause some of them to hang or timeout.
3. Compare the behaviour of `server.js` and `serverSolution.js`.