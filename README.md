# Cisco-SOHO-Network-Design
Cisco Packet Tracer project showcasing the design and implementation of a routed SOHO network for a small business with Admin, Sales, and HR departments.
# Building a SOHO Network for DataBridge Innovations

A practical Cisco Packet Tracer networking project focused on designing and configuring a Small Office/Home Office (SOHO) network infrastructure for a small business environment.

## Project Overview

This project simulates a real-world business scenario where a company named **DataBridge Innovations** requires a structured internal network to support communication across three departments:

- Admin Department
- Sales Department
- HR Department

The network was designed and implemented using Cisco Packet Tracer with the goal of enabling secure and reliable communication between all departments through proper IP addressing, routing, and connectivity testing.

---

## Objectives

The primary objectives of this project were to:

- Design a functional LAN topology
- Configure routers, switches, PCs, and a server
- Implement structured IP addressing
- Enable inter-department communication
- Test and troubleshoot network connectivity
- Gain hands-on experience with Cisco Packet Tracer

---

## Network Structure

| Department | Network/Subnet | Devices |
|---|---|---|
| Admin | 192.168.10.0/24 | 2 PCs & 1 Server |
| Sales | 192.168.20.0/24 | 2 PCs |
| HR | 192.168.30.0/24 | 2 PCs |

### Devices Used

- Cisco 2911 Router
- Cisco 2960 Switches
- PCs
- Server
- Copper Straight-Through Cables

---

## Skills Demonstrated

- Network Topology Design
- IPv4 Addressing & Subnetting
- Router Configuration
- Switch Configuration
- Interface Configuration
- Inter-network Routing
- Connectivity Testing
- Basic Network Troubleshooting
- Cisco Packet Tracer Simulation

---

## Network Topology

<img width="1536" height="647" alt="image" src="https://github.com/user-attachments/assets/15b7f7dc-f016-46c7-a739-d4ee36c3f532" />


---

## IP Addressing Scheme

| Device | IP Address | Default Gateway |
|---|---|---|
| Admin PC 1 | 192.168.10.10 | 192.168.10.1 |
| Admin PC 2 | 192.168.10.11 | 192.168.10.1 |
| Admin Server | 192.168.10.100 | 192.168.10.1 |
| Sales PC 1 | 192.168.20.10 | 192.168.20.1 |
| Sales PC 2 | 192.168.20.11 | 192.168.20.1 |
| HR PC 1 | 192.168.30.10 | 192.168.30.1 |
| HR PC 2 | 192.168.30.11 | 192.168.30.1 |

---

## 🔧 Router Configuration

Example router interface configuration:

```bash
# Enter privileged EXEC mode
enable
# Enter global configuration mode
configure terminal
# Set hostname
hostname databridge
# Assign IP address to interface
interface GigabitEthernet0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
exit
# Configure the second interface
interface GigabitEthernet0/1
ip address 192.168.20.1 255.255.255.0
no shutdown
exit
# Configure the third interface
interface GigabitEthernet0/2
ip address 192.168.30.1 255.255.255.0
no shutdown
exit
end

# Verify interfaces:
show ip interface brief

# Configure the 1st DHCP interface
configure terminal
interface GigabitEthernet0/1
ip helper-address 192.168.10.2
exit
# Configure the 2nd DHCP interface
interface GigabitEthernet0/2
ip helper-address 192.168.10.2
exit
end

```

---

## Connectivity Testing

Connectivity between departments was verified successfully using:

- `ping`
- ARP resolution
- End-to-end communication tests

### Example Test Results

- Admin ↔ Sales communication successful
- Admin ↔ HR communication successful
- Sales ↔ HR communication successful
- 0% packet loss after ARP resolution

> Insert ping result screenshots here
><img width="492" height="272" alt="image" src="https://github.com/user-attachments/assets/5e9e3c56-9bf0-4640-9f6c-6aa0050e1b69" />

> <img width="517" height="246" alt="image" src="https://github.com/user-attachments/assets/6c1fab46-6632-4d92-8797-0bd31a6f2d24" />

> <img width="522" height="261" alt="image" src="https://github.com/user-attachments/assets/fb622570-4241-44d4-a68e-aaa3ca50686a" />

<img width="547" height="282" alt="image" src="https://github.com/user-attachments/assets/967abc32-94f1-4bbe-9e27-6fdb510808cc" />

```md

```

---

## 📈 Project Outcomes

At the completion of this project, the following outcomes were achieved:

- Successful implementation of a routed SOHO network
- Reliable communication between departments
- Proper network segmentation using different subnets
- Improved understanding of routing and IP addressing
- Practical troubleshooting experience using Cisco Packet Tracer

---

## Future Improvements

Potential enhancements for this network include:

- VLAN implementation
- DHCP server configuration
- DNS configuration
- Access Control Lists (ACLs)
- Network security hardening
- Wireless connectivity
- Redundancy and scalability improvements

---

## Tools & Technologies

- Cisco Packet Tracer
- IPv4 Networking
- Cisco IOS CLI
- LAN Switching
- Routing Fundamentals

```
---

## 📚 Learning Outcome

This project provided practical exposure to designing and configuring a basic enterprise-style network. It strengthened my understanding of IP addressing, router configuration, network troubleshooting, and inter-network communication within a simulated environment.

---

