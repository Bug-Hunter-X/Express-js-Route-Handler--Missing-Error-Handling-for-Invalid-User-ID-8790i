# Express.js Route Handler: Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the provided code attempts to parse a user ID from the request parameters as an integer without verifying if the input is indeed a valid number. This can lead to unexpected errors or crashes.

The `bug.js` file shows the flawed code, while `bugSolution.js` presents a corrected version with robust error handling.

## Bug

The original code lacks error handling for the scenario where the `userId` parameter is not a valid number.  If the user enters a non-numeric value, `parseInt(userId)` will return `NaN`, causing subsequent operations to fail. 

## Solution

The solution involves checking if the parsed user ID is indeed a number using `isNaN()`. If it's not a number, an appropriate error response is sent, preventing crashes and ensuring better user experience.
