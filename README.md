# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the code fails to handle cases where the user ID parameter is not a valid number.

## Bug
The `bug.js` file contains the problematic code.  It attempts to parse the `userId` parameter as an integer without any error handling. If the `userId` is not a number (e.g., a string or null), `parseInt(userId)` will return `NaN`, and the `find` method will not find the user.  This may result in unexpected behavior or a crash.

## Solution
The `bugSolution.js` file provides a corrected version of the code. It includes error handling to check if `userId` is a number and gracefully handles the case where the user is not found.

## How to run
1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` (to see the buggy code in action).
4. Run `node bugSolution.js` (to see the corrected code).
