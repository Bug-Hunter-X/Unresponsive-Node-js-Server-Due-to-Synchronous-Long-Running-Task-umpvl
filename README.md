# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js applications: an unresponsive server caused by a long-running synchronous operation blocking the event loop.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version using asynchronous operations.

## Bug Description

The server in `bug.js` performs a computationally intensive task synchronously within the request handler.  This blocks the event loop, preventing the server from responding to new requests until the task completes.  This leads to unresponsiveness and poor performance.

## Solution

The solution in `bugSolution.js` addresses this by using asynchronous operations or offloading the task to a worker thread.  This ensures the event loop remains responsive, allowing the server to handle multiple requests concurrently.

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` to see the unresponsive server.
4. Run `node bugSolution.js` to see the corrected, responsive server.