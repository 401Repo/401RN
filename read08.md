[Home](https://401repo.github.io/401RN/README)

# Readings: HTTP and REST

![Express](https://miro.medium.com/max/1051/1*q9myzo5Au8OfsaSrCodNmw.png)

### What’s the difference between PUT and PATCH?

"You can think about them like this:

POST - it is used to indicate the server to create and store the resource you are sending. As an example, POST /api/log create a new log in the given API and, in case of sucess, it should return 201 Created or 202 Accepted (if the operation is async) while providing a Location and an ETag headers. It may fail if the entity already exists returning a 409 Conflit. Think about it like an insert into a table;

PUT - replaces the existing resource by the new one. As an example, PUT /api/log/1 will completely replace that resource for the new one. Optionally in the request you may include an If-Match with the ETag value to be sure you are replacing the expected version of that resource (preventing concurrency problems). In case of success, it should return a 200 Ok or 202 Accepted (async operations) with the new ETag. In case the entity does not exist, a 404 Not Found must be returned or a 409 Conflict if the version or any other value in the entity are not correct with internal server state (like referenced links). Think about it like an update to a complete row in a table;

PATCH - partially updates the resource into the server mapped by the provided data. As an example, PATCH /api/log/1 will only update properties mapped in the request body. Just like the PUT method it may include an If-Match with the ETag and in case of success 200 Ok or 202 Accepted with the new ETag value should be returned, or in case of a failure a 404 Not Found or 409 Conflict will be indicated with the same conditions as the PUT method. This about it like a partial update to a row in a table, where only some columns are affected;"

[Joao Simoes](https://www.quora.com/What-is-the-difference-between-PUT-POST-and-PATCH-for-RESTful-APIs)

### Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

[POSTMAN](https://www.postman.com/features/mock-api/)

[MOCKY](https://designer.mocky.io/)

[Swagger](https://inspector.swagger.io/builder?_ga=2.199452526.1527408979.1603209622-1494900163.1603209622)

### Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

since client is 400's the codes would be the 500's

### Compare and contrast SOAP and ReST

![SOAP VS REST](https://dzone.com/storage/temp/6632775-rest-vs-soap.png)

*SOAP*

SOAP is an acronym for Simple Object Access Protocol. It is an XML-based messaging protocol for exchanging information among computers. SOAP is an application of the XML specification.

[source](https://www.tutorialspoint.com/soap/what_is_soap.htm)

*REST Verbs*

![Verbs](https://cdn.lynda.com/video/159164-93-635298550191440052_338x600_thumb.jpg)

*CRUD verbs*

![verbs](https://docs.railsbridge.org/job-board/img/crud_grid.jpg)
*Swagger*

allows anyone — be it your development team or your end consumers — to visualize and interact with the API’s resources without having any of the implementation logic in place. It’s automatically generated from your OpenAPI (formerly known as Swagger) Specification, with the visual documentation making it easy for back end implementation and client side consumption.

[source](https://swagger.io/tools/swagger-ui/)

[Home](https://401repo.github.io/401RN/README)