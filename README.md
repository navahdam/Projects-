# Packet Sniffer with Firewall – Python GUI Tool

This is a Python-based Packet Sniffer with an Integrated Firewall, offering a real-time graphical interface to monitor, filter, and block network packets based on user-defined rules.

It combines the functionality of:
- A Packet Sniffer to monitor all network traffic
- A Personal Firewall to block traffic based on IP, port, or protocol
- A Live Graphing Tool to visualize blocked vs allowed traffic

## Features

### Packet Sniffer
- Captures live network packets using Scapy
- Logs each packet with:
  - Timestamp
  - Source/Destination IPs and ports
  - Protocol (TCP, UDP, ICMP, etc.)
- Saves all packet data to `packet_log.csv`

### Integrated Firewall
- Create blocking rules based on:
  - IP Address (e.g., `192.168.1.10`)
  - Port Number (e.g., `22`, `445`)
  - Protocol (e.g., `TCP`, `UDP`, `ICMP`)
- Automatically blocks and logs matching packets to `blocked_packets.csv`
- Provides an interface to add or remove rules easily
- Stores rules persistently in `firewall_rules.json`

### Real-Time Monitoring
- Live graph that shows packet activity:
  - Allowed vs Blocked packets over time
- Updates in real time as packets are captured

### Logging and Export
- Logs stored in CSV format with headers
- One-click export option for reporting or analysis

## Requirements

Install required dependencies using pip:

```bash
pip install pyqt5 scapy matplotlib
