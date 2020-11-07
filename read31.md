# Readings: Redux - Combined Reducers

### Review, Research, and Discussion

![source](https://reactgo.com/static/0e64ddc179ba16d628b380c1e6c8391d/72f41/multiple-reducers-redux.png)

### Why choose Redux instead of the Context API for global state?

- Persist state to a local storage and then boot up from it, out of the box.

- Pre-fill state on the server, send it to the client in HTML, and boot up from it, out of the box.

- Serialize user actions and attach them, together with a state snapshot, to automated bug reports, so that the product developers
can replay them to reproduce the errors.

- Pass action objects over the network to implement collaborative environments without dramatic changes to how the code is written.

- Maintain an undo history or implement optimistic mutations without dramatic changes to how the code is written.

- Travel between the state history in development, and re-evaluate the current state from the action history when the code changes, a la TDD.

- Provide full inspection and control capabilities to the development tooling so that product developers can build custom tools for their
apps.

- Provide alternative UIs while reusing most of the business logic.

[source](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)

### What is the purpose of a reducer?

A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

[source](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)

### What does an action contain?

Actions are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using store.dispatch() . Actions are plain JavaScript objects.

[source](https://redux.js.org/basics/Actions)

### Why do we need to copy the state in a reducer?

###### Rules of Reducers:

- They should only calculate the new state value based on the state and action arguments

Now check this out:

-  They are not allowed to modify the existing state. Instead, they must make immutable updates, by copying the existing state and making changes to the copied values.

- They must not do any asynchronous logic or other "side effects"

[source](https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers)

*immutable state*

Never mutate this.state directly, as calling setState() afterwards may replace the mutation you made. Treat this.state as if it were immutable.

[react docs](https://facebook.github.io/react/docs/react-component.html#state)

*time travel in redux*

The Redux DevTools records dispatched actions and the state of the Redux store at every point in time. This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app.

[source](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0)

*action creator*

An action creator is, quite simply, a function that creates an action. Do not confuse the two terms—again, an action is a payload of information, and an action creator is a factory that creates an action.

[source](https://redux.js.org/understanding/thinking-in-redux/glossary#action-creator)

*reducer*

A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

[source](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)

*dispatch*

The dispatch method is a method of the store object. An action is dispatched to trigger an update to the store.

[source](https://blog.bam.tech/developer-news/4-ways-to-dispatch-actions-with-redux)