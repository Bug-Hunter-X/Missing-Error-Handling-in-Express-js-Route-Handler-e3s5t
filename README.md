# Missing Error Handling in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file shows the erroneous code, while `bugSolution.js` provides a corrected version.

## Bug Description

The provided Express.js route handler attempts to find a user based on their ID. However, it lacks proper error handling for cases where the user ID is not a valid integer or if no user is found.  This can lead to unexpected behavior or crashes.

## Solution

The `bugSolution.js` file addresses this issue by adding comprehensive error handling:

- It checks if the user ID is a valid integer using `isNaN()`.
- It returns a 404 status code if the user is not found.
- It returns a 500 status code if the user ID is invalid.