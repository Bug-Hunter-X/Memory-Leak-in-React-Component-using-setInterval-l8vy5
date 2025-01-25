# React setInterval Memory Leak

This repository demonstrates a common mistake when using `setInterval` in React components: failing to clear the interval when the component unmounts. This leads to memory leaks and unexpected behavior.

## Bug

The `bug.js` file shows a component that uses `setInterval` to update a counter. However, it doesn't clear the interval when the component is unmounted, resulting in the interval continuing to run even after the component is gone from the DOM. This causes a memory leak.

## Solution

The `bugSolution.js` file demonstrates the correct way to use `setInterval` in a React component.  It uses the cleanup function provided by `useEffect` to clear the interval when the component is unmounted, preventing the memory leak.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the counter in the browser.  Unmounted the component and check your browser's console or task manager for memory usage. The bug version will show continuous memory increase.