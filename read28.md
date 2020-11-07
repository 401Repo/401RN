# Readings: Log In and Auth

### Review, Research, and Discussion

![source](https://cdn.auth0.com/blog/react-js/react.png)

### Why is the Context API useful?

>This new API solves one major problem–prop drilling. Even if you’re not familiar with the term, if you’ve worked on a React.js app, it has probably happened to you. Prop drilling is the processing of getting data from component A to component Z by passing it through multiple layers of intermediary React components. Component will receive props indirectly and you, the React Developer will have to ensure everything works out right.

This is usefull: the complexity of passing data across multiple components ahse been a recouring problem to solve in all of our applications so far. So Context API to me sounds like not the only solution to, but a proposed way to solve this problem of data broadcasting.

### Can a component outside of a provider get its context?

No and from waht i see is that we should log an error if we try. I get this reasoning from:

>The first thing we do is throw an error if we try to access the context outside of our provider. This is a great idea to improve the developer experience of your app (aka: make the console scream at you when you forget how context works).

[source](https://leewarrick.com/blog/the-problem-with-context/)

### What are some common use cases for using the Context API?

- Dynamic Context
- Updating Context from a Nested Component
- Consuming Multiple Contexts

### Describe “Context Hell”

>Context hell

>You may not need the context API if you are not mounting multiple instances of the context. When using the context API, splitting global state properties so as not to share a “god object” creates “Context hell,” a layer of countless contexts wrapping your React application. This very accurately resembles indention or callback hell. Your application can be easier to understand and maintain by not using tools to solve problems you do not have.

[source](https://medium.com/@Charles_Stover/you-may-not-need-a-global-god-state-in-react-206930033895)

*global state*

Definition. The global state of a distributed system is the set of local states of each individual processes involved in the system plus the state of the communication channels.

[source](http://www.cs.sfu.ca/CourseCentral/401/qshi1/slides/Presentation-1.ppt#:~:text=Definition,state%20of%20the%20communication%20channels.)

*global context*

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

*provider*

makes the Redux store available to any nested components that have been wrapped in the connect() function.

*consumer*

A React component that subscribes to context changes. This lets you subscribe to a context within a function component.

[source](https://reactjs.org/docs/context.html#contextconsumer)


