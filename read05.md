[Home](https://401repo.github.io/401RN/README)

# Readings: Advanced Mongo/Mongoose

![data modeling](https://miro.medium.com/max/594/1*vK4MHL_jpKKmUFGjE5H9jw.png)


#####    Why would a developer choose to make data models?

Reduce validation by having a clear list of requirements for the objects created. 

#####    What purpose do CRUD operations serve?

They stand for create, read, update, and delete. These are the basic functions that are needed to fundamentally build and maintain APIS.

#####    What kind of database is Postgres? What kind of database is MongoDB?

If you want freedom of non mapped tabular structure to handle any kind of data quickly the mongo is the way to go.

If you need rock solid SQL, and know what your pre mapped structure of data relations will be then prosgress works best.

#####    What kind of database is Postgres? What kind of database is MongoDB?

If you want freedom of non mapped tabular structure to handle any kind of data quickly the mongo is the way to go.

If you need rock solid SQL, and know what your pre mapped structure of data relations will be then prosgress works best.

####      What is Mongoose and why do we need it?

> Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

 - Nick Karnik

 That makes sence: we are premodeling and building schemas for our app. This makes sence now.

[Source](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)

### Document the following Vocabulary Terms

*database* 

a collection of data for an organisation, etc.

*data model*

The way to see the abstaraction of how data will relate to each other in an data organization.

*CRUD*

CREATE READ DELETE UP

*schema*

Map for an object validation purposes for databese

*sanitize*

making sure we accound for the commands coming in to our program and validate to ensure control of the data.

*Structured Query Language (SQL)*

A way to communicate with SQL databases to perform CRUD operations.

*Non SQL (NoSQL)*

Stores info in other ways than tables.

*MongoDB*

A non SQL database

*Mongoose*

A library for mongo DB 

*record*

a saved entry in a db

*Object Relation Mapping (ORM)*

What mongoose is to mongoDB

[Home](https://401repo.github.io/401RN/README)