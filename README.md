# Express.js Route Handler Error
This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  The `bug.js` file shows the erroneous code, which fails to handle cases where the user ID is not a valid integer. The `bugSolution.js` file provides a corrected version with robust error handling.

## Bug
The original code attempts to directly parse the `userId` from the request parameters as an integer and uses it to find a user from a `users` array.  If the `userId` is not an integer (e.g., a string or null), this will cause an error.

## Solution
The solution adds error handling to check if `userId` is a valid integer. If not, it responds with an appropriate error code (400 Bad Request) to indicate invalid input.  If the user is not found, it responds with a 404 Not Found error.