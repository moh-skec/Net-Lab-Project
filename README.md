# Project Overview

## Introduction

This project focuses on network routing protocols, specifically **EIGRP (Enhanced Interior Gateway Routing Protocol)** and **HSRP (Hot Standby Router Protocol)**. The document provides an in-depth discussion on the functionality, configuration, and optimization of these protocols in Cisco environments.

## Objectives

The key objectives of this project include:

- Understanding the fundamentals of **EIGRP** and **HSRP**.
- Configuring these protocols on Cisco routers.
- Implementing **Routing Redistribution**.
- Setting up network servers in **Packet Tracer**.
- Configuring **wireless routers** in **Packet Tracer**.

## EIGRP Protocol

### EIGRP Overview

EIGRP is an advanced distance-vector routing protocol developed by Cisco. It combines the best features of **distance vector** and **link-state protocols**, classifying it as a **hybrid protocol**. It offers fast convergence and efficient routing updates.

### HSRP Key Features

- Uses **DUAL (Diffusing Update Algorithm)** for loop-free routing.
- Supports **VLSM (Variable-Length Subnet Masking)**.
- Implements **Incremental Updates** to reduce network load.
- Allows **Route Summarization**.
- Supports **IPv4, IPv6, IPX, and Appletalk**.

### Components

EIGRP maintains three primary tables:

1. **Neighbor Table** - Lists directly connected neighbors.
2. **Topology Table** - Stores all learned routes.
3. **Routing Table** - Contains the best possible paths.

## HSRP Protocol

### Overview

HSRP provides **router redundancy** to ensure **high availability** in case of network failure. It allows multiple routers to work together, with one acting as the **Active Router** and another as the **Standby Router**.

### Key Features

- **Failover Mechanism**: If the active router fails, the standby router takes over.
- **Virtual IP Address**: Used as the default gateway for hosts.
- **Load Balancing**: Ensures efficient traffic distribution.
- **Preemption**: Allows a router with higher priority to take over.
- **Interface Tracking**: Adjusts router priority based on link availability.

### Router States

Routers in an HSRP group can be in one of the following states:

- **Disable**: HSRP is disabled.
- **Initial**: Router is starting up.
- **Learn**: Router is waiting to receive a hello packet.
- **Listen**: Router is monitoring hello packets.
- **Speak**: Router is exchanging hello messages.
- **Standby**: Backup router, ready to take over if the active router fails.
- **Active**: The router currently forwarding traffic.

## Routing Redistribution

Routing redistribution enables the exchange of routes between different routing protocols (e.g., EIGRP and OSPF). This allows routers to communicate effectively in **heterogeneous networks**.

## Network Configuration in Packet Tracer

### Server Configurations

- **DHCP Server**
- **DNS Server**
- **Mail Server**
- **Web Server**

### Wireless Router Setup

- Configure SSID and security settings.
- Implement **EtherChannel** for link aggregation.
- Apply **HSRP** for redundancy.
- Enable **SSH** for secure remote access.
- Set up static and dynamic routing as needed.

## Testing and Validation

To ensure proper functionality, the following tests should be performed:

- **Ping Tests** between devices to verify connectivity.
- **Traceroute** to examine the path packets take.
- **Show Commands** (`show ip route`, `show ip eigrp neighbors`, etc.) for debugging.
- **Failover Testing** to validate HSRP redundancy.

## Conclusion

This project provides a comprehensive study and implementation of **EIGRP** and **HSRP**, demonstrating how these protocols improve **network performance** and **fault tolerance**. The configurations and concepts discussed can be further expanded for **real-world networking scenarios**.

Finally, you can ensure that the [NetLab website](http://www.netlab.iut.ac.ir) is reachable from all end-user devices, switches, and routers by performing ping tests.
