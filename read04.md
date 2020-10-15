[Home](https://401repo.github.io/401RN/README)

# Data Modeling

![data modeling](https://cdn.ttgtmedia.com/rms/onlineimages/data_management-modeling_half_column_mobile.png)


#####    Name 3 advantages to Test Driven Development?

- Better program design and higher code quality

- Detailed project documentation

- TDD reduces the time required for project development

#####    In what case would you need to use beforeEach() or afterEach() in a test suite?

> "Essentially what happens in your test suit is that your Test Runner will register each it/test callback as a "Test" to be run, and will then ensure that all beforeAll, beforeEach, afterAll, and afterEach callbacks are run for each test appropriately to their nesting.

> "Because of this, yourdescribe callbacks essentially have the job of registering all of your it, beforeEach, beforeAll, afterAll, and afterEach callbacks. There really shouldn't be any code inside of your describe's (aside from declaring variables to reference) that is meant to set up or tear down for your tests."

- Zack DeRose

According to Zacks anectdote i would use beforeeach() when the test will change the conditions unlike beforeall() when a test wont change the conditions (as it will run once) and after each to reset whatever conditions i need between test.

#####    What is one downside of Test Driven Development

The test suite itself has to be maintained; tests may not be completely deterministic (i.e. reliant on external dependencies).

#####    What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

> Classes as you may know them from languages like Java don’t technically exist in JavaScript.

> Constructor functions are used, instead. The ES6 `class` keyword desugars to a constructor function:

class Foo {}
typeof Foo // 'function'

There's a great in detail article [here](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

#####    Write an example of a Higher Order function and describe the use case it solves

> Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions. Since we have already seen that functions are regular values, there is nothing particularly remarkable about the fact that such functions exist. The term comes from mathematics, where the distinction between functions and other values is taken more seriously.

Like using one to create other functions or change how they behave. 

#####    Name a use case for a static method

Static method are methods that require an object of a class to get created before when they actually called. To call them we need to create the object of the class in which it is defined. The static method gets a call in two ways one using this keyword another from the constructor... i guess that means i might have a class like Car or bird, and they might need a method that only affects them as a class rather than an atribute/behavior method would.

[Source](https://www.educba.com/javascript-static-method/)

### Document the following Vocabulary Terms

*FP* 

Functional programming (often abbreviated FP) is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Functional programming is declarative rather than imperative, and application state flows through pure functions. Contrast with object oriented programming, where application state is usually shared and colocated with methods in objects.

[source](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)

*pure function*

A pure function is a function where the return value is only determined by its input values, without observable side effects.

*immutable state*

In object-oriented and functional programming, an immutable object (unchangeable object) is an object whose state cannot be modified after it is created.

[source](https://en.wikipedia.org/wiki/Immutable_object)

*object*

instance of a class

*OOP*

The relation between the class (blueprints) of the objects and their actions to create logical  solutions in programs.

*class*

blueprint for objects

*prototype*

All JavaScript objects inherit properties and methods from a prototype.

-W3schools

*Super*

super([arguments]); // calls the parent constructor.

[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)

*inheritance*

a class passes down its attributes to its child classes

*constructor* 

Tells the class the attributes of the objects and their behaviors

*instance* 

the creations of a class object

*context* 

relates to this keyword

*this* 

It has different values depending on where it is used hence context:

   - In a method, this refers to the owner object.
   - Alone, this refers to the global object.
   - In a function, this refers to the global object.
   - In a function, in strict mode, this is undefined.
   - In an event, this refers to the element that received the event.
   - Methods like call(), and apply() can refer this to any object.

*jest* 

Jest is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase.

- jestjs.io

*CI* 

Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, 

*Unit Test*

TDD testing one test case

[Home](https://401repo.github.io/401RN/README)