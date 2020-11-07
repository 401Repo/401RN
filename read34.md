# Reading: React Native

### Review, Research, and Discussion

![source](https://www.appcoda.com/wp-content/uploads/2015/04/react-native.png)

### Compare and Contrast Redux Toolkit with Redux “Ducks”

The widely adopted ducks pattern suggests keeping all Redux functionality in a single file. This file will export a reducer function by default along with all actions creators and constants, if required. It also suggests the pattern for action types.

> Ducks is essentially a proposal for bundling reducers, action types, and actions all into the same file.

It can be a pattern in react redux, and work with the tool kit of redux, and doest have to be a vs "ducks" as far as i can tell.

[source](https://medium.com/swlh/the-good-the-bad-of-react-redux-and-why-ducks-might-be-the-solution-1567d5bdc698)


### What is the principle advantage of Redux Toolkit

Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience.

[source](https://redux.js.org/redux-toolkit/overview#:~:text=Redux%20Toolkit%20makes%20it%20easier,of%20skill%20level%20or%20experience.)


redux toolkit slices

Redux state is typically organized into "slices", defined by the reducers that are passed to combineReducers

[source](https://redux-toolkit.js.org/usage/usage-guide)

namespace

namespacing gives us much better control over which subspaces interact with specific sections of the state.

[source](https://ioof-holdings.github.io/redux-subspace/docs/basics/Namespacing.html)