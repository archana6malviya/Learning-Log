# 🌐 Network Basics

## 🧩 What is a Network?
A **network** is a group of connected devices that can **communicate** with each other using cables or wireless connections.

---

## 🖥️ Network Addresses
- Devices use **unique addresses** to find each other.  
- **IP Address(Internet Protocol Address):** Identifies devices on a network.

It is the address of a device on a network.
It helps devices find and talk to each other.

Think of it like:

📮 Home address → For houses
🌐 IP address → For computers  
Example:

192.168.1.10 (Local home network IP)

8.8.8.8 (Google DNS server)

Types:

Public IP → given by your internet provider

Private IP → used inside home/office network

IPv4 → 192.168.1.1

IPv6 → long format like 2001:0db8::1
- **MAC Address(Media Access Control Address):** Identifies the device’s hardware.  
- These ensure data reaches the **correct device**.
- It is a unique physical identifier burned into your device’s network card (Wi-Fi or Ethernet).

Think of it like:

🆔 Fingerprint → Unique to you
💻 MAC → Unique to each network device

Example:

A4:5E:60:12:AB:FF

👉 You CANNOT change it (permanently).
👉 Used inside the local network only.

| Feature    | IP Address             | MAC Address                 |
| ---------- | ---------------------- | --------------------------- |
| What it is | Location address       | Device identity             |
| Changes?   | Yes, changes often     | No, fixed                   |
| Given by   | Network / router       | Manufacturer                |
| Format     | 192.168.1.1            | A4:5E:60:AA:2C:31           |
| Used in    | Internet communication | Local network communication |

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

# 🧩 The OSI Model (Open Systems Interconnection)

The **OSI Model** explains how data moves through a network in **7 layers**.  
It helps network and security professionals understand, design, and troubleshoot communication systems.

---

## 🌐 TCP/IP vs OSI Model
| Feature | **TCP/IP Model** | **OSI Model** |
|----------|------------------|----------------|
| Layers | 4 | 7 |
| Developed By | U.S. DoD | ISO |
| Purpose | Practical, protocol-based | Theoretical, reference model |
| Use | Internet and modern networks | Learning & troubleshooting |

**TCP/IP Layers:** Network Access, Internet, Transport, Application  
**OSI Layers:** Physical, Data Link, Network, Transport, Session, Presentation, Application

---

## 🧱 OSI Layers (Top to Bottom)

### **Layer 7 – Application**
- Closest to the user — It provides an interface for applications to use the network to transmit data, and passes the data down to the presentation layer.
- Examples: **HTTP/HTTPS, SMTP, DNS, FTP**  
- Handles user services like web browsing, email, and file transfer.

---

### **Layer 6 – Presentation**
- Converts data formats for sending/receiving systems.
- It receives data from the application layer.
- The data is in a format the sending application understands, but not always in a standard format.
- This layer translates the data into a standard format that any computer can understand.
- It also handles encryption, decryption, compression, and other data transformations.
- After processing, it sends the data to the session layer.  
- Handles **encryption, compression, translation**.  
- Example: **SSL/TLS** encryption in HTTPS.

---

### **Layer 5 – Session**
- Manages and maintains communication **sessions** between devices.
- It receives properly formatted data from the presentation layer.

It tries to set up a connection (session) with the remote computer.

If the connection cannot be made, it sends an error and stops the process.

If a session is created, this layer maintains and manages it.

It works with the remote computer’s session layer to synchronize communication.

Each session is unique, so data from different tasks doesn’t mix (like opening two browser tabs).

Once the session is established and stable, it passes the data to the Transport Layer.
- Handles **authentication, reconnection, and checkpoints**.  
- Keeps sessions open during data transfer, then closes them.

---

### **Layer 4 – Transport**
- Ensures **reliable delivery**, **error control**, and **segmentation**.
- This layer chooses the protocol used to send data — mainly TCP or UDP.

TCP (Transmission Control Protocol):

Connection-based (creates a stable connection).

Reliable — ensures all data arrives correctly.

Resends lost packets and controls speed.

Used when accuracy is important (webpages, file transfer).

UDP (User Datagram Protocol):

No connection — just sends data without checking.

Faster but less reliable.

Used when speed matters more (video calls, streaming).

After choosing the protocol, the transport layer breaks data into smaller pieces:

TCP → segments

UDP → datagrams
- Protocols: **TCP (reliable)**, **UDP (fast)**.  
- Manages data flow and speed between systems.

---

### **Layer 3 – Network**
- Handles **routing and addressing** between different networks.
- This layer is responsible for finding the destination of your data.

It decides the best route to send data across large networks like the Internet.

It works with logical addresses, mainly IP addresses.

Logical addressing helps keep networks organized and properly structured.

The most common addressing format is IPv4 (example: 192.168.1.1).

In short, it handles routing — choosing the path your data should take.
- Uses **IP addresses** to deliver packets to destinations.  
- Devices: **Routers**  
- Protocols: **IP, ICMP**

---

### **Layer 2 – Data Link**
- Transfers data within the **same network (LAN)**.
- This layer deals with the physical addressing of data.

It takes the packet from the network layer and adds the MAC address of the destination device.

Every device has a Network Interface Card (NIC) with a unique MAC address burned in by the manufacturer.

MAC addresses cannot be changed (permanently), but they can be spoofed.

Data on a local network is delivered using the physical MAC address, not the IP address.

The data link layer also formats the data so it can be sent over the physical medium.

When receiving data, it checks for errors or corruption that may have occurred during transmission.
- Uses **MAC addresses** for local delivery.  
- Devices: **Switches, NICs**  
- Protocols: **HDLC, SDLC, NCP**

---

### **Layer 1 – Physical**
- Deals with **actual hardware and transmission** (cables, signals, hubs).
- Responsible for physical (MAC) addressing on the network.

Receives the packet from the network layer and adds the MAC address of the destination device.

Works with the Network Interface Card (NIC), which has a unique, manufacturer-assigned MAC address.

MAC addresses are burned into the hardware (cannot be changed, but can be spoofed).

Converts the data into frames, which are the Layer 2 data units.

Ensures the data is in the correct format for physical transmission.

Performs error detection (e.g., checking data integrity to see if corruption occurred during transmission).

Helps control how devices access the shared medium to avoid collisions.

Used by devices like switches, bridges, and NICs.

Plays a key role in ensuring data is delivered correctly within the local network (LAN).
- Converts data into bits (0s & 1s).  
- Devices: **Hubs, Modems, Cables**

---

## ✅ Key Takeaways
- **OSI = 7 Layers**, **TCP/IP = 4 Layers (simplified version)**  
- Both models describe **how data travels** from sender to receiver.  
- **OSI** helps in **troubleshooting**, **TCP/IP** helps in **implementation**.  
- Knowing both models is essential for network and security professionals.


# 🌐 IP Addresses & Network Communication

## ✅ What is an IP Address?
An **IP address (Internet Protocol address)** is a unique identifier that shows the **location of a device** on a network—similar to a home mailing address.

Two main versions:
- **IPv4:** Four numbers separated by dots (e.g., 192.168.1.1)  
- **IPv6:** 32-character hexadecimal address (allows more devices)

---

## 🌍 Public vs Private IP Addresses
- **Public IP:**  
  - Assigned by your ISP  
  - Visible on the internet  
  - Shared by all devices in your home (via router/NAT)

- **Private IP:**  
  - Used inside local networks (home, office)  
  - Not visible outside the network  
  - Each device gets its own private IP

---

## 🖧 MAC Addresses
- A **MAC address** is a unique hardware identifier assigned to a device’s network interface.  
- Switches use MAC addresses to deliver packets within a LAN.  
- A **MAC Address Table** stores device → switch port mappings (like an internal address book).

---

## 📌 Summary
- IPv4 = shorter, older; IPv6 = longer, newer, supports more devices  
- Public IP = internet-facing; Private IP = local network only  
- MAC addresses identify physical devices  
- IP + MAC work together to ensure data reaches the correct device


  # 🌍 Components of Network Layer Communication

The **Network Layer (Layer 3 of the OSI Model)** manages **addressing, routing, and delivery** of data packets across networks.

---

## ⚙️ Network Layer Operations
- Handles **IP addressing** and **packet delivery** between devices.  
- Routes packets **from one router to another** until reaching the destination IP.  
- Uses **routing tables** to remember network paths.  
- Each packet contains:
  - **Source & Destination IP**
  - **Protocol info**
  - **Packet size**

Packets can be:
- **IP Packets** → Used by TCP connections  
- **Datagrams** → Used by UDP connections  

---

## 📦 IPv4 Packet Structure
An **IPv4 Packet** has two parts:  
1. **Header (20–60 bytes)** – routing & control info  
2. **Data** – actual message content (up to 65,535 bytes total)

### 🧩 IPv4 Header Fields (13)
| Field | Function |
|-------|-----------|
| **Version (VER)** | Indicates protocol version (IPv4) |
| **Header Length (IHL)** | Defines where header ends, data begins |
| **Type of Service (ToS)** | Sets packet priority |
| **Total Length** | Total size of header + data |
| **Identification** | Marks fragments of large packets |
| **Flags** | Indicates fragmentation status |
| **Fragment Offset** | Shows position of fragment |
| **Time To Live (TTL)** | Limits packet lifetime across routers |
| **Protocol** | Indicates next-level protocol (TCP/UDP) |
| **Header Checksum** | Detects header corruption |
| **Source IP** | Sender’s IP address |
| **Destination IP** | Receiver’s IP address |
| **Options** | Extra security or routing settings |

---

## 🌐 IPv4 vs IPv6
| Feature | **IPv4** | **IPv6** |
|----------|-----------|-----------|
| **Address Format** | 4 decimal numbers (e.g., 198.51.100.0) | 8 groups of hex digits (e.g., 2002:0db8::1234) |
| **Length** | 32 bits (4 bytes) | 128 bits (16 bytes) |
| **Total Addresses** | ~4.3 billion | ~340 undecillion |
| **Header Complexity** | More fields (e.g., IHL, Flags) | Simplified; adds **Flow Label** |
| **Security** | Basic | Built-in efficiency & reduced collisions |

---

## 🔒 Security Insight
- Packet analysis reveals:
  - Source & destination info  
  - Protocols in use  
  - Routing and integrity data  
- Understanding packet headers helps identify **threats, spoofing, or misrouting**.

---

## ✅ Summary
- Layer 3 = **Routing, addressing, and packet delivery**  
- IPv4 header = **13 key fields** for control and delivery  
- IPv6 = **Larger, simpler, more secure** version of IPv4  
- Inspecting IP headers is vital for **network security analysis**








