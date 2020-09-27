# TCP

## TCP (Transmission Control Protocol)

### is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. 
### TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other. Together, TCP and IP are the basic rules defining the Internet. 

## How Transmission Control Protocol works
### TCP is a connection-oriented protocol, which means a connection is established and maintained until the application programs at each end have finished exchanging messages. It determines how to break application data into packets that networks can deliver, sends packets to and accepts packets from the network layer, manages flow control and -- because it is meant to provide error-free data transmission -- handles retransmission of dropped or garbled packets and acknowledges all packets that arrive. In the Open Systems Interconnection (OSI) communication model, TCP covers parts of Layer 4, the transport layer, and parts of Layer 5, the session layer.



###  Node.js has net module which provides an asynchronous network API for creating stream-based TCP or IPC servers and clients. We are going to use it to implement TCP server and client. This post is updated with Node v6.11.2.

## What is the OSI model?
### The Open Systems Interconnection (OSI) model is a conceptual model created by the International Organization for Standardization which enables diverse communication systems to communicate using standard protocols. In plain English, the OSI provides a standard for different computer systems to be able to communicate with each other.

![image](https://media.geeksforgeeks.org/wp-content/uploads/computer-network-osi-model-layers.png)
