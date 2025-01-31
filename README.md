# useEffect Hook Unexpected Behavior
This repository demonstrates an example of unexpected behavior in React's `useEffect` hook.  The initial implementation has a missing dependency causing the effect to run on every render instead of just once on mount. The solution shows how to correctly specify dependencies to achieve the desired behavior.

## Bug Description
The `useEffect` hook is intended to perform side effects after a component renders.  When an empty dependency array `[]` is specified, it is expected to run only once after the initial mount.  However, if a value used inside the `useEffect` is not included in the dependency array and changes, the effect may run unexpectedly, leading to performance issues or incorrect behavior.

## Bug Solution
The solution demonstrates the correct way to use the `useEffect` hook with the correct dependencies. By adding any values used from component state into the dependency array we ensure it re-runs only when those dependencies change.