# Next.js Runtime Error Not Caught by Error Handling

This repository demonstrates a bug in Next.js where a runtime error on a page is not caught by Next.js's error handling, resulting in a blank page for the user.

## Bug Description

The `pages/about.js` file contains a syntax error (missing closing tag). When navigating to the `/about` page, Next.js throws a runtime error, but this error is not gracefully handled, leading to a blank page. This can be frustrating for users who encounter this without understanding the root cause.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `http://localhost:3000/about`

You'll notice a blank page or an error message in your browser's console, indicating that the runtime error was not properly handled.

## Solution

The solution involves using try catch blocks in your page components. This is not an ideal fix but may work as a workaround.  Better solution would be to fix the underlying syntax error in the page components.  The solution is provided in `bugSolution.js`
