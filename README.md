# CCNA VLSM & Static Routing Lab

## 📌 Project Overview

A Cisco Packet Tracer lab designed to practice VLSM subnetting,
IP addressing, and static routing using a 192.168.5.0/24 network.

The network contains four LANs and a point-to-point connection
between two routers.

## 🎯 Objectives

- Apply VLSM subnetting
- Calculate network, broadcast, and usable IP addresses
- Configure IPv4 addressing on PCs and routers
- Configure router interfaces
- Configure static routes
- Verify connectivity using Ping

## 🌐 Network Requirements

| Network | Required Hosts | Subnet |
|---|---:|---|
| LAN 2 | 64 | /25 |
| LAN 1 | 45 | /26 |
| LAN 3 | 14 | /28 |
| LAN 4 | 9 | /28 |
| R1 ↔ R2 | 2 | /30 |

## 📋 IP Addressing

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| PC1 | NIC | 192.168.5.129 | 255.255.255.192 |
| R1 | G0/0 | 192.168.5.190 | 255.255.255.192 |
| PC2 | NIC | 192.168.5.1 | 255.255.255.128 |
| R1 | G0/1 | 192.168.5.126 | 255.255.255.128 |
| PC3 | NIC | 192.168.5.193 | 255.255.255.240 |
| R2 | G0/0 | 192.168.5.206 | 255.255.255.240 |
| PC4 | NIC | 192.168.5.209 | 255.255.255.240 |
| R2 | G0/1 | 192.168.5.222 | 255.255.255.240 |
| R1 | G0/0/0 | 192.168.5.225 | 255.255.255.252 |
| R2 | G0/0/0 | 192.168.5.226 | 255.255.255.252 |

## Static Routing

### R1
ip route 192.168.5.192 255.255.255.240 192.168.5.226

ip route 192.168.5.208 255.255.255.240 192.168.5.226

### R2
ip route 192.168.5.128 255.255.255.192 192.168.5.225

ip route 192.168.5.0 255.255.255.128 192.168.5.225

