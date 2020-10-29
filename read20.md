[Home](https://401repo.github.io/401RN/README)

# Readings: TCP Servers  

![Source](https://www.aggsoft.com/tcp-com/tcp-com-main-window.png)

### Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?

By declaring the event listeners on the back end we have logi at the ready able to manipulate the dom.

### Why are events sometimes better than asynchronous actions with callbacks?

The dont need to navigate to another system and await a response etc. 

### What does an EventEmitter instance do?

creates an istance of the event listener class.

### When is a program’s call stack, event queue, and event loop active?

![structure](https://miro.medium.com/max/1400/1*iHhUyO4DliDwa6x_cO5E3A.gif)


Stack: This is where all your javascript code gets pushed and executed one by one as the interpreter reads your program, and gets popped out once the execution is done. If your statement is asynchronous: setTimeout, ajax(), promise, or click event, then that code gets forwarded to Event table, this table is responsible for moving your asynchronous code to callback/event queue after specified time.

Heap: This is where all the memory allocation happens for your variables, that you have defined in your program.

Callback Queue: This is where your asynchronous code gets pushed to, and waits for the execution.

Event Loop: Then comes the Event Loop, which keeps running continuously and checks the Main stack, if it has any frames to execute, if not then it checks Callback queue, if Callback queue has codes to execute then it pops the message from it to the Main Stack for the execution.
Job Queue: Apart from Callback Queue, browsers have introduced one more queue which is “Job Queue”, reserved only for new Promise() functionality. So when you use promises in your code, you add .then() method, which is a callback method. These `thenable` methods are added to Job Queue once the promise has returned/resolved, and then gets executed.

[source](https://medium.com/@Rahulx1/understanding-event-loop-call-stack-event-job-queue-in-javascript-63dcd2c71ecd)

*Observer Pattern*

Observer is a behavioral design pattern that lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.

[source](https://refactoring.guru/design-patterns/observer)

*Listener*

our code that defines an event will happen and so to trigger the code associated as a callback

*Event Handler*

we define a listener to a callback function

*Event Driven Programming*

Simply put, event-driven programming is when a program is designed to respond to user engagement in various forms. It is known as a programming paradigm in which the flow of program execution is determined by “events.” Events are any user interaction, such as a click or key press, in response to prompt from the system. To visualize event programming more clearly, imagine the opposite of event-programming is a software that requires zero user interaction.

Events are monitored by a code (or function) known as an event listener. If the event listener detects that an assigned event has occurred, it will trigger a callback function, known as an event handler, which will perform said event, e.g. clicking (the event) a “print” button (event listener) activates the actual print process (event handler).

[source](https://www.edgetechacademy.edu/node-js/event-driven-programming/)

*Event Loop*

A loop with a defined timeout (should be anyways) that means an event will create a request and do 'something' or else we give an error on timeout if the request failed.

*Event Queue*

the order of the events to happen.

*Call Stack*

the slates that have the order of the js to execute.

*Emit/Raise/Trigger*

we use them to set the actions of the client to a back end code to execute on the set of the event/triger by creating an event listener to trigger: no listener no code executes on event.

*Subscribe*

Subscribers are easier to reuse because the knowledge of the events is kept in the class rather than in the service definition. This is the reason why Symfony uses subscribers internally.

Listeners are more flexible because bundles can enable or disable each of them conditionally depending on some configuration value.

[source](https://symfony.com/doc/current/event_dispatcher.html#listeners-or-subscribers)

*database*

A place to handle the data of an organization -  like our mongo db

[Home](https://401repo.github.io/401RN/README)