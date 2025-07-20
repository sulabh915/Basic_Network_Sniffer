# 🛡️ Packet Sniffer Tool (Linux)

A Python-based packet sniffer for educational and ethical hacking purposes. It captures, decodes, and displays network packets in real time—similar to Wireshark, directly in your terminal!

---

## Features

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

## Requirements

- Linux OS (uses `AF_PACKET`, Linux-specific)
- Python 3.x
- Root privileges (to open raw socket)

Install dependencies:

```bash
pip install prettytable
```

---

## Usage
```bash
sudo python3 packet_sniffer.py [--log]
```
### Arguments
  - --log: (optional) Save all captured packets to packet_log.txt

---

## Sample Output
```bash
[*] Packet Sniffer Started (Ethical Use Only)
+-----------------+-----------------+----------+----------+----------+--------+-----+----------------------------------------------------------+
|   Source IP     | Destination IP  | Protocol | Src Port | Dst Port | Length | TTL | Info                                                    |
+-----------------+-----------------+----------+----------+----------+--------+-----+----------------------------------------------------------+
| 192.168.0.5     | 93.184.216.34   | HTTP     | 55976    | 80       | 578    | 64  | TCP Seq=992207891 Ack=1333477122 | POST /userinfo.php...|
```

## Top Protocol Summary
```bash
+----------+---------+
| Protocol | Packets |
+----------+---------+
| TCP      | 10      |
| HTTP     | 8       |
| HTTPS    | 4       |
| DNS      | 1       |
| UDP      | 1       |
+----------+---------+
```

---

## Ethical Use Disclaimer
  This tool is for educational and authorized penetration testing only. Unauthorized packet sniffing may violate privacy laws.

---

## Log File Format (If Enabled)
```bash
Source IP       Destination IP  Protocol  SrcPort  DstPort  Len   TTL   Info
192.168.0.5     93.184.216.34   HTTP      55976    80       578   64    POST /userinfo.php HTTP/1.1 | POST Data: user=admin&pass=admin
```




