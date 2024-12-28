# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the code attempts to parse a user ID as an integer without any validation or error handling. This can lead to unexpected behavior or application crashes if the ID is not a valid integer.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides a corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install express` to install the required dependency.
3. Run `node bug.js`.
4. Try accessing a route with a non-numeric ID (e.g., `/users/abc`).

You should observe that the application crashes or returns an unexpected error.

## Solution

The corrected code in `bugSolution.js` adds error handling to check if the `userId` is a valid integer before attempting to parse it and to handle the case where the user is not found. This makes the application more robust and prevents unexpected errors.