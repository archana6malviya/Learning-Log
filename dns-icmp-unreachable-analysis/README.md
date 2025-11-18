# Network Troubleshooting: Destination Port Unreachable (ICMP Error)

This project demonstrates a real-world network troubleshooting scenario where users trying to access the website **www.yummyrecipesforme.com** received the error:

> **Destination port unreachable**

This issue occurred due to a failure in the DNS lookup stage, where UDP packets to port 53 resulted in ICMP error messages.  
Using a Linux VM, I recreated this scenario using `tcpdump`, `dig`, `netcat`, and packet analysis.

---

## 📌 Project Scenario

Customers reported they could not access a website and saw the message **“destination port unreachable.”**  
A network analyzer showed:

ICMP: udp port 53 unreachable


This meant DNS resolution was failing before the browser could send the HTTPS request.

---

## 📌 What This Project Demonstrates

✔ DNS request using UDP port 53  
✔ ICMP error messages for unreachable ports  
✔ Packet capture using tcpdump  
✔ Replaying and simulating the incident  
✔ Understanding browser → DNS server → web server flow  

---

## 📌 Tools Used

- **tcpdump** – Packet capture  
- **dig** – DNS lookup tool  
- **netcat (nc)** – Simulate UDP services  
- **curl** – Test HTTPS connectivity  
- **Wireshark** (optional) – PCAP analysis  

---

## 📌 Packet Flow

Browser → DNS Query (UDP 53) → DNS Server/Firewall
DNS Server/Firewall → ICMP "Destination Port Unreachable"
Browser → Cannot resolve hostname → Website won't load


---

## 📌 Files in This Repository

| File | Description |
|------|-------------|
| `README.md` | Overview of the project |
| `analysis.md` | Deep-dive technical analysis |
| `dns_issue.pcap` (optional) | Captured packets from tcpdump |
| `screenshots/` (optional) | Terminal output images |

---

## 📌 Linux VM Hands-On Steps (Quick Summary)

1. Install required tools  
2. Capture packets with tcpdump  
3. Trigger DNS queries using a fake DNS server  
4. Simulate UDP port unreachable  
5. Save packet captures  
6. Analyze ICMP responses  

Detailed simulation steps are included in `analysis.md`.

---

## 📌 Learning Outcomes

- Understand how DNS resolution works  
- Identify port-blocking issues  
- Analyze ICMP error messages  
- Use tcpdump for real-world troubleshooting  

---

## 📌 Author

Created as part of cybersecurity hands-on learning for portfolio building.

