# React Native FlatList TypeError: Cannot read properties of undefined (reading 'property')

This repository demonstrates a common error in React Native when using FlatList to render data that contains null or undefined values.  The error occurs because FlatList tries to access properties of these null/undefined items which results in a TypeError.

The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

## Bug
The bug arises from attempting to render a list item using data that may contain null or undefined values.  The code doesn't check for null/undefined before accessing properties, leading to the TypeError.

## Solution
The solution involves adding a check to ensure that each item in the data array is defined before attempting to access its properties.  This check prevents the error by skipping over null or undefined items, thereby avoiding the error.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the error in the `bug.js` example.
5. Replace `bug.js` with `bugSolution.js` and re-run to see the corrected version.
