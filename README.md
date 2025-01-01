# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake when using the `setInterval` function within the `useEffect` hook in React.  Failing to clean up the interval leads to a memory leak. The solution shows the correct way to handle `setInterval` for avoiding leaks.

## Bug
The `bug.js` file shows how an improper use of `setInterval` inside `useEffect` causes a memory leak.  The interval is never cleared, resulting in continuous updates even when the component unmounts.

## Solution
The `bugSolution.js` file demonstrates the correct approach. It uses the return value of `useEffect` to define a cleanup function that clears the interval when the component unmounts or when the dependency array changes.