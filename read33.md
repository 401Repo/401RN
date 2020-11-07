# Readings: Redux - Additional Topics

### Review, Research, and Discussion

![source](https://redux.js.org/img/redux-logo-landscape.png)

### What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount) of a Higher Order Component that wraps your app. However, you will not use the results of the API call directly in that component - it needs to be handled with a reducer that puts it into your app store. This will require you to use some sort of a thunk middleware to handle the asynchronous action.

[source](https://stackoverflow.com/questions/39356517/correct-way-to-pre-load-component-data-in-reactredux)

### When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

Store

*middleware*

Redux middleware function provides a medium to interact with dispatched action before they reach the reducer. Customized middleware functions can be created by writing high order functions (a function that returns another function), which wraps around some logic. Multiple middlewares can be combined together to add new functionality, and each middleware requires no knowledge of what came before and after. You can imagine middlewares somewhere between action dispatched and reducer.

[source](https://www.tutorialspoint.com/redux/redux_middleware.htm)

*thunk*

Thunk allows you to write action creators that return a function instead of an action. The inner function can receive the store methods dispatch and getState as parameters, but we'll just use dispatch.

[source](https://medium.com/@stowball/a-dummys-guide-to-redux-and-thunk-in-react-d8904a7005d3)


