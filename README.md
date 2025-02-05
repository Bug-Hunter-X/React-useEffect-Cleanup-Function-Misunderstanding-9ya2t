# React useEffect Cleanup Function Misunderstanding

This example demonstrates a common misunderstanding regarding the React `useEffect` hook's cleanup function.  The cleanup function is crucial for managing side effects, especially those involving subscriptions or timers, to prevent memory leaks and unexpected behavior. However, it's often misinterpreted as executing immediately after every render.

## The Issue

The provided code attempts to log a message after every render, mistakenly believing the cleanup function will execute immediately before each subsequent render. This is incorrect. The cleanup function *only* executes when the component is unmounted or the effect is replaced (due to dependency changes).

## The Solution

The solution clarifies the behavior of the cleanup function and demonstrates how to use it correctly for managing side effects that are tied to the component's lifecycle.