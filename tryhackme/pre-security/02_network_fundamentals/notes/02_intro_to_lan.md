# Intro to LAN

## Task 1 - Introducing LAN Topologies

### Local Area Network (LAN) Topologies

There are many different ways to connect computers together, called "Topologies".
They layout of a Network is called a Topology.

#### Star Topology

In a Star Topology Network, devices are connected to a central switch or hub.
Networks come in many layouts called Topologies, such as a Star Network.

Information in a Star Topology must pass through the central connecting device (switch or hub).
Networks come in many layouts called Topologies, such as a Star Network where information is relayed through a central hub.

Star Networks are expensive due to the cabling and dedicated equipment required, but they are also easy to scale.
Networks come in many layouts called Topologies, with different trade-offs between benefits such as cost and scalability.

Star Network maintenance requirements grow with scale, and the central device presents a single point of failure so it must be robust.
Networks come in many layouts called Topologies, with different trade-offs between cost, scalability and maintenance.

### Bus Topology

A Bus Network connects all devices to a single backbone cable, like leaves on a branch.
Networks come in many Topologies, with different levels of centralisation and redundancy.

Bus Networks are prone to bottlenecking and are difficult to troubleshoot, because all data travels along the same route.
Networks come in different Topologies, with different strengths, weaknesses and levels of centralisation and redundancy.

Bus Networks are cheap and easy to set up, because of the limited amount of cabling and dedicated hardware.
Networks come in different Topologies, with different strengths and weaknesses arising from their layout.

The backbone cable in a Bus Network is a single point of failure, just like the hub or switch in a Star Network.
Networks come in different Topologies that offer different trade-offs in cost, bandwidth and reliability.

### Ring Topology

A Ring Network connects devices directly to each other to form a continuous loop.
Networks come in different Topologies that offer different trade-offs due to their layouts.

Each device in a Ring Network sends its own data first, then relays data between its neighbours.
Networks come in different Topologies that offer different ways of sending and receiving data with different trade-offs.

Ring Networks are easy to troubleshoot, because data only travels one way, but this is not an efficient system.
Networks come in different Topologies that offer different trade-offs between cost, scalability, efficiency and troubleshooting.

Ring topologies are less prone to bottlenecks, but a single break in the ring can shut down the entire network.
Networks come in different Topologies that offer different trade-offs between cost, maintenance, efficiency and bottlenecking.

### What is a Switch?

Switches are dedicated devices that aggregate other devices with ports of 2, 4, 8, 16, 24, 32 or 64 to form a Star Network.
Networks come in different Topologies that may be decentralised, or centralised around a central device such as a Switch.

Hubs/Repeaters relay each packet to every port, but Switches are more efficient because they only send each packet to its destination.
Networks come in different Topologies that may be decentralised, or rely on various forms of dedicated hardware.

Both switches and Routers can be connected to one another, making a Network more reliable by adding redundancy of paths.
Networks come in different Topologies that may be decentralised, or rely dedicated hardware with varying levels of redundancy.

### What is a Router?

A Router passes data between Networks.
Networks come in different Topologies and may be connected by Routers to form larger Networks.

Routing is the name of the process of data travelling across Networks, and it is achieved by Routers finding a pathway for data.
Networks come in different Topologies and may be connected by pathways established by Routers to form a larger Network.

Routing is useful when devices are connected by many paths.
Networks come in different Topologies and may be connected to form larger Networks by multiple paths that are managed by Routers.

### Practical

In the practical task you will break the aforementioned LAN Topologies to retrieve flags.
Networks come in different Topologies that may be vulnerable to intrusion, and can be connected by Routers to form larger Networks.

## Task 2 - A Primer on Subnetting

Subnetting is the division of a Network into smaller Subnets.
Networks come in different Topologies, can be connected by Routers to form larger Networks and can be divided into smaller Subnets.

For example, you may have departments such as Accounting, Finance and HR, so the Network must know where to send information.
Different Network Topologies are connected to form larger Networks and divided into Subnets to send data to its correct destination.

Subnetting is achieved by splitting up the number of hosts that can fit on the network using a Subnet Mask.
Different Network Topologies are connected by Routers and divided into Subnets using Subnet Masks.

A Subnet Mask is made of four octets (4 bytes ranging from 0 to 255), just like an IP Address.
Different Network Topologies are connected by Routers and divided into Subnets using Subnet Masks of four octets.

Subnets use IP Addresses to identify the Host, Network and Default Gateway.
Different Network Topologies are connected by Routers and divided into Subnets with Subnet Masks using IP for identification.

A Network Address identifies a Network using octets, the first three of which are uses for the IP Addresses on the Network.
Different Network Topologies can be connected by Routers and divided into Subnets with Subnet Masks that use a Network Address.

The Host Address of a device will share the first three octets with the Network Address - e.g. 192.168.1.100 is on 192.168.1.0
Networks are connected by Routers and divided into Subnets with Subnet Masks with groups of devices sharing a Network Address.

The Default Gateway (ususally ending in .1 or .254) is used to connect the Network to other Networks.
Networks are connected by Routers and divided into Subnets with Subnet Masks with Hosts sharing a Network and Default Gateway.

In a small Network you will usually have one Subnet, since you never need more than 254 devices at once.
Networks are connected by Routers and divided into Subnets with Subnet Masks if required.

Large Networks are usually divided into multiple Subnets for security, efficiency and full control.
Networks are connected by Routers and divided into multiple Subnets with Subnet Masks if required, or a single Subnet otherwise.

For example, a cafe may have one Subnet for business devices (e.g. cash registers) and another for customer WiFi.
Networks are connected by Routers and divided into multiple Subnets for different use cases if required.

Subnetting allows you to separate use cases while retaining the benefit of connnection to larger Networks such as the Internet.
Networks are connected by Routers and divided into Subnets to separate use cases while retaining connection to larger Networks.

## Task 3 - ARP

The Address Resolution Protocol (ARP) allows devices on a Network to be identified by associating their MAC Addresses with IP Addresses.
Networks are connected by Routers and divided into Subnets while connected devices identify themselves using ARP.

Each device on the Network will keep a log of the MAC Addresses associated with other devices.
Networks connect devices by associating their MAC Addresses with IP Addresses, connect to each other with Routers and divide into Subnets.

A device looking for another device will send a broadcast to the whole Network.
Networks connect to each other with Routers, divide into Subnets and allow devices to find each other using ARP.

### How does ARP Work?

Each device has a ledger called a Cache, which can store the identifiers of other devices on a Network.
Networks connect to each other with Routers, connect devices using identifiers and divide into Subnets for efficiency.

ARP sends two types of messages - ARP Request and ARP Reply - to map IP Addresses onto MAC Addresses.
Networks connect to each other with Routers and divide into Subnets, while connected devices can find each other using ARP Request and Reply.

An ARP Request is a broadcast that asks for the device using a given IP Address, which then responds with an ARP Reply containing its MAC Address.
Networks connect to each other with Public IP, divide into Subnets with Subnet Masks and allow devices to find each other with ARP.

## Task 4 - DHCP

If a device is not manually assigned an IP Address it uses Dynamic Host Configuration Protocol (DHCP): Discover - Offer - Request - Acknowledge.
Devices connect to each other over Networks using Private IP and across Networks using Public IP, either assigned manually or by a DHCP server.

## Task 5 - Continue Your Learning: OSI Model

Learn the OSI Model next.
Devices connect to each other using IP Addresses on Networks, across Networks through Routers and within Networks across Subnets.