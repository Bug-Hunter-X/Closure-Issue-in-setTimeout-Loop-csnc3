# Closure Issue in setTimeout Loop
This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The expected behavior is to print numbers 0-9 with a one-second delay between each. However, due to the way closures work, the loop completes before the `setTimeout` callbacks execute, resulting in all callbacks printing the final value of 'i'.

**Bug:** The `bug.js` file contains the buggy code.

**Solution:** The `bugSolution.js` file demonstrates a fix using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, correctly capturing the value of `i`.