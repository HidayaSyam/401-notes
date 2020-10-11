### setState()

React components can, and often do, have state. State can be anything, but think of things like whether a user is logged in or not and displaying the correct username based on which account is active. Or an array of blog posts. Or if a modal is open or not and which tab within it is active.

React components with state render UI based on that state. When the state of components changes, so does the component UI.

That makes understanding when and how to change the state of your component important. At the end of this tutorial, you should know how setState works, and be able to avoid common pitfalls that many of us hit when when learning React.


Workings of `setState()`
setState() is the only legitimate way to update state after the initial state setup. Let’s say we have a search component and want to display the search term a user submits.

