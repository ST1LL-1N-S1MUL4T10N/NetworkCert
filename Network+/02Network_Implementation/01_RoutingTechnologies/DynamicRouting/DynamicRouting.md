
---

# 📘 CompTIA Network+ (N10-009) – Dynamic Routing Cheat Sheet  
**Topic 2.1 – Routing Concepts**  
**Source:** Professor Messer – Dynamic Routing

---

## 🔄 What is Dynamic Routing?
**Dynamic Routing** uses routing protocols to automatically build and maintain routing tables. Routers share information about reachable networks with each other—no manual updates required.

---

## ✅ Advantages of Dynamic Routing
| 🔹 Feature                  | 🔍 Description                                                     |
|----------------------------|---------------------------------------------------------------------|
| **Automatic Updates**      | Routers share route info dynamically (add/remove routers = auto update) |
| **Scalability**            | Handles large and complex networks better than static routing      |
| **Adaptability**           | Automatically responds to network changes (failures, new links)    |
| **Reduced Admin Overhead** | No need to manually SSH into routers to make changes               |

---

## ⚠️ Considerations / Disadvantages
- **Consumes CPU & RAM**
- **Initial configuration required**
- **More complex to troubleshoot**
- **Routing loops must be managed by the protocol**

---

## 🔧 How Dynamic Routing Works
1. **Routers advertise routes** to neighbors (often via multicast).
2. **Routers receive updates** and adjust their own routing tables.
3. **Routing decisions** are based on protocol-specific metrics (hop count, link state, etc.).
4. **Changes propagate** automatically through the network.

---

## 🧪 Example Scenario
Router 1 learns about:
- `10.10.20.0/24` via **EIGRP** update from Router 2 → next hop: `10.10.40.2`
- `10.10.30.0/24` via **EIGRP** update from Router 3 → next hop: `10.10.50.2`

This happens **automatically** without manual config.

---

## 📚 Common Dynamic Routing Protocols

### 🔷 EIGRP (Enhanced Interior Gateway Routing Protocol)
- **Type:** Advanced distance-vector
- **Vendor:** Cisco-centric (some support on other platforms)
- **Pros:**
  - Fast convergence
  - Loop prevention
  - Efficient updates (minimal traffic)
  - Easy to configure on Cisco gear
- **Best for:** Cisco-heavy environments

---

### 🔶 OSPF (Open Shortest Path First)
- **Type:** Link-state
- **Vendor Neutral:** Open standard (available across vendors)
- **Works in:** A single **Autonomous System (AS)**
- **Uses cost metric** based on bandwidth, delay, link state
- **Supports load balancing** if costs are equal
- **Pros:**
  - Fast convergence
  - Scalable
  - Well-documented

---

### 🌐 BGP (Border Gateway Protocol)
- **Type:** Path-vector
- **Used for:** Routing between **Autonomous Systems (AS)** (e.g. between ISPs)
- **Best for:** Internet/WAN routing
- **Highly scalable**
- **Slow convergence**, but extremely powerful and flexible
- **Fun Fact:** Known as the "three-napkins protocol" (original design sketched on napkins)

---

## 🧠 Metrics Used by Protocols
| Protocol | Metric Type             |
|----------|--------------------------|
| RIP      | Hop count                |
| OSPF     | Cost (based on bandwidth/delay) |
| EIGRP    | Composite (bandwidth, delay, reliability, load) |
| BGP      | Path attributes (AS path, etc.) |

---

## 📌 Summary
- **Dynamic Routing = Auto-updating, scalable routing**
- Choose protocol based on:
  - **Network size**
  - **Vendor environment**
  - **Convergence needs**
  - **Inter-vendor compatibility**
- Know your protocols: **EIGRP, OSPF, BGP**

---
