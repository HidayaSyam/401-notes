## Redux - Additional Topics

What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
  * When using Redux with server rendering, state of the app must be sent along in a response so the client can use it as the initial state. If any data is preloaded before HTML is generated, the client must have access to this data. If not, the markup generated on the client will not match the server markup, so the client would have to load the data again. 
  * [resource](https://redux.js.org/recipes/server-rendering)

When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
  * export actions created by action creators adn return a new state of the application. Each reducer takes two parameters - the previous state and an action object. Inside each reducer, a switch statement is used to detemrine when an action.type matches. If it matches, return the relevant property of action. 
  *[resource](https://medium.com/@stowball/a-dummys-guide-to-redux-and-thunk-in-react-d8904a7005d3)

## Vocabulary

Middleware - Provides third-party extension points between dispatching an action and the moment it reaches the reducer. It is used for logging, cash reporting, talking to an asynchronous API, and routing. 
  * [resource](https://redux.js.org/advanced/middleware)

Thunk - Redux middleware that allows the composition of action creators that return a function instead of an action. Can be used to delay the dispatch of an action, or to dispatch an action only if a certain condition is met. 
  * [resource](https://www.npmjs.com/package/redux-thunk)
