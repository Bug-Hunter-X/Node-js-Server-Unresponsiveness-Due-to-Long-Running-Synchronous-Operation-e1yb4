# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a server can become unresponsive due to a long-running synchronous operation within the request handler.  The `server.js` file contains a flawed implementation that blocks the event loop, leading to unresponsive behavior. The `serverSolution.js` provides a corrected version.

## Problem

Node.js is single-threaded and relies on the event loop to handle multiple requests concurrently.  When a long-running synchronous operation is executed, the event loop gets blocked, preventing the server from processing other requests, resulting in unresponsiveness.

## Solution

The solution involves using asynchronous operations (e.g., using promises, async/await or timers) to prevent the event loop from being blocked. The corrected code in `serverSolution.js` demonstrates this approach.