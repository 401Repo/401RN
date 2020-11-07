# Readings: Asynchronous Actions

### Review, Research, and Discussion

![source](https://miro.medium.com/max/800/1*uHumlKU6fado6sOF2eHVwg.jpeg)

### How granular should your reducers be?

It’s very easy to go full-warp with very specific events, dedicated for every change that occurs when a user is editing forms such as CHANGE_NAME, CHANGE_STREET, CHANGE_AGE, etc…

But it is not actually necessary if the logic behind the update is not different for all those fields. For those parts which require different handling in various reducers; dedicated action is the best solution. For others, sometimes a general action might be good enough.

[source](https://reactkungfu.com/2016/11/how-granular-are-your-redux-actions/)

### Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

##### PRO

My argument would be it is by design: your reducers are being alligned to the common named commands.

### Name a strategy for preventing the above

Dedicated conventions: wich means more work but it would keep everything nice and modularized in redux.


*store

Redux doesn't have a Dispatcher or support many stores. Instead, there is just a single store with a single root reducing function.

[source](https://redux.js.org/api/store)

*combined reducers

for context:

reducers (Object): An object whose values correspond to different reducing functions that need to be combined into one. 

hence:

It's very common to have multiple combined reducers in various places, which are composed together to create the root reducer.

[source](https://www.google.com/search?q=combined+reducers&oq=combined+&aqs=chrome.0.69i59j69i57j0i10i433i457j0i433l2j0j0i433j0.2784j0j9&sourceid=chrome&ie=UTF-8)
