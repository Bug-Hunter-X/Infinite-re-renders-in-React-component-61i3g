# Infinite Re-renders in React Component

This repository demonstrates a common React bug: infinite re-renders caused by a missing dependency array in the `useEffect` hook.  The `useEffect` hook, without a dependency array, will run after every render, potentially creating an infinite loop if it modifies state or props that trigger re-renders.  The solution shows how to correctly use the dependency array to control when the effect runs.

## Bug

The `bug.js` file contains a React component with an `useEffect` hook that lacks a dependency array. This causes the component to re-render continuously, leading to performance issues and potential crashes.

## Solution

The `bugSolution.js` file demonstrates the correct usage of the dependency array. By including `count` in the dependency array, the effect only runs when `count` changes.