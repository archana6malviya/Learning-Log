# 🌐 Network Protocols

## 📘 What is a Network Protocol?
A **network protocol** is a set of **rules and standards** that define how data is transmitted, received, and interpreted between devices over a network.  
Protocols ensure reliable, secure, and standardized communication between computers and other devices.

---
## ⚙️ Types of Network Protocols

### 🧠 1. Application Layer Protocols
Used for communication between user applications.

| Protocol | Full Form | Description |
|-----------|------------|-------------|
| **HTTP / HTTPS** | HyperText Transfer Protocol (Secure) | Transfers web pages between browsers and web servers. |
| **FTP / SFTP** | File Transfer Protocol / Secure File Transfer Protocol | Transfers files between systems. |
| **SMTP / POP3 / IMAP** | Simple Mail Transfer / Post Office Protocol / Internet Message Access Protocol | Manage email sending and receiving. |
| **DNS** | Domain Name System | Converts domain names into IP addresses. |

---

### 🚀 2. Transport Layer Protocols
Responsible for delivering data between systems.

| Protocol | Full Form | Description |
|-----------|------------|-------------|
| **TCP** | Transmission Control Protocol | Provides reliable, ordered, and error-checked data delivery. |
| **UDP** | User Datagram Protocol | Offers fast, connectionless transmission (used in streaming and gaming). |

---

### 🌍 3. Internet Layer Protocols
Handle logical addressing and routing of data packets.

| Protocol | Full Form | Description |
|-----------|------------|-------------|
| **IP (IPv4 / IPv6)** | Internet Protocol | Routes data packets across networks. |
| **ICMP** | Internet Control Message Protocol | Sends error and control messages (used by `ping`). |

---

### 🔌 4. Network Access Layer Protocols
Define how data is physically transmitted over the network.

| Protocol | Full Form | Description |
|-----------|------------|-------------|
| **Ethernet** | — | Used for wired LAN connections. |
| **Wi-Fi (IEEE 802.11)** | — | Wireless local area network communication. |
| **PPP** | Point-to-Point Protocol | Direct communication between two network nodes. |

---

# 1. DNS Resolution (Domain Name System)

**Protocol used:** DNS

Converts the human-readable domain name (e.g., www.example.com) into an IP address (e.g., 93.184.216.34).

**The browser checks:**

Browser cache

OS cache

Router cache

DNS server

# 2. Establishing a Connection

**Protocol used:** TCP or UDP

Most web traffic uses TCP for reliable connection.

**Browser performs a TCP three-way handshake with the web server:**

1. SYN  → Client requests a connection
2. SYN-ACK ← Server acknowledges
3. ACK  → Client confirms


If HTTPS is used, TLS/SSL handshake follows to create a secure encrypted channel.

# 3. Sending the Request

**Protocol used:** HTTP or HTTPS

**The browser sends an HTTP request to the server:**
Host: www.example.com


HTTPS uses HTTP over TLS (Transport Layer Security) for encryption.

# 4. Server Processing

The server receives the request, processes it, and prepares a response (e.g., HTML file, image, or JSON data).

# 5. Receiving the Response

**Protocol used:** HTTP or HTTPS

The server sends back an HTTP response:

HTTP/1.1 200 OK
Content-Type: text/html


The browser starts downloading webpage components (HTML, CSS, JS, images).

# 6. Rendering the Webpage

The browser parses the HTML, CSS, and JavaScript files to render the webpage on screen.

Additional resources may trigger more HTTP requests.

# 🌐 Sequence of Protocols Used During Web Browsing

When you browse a website (e.g., https://www.example.com), several network protocols work in order, each performing a specific task.

## 🔢 Order of Protocol Usage

| Step  | Purpose                                             | Protocol Used              | Description                                                                        |
| ----- | --------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------- |
| **1** | **Translate domain name to IP address**             | **DNS**                    | Converts `www.example.com` → `93.184.216.34`.                                      |
| **2** | **Establish network path**                          | **IP (Internet Protocol)** | Finds the best route to the server.                                                |
| **3** | **Establish connection between browser and server** | **TCP**                    | Creates a reliable connection using the three-way handshake (SYN → SYN-ACK → ACK). |
| **4** | **Secure the connection (if HTTPS)**                | **TLS / SSL**              | Encrypts data between browser and server for secure communication.                 |
| **5** | **Send web request**                                | **HTTP / HTTPS**           | Browser sends an HTTP request to                                                   |


| Step  | Process                                | Protocol Used                                                   | Purpose                                                                                    |
| ----- | -------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| **1** | **URL Entered in Browser**             | —                                                               | User initiates the request.                                                                |
| **2** | **DNS Lookup**                         | **DNS (Domain Name System)**                                    | Converts the domain name (`www.example.com`) into an IP address (e.g., `93.184.216.34`).   |
| **3** | **Connection Establishment**           | **TCP (Transmission Control Protocol)**                         | Creates a reliable connection between browser (client) and web server (via TCP handshake). |
| **4** | **Secure Connection Setup (if HTTPS)** | **TLS / SSL (Transport Layer Security / Secure Sockets Layer)** | Encrypts communication to ensure security.                                                 |
| **5** | **Send Web Request**                   | **HTTP / HTTPS (HyperText Transfer Protocol / Secure)**         | Browser requests a web page or resource from the server.                                   |
| **6** | **Data Routing**                       | **IP (Internet Protocol)**                                      | Routes packets across the internet between devices.                                        |
| **7** | **Data Transmission**                  | **Ethernet / Wi-Fi (Link Layer Protocols)**                     | Transfers data physically through the local network.                                       |
| **8** | **Response from Server**               | **HTTP / HTTPS**                                                | Server sends web page content (HTML, CSS, JS, images) to the browser.                      |
| **9** | **Rendering Web Page**                 | —                                                               | Browser interprets and displays the content to the user.                                   |

🔄 Simplified Flow
User → DNS → TCP → TLS (if HTTPS) → HTTP/HTTPS → IP → Ethernet/Wi-Fi → Server
Then the process reverses:
Server → IP → TCP → TLS → HTTP Response → Browser

💡 Summary

DNS resolves the domain name.

TCP establishes connection.

TLS secures data (only for HTTPS).

HTTP/HTTPS handles request and response.

IP manages routing.

Ethernet/Wi-Fi sends the data physically.

