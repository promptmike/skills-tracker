# OSI Model

## Task 1 - What is the OSI Model?

The Open Systems Interconnection Model (OSI) provides the framework for how networked devices will send, receive and interpret data.
Connected devices must follow a common model of communication to send, receive and interpret data on a Network.

The OSI Model allows devices with different functions and designs to communicate with each other.
Connected devices with different functions and designs can still communicate if they follow a common model.

The OSI Model has 7 layers: 7. Application, 6. Presentation, 5. Session, 4. Transport, 3. Network, 2. Data Link, 1. Physical.
Connected devices with different functions and designs can communicate by following a common model at different layers.

Information is added to the data as it moves through the OSI layers in a process called Encapsulation.
Connected devices with different functions and designs can communicate by Encapsulating data with a common model.

## Task 2 - Layer 1 - Physical

Physical hardware such as ethernet cables transmits binary data as electrical signals.
Connected devices with different functions can communicate by OSI Encapsulation, layer 1 of which is Physical.

## Task 3 - Layer 2 - Data Link

The Data Link layer receives a packet from the Network layer and adds the MAC Address (found on the Network Interface Card) of the destination.
Networked devices communicate by OSI Encapsulation, including Physical connection and Data Link.

MAC Addresses are burned into the NIC so they cannot be changed, although they can be spoofed, and they are used to identify data destinations.
Networked devices communicate by OSI Encapsulation, in which the Data Link must add the MAC Address to the Network layer packet.

The Data Link layer presents data in a format suitable for transmission.
Network layer packets are sent to the Data Link to have MAC Addresses added and be presented in the right format for Physical transmission.

## Task 4 - Layer 3 - Network

At the Network layer of OSI the data is reassembled and Routed through the most optimal connection path.
Network layer packets are reassembled and Routed, then the Data Link adds MAC Addresses and presents them for Physical transit.

The optimal path is determined by protocols such as Open Shortest Path First (OSPF) or Routing Information Protocol (RIP).
The Network reassembles and Routes packets using a route optimisation protocol, then the Data Link presents them for Physical transit.

Routing factors to consider are length (how many nodes), reliability (have packets been lost here before) and speed (how long the packets take).
The Network reassembles packets and chooses an optimal route, then the Data Link presents them with MAC Addresses for Physical transit.

At the Network layer everything is dealt with using IP Addresses, so devices such as Routers are known as Layer 3 Devices.
Layer 3 devices reassemble packets and choose an optimal route for them, the Data Link then presents them with MAC Addresses for Physical transit.

## Task 5 - Layer 4 - Transport

The Transport layer follows either the Transport Control Protocol (TCP) or User Datagram Protocol (UDP).
Transport uses TCP or UDP, Network reassembles and routes, Data Link adds MAC Address and presents for Physical transit.

TCP is designed for reliability and guarantee by constantly reserving a connection between the sending and receiving device.
Transport uses TCP for reliable connection, or else UDP, Network reassembles and routes, Data Link adds MAC Address and presents for Physical.

TCP incorporates error checking to make sure the data received from the Session layer is sent to the Network layer in the correct order.
Session data is sent to Transport and processed with TCP or UDP for the Network to reassemble and route, then Data Link presents for Physical.

TCP guarantees data accuracy, but requires a constant connection such that if a small amount of data is lost the whole chunk cannot be used.
Session data goes to Transport to be processed with TCP with constant connection for the Network to reassemble and route for Data Link.

TCP synchronises devices to prevent them being flooded with data, but this can cause bottlenecks as the connection must be reserved.
Session data goes to Transport with reserved TCP connection for the Network to reassemble and route, then Data Link adds MAC Address and presents.

TCP performs a lot more processes for reliability, but this does make it significantly slower than UDP as more work has to be done.
Session data goes to Transport for TCP reserved connection and error handling, then the Network routes it and Data Link adds MAC Addresses.

TCP is used for things like file sharing, browsing and emails, because accuracy is more important than speed.
Session data goes to Transport and a TCP connection is reserved if needed, then Network routes it and Data Link adds MAC Addresses for Physical.

Webservers break files into chunks called Packets, which are then reconstructed by the client.
Session Packets go to Transport, TCP connection is reserved if needed, Network routes the Packets and Data Link adds MAC Addresses for Physical.

UDP just sends data with no reserved connection, synchronisation, error checking or guarantees.
Session Packets go to Transport for TCP or UDP, Network routes them and Data Link adds MAC Addresses and presents for Physical transit.

UDP is faster than TCP, but does not check that the data is received.
Session Packets go to Transport for TCP, or UDP if guarantees are not needed, then Network routes them and Data Link adds MAC Addresses.

UDP leaves the Application layer to decide if there is any control on how quickly packets are sent, so it is flexible to developers.
Session Packets go to Transport for TCP or UDP, depending on priorities, then Network routes them and Data Link adds MAC addresses and presents.

UDP does not reserve a connection, but this can result in a terrible experience for the user if the connection is unstable.
Session Packets go to Transport for TCP (if guarantees are needed) or UDP (if speed is the priority), then Network routes them for Data Link.

UDP is useful for small pieces of data (e.g. ARP or DHCP) or large transfers where occasional errors don't matter (e.g. video streaming).
Session Packets go to Transport for TCP (if accuracy is the priority) or UDP (if speed is the priority), then Network, Data Link and Physical.

## Task 6 - Layer 5 - Session

The Session layer takes Packets already translated and formated by Presentation and establishes and maintains a connection to the destination.
Presentation Packets go to Session for a connection to the destination to be established, then go to Transport, Network, Data Link and Physical.

The Session can close a lost connection, or create Checkpoints where lost data is abandoned and only newer data is sent, savind bandwidth.
The Session layer manages the connection and creates Checkpoints, Transport sends data using the correct protocol, Network routes for Data Link.

Sessions are unique - data cannot travel between Sessions.
A unique Session manages connection and creates Checkpoints, Transport uses the correct protocol, Network routes, Data Link adds MAC Addresses.

## Task 7 - Layer 6 - Presentation

The Presentation layer is needed, because data must be standardised for transit even if it comes from very different software designs.
Data Packets are standardised by Presentation, sent to a Session, Transported by TCP or UDP and Routed by the Network for Data Link and Physical.

The Presentation layer acts as a translator for the Application layer (e.g. you can send emails between different email clients).
Presentation translates data, Session maintains connection, Transport applies protocol, Network routes, Data Link adds MAC Addresses for Physical.

Security features such as HTTPS are applied at the Presentation layer.
Presentation translates and secures, Session maintains connection, Transport applies protocol, Network routes, Data Link addresses for Physical.

## Task 8 - Layer 7 - Application

The Application layer establishes the rules for how the user should interact with data sent or received.
Applications interact with the user, Presentation translates, Session connects, Transport uses protocol, Network routes, Data Link addresses.

Some Applications are seen by the user with a GUI, while others such as DNS are used by servers.
Applications interact, Presentation translates, Session connects, Transport uses protocol, Network routes, Data Link addresses for Physical.

## Task 9 - Practical - OSI Game

Climb the levels in the correct order to escape the dungeon and find the flag.
Physical - Data Link - Network - Transport - Session - Presentation - Application.

## Task 10 - Continue Your Learning: Packets & Frames

Packets and Frames in the next room.
`1. Physical - 2. Data Link - 3. Network - 4. Transport - 5. Session - 6. Presentation - 7. Application is the OSI Model`