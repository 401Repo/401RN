[Home](https://401repo.github.io/401RN/README)

# Readings: HTTP and REST

![HTTP](https://phpenthusiast.com/theme/assets/images/blog/what_is_rest_api.png)



##### Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.


##### What is the advantage of an ORM, like Mongoose?

###### Advantages:

- Speeds-up Development - eliminates the need for repetitive SQL code.
- Reduces Development Time.
- Reduces Development Costs.
- Overcomes vendor specific SQL differences - the ORM knows how to write vendor specific SQL so you don't have to.

###### Disadvantages:

- Loss in developer productivity whilst they learn to program with ORM.
- Developers lose understanding of what the code is actually doing - the developer is more in control using SQL.
- ORM has a tendency to be slow.
- ORM fail to compete against SQL queries for complex queries.

[Source](https://stackoverflow.com/questions/4667906/the-advantages-and-disadvantages-of-using-orm)

##### How does the repository pattern compare with an ORM?

Repositories deal with Domain/Business objects (from the app point of view), an ORM handles db objects. A business objects IS NOT a db object, first has behaviour, the second is a glorified DTO, it only holds data.

[Source](https://stackoverflow.com/questions/10155517/repository-pattern-vs-orm#:~:text=Repositories%20deal%20with%20Domain%2FBusiness,DTO%2C%20it%20only%20holds%20data.)

##### When making a repository/facade, what flexibility do you gain?

Software developers use the repository pattern to separate the logic that retrieves the data and maps it to an entity model from the business logic that acts on the model. This enables the business logic to be agnostic to the type of data that comprises the data source layer.

[Source](https://garywoodfine.com/generic-repository-pattern-net-core/)

##### Name 3 cloud based NoSQL Databases

![Source](https://cdn.ttgtmedia.com/rms/onlineimages/cloud_computing-nosql_comparison.png)

### Document the following Vocabulary Terms

*lifecycle*

To put data science in context, we present phases of the data life cycle, from data generation to data interpretation. These phases transform raw bits into value for the end user. Data science is thus much more than data analysis, e.g., using techniques from machine learning and statistics; extracting this value takes a lot of work, before and after data analysis. Moreover, data privacy and data ethics need to be considered at each phase of the life cycle.

[Source](https://hdsr.mitpress.mit.edu/pub/577rq08d/release/3)

*collections*

MongoDB stores documents in collections. Collections are analogous to tables in relational databases.

[Source](https://docs.mongodb.com/manual/core/databases-and-collections/#collections)

*the “Repository” design pattern*

Repositories deal with Domain/Business objects (from the app point of view), an ORM handles db objects. A business objects IS NOT a db object, first has behaviour, the second is a glorified DTO, it only holds data.

[Source](https://stackoverflow.com/questions/10155517/repository-pattern-vs-orm#:~:text=Repositories%20deal%20with%20Domain%2FBusiness,DTO%2C%20it%20only%20holds%20data.)

*mongoose middleware*

Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.

[Source](https://mongoosejs.com/docs/middleware.html)

*Object Relation Mapping (ORM)*

Object-relational-mapping is the idea of being able to write queries like the one above, as well as much more complicated ones, using the object-oriented paradigm of your preferred programming language.

[Source](https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a)

[Home](https://401repo.github.io/401RN/README)