# Computer Networks Lab (CSBB 301)

**Student:** Kolan Jyotiradithya reddy
**Roll No.:** 241210061  
**Department:** Computer Science and Engineering

This repository contains the lab record of all 13 Computer Networks lab experiments. Each experiment has its own folder with the lab report (PDF) and, where needed, the Cisco Packet Tracer file (`.pkt`) and Python programs (`.py`).

---

## Tools Used

- **Cisco Packet Tracer 8.x**: network design and simulation (Experiments 3 to 11 and 13)
- **Python 3**: socket programming (Experiments 10 and 11)
- **Command Prompt / Terminal**: network commands (Experiment 2)
- **Wireshark / tshark, NS-3, OMNeT++, GNS3, pfSense, Mininet (SDN)**: explored in Experiment 12
- **Crimping tool, RJ45 connectors, UTP cable**: cable making (Experiment 1)

---

## List of Experiments

| No. | Experiment | Folder | Files |
|:---:|------------|--------|-------|
| 1 | Study of different types of network cables and practical implementation of cross-wired and straight-through cables using crimping tool | [`Lab_Experiment1`](Lab_Experiment1) | Report (PDF) |
| 2 | Study of basic network commands | [`Lab_Experiment2`](Lab_Experiment2) | Report (PDF) |
| 3 | Study and installation of various network devices | [`Lab_Experiment3`](Lab_Experiment3) | Report (PDF), Packet Tracer file |
| 4 | Study and configuration of network IP addressing | [`Lab_Experiment4`](Lab_Experiment4) | Report (PDF), Packet Tracer file |
| 5 | Connect the computers in Local Area Network (LAN) | [`Lab_Experiment5`](Lab_Experiment5) | Report (PDF), Packet Tracer file |
| 6 | Router configuration using Cisco Packet Tracer | [`Lab_Experiment6`](Lab_Experiment6) | Report (PDF), Packet Tracer file |
| 7 | Establishing peer-to-peer network connection of two systems using switch and router in a LAN | [`Lab_Experiment7`](Lab_Experiment7) | Report (PDF), Packet Tracer file |
| 8 | Examine Network Address Translation (NAT) | [`Lab_Experiment8`](Lab_Experiment8) | Report (PDF), Packet Tracer file |
| 9 | Simulate the implementation of various routing protocols (Static, RIP, EIGRP, OSPF) along with ARP, ICMP and IGMP | [`Lab_Experiment9`](Lab_Experiment9) | Report (PDF), Packet Tracer file |
| 10 | Connection-oriented client-server applications using TCP and UDP | [`Lab_Experiment10`](Lab_Experiment10) | Report (PDF), Packet Tracer file, Python programs |
| 11 | Study of socket programming and client-server model | [`Lab_Experiment11`](Lab_Experiment11) | Report (PDF), Packet Tracer file, Python programs |
| 12 | Exploring NS-3, OMNeT++, GNS3, pfSense, Wireshark tool, SDN etc. | [`Lab_Experiment12`](Lab_Experiment12) | Report (PDF) |
| 13 | DHCP server using Cisco Packet Tracer | [`Lab_Experiment13`](Lab_Experiment13) | Report (PDF), Packet Tracer file |

---

## Repository Structure

```
CN_LAB_241210061/
├── Lab_Experiment1/
│   └── Network_cables.pdf
├── Lab_Experiment2/
│   └── Network_commands.pdf
├── Lab_Experiment3/
│   ├── Network_Devices.pdf
│   └── Network_Devices.pkt
├── Lab_Experiment4/
│   ├── Network_IP_Addressing.pdf
│   └── Network_IP_Addressing.pkt
├── Lab_Experiment5/
│   ├── LAN_connection.pdf
│   └── LAN.pkt
├── Lab_Experiment6/
│   ├── Router_Configuration.pdf
│   └── Router_Configuration.pkt
├── Lab_Experiment7/
│   ├── Peer_to_Peer.pdf
│   └── peer_to_peer.pkt
├── Lab_Experiment8/
│   ├── NAT_exp8.pdf
│   └── NAT.pkt
├── Lab_Experiment9/
│   ├── Routing_Protocols.pdf
│   └── Routing_Protocols.pkt
├── Lab_Experiment10/
│   ├── TCP_UDP.pdf
│   ├── TCP_UDP_Client_Server.pkt
│   ├── tcp_server.py
│   ├── tcp_client.py
│   ├── udp_server.py
│   └── udp_client.py
├── Lab_Experiment11/
│   ├── Socket_Programming.pdf
│   ├── Socket_Programming.pkt
│   ├── server_tcp.py
│   ├── client_tcp.py
│   ├── server_udp.py
│   ├── client_udp.py
│   └── server_multi.py
├── Lab_Experiment12/
│   └── Network_Tools_Exploration.pdf
├── Lab_Experiment13/
│   ├── DHCP_Server.pdf
│   └── DHCP_Server.pkt
└── README.md
```

Each lab report contains the **Aim, Software / Hardware Requirements, Theory, Procedure, Observations and Conclusion** of the experiment.

---

## How to Open the Packet Tracer Files

1. Install **Cisco Packet Tracer 8.x** (free with a Cisco Networking Academy account).
2. Open Packet Tracer and go to **File > Open**, then select the `.pkt` file from the experiment folder.
3. Click on any PC and open **Desktop > Command Prompt** to run commands like `ping` and `ipconfig`, or open the router **CLI** tab to see its configuration.
4. Use **Simulation mode** to watch the packets move through the network.

---

## How to Run the Python Programs

Python 3 is needed. No extra libraries are required, as only the built-in `socket` and `threading` modules are used. Always start the **server first** in one terminal, then run the **client** in a second terminal.

### Experiment 10: TCP and UDP client-server

```bash
cd Lab_Experiment10

# TCP (port 5000)
python tcp_server.py      # Terminal 1
python tcp_client.py      # Terminal 2

# UDP (port 6000)
python udp_server.py      # Terminal 1
python udp_client.py      # Terminal 2
```

Expected output (TCP client):

```
[TCP Client] Connected to 127.0.0.1:5000
[TCP Client] Server replied: ACK: Hello TCP Server
```

Expected output (UDP client):

```
[UDP Client] Datagram sent
[UDP Client] Server replied: ACK: Hello UDP Server
```

### Experiment 11: Socket programming and client-server model

```bash
cd Lab_Experiment11

# TCP (port 12345)
python server_tcp.py      # Terminal 1
python client_tcp.py      # Terminal 2

# UDP (port 12345)
python server_udp.py      # Terminal 1
python client_udp.py      # Terminal 2

# Multi-client TCP server (handles 2 clients using threads)
python server_multi.py    # Terminal 1
python client_tcp.py      # Terminal 2
python client_tcp.py      # Terminal 3
```

> **Note:** On Linux / macOS use `python3` instead of `python`. If the error `Address already in use` is shown, wait for about one minute and run the server again.

---

## Course Details

- **Course:** Computer Networks (CSBB 301)
- **Department:** Computer Science and Engineering
