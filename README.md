# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies in the dependency array.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Problem
The original code attempts to log the count value on every render, resulting in an infinite loop because the effect always triggers a re-render. This is because each time the effect runs, it modifies the state, which then triggers the effect again, and so on. 

## Solution
The solution includes the `count` variable in the dependency array. This ensures that the effect only runs when the `count` value changes, preventing the infinite loop. 
