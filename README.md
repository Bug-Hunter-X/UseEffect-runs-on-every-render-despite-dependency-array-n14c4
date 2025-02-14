# React useEffect Bug: Unintended Re-renders

This repository demonstrates a common React bug involving the `useEffect` hook.  The `useEffect` hook is intended to perform side effects after a component renders, but in this case, it re-renders on every state change regardless of dependencies, leading to performance issues and unexpected behavior.

## Bug Description

The `useEffect` hook is incorrectly performing side effects after every render, even though no dependencies are explicitly provided, thus rendering unnecessarily frequently.

## Solution

The solution involves correctly defining the dependencies array in the `useEffect` hook.  This array specifies which values the effect should depend on for re-execution. If the effect depends on no values, it is only executed after the initial render.