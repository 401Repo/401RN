[Home](https://401repo.github.io/401RN/README)

# Readings: HTTP and REST

![Express](https://miro.medium.com/max/1051/1*q9myzo5Au8OfsaSrCodNmw.png)

### Name 3 real world use cases where you’d want to change the request with custom middleware

Your middleware is used to filter the body of a request for your purposes.

You want to validate cookies

You want to handle errors

### True or false: The route handler is middleware?

false

### In what ways can a middleware function end the process and send data to the browser?

logger, the 404 and 500 errors can display to user

### At what point in the request lifecycle can you “inject” middleware?

uppon incoming request

### What can cause express to error with “Request headers sent twice, cannot start a second response”

the next() failed ot be called leaving a request hanging.

*Middleware*

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

[source](https://expressjs.com/en/guide/using-middleware.html)

*Request Object*

The req object in Express.js allows you to examine every aspect about the request that the client made (whether by browser, by cURL, or mobile browser, etc.). This encompasses lots of things like the URL, user agent string, JSON data, form data… A lot! In this post you’ll learn the basics about the req object in Express.js...

[The post continues on here...](https://www.digitalocean.com/community/tutorials/nodejs-req-object-in-expressjs)

*Response Object*

The res object in Express.js, short for response, gives you a simple interface to respond to HTTP requests.

[A post just as the one before is here, and in the same in depth style...](https://www.digitalocean.com/community/tutorials/nodejs-res-object-in-expressjs)

*Application Middleware*

This kind of middleware method is bind to the app Object  using app.use() method.

[source](http://www.webdevelopmenthelp.net/2017/02/express-middleware-tutorial.html)

*Routing Middleware*

Router-level middleware can be used by using router.use() or router.METHOD().

[source](http://www.webdevelopmenthelp.net/2017/02/express-middleware-tutorial.html)

[Home](https://401repo.github.io/401RN/README)