# React useEffect Missing Dependency Bug

This repository demonstrates a common error in React's `useEffect` hook: a missing dependency in the dependency array.  This leads to the effect running only once instead of whenever the specified dependency changes.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides the corrected version.

## Bug Description
The `useEffect` hook is intended to update the counter every second. However, due to the missing `count` dependency, the `setInterval` function is only called once, resulting in a counter that only increments once and then stops. 

## Solution
The solution involves adding `count` to the dependency array of `useEffect`. This ensures that the `setInterval` function is called and cleared appropriately every time the `count` state changes.