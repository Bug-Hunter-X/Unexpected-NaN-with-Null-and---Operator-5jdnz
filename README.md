# JavaScript Bug: Unexpected NaN with Null and + Operator

This repository demonstrates a common yet subtle bug in JavaScript related to the loose typing of the plus (+) operator and its interaction with `null` values.

## Bug Description

When using the `+` operator to add a number to a `null` value, the result is `NaN` (Not a Number) due to type coercion. This behavior may be unexpected for developers accustomed to stricter type systems.  The intention is often to treat `null` as 0 in such scenarios.

## How to Reproduce

1. Clone the repository.
2. Open `bug.js`.
3. Run the code in a JavaScript environment (e.g., Node.js, browser's console).
4. Observe the output: `NaN`.

## Solution

The `bugSolution.js` file provides a solution that addresses this issue by explicitly handling `null` values before performing the addition.  This involves checking for `null` and replacing it with 0 to achieve the expected numerical sum.

## Lessons Learned

- JavaScript's loose typing can lead to unexpected behavior if not handled carefully.
- Always validate and handle potential `null` values before performing mathematical operations to avoid unexpected results such as `NaN`.
- Consider using stricter type checking methods or tools (like TypeScript) to prevent such issues in larger projects.
