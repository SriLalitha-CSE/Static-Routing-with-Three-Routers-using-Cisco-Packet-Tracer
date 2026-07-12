# Static Routing with Three Routers using Cisco Packet Tracer

## Overview

This project demonstrates the implementation of **Static Routing** in a network consisting of three routers. Each router connects to a separate LAN, and the routers communicate through serial links. Static routes are manually configured to enable communication between all networks.

This lab provides a practical understanding of how routers forward packets between different networks using manually configured routing tables.

---

## Objectives

- Design a network with three interconnected routers.
- Configure IP addresses for routers and end devices.
- Configure serial interfaces between routers.
- Implement static routing using the `ip route` command.
- Verify end-to-end connectivity using ping.
- Understand how routers forward packets between different networks.

---

## Software Used

- Cisco Packet Tracer

---

##  Network Topology

### Devices Used

- 3 Cisco Routers
- 3 Switches
- Multiple PCs
- Serial (DCE/DTE) Connections
- Copper Straight-Through Cables

Each router connects to:
- One Local Area Network (LAN)
- Neighboring routers through serial links

---

##  Network Addressing

### LAN Networks

| Network | Gateway Router |
|---------|----------------|
| 192.168.1.0/24 | Router 3 |
| 192.168.2.0/24 | Router 6 |
| 192.168.3.0/24 | Router 5 |

### Serial Connections

Example:

| Connection | IP Address |
|------------|------------|
| Router3 ↔ Router6 | 11.0.0.1 / 11.0.0.2 |

---

##  Configuration Performed

- Configured FastEthernet interfaces on all routers.
- Assigned IP addresses to all PCs.
- Configured serial interfaces between routers.
- Set clock rate on DCE serial interfaces.
- Enabled all interfaces using `no shutdown`.
- Added static routes using the `ip route` command.
- Verified routing tables.
- Tested communication between different LANs.

---

##  Key Commands Used

### Configure Interface

```bash
interface fastEthernet 0/0
ip address <IP_Address> <Subnet_Mask>
no shutdown
```

### Configure Serial Interface

```bash
interface serial 0/0/0
ip address <IP_Address> <Subnet_Mask>
clock rate 64000
no shutdown
```

### Configure Static Route

```bash
ip route <Destination_Network> <Subnet_Mask> <Next_Hop_IP>
```

### Verify Routing Table

```bash
show ip route
```

---

##  Verification

After configuring static routes:

- All router interfaces were active.
- Routing tables contained manually configured routes.
- PCs in different LANs successfully communicated using **ping**.
- End-to-end connectivity between all networks was established.

---

##  Concepts Learned

- Static Routing
- Router Configuration
- Serial Communication (DCE/DTE)
- Next-Hop Routing
- IP Addressing
- Routing Tables
- Interface Configuration
- Network Troubleshooting

---

##  Repository Contents

- `Static-Routing-3-Routers.pkt` – Cisco Packet Tracer simulation
- `README.md` – Project documentation

---

##  Future Improvements

- Implement Dynamic Routing (RIP, OSPF, EIGRP)
- Add redundant links for failover
- Configure Access Control Lists (ACLs)
- Perform route summarization

---
