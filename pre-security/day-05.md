# Day 05 — TryHackMe Pre Security

**Path:** TryHackMe Pre Security  
**Module:** Networking Fundamentals  
**Day:** 05  
**Rooms Completed:** What Is Networking, Intro to LAN, OSI Model, Packets and Frames, Extending Your Network

---

## 1. What Is Networking?

Today I learned the fundamentals of computer networking and how different devices communicate and exchange information.

### What Is a Computer Network?

A computer network is a group of interconnected devices that communicate with each other to share information and resources.

Examples of network-connected devices:

- Computers and laptops
- Smartphones
- Servers
- Printers
- Routers
- Smart devices

### Why Do We Need Networking?

Networking allows us to:

- Share files and information.
- Access websites and online services.
- Communicate through emails and messaging applications.
- Share hardware resources such as printers.
- Access remote servers.
- Transfer data between different devices.

### Types of Networks

**1. LAN — Local Area Network**

A network that connects devices within a limited geographical area.

Example: Computers connected within an office, school, or home.

**2. WAN — Wide Area Network**

A network that connects devices or smaller networks over large geographical areas.

Example: The Internet.

**3. Internet**

The Internet is a global network of interconnected networks that communicate using standardized protocols.

### IP Address

An IP (Internet Protocol) address is a logical address used to identify a network interface and enable communication across IP networks.

There are two main versions:

**IPv4**

- Uses 32 bits.
- Written as four decimal numbers separated by dots.
- Example: `192.168.1.10`

**IPv6**

- Uses 128 bits.
- Written using hexadecimal characters separated by colons.
- Example: `2001:db8::1`

### MAC Address

A MAC (Media Access Control) address is a link-layer address used to identify a network interface on a local network.

Example:

`00:1A:2B:3C:4D:5E`

### IP Address vs MAC Address

| IP Address | MAC Address |
|---|---|
| Logical network address | Link-layer address |
| Used for IP communication | Used for local network delivery |
| IPv4 uses 32 bits | Common Ethernet MAC addresses use 48 bits |
| Can change depending on network configuration | Usually assigned to a network interface |

### Important Networking Terms

- Network
- LAN
- WAN
- Internet
- IP Address
- IPv4
- IPv6
- MAC Address
- Network Protocol

---

## 2. Intro to LAN

Today I learned how devices communicate within a Local Area Network (LAN) and the basic networking devices responsible for connecting them.

### What Is a LAN?

A LAN is a network that connects multiple devices within a limited geographical area, such as a home, office, or school.

For example, when multiple computers connect to the same office network, they can communicate and share resources.

### Important LAN Concepts

**1. Switch**

A network switch connects multiple devices within a LAN.

It uses MAC addresses to forward Ethernet frames to the appropriate ports.

**2. Router**

A router connects different IP networks and forwards packets between them.

For example, a home router allows devices on a private home network to communicate with the Internet.

**3. DHCP — Dynamic Host Configuration Protocol**

DHCP automatically provides network configuration to devices.

It commonly assigns:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server Information

**4. DNS — Domain Name System**

DNS translates domain names into IP addresses so that devices can locate network services.

Example:

When I visit `google.com`, DNS helps resolve the domain name to an IP address.

**5. Private IP Address**

Private IP addresses are used within private networks and are not directly routed across the public Internet.

Common private IPv4 ranges:

- `10.0.0.0 – 10.255.255.255`
- `172.16.0.0 – 172.31.255.255`
- `192.168.0.0 – 192.168.255.255`

### Example of a Home LAN

Imagine a home network containing:

- One laptop
- Two smartphones
- One smart TV
- One wireless router

All these devices can connect to the same LAN through Wi-Fi or Ethernet.

The router can provide IP addresses through DHCP and connect the LAN to the Internet.

### Wired vs Wireless Networks

**Wired Network**

Devices connect using physical Ethernet cables.

Advantages:
- Generally stable connections.
- Often lower latency.
- Less susceptible to wireless interference.

**Wireless Network**

Devices connect using radio signals, commonly through Wi-Fi.

Advantages:
- Mobility.
- Easy connectivity.
- No physical cable required for each device.

### Important Terms

- LAN
- Switch
- Router
- DHCP
- DNS
- Private IP
- Ethernet
- Wi-Fi
- Default Gateway
- Subnet Mask

---

## 3. OSI Model

Today I learned about the OSI model, which explains how network communication can be understood through seven different layers.

### What Is the OSI Model?

OSI stands for Open Systems Interconnection.

It is a conceptual reference model that divides network communication into seven layers.

Each layer has specific responsibilities and works with the layers above and below it.

### The Seven Layers of the OSI Model

**Layer 7 — Application Layer**

This layer provides network services to applications.

Examples:
- HTTP
- HTTPS
- DNS
- SMTP

**Layer 6 — Presentation Layer**

This layer deals with data representation, formatting, encryption, and compression concepts.

Examples:
- Data encoding.
- Encryption and decryption.
- Data formatting.

**Layer 5 — Session Layer**

This layer manages communication sessions between applications.

Responsibilities include:
- Establishing sessions.
- Managing sessions.
- Terminating sessions.

**Layer 4 — Transport Layer**

This layer provides end-to-end transport of data between hosts.

Important protocols:

- TCP (Transmission Control Protocol)
- UDP (User Datagram Protocol)

TCP provides reliable, ordered delivery using mechanisms such as acknowledgements and retransmissions.

UDP provides a connectionless transport service without guaranteeing delivery or ordering.

**Layer 3 — Network Layer**

This layer handles logical addressing and routing packets between networks.

Important concepts:

- IP Address
- Routing
- Routers
- IPv4
- IPv6

**Layer 2 — Data Link Layer**

This layer handles communication over a local network link.

Important concepts:

- MAC Address
- Ethernet Frames
- Network Switches

**Layer 1 — Physical Layer**

This layer deals with the physical transmission of raw bits through a communication medium.

Examples:

- Ethernet cables.
- Fibre-optic cables.
- Radio signals.
- Electrical and optical signals.

### OSI Model Summary

| Layer | Name | Main Responsibility |
|---|---|---|
| 7 | Application | Network services for applications |
| 6 | Presentation | Data formatting and representation |
| 5 | Session | Managing communication sessions |
| 4 | Transport | End-to-end data transport |
| 3 | Network | IP addressing and routing |
| 2 | Data Link | Local delivery using frames |
| 1 | Physical | Transmission of bits |

### Easy Way to Remember the OSI Layers

From Layer 7 to Layer 1:

**A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing.

- Application
- Presentation
- Session
- Transport
- Network
- Data Link
- Physical

### Why Is the OSI Model Important in Cybersecurity?

The OSI model helps me:

- Understand how network communication works.
- Identify where network problems occur.
- Understand different networking protocols.
- Analyze network traffic.
- Understand how attacks can target different network layers.
- Develop a foundation for network security and penetration testing.

### Important Terms

- OSI Model
- Application Layer
- Presentation Layer
- Session Layer
- Transport Layer
- Network Layer
- Data Link Layer
- Physical Layer
- TCP
- UDP

---

## 4. Packets and Frames

Today I learned how information is divided into smaller units before being transmitted across a network.

### What Is Data Transmission?

When information is sent over a network, it is divided and encapsulated into smaller units so that it can be transmitted and processed efficiently.

Two important networking terms are packets and frames.

### What Is a Packet?

A packet is a unit of data at the Network Layer (Layer 3).

An IP packet generally contains:

- Source IP Address
- Destination IP Address
- Other IP header information
- Payload (the data being carried)

Packets help devices communicate across different networks.

### What Is a Frame?

A frame is a unit of data at the Data Link Layer (Layer 2).

An Ethernet frame generally contains:

- Source MAC Address
- Destination MAC Address
- Ethernet Type/Length information
- Payload
- Frame Check Sequence (FCS)

Frames are used to deliver data across a local network link.

### Packet vs Frame

| Packet | Frame |
|---|---|
| Network Layer (Layer 3) | Data Link Layer (Layer 2) |
| Contains IP addressing information | Contains link-layer addressing information |
| Used for communication between IP hosts | Used for delivery over a local network link |
| Encapsulated inside a frame when carried over Ethernet | Carries the packet as its payload |

### What Is Encapsulation?

Encapsulation is the process of adding protocol headers and, where applicable, trailers to data as it moves down the networking layers.

A simplified process:

1. Application data is created.
2. Transport Layer adds its header, creating a TCP segment or UDP datagram.
3. Network Layer adds an IP header, creating a packet.
4. Data Link Layer adds a frame header and trailer, creating a frame.
5. Physical Layer transmits the bits.

### What Is Decapsulation?

Decapsulation is the reverse process.

When data reaches the receiving device, each networking layer processes and removes its corresponding protocol information before passing the remaining data to the next layer.

### Basic Communication Flow

**Application Data → Segment/Datagram → Packet → Frame → Bits**

At the receiving end:

**Bits → Frame → Packet → Segment/Datagram → Application Data**

### TCP vs UDP

**TCP — Transmission Control Protocol**

- Connection-oriented.
- Provides reliable, ordered data delivery.
- Uses acknowledgements and retransmissions.
- Commonly used by HTTP(S) and many other applications.

**UDP — User Datagram Protocol**

- Connectionless.
- Does not guarantee delivery or ordering.
- Has less transport-layer overhead than TCP.
- Commonly used for DNS queries, streaming, and real-time applications.

### Why Packets and Frames Matter in Cybersecurity

Understanding packets and frames helps me:

- Analyze network traffic.
- Understand how devices communicate.
- Investigate suspicious network activity.
- Learn packet capture tools such as Wireshark.
- Understand network-based attacks.
- Identify source and destination addressing information.

### Important Terms

- Data Transmission
- Packet
- Frame
- Encapsulation
- Decapsulation
- TCP
- UDP
- Source Address
- Destination Address
- Payload

---

## 5. Extending Your Network

Today I learned how networks can be expanded beyond a single LAN using additional networking devices and technologies.

### Why Do We Need to Extend Networks?

A small network may contain only a few connected devices.

However, organizations need to connect multiple departments, buildings, and remote locations.

Network extension allows devices in different networks to communicate with each other.

### Important Networking Devices

**1. Router**

A router connects different networks and forwards packets based on IP addresses.

Example:

Connecting a home LAN to the Internet.

**2. Switch**

A switch connects devices within a LAN and forwards frames using MAC addresses.

**3. Wireless Access Point (WAP)**

A Wireless Access Point allows wireless devices to connect to a wired network using Wi-Fi.

It extends wireless connectivity to devices such as laptops and smartphones.

**4. Firewall**

A firewall monitors and controls network traffic according to configured security rules.

It can allow or block traffic based on factors such as IP addresses, ports, protocols, and connection state.

### What Is NAT?

NAT stands for Network Address Translation.

It modifies IP address information as packets pass through a network device.

A common example is a home router using NAT to allow multiple devices with private IP addresses to share a public IPv4 address when accessing the Internet.

### What Is Port Forwarding?

Port forwarding is a technique that directs incoming network traffic arriving at a particular port to a specified device and port inside a private network.

Example:

A router may forward incoming traffic on a particular port to an internal web server.

Port forwarding should be configured carefully because it can expose internal services to external networks.

### What Is a Subnet?

A subnet is a logical division of an IP network.

Subnetting divides a larger network into smaller networks.

Benefits include:

- Better network organization.
- More efficient IP address allocation.
- Separation of network segments.
- Improved traffic management.
- Support for security boundaries.

### What Is a VPN?

VPN stands for Virtual Private Network.

A VPN creates a protected communication tunnel over an underlying network, commonly the Internet.

It can be used to:

- Connect remote employees to company networks.
- Protect traffic over untrusted networks.
- Connect geographically separated networks.

### Why Network Extension Matters in Cybersecurity

Understanding how networks are extended helps me:

- Identify different network segments.
- Understand routers and access points.
- Learn how NAT and port forwarding work.
- Understand network exposure.
- Recognize the importance of firewall rules.
- Learn how attackers may move between accessible network systems.

### Important Terms

- Router
- Switch
- Wireless Access Point
- Firewall
- NAT
- Port Forwarding
- Subnet
- VPN
- Network Segmentation

---

## 6. What I Learned Today

Today I completed five rooms in the Networking Fundamentals module.

1. **What Is Networking:** Learned how devices communicate and exchange information using networks, IP addresses, and MAC addresses.
2. **Intro to LAN:** Learned how devices connect within a local network using switches, routers, DHCP, and DNS.
3. **OSI Model:** Understood the seven layers of network communication and their individual responsibilities.
4. **Packets and Frames:** Learned how data is encapsulated into segments, packets, and frames before transmission.
5. **Extending Your Network:** Learned how routers, switches, wireless access points, NAT, VPNs, and subnets help expand networks.

These concepts have helped me build a stronger foundation in networking, which is essential for learning penetration testing and network security.

---

## 7. Things I Need to Revise

- [ ] LAN vs WAN
- [ ] IP Address vs MAC Address
- [ ] IPv4 vs IPv6
- [ ] Private vs Public IP Address
- [ ] Switch vs Router
- [ ] DHCP vs DNS
- [ ] Seven layers of the OSI Model
- [ ] TCP vs UDP
- [ ] Packet vs Frame
- [ ] Encapsulation vs Decapsulation
- [ ] NAT and Port Forwarding
- [ ] Subnetting basics
- [ ] Wireless Access Point
- [ ] VPN and Firewall

---

## 8. Self-Assessment

Before moving to the next topic, I should be able to answer these questions:

1. What is a computer network?
2. What is the difference between LAN and WAN?
3. What is the difference between an IP address and a MAC address?
4. What is the purpose of a network switch?
5. What is the difference between a router and a switch?
6. What are the seven layers of the OSI model?
7. Which OSI layer is responsible for routing?
8. What is the difference between TCP and UDP?
9. What is the difference between a packet and a frame?
10. What happens during encapsulation?
11. What is the purpose of DHCP and DNS?
12. What is NAT, and why is it used?
13. What is port forwarding?
14. Why do organizations divide networks into subnets?
15. What is the purpose of a VPN?

---

## TryHackMe Progress

**Pre Security — Networking Fundamentals**

- [x] What Is Networking
- [x] Intro to LAN
- [x] OSI Model
- [x] Packets and Frames
- [x] Extending Your Network

**Day 05 Status: Completed ✅**
