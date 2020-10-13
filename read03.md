[Home](https://401repo.github.io/401RN/README)

# Classes, Inheritance, Functional

![node](https://cdn-media-1.freecodecamp.org/images/1*DF0g7bNW5e2z9XS9N2lAiw.jpeg)


#####    Why would you want to run JavaScript code outside of a browser?

Outside of a browser we are no longer concerned to displaying tot eh client and instead we are now using node to interact with the database and maybe do restful API work etc outside of the "visual".

#####    What is the difference between a module and a package?

A module is a file that we can reference while a package is a place for the modules to ive in.

#####    What does the node package manager do?

While this is a very high level way to look at it: the NPM manages and keeps track of the dependency of the nodes. It is where we are able to store the nodes and export them for our JS needs as they arise.

### Document the following Vocabulary Terms

*ecosystem* 

The JS ecosystems emcompases: The different aspects of JavaScript: Front-end development, Command line interface (CLI) applications, Desktop (GUI) applications, Mobile applications, Back-end development, Any combination of the above.

[source](https://medium.com/@krposlek/overview-of-the-javascript-ecosystem-8ec4a0b7a7be)

*Node.js*

As an asynchronous event-driven JavaScript runtime, Node.js is designed to build scalable network applications.

[source](https://nodejs.org/en/about/)

*V8 Engine*

V8 is Google's open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node. js, among others. It implements ECMAScript and WebAssembly, and runs on Windows 7 or later, macOS 10.12+, and Linux systems that use x64, IA-32, ARM, or MIPS processors.

[source](https://v8.dev/)

*module*

A module is just a file. One script is one module. As simple as that.

[source](https://javascript.info/modules-intro)

*package*

A package in Node.js contains all the files you need for a module.

Modules are JavaScript libraries you can include in your project.

[source](https://www.w3schools.com/nodejs/nodejs_npm.asp)

*node package manager (npm)*

npm , short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node. js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

[source](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/)

*server*

A Node. js server makes your app available to serve HTTP requests. It provides the interaction between users and your application. Creating and starting a server is easy with Node. js's built-in http module.

[source](https://stackabuse.com/how-to-start-a-node-server-examples-with-the-most-popular-frameworks/)

*environment*

a runtime enviroment, the node.js allows us to run js in its enviroment.

*interpreter*

js interpreter or a Node. js on Windows Subsystem for Linux. The term local Node. js interpreter denotes a Node. js installation on your computer.

*compiler* 

Standard Node.js is built against V8, which compiles every Javascript code snippet into native instructions. You may use --print_code flag in the command line to see which scripts are getting compiled, and compiled into what.

#####    Provide code snippets showing 3 different ways to export a function from a node module

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