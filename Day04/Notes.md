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


# 🌐 The TCP/IP Model

## 1. Introduction
The **TCP/IP model (Transmission Control Protocol / Internet Protocol)** is the **foundation of modern networking**.  
It defines how data moves between devices over the internet or any network.  
It has **4 layers**, each with specific communication roles.

---

## 2. Layers of the TCP/IP Model
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

# 🌐 TCP/IP Model — Brief Notes

## 🧱 1. Network Access Layer
- Handles **creation and transmission** of data packets.  
- Involves **hardware**: hubs, modems, cables, and switches.  
- Uses **MAC addresses** for device identification.  
- **ARP (Address Resolution Protocol):** Maps IP ↔ MAC addresses for local communication.  
- Ensures data moves through the **physical network** efficiently.

---

## 🌍 2. Internet Layer
- Adds **IP addresses** to packets (source & destination).  
- Decides if data stays on the **LAN** or goes to a **remote network (WAN/Internet)**.  
- Handles **routing** and **network-to-network communication**.

**Key Protocols:**
- **IP (Internet Protocol):** Directs packets to their destination.  
- **ICMP (Internet Control Message Protocol):** Reports errors and network status (used in `ping`, `traceroute`).  
- Works with **TCP/UDP** for final delivery.

---

## 🚚 3. Transport Layer
- Manages **end-to-end communication** and **flow control**.  
- Ensures reliable or fast delivery depending on protocol.  
- Handles **error detection**, **connection status**, and **data integrity**.

**Main Protocols:**
- **TCP (Transmission Control Protocol):**  
  - Connection-oriented, reliable, retransmits lost data.  
  - Used for web browsing, emails, file transfers.  
- **UDP (User Datagram Protocol):**  
  - Connectionless, faster, less reliable.  
  - Used in video streaming, gaming, voice calls.

---

## 💻 4. Application Layer
- Defines **how applications interact** with the network.  
- Handles **user-facing services** like file sharing and email.  
- Similar to the top 3 layers of the OSI model (Application, Presentation, Session).  
- Relies on lower layers for actual data transfer.

**Common Protocols:**
- **HTTP / HTTPS** – Web browsing  
- **SMTP** – Email sending  
- **SSH** – Secure remote access  
- **FTP** – File transfer  
- **DNS** – Converts domain names to IPs  

---

## ✅ Summary
- **Network Access:** Physical transmission, ARP  
- **Internet:** IP addressing & routing  
- **Transport:** Reliable delivery (TCP/UDP)  
- **Application:** User services (HTTP, DNS, FTP, SMTP)

**The OSI model**
The OSI visually organizes network protocols into different layers. Network professionals often use this model to communicate with each other about potential sources of problems or security threats when they occur. 

The TCP/IP model combines multiple layers of the OSI model. There are many similarities between the two models. Both models define standards for networking and divide the network communication process into different layers. The TCP/IP model is a simplified version of the OSI model.
**IP addresses & network communication**

  
