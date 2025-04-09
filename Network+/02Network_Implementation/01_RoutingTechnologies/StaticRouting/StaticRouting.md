
---

# 📘 CompTIA Network+ (N10-009) - Static Routing Cheat Sheet  
**Topic 2.1 – Routing Concepts**  
**Source:** Professor Messer – Static Routing

---

## 🔄 What is Static Routing?
**Static routing** is a method where routes are manually configured by a network administrator rather than dynamically discovered.

---

## 🧠 How Routing Works (Basic Steps)
1. **Router receives a packet**
2. **Examines the destination IP address**
3. **Checks its routing table:**
   - If the destination is on a directly connected subnet → send it there
   - If not → look for a **next hop** (another router to forward it to)
   - If no route is found → **drop the packet**

---

## 🗺️ Routing Table Types
- **Directly Connected Routes** – Subnets physically connected to the router’s interfaces.
- **Static Routes** – Manually entered by an admin.
- **Dynamic Routes** – Learned through routing protocols (covered separately).

---

## 🧰 Static Routing Overview
| 🔹 Feature             | 🔍 Description                                       |
|-----------------------|------------------------------------------------------|
| **Manual config**     | Admin types in routes manually                      |
| **Low overhead**      | No CPU/memory used for route calculation            |
| **Predictable**       | No changes unless you make them                     |
| **Stable & secure**   | No dynamic updates from unknown sources             |
| **Best for**          | Small/stub networks, simple topologies              |
| **Not ideal for**     | Large, complex, or frequently changing networks     |

---

## ⚠️ Static Routing – Gotchas
- **No automatic rerouting** if a link fails
- **Manual updates** required if network changes
- **Scaling issues** in large environments
- **Risk of routing loops** due to misconfiguration

---

## 🧪 Example Scenario
**Router 1 Connections:**
- 10.10.10.0/24 (LAN)
- 10.10.40.0/24 (link to Router 2)
- 10.10.50.0/24 (link to Router 3)

**Other Subnets:**
- 10.10.20.0/24 (behind Router 2)
- 10.10.30.0/24 (behind Router 3)

**Problem:**  
Router 1 doesn’t know about 10.10.20.0 or 10.10.30.0 — it will drop traffic for them unless we add static routes.

---

## 🛠️ Static Route Configuration Example
On Router 1 (pseudo-Cisco syntax):
```bash
ip route 10.10.20.0 255.255.255.0 10.10.40.2
ip route 10.10.30.0 255.255.255.0 10.10.50.2
```
- Sends packets for 10.10.20.0/24 to **Router 2** (10.10.40.2)
- Sends packets for 10.10.30.0/24 to **Router 3** (10.10.50.2)

---

## 🧩 Stub Network
A **stub network** is a single-homed network (only one path in or out).  
Perfect use case for static routing.

---

## 📌 Summary
- Static routes are **manual**, **reliable**, and **low-overhead**.
- Great for small networks and **stub sites**.
- Require **manual maintenance** and don't adapt to **topology changes**.
- Be careful to avoid misconfigurations and **routing loops**.

---
