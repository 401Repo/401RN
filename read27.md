# Readings: Socket.io

### Review, Research, and Discussion

![source](https://miro.medium.com/max/812/0*xAADmPJN52Yy6XJV.jpg)

### What is the benefit of transforming data into packets?

its a way of data encpsulation. So as to better move data quickly in the network.

### UDP is often refereed to as a connectionless protocol. Why is this?

Several reaasons:

Capturing and Analyzing User Datagram Protocol

UDP is another popular Layer 4 protocol. DNS, TFTP, and many other protocols rely on UDP for their data transmission.


UDP is a connectionless protocol. No connection needs to be established between the source and destination before you transmit data.


UDP does not have a mechanism to make sure that the payload is not corrupted. As a result, the application must take care of data integrity all by itself.


The UDP header is pretty straightforward. It includes only source and destination port numbers, length of the frame, and a UDP message checksum.

[source](https://www.sciencedirect.com/topics/computer-science/connectionless-protocol#:~:text=Capturing%20Network%20Data%20for%20Analysis&text=UDP%20is%20a%20connectionless%20protocol,the%20payload%20is%20not%20corrupted.)

### Can a socket server application have multiple socket connections?

If the data is statelesss it is possible, but a stateful protocol needs a tuple with information and i think it would cause identifcation/ validation errors.

### Can a socket connection application be connected to multiple socket servers?

Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to.

[source](https://stackoverflow.com/questions/11129212/tcp-can-two-different-sockets-share-a-port/11129641#:~:text=A%20server%20socket%20listens%20on%20a%20single%20port.&text=Multiple%20connections%20on%20the%20same,system%20resources%20allow%20it%20to.)

### Can an application be both a socket server and a socket connection?

Yes, you definitely can.

You will have to use threads. I have implemented this in C++ by spawning a thread for a server and another thread for a client.

And here, one thing to notice that client host will be a localhost as both lie on the same machine and you are just creating two different socket with help of two different threads for sending and listening. (server being the listener, and client being the sender).

If you are using TCP, you might have to add a delay in connecting a client after a server thread is spawned, reason being the server socket need to be ready and listening when a client is trying to connect. And if it does not find an active server to connect to, the connection might fail.

Not sure you are looking for the same thing which I have mentioned here.

Hope this answer helps

[source](https://www.quora.com/Can-you-make-a-client-socket-and-a-server-socket-in-one)

##### Document the following Vocabulary Terms

- Term

a server client terminal written in js (i think)

- OSI Model

The Open Systems Interconnection model (OSI model) is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard communication protocols.

The model partitions the flow of data in a communication system into seven abstraction layers, from the physical implementation of transmitting bits across a communications medium to the highest-level representation of data of a distributed application. Each intermediate layer serves a class of functionality to the layer above it and is served by the layer below it. Classes of functionality are realized in software by standardized communication protocols.

[source](https://en.wikipedia.org/wiki/OSI_model)

- TCP Model
TCP/IP Model
Last Updated: 30-09-2020
Prerequisite – Layers of OSI Model

The OSI Model we just looked at is just a reference/logical model. It was designed to describe the functions of the communication system by dividing the communication procedure into smaller and simpler components. But when we talk about the TCP/IP model, it was designed and developed by Department of Defense (DoD) in 1960s and is based on standard protocols. It stands for Transmission Control Protocol/Internet Protocol. The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. The layers are:

Process/Application Layer
Host-to-Host/Transport Layer
Internet Layer
Network Access/Link Layer


![source](https://media.geeksforgeeks.org/wp-content/uploads/tcpAndOSI.png)

[source](https://www.geeksforgeeks.org/tcp-ip-model/)

- TCP

Transmission Control Protocol

- UDP

User Datagram Protocol

- Packets

encapsulated data sent over a server

- Socket

bi directional communication