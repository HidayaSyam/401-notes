# Message Queues
### A message queue is a queue of messages sent between applications. It includes a sequence of work objects that are waiting to be processed.

### A message is the data transported between the sender and the receiver application; it's essentially a byte array with some headers at the top. An example of a message could be something that tells one system to start processing a task, it could contain information about a finished task or just be a plain message.

### Message queues
#### A message queue provides an asynchronous communications protocol, which is a system that puts a message onto a message queue and does not require an immediate response to continuing processing. Email is probably the best example of asynchronous communication. When an email is sent, the sender continues to process other things without needing an immediate response from the receiver. This way of handling messages decouples the producer from the consumer so that they do not need to interact with the message queue at the same time.


- What does it mean that web sockets are bidirectional? Why is this useful?
  -  An important consequence is that you may efficiently push data from the server to the client. Underlying sockets are just kept open (or reopened when needed if they couldn't be kept open). ... In HTTP/1.0 a separate connection to the same server is made for every resource request.
- Does socket.io use HTTP? Why?
  - The WebSocket protocol enables interaction between a web browser (or other client application) and a web server with lower overhead than half-duplex alternatives such as HTTP polling, facilitating real-time data transfer from and to the server.
- What happens when a client emits an event?
  - The event gets passed to the server through websockets. Its a tcp connection from the browser to the server. The connection is full duplex meaning the server can send real time data to the client and vise versa.
- What happens when a server emits an event?
  - The events module allows us to easily create and handle custom events in Node.js. This module includes the EventEmitter class, which is used to raise and handle the events.

  Almost the whole of the Node.js core API is built around this module, which emits named events that cause function objects (also known as listeners) to be called. At the end of the article, we should have built a very simple module that implements the event module.
- What happens if a client “misses” an event?
  - If the client misses an event, it can cause a website to freeze and become unstable. Also, some of the other functions that were relying on the event listeners will be missed. 
- How can we mitigate this?
  - We can have an error handler to prevent any unwanted failures. 

### Terms

1. Web Socket - is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server. With this API, you can send messages to a server and receive event-driven responses without having to poll the server for a reply.
1. Socket.io - Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server. It consists of;
  - a Node.js server:
  - a Javascript client library for the browser (which can be also run from Node.js
1. Client - Client-side means that the JavaScript code is run on the client machine, which is the browser. 
1. Server - Server-side JavaScript means that the code is run on the server which is serving web pages.

