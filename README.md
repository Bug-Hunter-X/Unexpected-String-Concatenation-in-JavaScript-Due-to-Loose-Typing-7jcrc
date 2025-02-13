# Unexpected String Concatenation in JavaScript

This example demonstrates a common error in JavaScript stemming from its loose typing system.  When adding numbers and strings, JavaScript will perform string concatenation instead of numerical addition if either operand is a string.

## The Bug

The `foo` function intends to add two numbers. However, due to JavaScript's implicit type coercion, when a string is involved, it treats the operation as string concatenation.

## The Solution

The solution is to explicitly convert the inputs to numbers before performing the addition using `parseInt()` or `Number()`.  This ensures that the addition operation behaves as expected, regardless of the input types.

## How to Reproduce

1.  Save the code in `bug.js`.
2.  Run the code using a JavaScript interpreter (e.g., Node.js): `node bug.js`

You'll observe that the results for lines involving string inputs are unexpected string concatenations.