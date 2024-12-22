# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency.

## Problem
The `useEffect` hook in `bug.js` logs the current count to the console after every render.  Because `setCount` changes the count after each click, the component re-renders, and the effect runs again, leading to an infinite loop and potential crashes. 

## Solution
The solution (`bugSolution.js`) correctly includes `count` in the dependency array. This ensures that the effect only runs when `count` changes, preventing the infinite loop.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console and the browser's behavior. The original buggy version will rapidly fill the console and potentially crash your browser.
5. Switch to `bugSolution.js` to see the corrected behavior.