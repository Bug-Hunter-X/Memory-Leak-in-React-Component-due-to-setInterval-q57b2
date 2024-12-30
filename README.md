# React setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks caused by improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file contains the problematic code. The `bugSolution.js` file provides a corrected version.

The issue arises when `setInterval` is used without a cleanup function in `useEffect`. This prevents the interval from being cleared when the component unmounts, leading to a memory leak. The solution involves returning a cleanup function from `useEffect` to clear the interval.