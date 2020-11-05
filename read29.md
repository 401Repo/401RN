# Readings: Custom Hooks

### Review, Research, and Discussion

![source](https://miro.medium.com/max/3280/1*uZ8WSki-46Kkls1TefrLIQ.jpeg)

### What does a component’s lifecycle refer to?

Each component in React has a lifecycle which you can monitor and manipulate during its three main phases.

The three phases are: Mounting, Updating, and Unmounting.

[source](https://www.w3schools.com/react/react_lifecycle.asp)

### Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

Using useCallback should be preferred in the following cases

    If you are passing the function on to child component as props and the child component doesn't often need re-rendering except when a certain prop change then useCallback might prevent certain re-renders. However if you state is complex and you need multiple such functions to be passed on to children as props, it better to shift to useReducer instead of useState and pass on the dispatch method to child components

    You are specifying a function as a dependency to useEffect. In such as case you must ensure that the function in not recreated on every render or the useEffect will be triggered on every render.

[source](https://stackoverflow.com/questions/57156582/should-i-wrap-all-functions-that-defined-in-component-in-usecallback)

### Why are functional components preferred over class components?

>"Syntax

>The most obvious one difference is the syntax. A functional component is just a plain JavaScript function which accepts props as an argument and returns a React element.

>A class component requires you to extend from React.Component and create a render function which returns a React element. This requires more code but will also give you some benefits which you will see later on."

According to this we would have an argument that functional would be faster for a programmer to code. But it seems there more functionalities to class components if not more work.

[source](https://medium.com/@Zwenza/functional-vs-class-components-in-react-231e3fbd7108)

### What is wrong with the following code?

Thiking in Angualer terms i would thing we arent exporting it. Maybe im missing the point of the lifecycle at 0, but its one of the most obvious thing i would to go in my "why is my component not rendering?" question but i have to do more homework to know by sight. 

*state hook*

Returns a stateful value, and a function to update it.

[source](https://reactjs.org/docs/hooks-reference.html)

*effect hook*

Accepts a function that contains imperative, possibly effectful code.

[source](https://reactjs.org/docs/hooks-reference.html)

*reducer hook*

An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

[source](https://reactjs.org/docs/hooks-reference.html)

