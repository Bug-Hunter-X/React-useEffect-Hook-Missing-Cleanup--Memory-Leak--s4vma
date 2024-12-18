# React useEffect Hook Missing Cleanup

This repository demonstrates a common error in React applications: forgetting to include a cleanup function in the `useEffect` hook. This can lead to memory leaks and unexpected behavior.

## The Problem

The `bug.js` file shows a `MyComponent` that uses the `useEffect` hook without a return statement. This means that any cleanup operations (like event listeners, timers, or subscriptions) will not be properly removed when the component unmounts.

## The Solution

The `bugSolution.js` file provides the corrected code.  The `return` statement in the `useEffect` function provides a cleanup function that executes before the component unmounts.  This ensures that any resources used by the component are released, preventing potential memory leaks.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output when the component is mounted and unmounted.