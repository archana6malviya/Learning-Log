**Learning Objectives**
- Types of Networks
- Physical components of a network
- TCP/IP model provides a framework for network communication
- Data is sent and received over a network
- Network Architecture

A network is a group of connected devices.

The devices on a network can communicate with each other over network cables, or wireless connections.

Devices need to find each other on a network to establish communications. 
These devices will use unique addresses, or identifiers, to locate each other. 
The addresses will ensure that communications happens with the right device. 
These are called the IP and MAC addresses. 
Devices can communicate on two types of networks: 
A local area network, also known as a LAN, and a wide area network, also known as a WAN.
A local area network, or LAN, spans a small area like an office building, a school, or a home. For example, when a personal device like your cell phone or tablet connects to the WIFI in your house, they form a LAN. 

A wide area network or WAN spans a large geographical area like a city, state, or country.

**🧩 Network Devices**
🔌 1. Hub

Connects multiple computers in a network.

Broadcasts data to all devices (no intelligence).

Layer: 1 – Physical Layer.

Limitation: Causes network congestion and collisions.

🔀 2. Switch

Connects devices within a LAN and forwards data only to the intended device.

Uses MAC addresses for communication.

Layer: 2 – Data Link Layer.

Benefit: Reduces collisions and increases efficiency.

🌐 3. Router

Connects different networks (e.g., LAN to Internet).

Routes data using IP addresses.

Layer: 3 – Network Layer.

Benefit: Directs traffic efficiently and supports NAT, DHCP, and security policies.

🧱 4. Firewall

Monitors and filters traffic based on security rules.

Protects internal network from unauthorized access.

Layer: 3–7.

Benefit: Enforces network security at the perimeter or host level.

🌍 5. Modem

Converts digital signals to analog and vice versa for Internet access.

Layer: 1 – Physical Layer.

Use: Connects local network to the ISP.

🧠 6. Access Point (AP)

Provides wireless connectivity to devices.

Extends wired network using Wi-Fi.

Layer: 2 – Data Link Layer.

Use: Offices, homes, and public Wi-Fi zones.

🔄 7. Bridge

Connects two LAN segments to manage traffic.

Uses MAC addresses to forward data.

Layer: 2 – Data Link Layer.

📡 8. Gateway

Acts as a translator between networks using different protocols.

Layer: 3–7.

Use: Connects an enterprise network to external systems (e.g., Internet).

🕹️ 9. Repeater

Boosts or regenerates weak signals.

Layer: 1 – Physical Layer.

Use: Extends network distance.
| Device       | Layer | Function Summary                | Example Use Case            |
| ------------ | ----- | ------------------------------- | --------------------------- |
| Hub          | 1     | Broadcasts all data             | Small, legacy networks      |
| Switch       | 2     | Forwards by MAC address         | LAN traffic control         |
| Router       | 3     | Routes packets between networks | Connect LAN to Internet     |
| Firewall     | 3–7   | Blocks/filters unwanted traffic | Network perimeter defense   |
| Modem        | 1     | Connects to ISP                 | Home Internet access        |
| Access Point | 2     | Wireless connectivity           | Office Wi-Fi                |
| Bridge       | 2     | Connects LAN segments           | Segment traffic             |
| Gateway      | 3–7   | Protocol translation            | Connect dissimilar networks |
| Repeater     | 1     | Extends signal range            | Extend network distance     |

Virtualization tools are pieces of software that perform network operations. Virtualization tools carry out operations that would normally be completed by a hub, switch, router, or modem, and they are offered by Cloud service providers. These tools provide opportunities for cost savings and scalability.




**Cloud Networks**
1. What is a Cloud Network?

A cloud network is an IT infrastructure where some or all of the network resources and services are hosted in the cloud.
Instead of being fully on-premises, parts of the network—like routers, firewalls, servers, and storage—are managed and delivered via cloud platforms (e.g., AWS, Azure, Google Cloud).
| Type              | Description                                                    | Example                 |
| ----------------- | -------------------------------------------------------------- | ----------------------- |
| **Public Cloud**  | Shared cloud infrastructure managed by third parties           | AWS, Azure, GCP         |
| **Private Cloud** | Dedicated cloud environment for one organization               | VMware Cloud, OpenStack |
| **Hybrid Cloud**  | Combines private + public clouds for flexibility               | AWS Outposts, Azure Arc |
| **Multi-Cloud**   | Uses multiple cloud providers for redundancy or specialization | AWS + GCP mix           |

3. Components of a Cloud Network

Cloud Router: Virtual router connecting cloud and on-prem resources

Virtual Private Cloud (VPC): Isolated cloud network space

Load Balancer: Distributes traffic across servers

Firewall / Security Group: Controls inbound and outbound traffic

Cloud Storage: Scalable data storage (e.g., S3 buckets, Azure Blob)

VPN Gateway: Connects on-premises networks securely to the cloud
5. Key Benefits

🌐 Scalability: Quickly adjust to demand.

💰 Cost Efficiency: Pay only for what you use.

🧩 Flexibility: Integrate with multiple environments.

🔒 Security: Built-in encryption, identity, and access controls.

🕒 High Availability: Redundant systems prevent downtime.


**Intro to network communication**
Communication over a network happens when data is transferred from one point to another. Pieces of data are typically referred to as data packets. A data packet is a basic unit of information that travels from one device to another within a network. When data is sent from one device to another across a network, it is sent as a packet that contains information about where the packet is going, where it's coming from, and the content of the message.
 A data packet is very similar to a physical letter. It contains a header that includes the internet protocol address, the IP address, and the media access control, or MAC, address of the destination device. It also includes a protocol number that tells the receiving device what to do with the information in the packet. Then there's the body of the packet, which contains the message that needs to be transmitted to the receiving device. 
Finally, at the end of the packet, there's a footer, similar to a signature on a letter, the footer signals to the receiving device that the packet is finished.
 Network performance can be measured by bandwidth. Bandwidth refers to the amount of data a device receives every second. You can calculate bandwidth by dividing the quantity of data by the time in seconds. Speed refers to the rate at which data packets are received or downloaded. Security personnel are interested in network bandwidth and speed because if either are irregular, it could be an indication of an attack. 
Packet sniffing is the practice of capturing and inspecting data packets across the network. Communication on the network is important for sharing resources and data because it allows organizations to function effectively. Coming up, you'll learn more about the protocols to support network communication. 
**The TCP/IP model**
1. Introduction

The TCP/IP model (Transmission Control Protocol / Internet Protocol) is the foundation of modern networking.
It defines how data is transmitted from one device to another over the internet or any network.

It has 4 layers, each responsible for specific communication functions.
2. Layers of the TCP/IP Model
| Layer                    | Function                                                        | Protocols                               | Devices                |
| ------------------------ | --------------------------------------------------------------- | --------------------------------------- | ---------------------- |
| **Application Layer**    | Provides services for network applications and user interaction | HTTP, HTTPS, FTP, DNS, SMTP, POP3, DHCP | Computers, servers     |
| **Transport Layer**      | Ensures reliable data transfer and manages error detection      | TCP, UDP                                | Gateways, firewalls    |
| **Internet Layer**       | Handles logical addressing and routing of packets               | IP (IPv4/IPv6), ICMP, ARP               | Routers                |
| **Network Access Layer** | Defines how data is physically sent over the medium             | Ethernet, Wi-Fi, PPP, MAC               | Switches, NICs, cables |

3. TCP/IP vs OSI Model
   | Feature      | TCP/IP Model                     | OSI Model                                            |
| ------------ | -------------------------------- | ---------------------------------------------------- |
| Layers       | 4                                | 7                                                    |
| Developed By | U.S. Department of Defense (DoD) | ISO (International Organization for Standardization) |
| Approach     | Practical, protocol-based        | Theoretical, conceptual                              |
| Most Used    | Internet & modern networks       | Reference for learning                               |
4. How TCP/IP Works (Data Flow)

Application Layer – User sends a message (e.g., an email or web request).

Transport Layer – Data is divided into segments (TCP) or datagrams (UDP).

Internet Layer – Adds IP addresses and determines the path (routing).

Network Access Layer – Converts packets into bits and sends them via physical media.

At the destination, the process is reversed to reassemble the original message.
6. Key Protocols Explained

TCP (Transmission Control Protocol) → Reliable, connection-oriented communication.

UDP (User Datagram Protocol) → Faster, connectionless communication.

IP (Internet Protocol) → Logical addressing and routing.

DNS (Domain Name System) → Translates domain names into IP addresses.

HTTP/HTTPS → Used for web communication.

ICMP (Internet Control Message Protocol) → Used by ping and traceroute tools for diagnostics.

✅ Summary

TCP/IP = Backbone of the Internet.

4 layers work together for data transfer.

TCP ensures reliability; IP ensures routing.

Combines both hardware and software aspects of networking.

**The OSI model**
**IP addresses & network communication**

  
