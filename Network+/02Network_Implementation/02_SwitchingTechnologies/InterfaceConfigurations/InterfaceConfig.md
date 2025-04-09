
---

# 🖧 Interface Configurations – Network+ (N10-009) – Section 2.2

## ⚙️ Ethernet Interface Basics
### 🔹 Speed
- Common: **10 Mbps**, **100 Mbps**, **1 Gbps**, **10 Gbps**+
- Must **match on both ends** (e.g. PC & switch)
- Usually **auto-negotiated**

### 🔹 Duplex
- **Half Duplex**: One direction at a time  
- **Full Duplex**: Send and receive simultaneously  
- Must **match on both sides**
  - Mismatch = Poor performance (e.g. collisions, retransmits)

### Troubleshooting Tip:
- **No Link Light** → Speed mismatch  
- **Poor Performance** → Duplex mismatch

---

## 🌐 IP Configuration
- Must be set correctly for communication to work:
  - **IP Address**
  - **Subnet Mask**
  - **Default Gateway**
  - **DNS**
- Errors in config can cause **no connectivity** or **limited access**

---

## 🔗 Link Aggregation (Port Bonding)
- Combines multiple interfaces into **one logical link**
- Increases bandwidth (e.g., 4 x 1 Gbps = 4 Gbps)
- Prevents loops when **properly configured**
- Also called:
  - **LAG** (Link Aggregation Group)
  - **EtherChannel** (Cisco term)

### 🔸 LACP – Link Aggregation Control Protocol
- **IEEE 802.3ad**
- Auto-negotiates link aggregation setup
- Sends LACP packets between devices

---

## 📦 MTU – Maximum Transmission Unit
- **Default MTU**: 1500 bytes (standard Ethernet frame)
- If packet > MTU → Fragmentation
  - Causes **inefficiency**, retransmission if fragments lost
- Can be set **manually** if auto-detection fails (due to firewalls, filters)

---

## 🧱 Jumbo Frames
- Increases MTU up to **9,216 bytes**
  - Common setting: **9,000 bytes**
- Advantage: Fewer frames = more efficient data transfer
  - 1 jumbo frame ≈ 6 standard frames

### ⚠️ Requirements:
- All network devices **must support jumbo frames**
  - Switches, routers, endpoints
- If any device doesn’t → frame gets **dropped**

---

## 🧠 Quick Summary
| Feature               | Notes                                                                 |
|----------------------|-----------------------------------------------------------------------|
| **Speed**            | Match on both ends (auto preferred)                                   |
| **Duplex**           | Full recommended; mismatch causes poor performance                    |
| **IP Config**        | Must match assigned network settings                                  |
| **Link Aggregation** | Combines ports for higher throughput; uses LACP for auto setup        |
| **MTU**              | Max size before fragmentation (1500 bytes default)                    |
| **Jumbo Frames**     | Up to ~9000 bytes; more efficient but needs end-to-end support        |

---
