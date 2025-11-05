# Learning Objectives
- **Types of Networks**
- **Physical components of a network**
- **TCP/IP model provides a framework for network communication**
- **Data is sent and received over a network**
- **Network Architecture**

# 🌐 Network Basics

## 🧩 What is a Network?
A **network** is a group of connected devices that can **communicate** with each other using cables or wireless connections.

---

## 🖥️ Network Addresses
- Devices use **unique addresses** to find each other.  
- **IP Address:** Identifies devices on a network.  
- **MAC Address:** Identifies the device’s hardware.  
- These ensure data reaches the **correct device**.

---

## 🌍 Types of Networks

| Type | Full Form | Description | Example |
|------|------------|-------------|----------|
| **LAN** | Local Area Network | Covers a small area like a home or office | Home Wi-Fi |
| **WAN** | Wide Area Network | Covers large areas like cities or countries | The Internet |

---

## ✅ Summary
- Networks connect devices for communication.  
- IP & MAC addresses identify devices.  
- LAN = small area; WAN = large area.

# 🧩 Network Devices 

## 1. **Hub**
- Connects multiple computers in a network.  
- Broadcasts data to all devices (no filtering).  
- **Layer:** 1 – Physical  
- ⚠️ Causes network congestion and collisions.


## 2. **Switch**
- Connects devices within a LAN.  
- Forwards data only to the target device using **MAC addresses**.  
- **Layer:** 2 – Data Link  
- ✅ Reduces collisions and improves speed.

## 3. **Router**
- Connects different networks (LAN ↔ Internet).  
- Routes data using **IP addresses**.  
- **Layer:** 3 – Network  
- ✅ Directs traffic efficiently; supports NAT, DHCP, and security.


## 4. **Firewall**
- Monitors and filters network traffic.  
- Protects from unauthorized access.  
- **Layer:** 3–7  
- 🔒 Enforces security rules.

## 5. **Modem**
- Converts digital ↔ analog signals for Internet access.  
- **Layer:** 1 – Physical  
- 🌐 Connects local network to ISP.

## 6. **Access Point (AP)**
- Provides wireless (Wi-Fi) connectivity.  
- Extends wired networks.  
- **Layer:** 2 – Data Link  
- 📶 Used in homes, offices, and public zones.

---

## 7. **Bridge**
- Connects two LAN segments.  
- Uses **MAC addresses** to forward traffic.  
- **Layer:** 2 – Data Link  

---

## 8. **Gateway**
- Translates between different network protocols.  
- **Layer:** 3–7  
- 🌍 Connects internal and external networks.

---

## 9. **Repeater**
- Regenerates weak signals to extend range.  
- **Layer:** 1 – Physical
----

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

---
## ☁️ **Virtualization Tools**
- Software-based versions of physical network devices (hub, switch, router, modem).  
- Offered by **cloud providers** for **cost savings** and **scalability**.  




# ☁️ Cloud Networks

## 1. What is a Cloud Network?
A **cloud network** is an IT setup where some or all networking resources (routers, firewalls, servers, storage) are hosted in the **cloud** instead of on-premises.  
Cloud platforms like **AWS**, **Azure**, and **Google Cloud** deliver these services.

---

## 2. Types of Cloud Networks

| Type | Description | Example |
|------|--------------|----------|
| **Public Cloud** | Shared infrastructure managed by third parties | AWS, Azure, GCP |
| **Private Cloud** | Dedicated cloud for one organization | VMware Cloud, OpenStack |
| **Hybrid Cloud** | Mix of private + public for flexibility | AWS Outposts, Azure Arc |
| **Multi-Cloud** | Uses multiple cloud providers | AWS + GCP |

---

## 3. Components

- **Cloud Router** – Connects cloud and on-prem networks  
- **VPC (Virtual Private Cloud)** – Isolated cloud network space  
- **Load Balancer** – Distributes traffic evenly  
- **Firewall / Security Group** – Controls incoming & outgoing traffic  
- **Cloud Storage** – Scalable storage (e.g., S3, Azure Blob)  
- **VPN Gateway** – Secure link between on-prem and cloud  

---

## 4. Key Benefits

- 🌐 **Scalability:** Easily scale up or down  
- 💰 **Cost Efficiency:** Pay only for what you use  
- 🧩 **Flexibility:** Works with multiple environments  
- 🔒 **Security:** Encryption & access control  
- 🕒 **High Availability:** Redundant systems reduce downtime


# 💬 Intro to Network Communication

## 🧠 What is Network Communication?
Network communication happens when **data is transferred** from one device to another across a network.  
Data is sent in small units called **data packets**.

---

## 📦 Data Packets
A **data packet** is like a digital letter — it carries all the info needed for delivery.

| Part | Description |
|------|--------------|
| **Header** | Contains source & destination IP and MAC addresses, plus protocol info |
| **Body** | The actual data/message being sent |
| **Footer** | Marks the end of the packet (like a signature) |

---

## ⚙️ Network Performance
- **Bandwidth:** Amount of data transferred per second  
  → `Bandwidth = Data / Time`
- **Speed:** How fast data packets are sent or received  
- **Monitoring:** Sudden drops or spikes in bandwidth/speed may signal a network issue or attack  

---

## 🕵️ Packet Sniffing
**Packet sniffing** = capturing and inspecting packets on a network.  
Used by network admins and security teams to **monitor**, **analyze**, or **detect threats**.

---

## ✅ Why It Matters
- Enables data sharing and communication  
- Improves organizational efficiency  
- Supports other network functions and protocols

**The TCP/IP model**
# 🌐 The TCP/IP Model

## 1. Introduction
The **TCP/IP model (Transmission Control Protocol / Internet Protocol)** is the **foundation of modern networking**.  
It defines how data moves between devices over the internet or any network.  
It has **4 layers**, each with specific communication roles.

---

2. Layers of the TCP/IP Model
| Layer                    | Function                                                        | Protocols                               | Devices                |
| ------------------------ | --------------------------------------------------------------- | --------------------------------------- | ---------------------- |
| **Application Layer**    | Provides services for network applications and user interaction | HTTP, HTTPS, FTP, DNS, SMTP, POP3, DHCP | Computers, servers     |
| **Transport Layer**      | Ensures reliable data transfer and manages error detection      | TCP, UDP                                | Gateways, firewalls    |
| **Internet Layer**       | Handles logical addressing and routing of packets               | IP (IPv4/IPv6), ICMP, ARP               | Routers                |
| **Network Access Layer** | Defines how data is physically sent over the medium             | Ethernet, Wi-Fi, PPP, MAC               | Switches, NICs, cables |


## 3. Data Flow (How It Works)
1. **Application Layer** – Creates data (e.g., web request).  
2. **Transport Layer** – Breaks data into segments (TCP/UDP).  
3. **Internet Layer** – Adds IP addresses and routes packets.  
4. **Network Access Layer** – Sends bits through the physical medium.  
🔁 The process reverses at the destination to rebuild the message.

---
## 5. Key Protocols
- **TCP:** Reliable, connection-oriented communication  
- **UDP:** Fast, connectionless communication  
- **IP:** Logical addressing and routing  
- **DNS:** Translates domain names to IPs  
- **HTTP/HTTPS:** Web communication  
- **ICMP:** Diagnostics (used by `ping`, `traceroute`)

---

## ✅ Summary
- TCP/IP = Internet’s backbone  
- 4 layers work together for communication  
- **TCP ensures reliability**, **IP handles routing**  
- Combines hardware & software network functions

**brief**
The network access layer -creation of data packets and their transmission across a network. This includes hardware devices connected to physical cables and switches that direct data to its destination
Hubs, modems, cables, and wiring 
The address resolution protocol (ARP) is part of the network access layer. Since MAC addresses are used to identify hosts on the same physical network, ARP is needed to map IP addresses to MAC addresses for local network communication.

the internet layer- The internet layer is where IP addresses are attached to data packets to indicate the location of the sender and receiver. The internet layer also focuses on how networks connect to each other. For example, data packets containing information that determine whether they will stay on the LAN or will be sent to a remote network, like the internet.
 The internet layer also determines which protocol is responsible for delivering the data packets and ensures the delivery to the destination host. Here are some of the common protocols that operate at the internet layer:

Internet Protocol (IP). IP sends the data packets to the correct destination and relies on the Transmission Control Protocol/User Datagram Protocol (TCP/UDP) to deliver them to the corresponding service. IP packets allow communication between two networks. They are routed from the sending network to the receiving network. TCP in particular retransmits any data that is lost or corrupt.

Internet Control Message Protocol (ICMP). The ICMP shares error information and status updates of data packets. This is useful for detecting and troubleshooting network errors. The ICMP reports information about packets that were dropped or that disappeared in transit, issues with network connectivity, and packets redirected to other routers.
 The transport layer includes protocols to control the flow of traffic across a network. 
These protocols permit or deny communication with other devices and include information about the status of the connection. Activities of this layer include error control, which ensures data is flowing smoothly across the network. 
The transport layer is responsible for delivering data between two systems or networks and includes protocols to control the flow of traffic across a network. TCP and UDP are the two transport protocols that occur at this layer. 

Transmission Control Protocol 
The Transmission Control Protocol (TCP) is an internet communication protocol that allows two devices to form a connection and stream data. It ensures that data is reliably transmitted to the destination service. TCP contains the port number of the intended destination service, which resides in the TCP header of a TCP/IP packet.

User Datagram Protocol 
The User Datagram Protocol (UDP) is a connectionless protocol that does not establish a connection between devices before transmissions. It is used by applications that are not concerned with the reliability of the transmission. Data sent over UDP is not tracked as extensively as data sent using TCP. Because UDP does not establish network connections, it is used mostly for performance sensitive applications that operate in real time, such as video streaming.
at the application layer, protocols determine how the data packets will interact with receiving devices. Functions that are organized at application layer include file transfers and email services. 
The application layer in the TCP/IP model is similar to the application, presentation, and session layers of the OSI model. The application layer is responsible for making network requests or responding to requests. This layer defines which internet services and applications any user can access. Protocols in the application layer determine how the data packets will interact with receiving devices. Some common protocols used on this layer are: 

Hypertext transfer protocol (HTTP)

Simple mail transfer protocol (SMTP)

Secure shell (SSH)

File transfer protocol (FTP)

Domain name system (DNS)

Application layer protocols rely on underlying layers to transfer the data across the network.
<img width="11319" height="4707" alt="RbNt47PDRTGJZ6q_QtaNMg_9b9098ac04e84c2d8ad04b220c5456f1_CS_R-210_TCP-vs-OSI" src="https://github.com/user-attachments/assets/2afbfbb3-11aa-4a44-9523-cd339982bbb5" />

**The OSI model**
The OSI visually organizes network protocols into different layers. Network professionals often use this model to communicate with each other about potential sources of problems or security threats when they occur. 

The TCP/IP model combines multiple layers of the OSI model. There are many similarities between the two models. Both models define standards for networking and divide the network communication process into different layers. The TCP/IP model is a simplified version of the OSI model.
**IP addresses & network communication**

  
