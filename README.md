# React 19 useEffect Runs After Every Render

This repository demonstrates an uncommon bug in React 19 where the `useEffect` hook runs after every render, even when dependencies are correctly specified. This can lead to performance issues, especially in complex applications.

## Bug Description

The provided `MyComponent` uses a `useEffect` hook without specifying any dependencies. As a result, the effect runs after every render, causing the `console.log` statement to execute repeatedly.  This is inefficient and can hinder performance.

## Solution

The solution is to add a dependency array to the `useEffect` hook. This array specifies which values the effect should depend on. Only when these values change will the effect run again.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`. Observe the console log.

## How to Solve

Refer to the `bugSolution.js` for the corrected code.