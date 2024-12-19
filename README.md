# React useEffect Hook Infinite Re-renders Bug

This repository demonstrates a common error in React's `useEffect` hook that leads to infinite re-renders.  The issue stems from omitting the dependency array in `useEffect`, causing the effect to run after every render, creating a loop.

## Bug Description

The `MyComponent` component uses `useState` to manage a count.  The `useEffect` hook logs the count to the console.  Without a dependency array, the effect runs on every render, triggering another render, and so on.

## Solution

The solution is to provide the `count` variable as a dependency in the `useEffect` hook's dependency array. This ensures the effect only runs when the value of `count` changes.
