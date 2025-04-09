
---

# 🌳 Spanning Tree Protocol (STP) – Network+ N10-009 – 2.2

## 🚨 The Loop Problem
- **Switch loops** occur when there are multiple active paths between switches.
- Ethernet has **no loop prevention at Layer 2**, so:
  - Frames loop endlessly
  - MAC address tables become unstable
  - Network becomes **flooded and unusable**

### Example:
```
Switch A ─── Switch B
   │           │
   └───────────┘ ← Creates a loop!
```

---

## 🛡️ The Solution: Spanning Tree Protocol (STP)
- Prevents loops by **blocking redundant paths**
- Defined in **IEEE 802.1D**
- Automatically **detects loops and disables** one or more ports to eliminate them

### STP Port States:
| State         | Description |
|---------------|-------------|
| **Blocking**  | Port is disabled to prevent loops |
| **Listening** | Clears old MAC table entries, prepares for learning |
| **Learning**  | Learns MAC addresses, no forwarding yet |
| **Forwarding**| Actively forwards traffic |
| **Disabled**  | Admin or error-disabled (not in STP) |

---

## 🌐 Key STP Roles
| Role             | Purpose |
|------------------|---------|
| **Root Bridge**  | Central reference point for all STP calculations |
| **Root Port (RP)** | Port with the **best path to Root Bridge** |
| **Designated Port (DP)** | One per segment, forwards traffic toward Root |
| **Blocked Port** | Does **not forward** to avoid loops |

> ⚠️ Only **one Root Bridge** exists per STP domain.

---

## 🔁 Example Scenario
- Devices on Network A → communicating with Network M via Bridge 6
- Link between them fails
- STP **unblocks** previously blocked port (e.g., on Bridge 11)
- **Reroutes traffic dynamically** without causing a loop

---

## ⚡ Rapid Spanning Tree Protocol (RSTP)
- **IEEE 802.1W**
- Faster convergence: **~6 seconds** (vs. STP’s 30–50 sec)
- Backward compatible with 802.1D
- Same logic as STP but:
  - Faster transitions
  - Adds role like **Alternate Port** and **Backup Port**

---

## 🧠 Summary Table

| Feature                 | STP (802.1D)         | RSTP (802.1W)       |
|-------------------------|----------------------|----------------------|
| Loop Prevention         | ✅ Yes               | ✅ Yes               |
| Convergence Time        | ⏳ 30–50 seconds     | ⚡ ~6 seconds         |
| Port States             | 5 states             | Fewer states (simplified) |
| Backwards Compatible?   | N/A                  | ✅ Yes               |

---

## 💡 Key Terms to Know
- **Bridge**: A switch in STP terminology  
- **Root Bridge**: The "main" switch STP uses as a baseline  
- **Convergence**: Process of recalculating paths after topology change  
- **L2 Redundancy**: What STP manages to ensure fault tolerance without loops  

---
