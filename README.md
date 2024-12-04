# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling for invalid input.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

The issue occurs when a user ID is passed to the `/users/:id` route that cannot be parsed as an integer.  The original code fails to handle this case, potentially leading to a server crash or unexpected behavior.  The solution adds input validation and comprehensive error handling to prevent this issue.

## How to reproduce the bug:

1. Clone this repository.
2. Run `npm install express` to install the required dependency.
3. Run `node bug.js`.
4. Send a request to `/users/abc` (or any non-integer value) using a tool like `curl` or Postman.  Observe the error.

## How to run the solution:

1. Run `node bugSolution.js`.
2. Send a request to `/users/abc` again. Note the graceful error handling.