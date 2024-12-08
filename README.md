# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by an incorrectly specified dependency array.

## Description
The `useEffect` hook in the `bug.js` file has an empty dependency array `[]`. This causes the effect to run after every render, including when the component re-renders due to the state update.  This creates a vicious cycle, leading to an infinite loop and potential browser crashes.

## Solution
The `bugSolution.js` file corrects this by including `count` in the dependency array `[count]`. This ensures that the effect only runs when the value of `count` changes.