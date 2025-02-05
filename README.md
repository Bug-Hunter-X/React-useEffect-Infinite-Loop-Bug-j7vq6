# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving infinite loops within the `useEffect` hook.  The issue stems from improperly managing state updates within the dependency array of `useEffect`.  The provided solution illustrates the correct approach to prevent this issue.

## Bug Description

The `bug.js` file contains a React component that attempts to increment a counter using `useEffect`. However, the dependency array `[count]` incorrectly includes the `count` state variable.  This causes an infinite loop because every time `setCount` is called, `count` changes, triggering another `useEffect` call, leading to a continuous cycle of updates.

## Solution

The `bugSolution.js` file shows how to fix the problem. The solution involves creating a conditional useEffect which prevents the infinite loop by introducing a condition or other changes in useEffect's logic to update count only under certain conditions which prevents infinite loop. 
