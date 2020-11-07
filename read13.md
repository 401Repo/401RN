[Home](https://401repo.github.io/401RN/README)

# Readings: Authentication

![Source](https://bs-uploads.toptal.io/blackfish-uploads/blog/post/seo/og_image_file/og_image/15921/secure-rest-api-in-nodejs-18f43b3033c239da5d2525cfd9fdc98f.png)

#### Explain what a “Singleton” is (in Computer Science terms)

Its when a class is designed so that it will only create one intance of the class at a time. this is coputer science 101. It is a computer programing pattern or 'singleton' pattern.

#### Explain how the Singleton pattern can be used with Node modules, specifically with classes

from [Deniv Soni](https://medium.com/better-programming/what-is-a-singleton-2dc38ca08e92)

## Use Case

Common use-cases for the singleton design pattern include factories, builders, and objects that hold program state.
Singletons are sometimes considered to be an alternative to global variables or static classes.

Compared to global variables, singletons have the following benefits:
Singleton instance fields don’t take up space in the global namespace
Singletons may be lazily initialized (to be discussed further)
Primarily due to the fact that a singleton holds an instantiated object, whereas static classes do not, singletons have the following advantages over static classes:
- Singletons can implement interfaces
- Singletons can be passed as parameters
- Singletons can have their instances swapped out (such as for testing purposes)
- Singletons can be handled polymorphically, so there may exist multiple implementations

#### If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

Well i mean, we already are. I have no doubt that there are timestamps and also loggers, but we arent using them. Also, our single router settup is a case for middleware. Express handles a lot for us, but at them moment us students are working on middleware too.

*Router Middleware*

The middleware where we settup the routing for our apps using express.

*Dynamic Module Loading*

Exporting in node our nodes but loading them only as needed.  

*Singleton Pattern*

A computer programing class pattern that creates a single instance of a class at a time.

*CRUD -> REST Method Matches*

To me this means that when i have a user model-finder and get my schema up to notice that crud and mongo-mongoose methods might not match in name so i have to keep and eye that every crud operation is included for every route.

*Mock Testing*

Testing with supergoose and other ways to bypass the live authentication for a tewsting purpose.

[Home](https://401repo.github.io/401RN/README)
