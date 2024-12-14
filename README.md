# Unhandled Error in Asynchronous Node.js Server

This repository demonstrates an example of an uncommon error in Node.js: an unhandled exception within an asynchronous callback leading to server crashes.  The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides a corrected version with proper error handling.

## Problem

Asynchronous operations in Node.js often involve callbacks or Promises.  If an error occurs within an asynchronous callback and isn't handled appropriately using a `try...catch` block or `.catch()` method, it can lead to unexpected crashes of the Node.js process.

## Solution

The solution involves wrapping the asynchronous operation within a `try...catch` block to handle any potential errors gracefully.  This prevents the server from crashing and allows for better error management and recovery.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js` to observe the server crashing intermittently.
4. Run `node bugSolution.js` to see the corrected version handling errors properly.