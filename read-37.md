## Redux - Combined Reducers

Why choose Redux instead of the Context API for global state?
  * Redux can work better for applications with complex state with high-frequency updates does not require a re-render on each update and is much easier to implement. 
  * [resource](https://dev.to/ibrahima92/redux-vs-react-context-which-one-should-you-choose-2hhh)

What is the purpose of a reducer?
  * A reducer is an alternative to **useState**. It is mostly used for more complext state. It receives two parameters, state and action. It's purpose is to determine changes to an application's state. Redux relies heaviily on reducer functions to to take the previous state and an action in order to execute the next state. 
  * [resource](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function%20that%20determines%20changes%20to%20an%20application's%20state.&text=Redux%20relies%20heavily%20on%20reducer,to%20execute%20the%20next%20state.)

What does an action contain?
  * Actions are plain JavaScript objects that contain information such as the type of action to perform. 
  * [resource](https://www.geeksforgeeks.org/introduction-to-redux-action-reducers-and-store/#:~:text=Actions%3A%20Actions%20are%20a%20plain,fields%20contain%20information%20or%20data.)

Why do we need to copy the state in a reducer?
  * Every level of nesting must be copied and updated as a key to updating nested data. 
  * [resource](https://redux.js.org/recipes/structuring-reducers/immutable-update-patterns)

## Vocabulary

* Immutable State -In object-oriented and functional programming, it is an object whose state cannot be modified after it is created. These are typically strings and other contrete objects that cannot be changed to improve readability and runtime efficiency
  * [resource](https://en.wikipedia.org/wiki/Immutable_object#:~:text=In%20object%2Doriented%20and%20functional,modified%20after%20it%20is%20created.)

* Time travel in Redux - A way of keeping original state intact using an undo/redo time travel implementation powered by diffs and merges. 
  * [resource](https://www.npmjs.com/package/redux-time-travel)

* Action Creator - Functions in Redux that create actions, which are payloads of informatoin that send data from an application to a "store." They simply return an action, making the action portable and easy to test. The often trigger a dispatch.
  * [resource](https://redux.js.org/basics/actions)

* Reducer - They specify how the application's state changes in response to actions sent to the store. It is a pure function that takes the  previous state and an action, and returns the next state. 
  * [resource](https://redux.js.org/basics/reducers)

* Dispatch - A function of the Redux store, which is used to trigger state change. Components do not have access to the store directly. Redux provides two ways to let components "dispatch" actions. 
  * [resource](https://react-redux.js.org/using-react-redux/connect-mapdispatch)
