# Stale Closure in useEffect with setInterval

This repository demonstrates a common error in React when using the `useEffect` hook with `setInterval`.  The issue arises from an incorrectly handled closure within the `setInterval` callback, leading to stale closures and unexpected behavior.

## Problem
The `bug.js` file contains a component that attempts to increment a counter every second using `setInterval` within a `useEffect` hook. However, the closure over the `setCount` function is not properly managed, resulting in the counter not updating correctly or unexpectedly stopping after a certain amount of time.

## Solution
The `bugSolution.js` file provides a corrected implementation.  The solution uses a functional update to ensure that `setCount` always uses the latest state value, solving the stale closure problem.

## How to run
1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.