# useEffect Cleanup Function Issue in React

This repository demonstrates a common issue with React's `useEffect` hook where the cleanup function within the effect does not behave as expected. The cleanup function is designed to run before the component unmounts or before the effect is re-run with a different set of dependencies. This example shows a scenario where the cleanup function is unexpectedly not being called, leading to potential memory leaks or unexpected behavior.

## Problem

The provided `MyComponent` uses `useEffect` to log the current count and also includes a cleanup function.  The expectation is that the cleanup function will log 'Cleanup' before the component unmounts or when the `count` value changes.  In this specific setup, the cleanup may not execute as intended if the component is unmounted quickly or if useEffect's dependencies aren't properly managed. 