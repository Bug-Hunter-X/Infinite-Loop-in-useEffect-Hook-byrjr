# Infinite Loop in useEffect Hook

This repository demonstrates a common error in React applications: creating an infinite loop within the `useEffect` hook.  The provided `bug.js` file shows a component that attempts to update its state continuously.  The solution in `bugSolution.js` demonstrates how to fix this issue.

## Description
The problem lies in the dependency array of the `useEffect` hook. The `count` state variable is included in the array. Every time the `count` is updated by `setCount(count + 1)`, `useEffect` rerenders the component, leading to another state update, and thus, an infinite loop.