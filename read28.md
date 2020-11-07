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


=======
# Readings: Hooks API

### Review, Research, and Discussion

![source](https://miro.medium.com/max/2536/1*u0sz5awokC7KveVhyLKjGg.png)


### Why do we not need more .html pages in a multi-page React app?

Well, the components will take up the availble realstate of the page, so we can just control what we want to show up on teh page at any given time.

### If we wanted a component to show up on every page, where would we put it and why?

If we are looking at the hooks then i would thing about using conetext:

>Inside all the components where you need to use the Context, you will have to use the other, most important Hook, useContext! Passing it the AppStateContext.

>After that, you will be able to access the values passed to the context. In this case, we have the functions SetMessage and SetError to manage all the notifications of our app in a centralized way.

>You can also import only the values you need from the Context.

[source](https://medium.com/better-programming/react-global-component-with-hooks-d1471488cf73)

### What does props.children contain?

What even is ‘children’?

The React docs say that you can use props.children on components that represent ‘generic boxes’ and that don’t know their children ahead of time. For me, that didn’t really clear things up. I’m sure for some, that definition makes perfect sense but it didn’t for me.

My simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.

*Composition*

What's composition in general? It's the ingredients and the arrangement of these ingredients to create something bigger out of it. It's the samples in a piece of music that make up a track. It's the fruits that are used for the perfect smoothie.

*Children / Child Components*

Children allow you to pass components as data to other components, just like any other prop you use. The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children!

[source](https://buildwithreact.com/article/component-children)

*Hash Routing*

A Router that uses the hash portion of the URL (i.e. window.location.hash) to keep your UI in sync with the URL.

IMPORTANT NOTE: Hash history does not support location.key or location.state. In previous versions we attempted to shim the behavior but there were edge-cases we couldn’t solve. Any code or plugin that needs this behavior won’t work. As this technique is only intended to support legacy browsers, we encourage you to configure your server to work with <BrowserHistory> instead.

basename: string

The base URL for all locations. A properly formatted basename should have a leading slash, but no trailing slash.

[source](https://reactrouter.com/web/api/Link)

A single child element to render.


*Link Routing*

Provides declarative, accessible navigation around your application.

[source](https://reactrouter.com/web/api/Link)

