# React 19 useEffect Bug: Missing Dependency

This repository demonstrates a common error in React 19's `useEffect` hook where omitting a state variable from the dependency array causes unexpected behavior, often leading to an infinite render loop.  The solution shows how to correctly include the state variable in the dependency array to fix the issue.

## Bug Description
The `useEffect` hook in the provided `bug.js` file is missing `count` from its dependency array. This means that the effect runs after every render, regardless of whether the `count` value has actually changed.  This leads to an infinite loop, as the console continually logs the current count, and the component repeatedly re-renders.

## Solution
The corrected code, `bugSolution.js`, demonstrates the correct usage of `useEffect`. By including `count` in the dependency array, the effect now only runs when the value of `count` changes.