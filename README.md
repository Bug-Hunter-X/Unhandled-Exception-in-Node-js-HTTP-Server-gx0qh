# Unhandled Exception in Node.js HTTP Server

This repository demonstrates a common error in Node.js where an unhandled exception within an HTTP request listener can cause the server to crash without proper error handling.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version with robust error handling.

## Problem

The original code lacks error handling within the `requestListener`.  If an unexpected error occurs during request processing, the server will crash, resulting in downtime. 

## Solution

The solution involves using a `try...catch` block within the request listener to gracefully handle potential exceptions.  This prevents server crashes and allows for logging or returning appropriate error responses to clients. 