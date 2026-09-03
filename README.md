# Offensive Security & Lab Infrastructure

Welcome to my cybersecurity documentation repository. This repository logs my hands-on experience, lab architectures, network fundamentals, and offensive security exercises.

##  Current Lab Setup

- **Hypervisor:** Oracle VM VirtualBox
- **Attacker Machine:** Kali Linux (64-bit)
- **Target Machine:** Metasploitable 2 (Linux)
- **Network Configuration:** Isolated Host-Only Adapter (Subnet: `192.168.56.0/24`)

### Network Architecture & Verification
To ensure lab safety, Metasploitable 2 is isolated from the physical home network. Communication between the attacker and target was verified via ICMP ping:

- **Target IP:** `192.168.56.101`
- **Verification Command:** `ping -c 4 192.168.56.101` (0% packet lo
<img width="1920" height="892" alt="image" src="https://github.com/user-attachments/assets/120fa546-16b7-445e-bbfd-1b6e6126159e" />


##  Core Networking Concepts Learned
- **Full-Duplex vs. Half-Duplex:** Bidirectional data flow vs. single-direction collision domain limitations.
- **CSMA/CD:** Carrier Sense Multiple Access with Collision Detection handling media contention.
- **Network Isolation:** Isolating vulnerable targets on dedicated virtual interfaces to prevent external exposure.<img width="447" 
