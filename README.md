# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite render loop because the effect is improperly configured, leading to a continuous re-rendering of the component.

## Bug Description

The `useEffect` hook in the provided `MyComponent` function lacks the correct dependency array.  Without specifying a dependency array (or using an empty array `[]`), the effect runs after every render.  This creates a feedback loop where the effect updates the state, triggering a re-render, causing the effect to run again, and so on.

## Solution

The solution involves correctly specifying the dependency array.  By including `count` in the dependency array `[count]`, the effect only runs when the `count` variable changes.

## How to reproduce:
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the infinite loop in the console.

## Solution: 
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the corrected behavior in the console and UI.