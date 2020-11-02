
# React Props

![Source](https://scriptverse.academy/img/tutorials/reactjs-components-props.png)

### Does a deployed React application require a server?

You always need a way to get to the internet w your content, i guess it comes down to how react does it; "React. js does not use a web server to create virtual DOMs. It builds the virtual DOM and does its diff operations on the client's browser."

[source](https://stackoverflow.com/questions/26696204/does-react-js-require-server-side)

### Why do we prefer to test a React application at the behavior rather than the unit level?

Because we can modularize our testing by testing components rather than granular units of each component of the app; the thought being that we are testing the app as is rather than could be: we test the current app.

### What does npm run build do?

creates our base app

### Describe the actual composition / architecture of a React application

api/
  APIUtils.js
  APIUtils.test.js
  ProfileAPI.js
  UserAPI.js
components/
  Avatar.js
  Avatar.css
  Feed.js
  Feed.css
  FeedStory.js
  FeedStory.test.js
  Profile.js
  ProfileHeader.js
  ProfileHeader.css

*BDD*

behavior driven development, wich i imagine is why we test the app not the units

*Acceptance Tests*

see is we get satisfactory modules in our app by the user.

*mounting*

Mounting
These methods are called in the following order when an instance of a component is being created and inserted into the DOM:

constructor()
static getDerivedStateFromProps()
render()
componentDidMount()

[source](https://reactjs.org/docs/react-component.html)

*build*

create a new module / app version.

[Home](https://401repo.github.io/401RN/README)