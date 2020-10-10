# React

![image](https://image.slidesharecdn.com/reactjs-introduction-150311040508-conversion-gate01/95/react-js-introduction-10-638.jpg?cb=1426046763)


# JSX
### JSX : it is a syntax extension to JavaScript , We recommend using it with React to describe what the UI should look like.

#### Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages

![image](https://miro.medium.com/max/1886/1*NyJLmk71DRifYH6E1saRkw.png)

#### can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions and we can Specifying Attributes with JSX maybe using qoutes for literals  or curly braces to embed a JavaScript expression like image url

### Updating the Rendered Element
#### React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

####  With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().
