# Day 3: Network Connection Triage

## Overview
Active network connection audit performed to map local outbound traffic to infrastructure owners and identify anomalous remote communications using `netstat -an`.

**Command Execution Snapshot:**

<img width="369" height="59" alt="Screenshot 2026-09-11 182007" src="https://github.com/user-attachments/assets/c1d2ab29-2dfb-462f-99da-cdb3b15ca46b" />


## Network Findings

<img width="395" height="36" alt="Screenshot 2026-09-11 181947" src="https://github.com/user-attachments/assets/94c588b2-449c-464b-ad5a-262e22d1fc69" />

### 1. Telegram IP (`149.154.167.92`)
* **Owner:** Telegram Messenger Inc.
* **Status / Observation:** The application was closed, yet an active connection or background sync process was detected.
* **Analysis:** Modern messaging apps utilize background helper services or persistent keep-alive sockets for push notifications even when the primary UI is closed.

### 2. Microsoft IP (`98.66.133.184`)
* **Owner:** Microsoft Corporation
* **Status / Observation:** Active connection established to Microsoft cloud infrastructure.
* **Analysis:** Standard operating system telemetry, background update checks, or cloud-synced background applications. Expected baseline traffic for a Windows machine.

### 3. DigitalOcean IP (`137.184.135.31`)
* **Owner:** DigitalOcean, LLC (Cloud Hosting Provider)
* **Status / Observation:** Active connection to an external cloud VPS provider.
* **Analysis:** Initially unrecognized. DigitalOcean is a cloud infrastructure provider frequently used for hosting third-party apps, personal development projects, or VPN endpoints.I checked the associated process and confirmed that the connection was
related to a legitimate application/service running on the system.

## Triage Conclusion
The network baseline is consistent with standard application behavior. The presence of DigitalOcean highlights the importance of mapping obscure IP addresses to cloud hosting providers rather than assuming malicious intent immediately.
