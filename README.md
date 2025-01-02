# Uncommon HTML Bug: Accessing Child Node After Clearing Content

This repository demonstrates a subtle bug that can occur in HTML/JavaScript when manipulating the DOM. The bug arises from attempting to access a child node of an element after its content has been cleared using `innerHTML = ""`.

The `bug.html` file contains the buggy code.  The `bugSolution.html` file provides a corrected version.

## Bug Description

The original code clears the content of a div element and then attempts to modify the `nodeValue` of its `firstChild`. However, after clearing the content, `firstChild` becomes `null`, leading to an error.

## Solution

The solution involves checking if `firstChild` exists before attempting to access or modify it.  This ensures that the code handles the case where the element has no children gracefully.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Click the button.  You will likely see a JavaScript error in your browser's console.
4. Open `bugSolution.html`.  Click the button; it should work correctly without any errors.