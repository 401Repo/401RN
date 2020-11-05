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