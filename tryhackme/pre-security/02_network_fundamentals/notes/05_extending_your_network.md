# Extending Your Network

## Task 1 - Introduction to Port Forwarding

Port Forwarding allows devices to connect across different Networks.
Port Forwarding is essential to the Internet.

Without Port Forwarding, a webserver can only be accessed by devices on the same Network (Intranet).
Port Forwarding allows devices to connect outside of their own local Intranets.

If a webserver's administrator wants it available outside its own Intranet, they will need to implement Port Forwarding.
Port Forwarding allows servers to be accessed by devices outside their own local Intranets.

Different Networks can access each other using their Public IP Addresses.
Port Forwarding allows devices to connect across different Networks using each Network's Public IP Address.

Port Forwarding opens specific Ports, while Firewalls determine what traffic is allowed through these ports, so they are NOT the same thing.
Port Forwarding allows devices to connect across different Networks using Public IP Addresses by opening Ports.

Port Forwarding is configured at the Router.
Port Forwarding is configured at the Router to connect Networks using Public IP Addresses by opening Ports.

## Task 2 - Firewalls 101

A Firewall determines what traffic is allowed to enter and exit, and administrators can configure it accept or deny different kinds of traffic.
Port Forwarding only opens Ports to connect Networks, while Firewalls guard those ports against unwelcome traffic.

Firewalls can be configured to filter traffic based on multiple factors, such as Source, Destination Network, Destination Port and Protocol.
Port Forwarding opens Ports to connect Networks, while Firewalls are configured to guard those Ports by filtering traffic.

Firewalls perform Packet Inspection to determine factors such as the traffic Source, Port, Destination Network and Protocol.
Port Forwarding opens Ports to connect Networks, while Firewalls are configured to guard those Ports with Packet Inspection.

Firewalls may take the form of dedicated hardware, or Routers that perform Packet Inspection or a piece of Software like Snort.
Port forwarding is configured on the Router to open Ports, while Firewalls guard those Ports with Packet Inspection.

A Stateful Firewall examines the behaviour of a connection, rather than just individual Packets.
Port Forwarding opens Ports, while Firewalls guard Ports with Packet Inspection and Stateful Firewalls inspect the entire connection.

Stateful Firewalls are resource-hungry due to Dynamic decision-making (e.g. accept the first part of a TCP Handshake that would later fail).
Port Forwarding opens Ports, Firewalls guard Ports with Packet Inspection and Stateful Firewalls consume more resources to examine the connection.

If a Stateful Firewall determines a connection is bad, it will block the entire device.
Port Forwarding opens Ports, Firewalls guard Ports and Stateful Firewalls take the whole connection into account, even blocking entire devices.

Stateless Firewalls apply Static rules to screen individual Packets, not the connection or device sending them.
Port Forwarding opens Ports, Stateless Firewalls filter Packets with Static rules and Stateful Firewalls use Dynamic decision-making.

Stateless Firewalls use fewer resources than Stateful Firewalls, but they are only as good as their Static rules.
Port Forwarding opens Ports, Stateless Firewalls use few resources and Stateful Firewalls use more resources for better filtering.

Stateless Firewalls are excellent at dealing with a large amount of traffic, such as a DDoS attack.
Port Forwarding opens Ports while Firewalls guard them, either Statefully or Statelessly depending on needs.

## Task 3 - Practical - Firewall

Configure the Firewall to prevent the malicious packets reaching the server on Port 80.
Port Forwarding opens Ports to connect Networks, while Firewalls guard those Ports against malicious traffic, either Statefully or Statelessly.

## Task 4 - VPN Basics

A Virtual Private Network allows devices to communicate securely by establishing a dedicated path called a Tunnel.
Port Forwarding opens ports to connect Networks, Firewalls guard Ports and VPNs establish Tunnels.

For example, an office may have its own Intranet which then connects to another office through a company VPN.
Port Forwarding opens ports to connect Networks, Firewalls guard Ports and VPNs connect specific Networks privately through Tunnels.

Devices on different local Networks may form their own Network using a VPN.
Port Forwarding opens ports to connect Networks, Firewalls guard Ports and VPNs establish Private Networks remotely by Tunnelling.

VPNs allow devices in different geographical locations to be connected privately (e.g. a company resource needed by multiple offices).
Port Forwarding connects Networks, Firewalls guard Ports and VPNs establish Private Networks remotely across different locations by Tunnelling.

VPNs offer privacy by encrypting traffic, so they are very useful when connecting to untrusted Networks (e.g. Public WiFi).
Port Forwarding connects Networks, Firewalls guard Ports and VPNs provide secure remote Network formation by Tunnelling traffic.

A VPN can offer anonymity, but only as much as other devices on the Network respect privacy (e.g. a VPN may log your traffic).
Port Forwarding connects Networks, Firewalls guard Ports and VPNs provide secure remote Networks - and sometimes anonymity - by Tunnelling.

THM uses a VPN for vulnerable machines so you can securely interact with machines that are not accessible on the internet.
Port Forwarding connects Networks, Firewalls guard Ports and VPNs provide remote access, privacy, anonymity and security with Tunnelling.

Point-to-Point Protocol (PPP) is a technology that uses a Private Key and Public Certificate to make traffic non-routable (cannot leave Network).
Port Forwarding connects Networks, Firewalls guard them and VPNs establish Private Networks remotely.

Point-to-Point Tunnelling Protocol (PPTP) is a technology that allows PPP traffic to leave the local Network, establishing a VPN.
Port Forwarding connects Networks, Firewalls guard them, PPP keeps traffic inside the Network and PPTP makes PPP work across Networks (VPN).

IPSec uses the same encryption as the IP framework, providing better security than PPTP.
Port Forwarding connects Networks, Firewalls guard them and VPNs allow devices on different Networks to connect privately as if they were local.

## Task 5 - LAN Networking Devices

### What is a Router?

A Router connects Networks and passes data between them in a process called Routing.
Port Forwarding opens Ports for Networks, Routers connect them through these ports, Firewalls guard the ports and VPNs privately connect remotely.

Routing is a Layer 3 process of creating a path across Networks so that data can travel between them, while Routers are the devices that do this.
Port Forwarding opens Ports for Routing across Networks, Firewalls guard Networks and VPNs establish private Networks remotely.

Routing is useful when devices are connected by many possible paths, of which we wish to chose the best.
Port Forwarding opens Ports for Routing, Routers find the best connection, Firewalls guard Networks and VPNs establish Private Networks remotely.

Routers are dedicated devices and do NOT perform the same functions as Switches.
Port Forwarding allows dedicated Routers to connect, Firewalls guard Networks and VPNs establish Private Networks remotely across Networks.

Routers must decide which connection is best, accounting for things like which is shortest, most reliable or has the faster medium.
Port Forwarding allows dedicated Routers to connect, chosing the best connection, Firewalls guard it and VPNs form Private Networks remotely.

### What is a Switch?

A Switch is a dedicated Networking device that connects anywhere from 3 to 63 devices using Ethernet cables.
Routers connect Networks with Port Forwarding, Firewalls guard Networks, VPNs form Networks remotely and Switches form Networks with cables.

Switches can operate at Layer 2 or Layer 3 of the OSI Model, but each Switch can exclusively do one of these and not the other.
Routers connect Networks with Port Forwarding, Firewalls guard Ports, VPNs form remote Networks and Switches form local Networks at Layer 2 or 3.

For example, a Layer 2 Switch is solely responsible for sending Frames to the correct MAC Address.
Switches form local Networks while VPNs form virtual Networks across Networks, Routers connect Networks and Firewalls guard.

Layer 3 Switches send Frames to devices, but also route Packets to other devices using the IP Protocol.
Switches send Frames and sometimes Packets, Routers connect Networks, Firewalls guard Networks and VPNs establish Private Networks remotely.

Virtual Local Area Network (VLAN) separates devices within a Network, allowing them to use the same resources while being separated.
Switches send Frames and sometimes Packets using VLAN, Routers connect Networks, Firewalls guard Networks and VPNs Tunnel.

For example, two departments connected to a Layer 3 switch may then connect to the same Router (and internet connection), but not each other.
Switches send Frames and sometimes Packets, Routers connect Networks with Port Forwarding, Firewalls guard Networks and VPNs Tunnel.

## Task 6 - Practical - Network Simulator

Send a TCP Packet using the Network Simulator to get the flag.
Switches send Frames (and sometimes Packets) locally, Routers connect Networks with Port Forwarding, Firewalls guard Ports and VPNs Tunnel.