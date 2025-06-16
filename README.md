# 🛡️ Packet Sniffer Tool (Linux) - codealpha_task

A Python-based packet sniffer for educational and ethical hacking purposes. It captures, decodes, and displays network packets in real time—similar to Wireshark, directly in your terminal!

---

## ✨ Features

- Live capture of network traffic (Ethernet / IPv4)
- Displays:
  - Source & Destination IP
  - Protocol (TCP, UDP, ICMP, HTTP, HTTPS, DNS, etc.)
  - Ports
  - TTL
  - Packet Length
  - Protocol-specific Info
  - HTTP Request types (`GET`, `POST`) and payloads
- Protocol frequency tracking (top protocols table)
- Logging to file (optional)
- Beautiful tabular output using `PrettyTable`

---

## 🧰 Requirements

- Linux OS (uses `AF_PACKET`, Linux-specific)
- Python 3.x
- Root privileges (to open raw socket)

Install dependencies:

```bash
pip install prettytable

