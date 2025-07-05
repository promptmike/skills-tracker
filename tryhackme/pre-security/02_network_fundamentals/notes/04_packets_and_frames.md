# Packets and Frames

## Task 1 - What are Packets and Frames

Packets and Frames are small chunks of data, but frames are only at Layer 2 (Data Link) so there are no IP Addresses.
Data is broken down into small chunks called Frames at Layer 2 and Packets above Layer 2.

Frames are Encapsulated within Packets which are sent to IP Addresses, but the Frame only has the destination MAC Address.
Data is broken down into Packets addressed to IP Addresses and Encapsulated in Frames addressed to MAC addresses.

Transmitting large files all at once can cause bottlenecking, so breaking them down into Packets improves performance.
Data is broken down into Packets with IP addressing and Encapsulated within Frames with MAC addressing to prevent bottlenecking.

Data is broken into Packets and Frames server-side to be reassembled client-side.
Data is broken into Packets with IP addressing and Encapsulated within Frames with MAC addressing to be reassembled client-side.

Different types of Packets can have different structures, so standardisation is important.
Data is broken into Packets with IP addressing and Encapsulated within Frames with MAC addressing following standardised rules for transfer.

IP Packets have Headers that provide additional information.
Data is broken into Packets with Headers and IP Addressing and Encapsulated within Frames with MAC addressing following common standards.

Time To Live is a Header that sets an expiry time for a Packet so it does not slow down your Network if it fails to reach its destination.
Data is broken into Packets with Headers to show Routers what to do with it and Encapsulated within Frames with the destination MAC Address.

A Checksum Header is used by protocols such as TCP/IP to check the integrity of data and detect data corruption.
Data is broken into Packets with Headers to provide useful information such as TTL or Checksum, then Encapsulated within Frames.

Source Address is a Header containing the IP Address of the source so that the receiver knows where to reply to.
Data is broken into Packets with Headers containing information such as TTL, Checksum or Source Address, then Encapsulated in Frames.

Destination Address is a Header containing the IP Address of the destination so that Routers know where to send it.
Packets have Headers with information such as TTL, Checksum, Source Address and Destination Address and are Encapsulated in Frames.

## Task 2 - TCP/IP (The Three-Way Handshake)

Transmition Control Protocol / Internet Protocol (TCP/IP) is a standard set of rules that allow different Applications to communicate.
Packets have Headers with information such as TTL, Checksum, Source and Destination, are Encapsulated in Frames and sent by standard protocols.

The TCP/IP Model contains 4 Layers that summarise the Layers of the OSI Model.
Packets have Headers with useful information and are Encapsulated by Layers of standard Models.

The Layers of TCP/IP are Application - Transport - Internet - Network Interface.
Data is broken into Packets with Headers and Encapsulated by Layers of a standard Model such as TCP/IP.

Information is added to a Packet at each Layer of TCP/IP (Encapsulation) and then removed as it goes back up the Layers (Decapsulation).
Data is broken into Packets with Headers and Encapsulated by Layers of a standard Model such as TCP/IP, then Decapsulated moving back up Layers.

TCP is connection-based, meaning it must establish a connection between client and server before information is sent.
Data is broken into Packets with Headers and Encapsulated by Layers of a standard Model such as the connection-based TCP/IP Model.

TCP guarantees data will be received by using a three-way handshake.
Packets are given Headers and Encapsulated by Layers of a standard Model like the connection-based TCP/IP Model that uses a three-way-handshake.

TCP guarantees data integrity, but if a small amount of data is lost the whole chunk must be re-sent.
Packets are Encapsulated by Layers of a Model such as TCP/IP which guarantees receipt, but can be inefficient due to needing a stable connection.

TCP synchronises devices to prevent flooding of data in the wrong order, but it can lead to bottlenecking as the connection must be reserved.
Packets are Encapsulated by Layers of a Model such as TCP/IP which provides strong guarantees, but can be slow and prone to bottlenecking.

TCP performs a lot of processes for reliability, but this makes it slower than UDP as more work must be done.
Packets are Encapsulated by Layers of a Model such as TCP/IP which provides reliability and guarantees, but is much slower than UDP.

TCP Packets contain Headers that are added from Encapsulation.
Packets are given Headers by Encapsulation in Models such as TCP/IP which is very reliable or UDP which is much faster.

Source Port is a TCP Header that contains the Port to send from, selected randomly from any Ports 0 - 65535 that are not already in use.
Packets are given Headers such as Source Port (2^16 options) by Encapsulation in reliable Models like TCP/IP or fast Model like UDP.

Destination Port is a TCP Header containing the Port to send the Packet to (e.g. a Webserver on Port 80).
Packets are given Headers such as Source Port (2^16 options) or Destination Port (predetermined) by Encapsulation in Models such as TCP/IP.

Source IP is a TCP Header containing the IP Address of the device sending the Packet.
Packets are given Headers such as Source Port (2^16 options), Destination Port (predetermined) or Source IP by Encapsulation in Layers of a Model.

Destination IP is a TCP Header containing the IP Address of the device the Packet is destined for.
Packets are given Headers such as Source Port, Destination Port, Source IP and Destination IP by Encapsulation in Layers of a Model like TCP/IP.

Sequence Number is a TCP Header containing a random number (more on this later).
Packets are given Headers such as Source Port, Destination Port, Source IP, Destination IP and Sequence Number by Encapsulation in Models.

The Acknowledgement Number is a TCP Header that returns the Sequence Number +1 (more on this later).
Packets are given Headers such as Source Port, Destination Port, Source IP, Destination IP, Sequence Number and Acknowledgement Number.

The Checksum is a TCP Header containing the result of a calculation performed on the data so that it can be checked for integrity.
Packets have Headers such as Source Port, Destination Port, Source IP, Destination IP, Sequence Number, Acknowledgement Number and Checksum.

The Data Header is a TCP Header that contains the Packet data to be sent.
Packet Headers include Source Port, Destination Port, Source IP, Destination IP, Sequence Number, Acknowledgement Number, Checksum and Data.

Flag is a TCP Header determining how devices should handle the Packet during the Handshake process.
TCP Headers include Source Port, Destination Port, Source IP, Destination IP, Sequence Number, Acknowledgement Number, Checksum, Data and Flag.

The Three-Way Handshake uses special messages to establish a connection in the TCP Model.
TCP/IP Headers contain Data, integrity checks and information on what to do with the Data, while the Three-Way Handshake establishes connection.

The SYN TCP Packet is the first step in the Three-Way Handshake, sent by the client to attempt a connection.
TCP/IP Headers contain Data, integrity checks and data handling information, while the Three-Way Handshake sends special packets like SYN.

The SYN/ACK TCP Packet (step 2) is a special message sent by the server to acknowledge the client's attempt to establish a connection.
TCP/IP Headers contain Data, integrity checks and handling information, while the Three-Way Handshake sends special packets like SYN and SYN/ACK.

The ACK TCP Packet (step 3) can be sent be client or server to acknowledge that a Packet or series of Packets has been received.
TCP/IP Headers contain Data and additional information, while the Three-Way Handshake sends special messages like SYN, SYN/ACK and ACK.

A DATA TCP Packet contains the data to be sent and is only sent after a connection has been established.
TCP/IP sends different types of Packets with different Headers, including SYN, SYN/ACK then ACK to establish connection, followed by DATA.

The FIN TCP Packet cleanly closes a connection when it is no longer needed.
TCP Packets contain information in Headers and come in different types such as SYN, SYN/ACK and ACK (connect), DATA (data) and FIN (close).

The RST packet can be sent as a last resort to terminate a connection abruptly.
TCP Packets contain information in Headers and come in types such as SYN, SYN/ACK and ACK (connect), DATA (data), FIN (disconnect) and RST (stop).

The Three-Way Handshake is `1. SYN (attempt connection) - 2. SYN/ACK (acknowledge connection attempt) - 3. ACK (acknowledge connection)`
TCP Packets establish connection with a Three-Way Handshake and send Data with Headers for reliable transmition.

Data sent by TCP is given a random number sequence which is incremented so that the correct order can be reconstructed.
TCP Packets establish connection with a Three-Way Handshake and send Data with Headers for sequence and integrity checking.

SYN establishes client sequence, SYN/ACK establishes server sequence and acknowledges client sequence, ACK acknowledges server sequence.
TCP Packets establish connection with a Three-Way Handshake that sets up an incrementing number sequence to keep data in the correct order.

### TCP Closing a Connection:

TCP will close a connection after it establishes that the receiving device has received all of the data.
TCP Packets establish connection and preserve data order with a Three-Way Handshake and number sequencing, then close the connection.

It is best practice to close TCP connections as soon as possible, because they reserve system resources on devices.
TCP Packets perform Three-Way Handshake to connect and exchange sequences, then close connection as soon as possible.

To close a TCP connection one device sends a FIN Packet and the other acknowledges this.
TCP Packets can establish connections, exchange order-preserving sequences, send data, close connections and acknowledge connection closure.

For example, Alice sends Bob a FIN, Bob sends and ACK and a FIN, then Alice sends an ACK.
TCP Packets establish connection, exchange order-preserving sequences, provide checksums, send data, close connections and acknowledge each step.

## Task 3 - Practical - Handshake

Help Alice and Bob communicate in TCP to get the flag.
TCP Packets have Headers to establish connections, preserve data order, checksum data, send data, close connections and acknowledge each step.

## Task 4 - UDP/IP

The User Datagram Protocol (UDP) is another protocol that can be used to transmit data between Networked devices.
Packets have Headers to provide information on what to do with them, get routed by Networks and are Encapsulated in Frames by the Data Link.

UDP is a stateless protocol, requiring no synchronisation, so a connection does not need to be established and reserved.
Packets can be sent using connection-based or stateless protocols to a Network, which then routes them for Encapsulation in Frames by Data Link.

UDP is used in situation where data loss is acceptable, but slow speed is not acceptable.
Packets can be sent using different protocols for different use cases, then they are routed by a Network and Encapsulated in Frames by Data Link.

UDP is much faster than TCP, but does nothing to check if data is received or not.
Packets can be sent using different protocols for different use cases, depending on the needs of the user, then they are Encapsulated in Frams.

UDP leaves the Application layer to decide if there is any control over how fast Packets are sent, so it is flexible to developers.
Packets are sent using protocols for different use cases of the user and developer, routed through Networks and Encapsulated in Frames.

UDP does not reserve a connection like TCP does, but if the connection is unstable this can result in a terrible user experience.
Packets are sent using stateless or connection-based protocols for different use-cases, routed through Networks and Encapsulated in Frames.

UDP has no process for establishing connection, reserving connection or checking receipt, so there are no safeguards like those offered by TCP.
Packets are sent using fast protocols or guaranteeing protocols depending on use-case, routed through Networks and Encapsulated in Frames.

UDP Packets are simpler than TCP Packets and have fewer Headers, but they do share some common standards.
Packets can be simple or complex depending on protocol, but all will be routed by a Network and Encapsulated in Frames with MAC Addresses.

Time To Live (TTL) is a UDP Header than sets an expiry time for the Packet so it does not slow down your Network if it fails to reach destination.
TCP and UDP share some Headers and not others, but all Packets will be routed through a Network and Encapsulated in Frames by Data Link.

Source Address is a UDP Header containing the IP Address of the sending device so that the receiver knows where to reply to.
TCP and UDP share some Headers such as TTL and Source Address, but not all, and their Packets are all routed through Networks and Encapsulated.

Destination Address is a UDP Header containing the IP Address of the destination device so the data can be routed there.
TCP and UDP share some, but not all, Headers and their Packets are all routed through Networks and Encapsulated in Frames by the Data Link.

Source Port is a UDP Header containing the port used to send the Packet, chosen at random from available ports in the range 0 - 65535.
TCP and UDP Packets share some, but not all, Headers and are both routed by Networks and Encapsulated in Frames with MAC Addresses by Data Link.

Destination Port is a UDP Header containing the Port Number that an application or service is running on the remote host (e.g. webserver on 80).
TCP and UDP share some Headers, but TCP Packets have more, and both are routed by Networks and Encapsulated in Frames with MAC Addresses.

Data is a UDP Header containing the data that is to be transmitted.
TCP and UDP Packets both have TTL, Source Address, Destination Address, Source Port, Destination Port and Data Headers, but TCP has more.

Where TCP offers a Three-Way Handshake, UDP simply has the client send a Request and the server send a series of Responses.
TCP and UDP Packets share some Headers, but TCP has more and TCP establishes a connection where UDP simply respondes to requests.

## Task 5 - Ports 101 (Practical)

Ports are an essential point at which data can be exchanged, like a harbour port taking cargo from ships.
Packet Headers depend on protocol, but all Packets must be routed through a Network, Encapsulated in Frames and received by a Port.

Ports enforce what can be sent and where, like a harbour port that only takes a particular kind of ship.
Packets can have different Layer 4 Headers depending on protocol, but must be routed by Network, Encapsulated in Frames and received by a Port.

Different applications can use common Port standards to interpret data from the same port the same way and thus preserve compatibility.
Packets can have different Layer 4 Headers depending on protocol, but will be sent to server Ports based on common standards for compatibility.

For example, web browsers send HTTP data over Port 80, but everything else is up to the designers and users.
Packets can have different Headers depending on protocol, but will be sent to server Ports based on compatibility standards (e.g. http port 80).

Several protocols have been allocated a standard Port rule, and ports in the range 0 - 1024 are known as Common Ports.
Packets Headers vary by protocol, but everything is routed through Networks and Encapsulated in Frames to send to Ports.

File Transfer Protocol (FTP) uses Port 21 to share files to a central location based on a client-server model.
Packet Headers vary by protocol, but Destination Ports follow common standards such as Port 21 for FTP.

Secure Shell (SSH) uses Port 22 to provide a text-based remote interface.
Packet Headers vary by protocol, but Destination Ports follow common standards such as Port 21 for FTP or Port 22 for SSH.

HyperText Transfer Protocol (HTML) uses Port 80 to serve web pages.
Packet Headers vary, but Destination Ports follow common standards such as Port 21 for FTP, Port 22 for SSH and Port 80 for HTTP.

HyperText Transfer Protocol Secure (HTTPS) uses Port 443 to provide the same service is HTTP in a more secure way using encryption.
Headers vary, but Destination Ports follow common standards such as Port 21 for FTP, Port 22 for SSH, Port 80 for HTTP and Port 443 for HTTPS.

Server Message Block (SMB) uses Port 445 to provide a service similar to FTP with the addition of device sharing (e.g. share a printer).
Destination Ports follow common standards such as Port 21 for FTP, Port 22 for SSH, Port 80 for HTTP, Port 443 for HTTPS and Port 445 for SMB.

Remote Desktop Protocol (RDP) uses Port 3389 to provide a graphical remote interface.
Ports follow common standards like Port 21 for FTP, Port 22 for SSH, Port 80 for HTTP, Port 443 for HTTPS, Port 445 for SMB and Port 3389 for RDP.

A table of common ports can be found at [VMaxx](https://www.vmaxx.net/techinfo/ports.htm).
Ports follow common standards like Port 21 for FTP, Port 22 for SSH, Port 80 for HTTP, Port 443 for HTTPS, Port 445 for SMB and Port 3389 for RDP.

You can use non-standard ports, but applications assume the standard so you will need to specify with a colon (e.g. myurl:8080)
Packet Headers vary by Protocol, but Destination Ports usually follow common standards and non-standard ports must be specified for applications.

### Practical Challenge:

Connect to 8.8.8.8:1234 to get the flag.
Packets are given Headers by Protocols including random Source Port, but Destination Port usually follows a common standard.

## Task 6 - Continue Your Learning: Extending Your Network

Join the final room of the Networking module.
Networks take Packets with Headers varying by Protocols and route them for Encapsulation in Frames to be sent to Destination Ports.