
# React Message Queues

![Source](https://docs.servicestack.net/images/messaging/servicestack-mqclients.png)

### What does it mean that web sockets are bidirectional? Why is this useful?

It means it is a web socket:

What is WebSocket?
WebSocket is a relatively new piece of the web development toolkit. In short, it’s a new type of communications protocol that is different from HTTP. WebSocket allows a single TCP socket connection to be hijacked so that the client-server relationship can relay bi-directional, full-duplex (or sometimes also referred to as double-duplex) messages instantaneously. An example of a full-duplex communications system include your cell phone: both parties can speak and hear the other at the same time.

[source](https://medium.com/@nerdplusdog/websocket-simultaneous-bi-directional-client-server-communication-e7948203054b)

### Does socket.io use HTTP? Why?

Its a new type of communication protocol than http requests

### What happens when a client emits an event?

It seems to be the way we can trigger events on the server and pieces in the process of communication. 

There has to be a handshake and then there is a channel that is subscribd to for the messageing to be expected.

### What happens if a client “misses” an event?
### How can we mitigate this?

There seems to be ways to prevent this loss of data by having a buffer for the communication, and also there is the ability to create work around fro buffer overflow. At teh end of the day JS is a single thread language and we need async functions to take these considderations for our purposes.

Web Socket

new information protocol that enables instant communitcation (vs http requests)

Socket.io

the websocket js library

Client

our compute / the people accesing the data

Server

the computer hosting our app over the internet / accesible to users.

[Home](https://401repo.github.io/401RN/README)