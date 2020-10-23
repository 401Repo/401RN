[Home](https://401repo.github.io/401RN/README)

# Readings: Express Api

![Express](https://res.cloudinary.com/practicaldev/image/fetch/s--00h6CjGb--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://www.maxrooted.com/panduan-membangun-rest-api-expressjs-mysql/cover.png)

### How does route prefixing work with an external routing module?

A route is the “name” you use to access endpoints, used in the URL. A route can have multiple endpoints associated with it, and which is used depends on the HTTP verb.

For example, with the URL http://example.com/wp-json/wp/v2/posts/123:

The “route” is wp/v2/posts/123 – The route doesn’t include wp-json because wp-json is the base path for the API itself.
This route has 3 endpoints:
GET triggers a get_item method, returning the post data to the client.
PUT triggers an update_item method, taking the data to update, and returning the updated post data.
DELETE triggers a delete_item method, returning the now-deleted post data to the client.

### When routing, what’s the difference between app.get('/data/:id') and app.get('/data/:name')?

one is specific to a mongo ID while the other can have a one to many relationship

### Explain how Express handles routing conflicts?

WE have the errors under the predefined routes to display if none of our defined paths are hit by the request.

[source](https://developer.wordpress.org/rest-api/extending-the-rest-api/routes-and-endpoints/)

### What are the ways that a browser can send “data” or request variables to an HTTP server

Web servers and HTTP (a primer)
Web browsers communicate with web servers using the HyperText Transfer Protocol (HTTP). When you click a link on a web page, submit a form, or run a search, the browser sends an HTTP Request to the server.

This request includes:

- A URL identifying the target server and resource (e.g. an HTML file, a particular data point on the server, or a tool to run).
- A method that defines the required action (for example, to get a file or to save or update some data). The different methods/verbs and their associated actions are listed below:
- GET: Get a specific resource (e.g. an HTML file containing information about a product, or a list of products). 
- POST: Create a new resource (e.g. add a new article to a wiki, add a new contact to a database). 
- HEAD: Get the metadata information about a specific resource without getting the body like GET would. You might for example use a HEAD request to find out the last time a resource was updated, and then only use the (more "expensive") GET request to download the resource if it has changed. 
- PUT: Update an existing resource (or create a new one if it doesn't exist).
- DELETE: Delete the specified resource.
- TRACE, OPTIONS, CONNECT, PATCH: These verbs are for less common/advanced tasks, so we won't cover them here.

[Source](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Client-Server_overview)

*Routing*

Routing is order sensitive. The first match always wins. So it is important that you order you routes from most-specific to least-specific.

Thats why we use the errors are the bottom of the routing structure.

[Source](https://stackoverflow.com/questions/36274985/how-to-map-webapi-routes-correctly)

*Route Prefixing*

They are the endpoints defined in our server that helps to perform operations for a particular client request.

[source](https://www.freecodecamp.org/news/express-explained-with-examples-installation-routing-middleware-and-more/)

*Request “Body”*

When you need to send data from a client (let's say, a browser) to your API, you send it as a request body.

A request body is data sent by the client to your API. A response body is the data your API sends to the client.

Your API almost always has to send a response body. But clients don't necessarily need to send request bodies all the time.

[source](https://fastapi.tiangolo.com/tutorial/body/)

*Request “Query”*
*Request “Params”*

REST API query parameters
You can use query parameters to control what data is returned in endpoint responses.

[Source](https://docs.oracle.com/en/cloud/saas/commerce-cloud/19d/occ-developer/rest-api-query-parameters.html)

![Params](https://docs.bmc.com/docs/ars1908/files/881403083/887396615/1/1565946299678/image2019-8-16_14-19-27.png)

[Home](https://401repo.github.io/401RN/README)