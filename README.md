# MongoDB $inc Operator Error: Unexpected Behavior with Non-Numeric Values
This example demonstrates an uncommon error when using the `$inc` operator in MongoDB update operations.  The `$inc` operator is designed to increment or decrement numeric values.  Attempting to use it on a non-numeric field will result in unexpected behavior, rather than a clear error message.

## Bug Description
The provided `bug.js` file shows an incorrect usage of the `$inc` operator. The value being incremented is a string rather than a number. This leads to unpredictable results, which are not always caught as straightforward errors.

## Solution
The `bugSolution.js` file corrects the error by ensuring the `count` field is a number before applying the `$inc` operation.

## How to reproduce
1. Set up a MongoDB instance.
2. Create a collection in your database.
3. Insert a document with a string value for the 'count' field.
4. Run the code from `bug.js`.
5. Observe the unexpected output or unexpected state of the document.
6. Run the code from `bugSolution.js` to see the correct behavior.