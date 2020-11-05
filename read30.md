# Readings: Context API

### Review, Research, and Discussion

![source](https://miro.medium.com/max/1145/1*NLLOEvis3UhMN2gCKKyjfg.png)

###    Describe use cases for useMemo() and useReducer()

>When Should We Employ useReducer

>useReducer is best used when you are dealing with a complex object where individual properties need to be operated on.

>For example, if your app pulls in a complex data object like this, and you need to update different properties within it, you should use useReducer.

That makes sense: there will be plenty of rendering of object properties, especially if we hit an API or are rendering based on attributes.

>The solution is that we use React.memo on the CountButton component, but React.memo only avoids a re-render if its props haven’t changed.

>Since updateCount keeps getting re-initialized in the parent, the prop will look different to React.memo, so it will re-render. But if we use useCallback on updateCount, then it will ONLY re-initialize the function if the specified dependencies change.

I guess we would use memo if we dont want to re-render if props havent changed.

[source](https://medium.com/@binyamin/react-hooks-usereducer-usecallback-usememo-5e5af9b0257a)

###    Why do custom hooks need the use prefix?

Because React has a naming convention, and this prefeix convention helps react find out if hooks are used inproperly.

[source](https://stackoverflow.com/questions/59809947/why-are-react-hooks-named-in-this-fashion-usexxx)

###    What do custom hooks usually do?

They need the 'use' prefix

###    Using any list of custom hooks, research and name one that you think will be useful in your applications
    
I would create one called useLoadingWheel, being mindfull of the convention. on init  would return an html animation and it would only load while things are lagging to render.     
    
###    Describe how a hook that fetches API data might work

There's great exapmples of custom hooks that do this, one of the biggest emphasis the post talk about is that we have to account for that request time to hit the API and come back:

> In the code, we are using async/await to fetch data from a third-party API. According to the documentation every function annotated with async returns an implicit promise: "The async function declaration defines an asynchronous function, which returns an AsyncFunction object. An asynchronous function is a function which operates asynchronously via the event loop, using an implicit Promise to return its result. ". However, an effect hook should return nothing or a clean up function. That's why you may see the following warning in your developer console log: 07:41:22.910 index.js:1452 Warning: useEffect function must return a cleanup function or nothing. Promises and useEffect(async () => ...) are not supported, but you can call an async function inside an effect.. That's why using async directly in the useEffect function isn't allowed. Let's implement a workaround for it, by using the async function inside the effect.

and just like we create an OR for a default variable, we can programatically create a custom hook to search specific topics from an API by built in defaults: Like say wee are hitting the pokeAPI, when we have a custom for all pokemon, or all by type, or all by generation:we can hit the API programttically with a custom hook.

[source](https://www.robinwieruch.de/react-hooks-fetch-data)

