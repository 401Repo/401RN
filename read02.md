[Home](https://401repo.github.io/401RN/README)

# Review, Research, and Discussion 

### Describe (in plain English) what Array.map() does

![array map](https://scriptverse.academy/img/tutorials/js-array-map.png)

In plain english how would i mention the benefit of array.map() to a 301 student? well i would think about my own anectdotal sittuation: i was just learaning to use forEach(), so i wondered why i should bother to use .map since thye sound like they are the same: the should in theory both target each item in an array, right?

Well the reason to use a .map is because it takes a call back function, so instead of having to say, iterate an array using a for each and the doing extra steps, we can bypass the extra steps by using the callback to automatically handle each element. 

.map wont change the old array, but it doesnt have to/ 

[source](https://www.digitalocean.com/community/tutorials/4-uses-of-javascripts-arraymap-you-should-know)

### Describe (in plain English) what Array.reduce() does

![array reduce](https://res.cloudinary.com/practicaldev/image/fetch/s--YtWZoX0Y--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/mgcuihl4bicusutctlow.png)


.reduce is the wildcard: while .map will provide as many transfirmed elements via a callback function, reduce will give as many or few and whatever types as needed. Thats my 2 cents and also very viable answer. It needs to be studied rather than quickly grasped. 

[source](https://dev.to/chrisachard/map-filter-reduce-crash-course-5gan)

### Describe Super agent 

Super agent goes on to api paths to fetch data for us, and because the data may be vast or not there we dont know how long it will take to fetch it. because of this super agent work with promise that allow us to continue our js programs while knowing that that data will eventually be brought back. 

![super agent](https://static.observableusercontent.com/thumbnail/af6499a8067ea165d26f959a0d2746a4e079d295796c70e574115913e35c8072.jpg)

a .then is the way super agent successfully brings back data. a .catch helper method let us know there was an error. 

![super agent](https://twilio-cms-prod.s3.amazonaws.com/original_images/Copy_of_Language_template_-_node2.png)


Now, lets say that you need one promise to make use of a nother promise... what then? well we can chain succefull promises, but it comes at the cost of time. while async promises will save us time at the cost of order. it all depends on your needs but that is the main reason. So callback funtions dont have to be async all the time.

[source](https://www.twilio.com/blog/5-ways-to-make-http-requests-in-node-js-using-async-await)


[Home](https://401repo.github.io/401RN/README)