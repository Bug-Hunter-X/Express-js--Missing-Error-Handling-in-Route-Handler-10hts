# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.

The `bug.js` file shows a route handler that fetches a user by ID.  If the ID is invalid, it causes an error because it doesn't handle the `user` variable being `undefined`.

The `bugSolution.js` file provides a corrected version with error handling. It checks if the user exists before attempting to send the response.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`.  Try accessing the route with a valid and an invalid user ID.
4. Repeat for `bugSolution.js` to see the corrected behavior.

## Lesson Learned

Always handle potential errors in Express.js route handlers.  Check for `null`, `undefined`, or other invalid input before using the values.