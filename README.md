# Unhandled Promise Rejection/Callback Error in Node.js Server

This repository demonstrates a common error in Node.js servers: unhandled promise rejections or callback errors in asynchronous operations.  The server simulates an asynchronous operation that may fail, and without proper error handling, this failure can lead to intermittent 500 errors.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version with robust error handling.

## Running the Code

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to see the problematic behavior.  You'll likely experience intermittent 500 errors.
4. Run `node bugSolution.js` to see the improved error handling and consistent behavior.

## Problem and Solution

The original code lacks a mechanism for catching and handling errors that may arise during the asynchronous operation.  The improved code uses a `try...catch` block to gracefully handle errors and prevent the server from crashing or returning a 500 error.