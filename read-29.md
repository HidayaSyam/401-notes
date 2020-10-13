## React Router 

### React Router has been broken into three packages: react-router, react-router-dom, and react-router-native.

### When starting a new project, you need to determine which type of router to use. 
### For browser based projects, there are BrowserRouter and HashRouter components.
- ### The BrowserRouter should be used when you have a server that will handle dynamic requests (knows how to respond to any possible URI)
- ### the HashRouter should be used for static websites (where the server can only respond to requests for files that it knows about).


### path-to-regexp package to determine if a route element’s path prop matches the current location. It compiles the path string into a regular expression, which will be matched against the location’s pathname.

### Creating our routes
#### Routes can be created anywhere inside of the router, but often it makes sense to render them in the same place. You can use the <Switch> component to group Routes. The Switch will iterate over its children elements (the routes) and only render the first one that matches the current pathname.


### What does the Route render?
Routes have three props that can be used to define what should be rendered when the route’s path matches. Only one should be provided to a Route element.

- ### component — A React component. When a route with a component prop matches, the route will return a new element whose type is the provided React component (created using React.createElement).
- ### render — A function that returns a React element 5. It will be called when the path matches. This is similar to component, but is useful for inline rendering and passing extra props to the element.
- ### children — A function that returns a React element. Unlike the prior two props, this will always be rendered, regardless of whether the route’s path matches the current location.
