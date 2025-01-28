# Uncommon HTML Bug: Accessing Non-Existent Element's innerHTML

This repository demonstrates a subtle bug in HTML where attempting to access the `innerHTML` property of a non-existent element can lead to unexpected behavior and potentially silent errors, especially in older browsers.

## Bug Description
The `bug.html` file shows how attempting to access the `innerHTML` of an element that doesn't exist doesn't throw an error or warning.  This might mask other issues and lead to hard-to-debug problems.

## Solution
The `bugSolution.html` file provides a corrected version.  Before accessing the element's `innerHTML`, it first checks for the element's existence using `getElementById`.  If the element is null, no attempt is made to access its `innerHTML`, preventing the bug.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe that the script runs without throwing an error, even though it tries to access a non-existent element.
4. Open `bugSolution.html`. This version addresses the bug with error handling.
