# Network Traffic Analysis: HTTP Plain-Text Interception with Wireshark

## 1. Overview

* **Objective:** Demonstrate how unencrypted HTTP traffic transmits data in clear text and how network monitoring tools like Wireshark can intercept and read it.
* **Attacker / Analyzer:** Kali Linux (Wireshark)
* **Target / Environment:** Controlled local test server (`192.168.56.102:8000` or lab server)
* **Core Takeaway:** Encryption matters. Protocols lacking SSL/TLS expose sensitive parameters, headers, and credentials to anyone on the same network segment.

---

## 2. Lab Setup & Interface Selection

Before capturing traffic, Wireshark must be configured to listen on the correct network interface tied to the lab environment.

* **Action:** Open Wireshark with proper privileges and select the active network interface (such as `eth1` or your host-only adapter).

<img width="1545" height="877" alt="image" src="https://github.com/user-attachments/assets/b549d704-82c2-4967-a2d1-510bc0d8ce07" />

---

## 3. Generating Unencrypted Traffic

To analyze network behavior, a simple client-to-server interaction must take place over standard, unencrypted HTTP rather than HTTPS.

<img width="921" height="203" alt="Screenshot 2026-09-12 205255" src="https://github.com/user-attachments/assets/6b1b8244-15fa-454c-acd4-66a8db2bd71f" />

  
<img width="1350" height="673" alt="image" src="https://github.com/user-attachments/assets/ea3c0deb-a708-4a47-a7c5-6b0374889725" />


---

## 4. Live Packet Capture

Once traffic starts flowing, Wireshark logs every raw packet passing across the selected interface, capturing background network noise alongside your target traffic.


<img width="1911" height="805" alt="image" src="https://github.com/user-attachments/assets/ecbac427-67b0-4cbe-90d3-6360dd8df8f0" />

---

## 5. Filtering for HTTP Traffic

A raw capture contains extensive background traffic (like ARP, DNS, and TCP handshakes). Filtering isolates only the relevant protocol data.


<img width="1909" height="439" alt="image" src="https://github.com/user-attachments/assets/da1cbc57-b524-4d62-a7bc-768a157ec1cd" />


---

## 6. Stream Analysis & Findings (Proof of Concept)

The ultimate test of clear-text vulnerability is reassembling individual packets into a readable conversation stream.


<img width="1276" height="826" alt="image" src="https://github.com/user-attachments/assets/9382b5d2-8cc8-4512-95df-8e4010171a18" />


### What This Proves:

* **Client Request (Red):** Exposes browser metadata, user agents (`Mozilla/5.0`), and requested URIs in plain text.
* **Server Response (Blue):** Exposes backend server details (`Python/3.13.12`) and payload data without cryptographic protection.
* **The Risk:** Any observer situated along the transit path can read form inputs, cookies, or basic credentials instantly.

---

## 7. Remediation & Key Takeaways

* **Deploy TLS/SSL:** Always enforce HTTPS for web applications to wrap transport streams in encryption.
* **Avoid Clear-Text Protocols:** Legacy protocols like HTTP, Telnet, and FTP should be replaced with modern encrypted equivalents (HTTPS, SSH, SFTP).
* **Network Visibility:** For security analysts (SOC), understanding how easily clear-text traffic is read underscores why zero-trust segmentation and encrypted internal traffic policies are critical.
