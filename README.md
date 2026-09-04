# Introduction to the Computer Networking

Welcome to my cybersecurity documentation repository. This repository logs my hands-on experience, lab architectures, network fundamentals, and offensive security exercises.

##  Current Lab Setup

- **Hypervisor:** Oracle VM VirtualBox
- **Attacker Machine:** Kali Linux (64-bit)
- **Target Machine:** Metasploitable 2 (Linux)
- **Network Configuration:** Isolated Host-Only Adapter (Subnet: `192.168.56.0/24`)

### Network Architecture & Verification
To ensure lab safety, Metasploitable 2 is isolated from the physical home network. Communication between the attacker and target was verified via ICMP ping:

- **Target IP:** `192.168.56.101`
- **Verification Command:** `ping -c 4 192.168.56.101` (0% packet lost)
<img width="1920" height="892" alt="image" src="https://github.com/user-attachments/assets/120fa546-16b7-445e-bbfd-1b6e6126159e" />


##  Core Networking Concepts Learned
- **Full-Duplex vs. Half-Duplex:** Bidirectional data flow vs. single-direction collision domain limitations.
- **CSMA/CD:** Carrier Sense Multiple Access with Collision Detection handling media contention.
- **Network Isolation:** Isolating vulnerable targets on dedicated virtual interfaces to prevent external exposure. 


# Network Fundamentals: Core IP Concepts

A quick summary of IP addressing, subnet concepts, and IPv6 features.

---

## 1. IPv4 Structure & Classes

IPv4 uses 32-bit addresses split into 4 octets (e.g., `192.168.1.1`).

* **Class A (`1–126`):** Very large networks.
* **Class B (`128–191`):** Medium-sized networks.
* **Class C (`192–223`):** Small local networks.
* **Class D (`224–239`):** Reserved for Multicast.
* **Class E (`240–255`):** Reserved for Research.

---

## 2. Public vs. Private IPs & NAT

* **Private IP:** Internal address used inside a local network (e.g., `192.168.x.x` or `10.x.x.x`).
* **Public IP:** External address assigned by your ISP to your router; visible to the internet.
* **NAT:** Translates multiple private IPs into one single public IP so your entire home shares one internet connection.

<img width="1920" height="891" alt="VirtualBox_kali-linux-2026 2-virtualbox-amd64_04_09_2026_23_21_04" src="https://github.com/user-attachments/assets/670a014c-c6d9-42f8-8fa3-a5eed656e992" />

*Output of `ifconfig` on Kali Linux showing active interfaces: NAT internet connection (`eth0`), host-only lab network (`eth1`), and internal loopback (`lo`).*

---

## 3. Static vs. Dynamic IPs

* **Dynamic IP:** Automatically assigned by the router (via DHCP); changes over time. Default for home devices.
* **Static IP:** Manually configured and permanent. Used for servers and lab targets so their address never changes.

---

## 4. IPv6 Key Features

* **128-Bit Address:** Solves the IPv4 address shortage using hexadecimal format.
* **Faster Routing:** Simplified, fixed-size headers allow routers to forward traffic faster.
* **Built-in Security:** Includes integrated IPSec by default.
* **Flexible Setup:** Supports both Stateful (DHCPv6) and Stateless (SLAAC) autoconfiguration.
