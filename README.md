# JavaScript Closure Issue with setTimeout

This example demonstrates a common closure problem in JavaScript when using `setTimeout` within a loop.  The expected behavior is to log the numbers 0 through 9 sequentially after a one-second delay each. However, due to how closures work in JavaScript, all the `console.log` statements end up accessing the final value of `i` (which is 10). 

The solution shows how to fix this issue using an immediately invoked function expression (IIFE) to create a new scope for each iteration, effectively capturing the correct value of `i` for each `setTimeout` call. 

**Steps to reproduce:** 

1.  Clone the repository
2.  Run `node bug.js` to observe the unexpected behavior.
3.  Run `node bugSolution.js` to see the corrected behavior.