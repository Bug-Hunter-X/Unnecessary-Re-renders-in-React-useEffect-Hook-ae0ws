# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common issue in React applications where the `useEffect` hook causes unnecessary re-renders.  The provided code shows a `useEffect` hook without dependencies, leading to infinite renders. The solution demonstrates how to fix this by correctly specifying dependencies.

## Bug
The `useEffect` hook runs after every render because of the missing dependency array. This leads to unnecessary console logs and performance issues.

## Solution
Adding an empty dependency array `[]` to the `useEffect` hook ensures it runs only once after the initial render.  Alternatively, list the state variables that trigger the effect.