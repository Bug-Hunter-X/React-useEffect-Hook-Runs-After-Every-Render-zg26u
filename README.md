# React useEffect Hook Runs After Every Render

This repository demonstrates a common React bug where the `useEffect` hook runs after every render, leading to performance issues and unexpected behavior. The solution shows how to use the `useEffect` hook correctly to avoid these problems.

## Bug
The provided `MyComponent` uses `useEffect` without specifying dependencies.  This causes the effect to run on every render, leading to an infinite loop of console logs and potential performance problems.

## Solution
The solution utilizes the optional dependency array in `useEffect`. This array determines when the effect should run. By listing `count` as a dependency, the effect now only runs when `count` changes.