# Uncommon HTML Bug: Race Condition in DOM Access

This repository demonstrates a subtle bug in HTML related to timing issues when JavaScript interacts with the DOM. The script attempts to modify the content of a div element before the browser has finished rendering it, leading to unexpected results or errors.

## The Bug

The `bug.html` file contains a simple HTML page with a div element and a script. The script tries to modify the div's `innerHTML` property before the browser has fully loaded the page. This can result in an error in some browsers or simply no change in others.

## The Solution

The `bugSolution.html` file fixes the issue by using the `DOMContentLoaded` event listener. This ensures that the JavaScript code executes only after the HTML document is fully parsed and ready, preventing the race condition.