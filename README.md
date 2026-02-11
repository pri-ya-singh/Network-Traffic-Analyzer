# 📡 Network Traffic Analyzer

## 📌 Project Overview

Network Traffic Analyzer is a real-time packet inspection tool built using **C++ (libpcap)** and **Python (Scapy)**.  
The system captures live network packets, analyzes protocol-level data, and visualizes traffic statistics.

The project demonstrates hands-on implementation of:

- Low-level packet capture
- TCP/IP protocol analysis
- Network header parsing
- Cross-platform traffic monitoring
- Data visualization of live traffic

---

## 🚀 Key Features

- **Real-time Packet Capture**
  Captures live packets directly from network interfaces.

- **Low-Level Monitoring (C++ / libpcap)**
  Uses libpcap on Ubuntu for efficient, high-performance packet sniffing.

- **Cross-Platform Support**
  Supports packet capture on:
  - Linux (libpcap)
  - Windows (Npcap + Scapy)

- **Protocol Classification**
  Identifies and classifies:
  - TCP
  - UDP
  - Other IP-based traffic

- **Traffic Visualization**
  Generates bar charts and pie charts to represent protocol distribution and packet statistics.

---

## 🏗️ System Architecture

The project is divided into two major modules:

---

### 1️⃣ C++ Packet Sniffer (Linux - libpcap)

Responsibilities:
- Captures raw packets from network interface
- Extracts Ethernet, IP, TCP, and UDP headers
- Parses source/destination IP addresses
- Extracts port numbers and protocol types
- Aggregates protocol-level statistics

---

### 2️⃣ Python Packet Analyzer (Windows/Linux - Scapy)

Responsibilities:
- Captures packets using Scapy
- Filters traffic by protocol
- Extracts metadata (IP, ports, protocol)
- Computes traffic distribution
- Visualizes results using Matplotlib

---

## ⚙️ Core Functionalities

### 🔹 Packet Capture

Uses:

- `pcap_open_live()` (libpcap)
- `sniff()` (Scapy)

Captures packets directly from the NIC in real time.

---

### 🔹 Protocol Parsing

Parses:

- Ethernet Header
- IPv4 Header
- TCP Header
- UDP Header

Extracted fields include:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol Type
- Packet Length

---

### 🔹 Traffic Classification

Packets are categorized into:

- TCP Traffic
- UDP Traffic
- Other IP Protocols

Statistics are aggregated for traffic distribution analysis.

---

### 🔹 Data Visualization

Using Matplotlib:

- Bar Charts for protocol comparison
- Pie Charts for traffic distribution
- Real-time aggregated statistics

---

## 🛠️ Technologies Used

- **C++**
- **Python**
- **libpcap**
- **Scapy**
- **Npcap (Windows)**
- **Matplotlib**
- **TCP/IP Networking**
- **Linux (Ubuntu)**
- **Windows**

---

## 🖥️ How to Run

### 🔹 Linux (C++ Version)

1. Install libpcap:
   ```bash
   sudo apt install libpcap-dev
