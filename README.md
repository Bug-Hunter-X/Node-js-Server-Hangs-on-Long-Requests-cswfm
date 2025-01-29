# Node.js Server Hang on Long Requests

This repository demonstrates a common issue in Node.js servers: hanging on long-running requests.  The provided `server.js` file showcases a simple Express.js server that simulates a long task, causing the server to become unresponsive during that time.  The `serverSolution.js` file provides a solution using asynchronous request handling.

## Problem

Node.js is single-threaded.  When a long-running task is executed in a request handler, it blocks the event loop, preventing other requests from being processed. This leads to server unresponsiveness and poor performance.

## Solution

The solution involves using asynchronous programming techniques to handle long-running tasks without blocking the event loop.  This example uses `setTimeout` within a Promise to simulate an asynchronous operation.  More complex tasks might use other techniques, such as worker threads or message queues.