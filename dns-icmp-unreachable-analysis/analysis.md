# Technical Analysis: Destination Port Unreachable Issue

This document contains the deep technical explanation, simulation steps, packet captures, commands, and root cause analysis of the DNS port unreachable issue.

---

## 1. Background of the Incident

When attempting to access a client website (`www.yummyrecipesforme.com`), customers received: **Destination port unreachable**

A packet analyzer revealed:**ICMP: udp port 53 unreachable**

This indicates DNS lookup failed before an HTTPS connection could be made.

---

## 2. Network Flow Diagram

Browser
│
├── DNS Query (UDP 53)
│
▼
DNS Server / Firewall
│
└── ICMP Error → "udp port 53 unreachable"


Because DNS failed, the browser cannot obtain the IP → page fails to load.

---

## 3. Tools Used

| Tool | Purpose |
|------|---------|
| `tcpdump` | Capture traffic and see ICMP errors |
| `dig` | DNS lookup generator |
| `netcat (nc)` | Simulate/close ports to trigger ICMP errors |
| `curl` | Test HTTP/HTTPS requests |
| `Wireshark` | (Optional) Analyze PCAP visually |

---

## 4. Hands-On Simulation on Linux VM

Follow these exact steps to reproduce the real-world error.

---

### **STEP 1 — Install Required Tools**

```bash
sudo apt update
sudo apt install tcpdump dnsutils netcat-traditional curl -y

STEP 2 — Start tcpdump to Capture DNS & ICMP Traffic
sudo tcpdump -i any -nn port 53 or icmp
Leave this running.

STEP 3 — Trigger the DNS Query to a Fake DNS Server

We use a non-existent IP so packets cannot reach a DNS server:
dig @10.10.10.10 google.com

You may see:
connection timed out; no servers could be reached

And tcpdump will show:
ICMP 10.10.10.1 → <your_VM> udp port 53 unreachable

This simulates the exact Coursera incident.
STEP 4 — Save a Packet Capture for GitHub
Run:
sudo tcpdump -i any -nn port 53 or icmp -w dns_issue.pcap
Repeat the dig command while tcpdump is saving packets.

STEP 5 — Simulate "Destination Port Unreachable" Using Netcat
Start a UDP listener:
sudo nc -ulvp 9999
sudo nc -ulvp 9999
Stop it (Ctrl + C).
Now send UDP traffic:
echo "test" | nc -u 127.0.0.1 9999
tcpdump will show:
ICMP 127.0.0.1 → 127.0.0.1: destination port unreachable

This demonstrates how ICMP messages work.

5. Root Cause of the Original Incident
The “destination port unreachable” occurred because:
DNS port 53 UDP traffic was blocked
This prevented DNS resolution.
Without DNS → browser cannot find the server IP → website fails.
The ICMP message pointed directly to the cause.

6. Mitigation

Ensure firewall allows outbound UDP 53

Ensure DNS server is reachable

Monitor DNS availability

Set backup DNS resolvers

SIEM alerts for repeated ICMP unreachable events

7. Key Takeaways

DNS failures often produce ICMP unreachable messages

tcpdump is essential for packet-level troubleshooting

ICMP errors help identify blocked ports

Simulating errors in a VM strengthens practical cybersecurity skills

8. Screenshots (Place in /screenshots/ folder)

Add:

tcpdump output

dig errors

netcat test

Wireshark PCAP screenshots

9. Conclusion

This project recreates and analyzes a real corporate networking issue using practical tools. It shows clear understanding of DNS, TCP/UDP, and ICMP at a packet level — excellent for cybersecurity portfolios.


---

# ✅ **3. YOUR FULL LINUX VM SIMULATION GUIDE (step-by-step)**

### **1. Install everything**
```bash
sudo apt update
sudo apt install tcpdump dnsutils netcat-traditional curl -y

2. Start capturing DNS & ICMP traffic
sudo tcpdump -i any -nn port 53 or icmp

3. Trigger DNS traffic to a fake server
dig @10.10.10.10 google.com
You will see timeouts + ICMP errors in tcpdump.

4. Save PCAP
sudo tcpdump -i any -nn port 53 or icmp -w dns_issue.pcap

5. Simulate UDP unreachable using netcat
Start listener:
sudo nc -ulvp 9999
Stop it.

Send data:
echo "hello" | nc -u 127.0.0.1 9999

In tcpdump, ICMP will appear.

6. Upload dns_issue.pcap and screenshots to GitHub
