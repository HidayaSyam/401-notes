## Custom Hooks

### A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks.

### a custom Hook doesn’t need to have a specific signature. We can decide what it takes as arguments, and what, if anything, it should return. In other words, it’s just like a normal function. Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.

- Extract duplicated logic from components
- offer the flexibility of sharing logic

## useReducer
### useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.


