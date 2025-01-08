# React useEffect Hook: Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: omitting a dependency from the dependency array, leading to an infinite render loop.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides the corrected version.

## Bug
The original code lacked `count` in the dependency array of the `useEffect` hook. This means the effect ran after every render, regardless of changes in `count`, leading to an infinite loop of console logs and component re-renders. 

## Solution
The corrected code includes `count` in the dependency array. The effect now only runs when the value of `count` changes, resolving the infinite loop.