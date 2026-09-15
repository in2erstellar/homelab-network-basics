# Homelab Network Basics

## Objective
Basic network topology using pfSense firewall and VirtualBox internal networks.

## IP Schema Matrix

| Component | Interface / Role | IP Address / Configuration |
| :--- | :--- | :--- |
| **pfSense** | WAN | DHCP (Bridged / NAT from Host) |
| **pfSense** | LAN | 192.168.1.1 / 24 |
| **Client VM (Ubuntu)** | Network Interface | DHCP (Assigned 192.168.1.x) |

## Implemented Tasks
- Configured virtual lab environment with pfSense and Ubuntu Client.
- Set up internal network routing and DHCP on pfSense.
- Configured strict Firewall rules on the LAN interface to block specific ICMP traffic to `8.8.8.8` while keeping other external traffic (`1.1.1.1`) allowed, demonstrating rule hierarchy.
- Verified rule execution using `ping` and reviewed dropped packets in pfSense Firewall logs.
