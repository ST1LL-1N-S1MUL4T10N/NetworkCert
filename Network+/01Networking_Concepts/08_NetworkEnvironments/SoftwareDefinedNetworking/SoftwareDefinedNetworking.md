
---

## 🧠 **Software Defined Networking (SDN) – Network+ N10-009 (1.8)**

### 🔧 **What is SDN?**
- A **network architecture** approach that **separates the control plane from the data plane**.
- Moves traditional hardware-based network functions into **software-based, virtualized functions**.

---

### 🧩 **Three Planes of SDN:**

| Plane             | Function                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Data Plane** (Infrastructure Layer) | Responsible for **forwarding traffic** (e.g., routing, switching, NAT, encryption). This is the **"heavy lifting"** part of the device. |
| **Control Plane** | Decides **how** traffic is forwarded. Includes **routing tables**, **NAT rules**, **switching logic**, etc. |
| **Management Plane** | Used to **configure/manage** devices (e.g., SSH, web GUI, API access). Controlled by the network admin. |

---

### 🧱 **Virtualizing Network Functions**
- Traditional devices (routers, switches, firewalls) are broken down into software-based components.
- Allows network infrastructure to be **virtualized, scalable, and dynamic**.
- Enables **centralized control**, **faster changes**, and **automation**.

---

## 🌐 **SD-WAN (Software Defined – Wide Area Network)**

### 📦 **Why SD-WAN?**
- Traditional WANs connected remote sites to a central data center.
- Now, services are in **the cloud**, across **multiple providers/locations**.
- SD-WAN handles **cloud-first environments** by being **application-aware** and **transport agnostic**.

---

### 🔑 **Key SD-WAN Features:**

| Feature                      | Description                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------|
| **Application-Aware Routing** | Knows what app is in use (e.g., email, video, DB) and routes traffic to the **nearest or most efficient** path. |
| **Zero-Touch Provisioning** | Devices auto-configure themselves with **no manual intervention**, even when services move. |
| **Transport Agnostic**       | Works across **any connection type** (fiber, 5G, DSL, etc.).                                |
| **Centralized Policy Control** | Policies are configured once and **pushed to all SD-WAN routers** centrally.               |

---

### 📍 **Old vs. New WAN**

| Traditional WAN                         | SD-WAN                                                |
|----------------------------------------|-------------------------------------------------------|
| All traffic routed to central data center | Cloud traffic sent directly to **cloud-based apps**    |
| Static, hardware-based config          | Dynamic, software-defined, **automated provisioning** |
| Manual config on each router           | **Centralized policy management**                     |

---

### 🧠 Real-World Benefit:
> If a user at a remote site needs access to email (now hosted in the cloud), SD-WAN intelligently routes them directly to that email service—no need to backhaul traffic through a central data center.

---
