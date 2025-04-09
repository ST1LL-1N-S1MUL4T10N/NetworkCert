
---

## 🧭 Routing Technologies – CompTIA Network+ N10-009 (2.1)  
**Key Topics**: Routing Tables, Route Selection, Administrative Distance, Metrics, FHRP, Subinterfaces

---

### 📘 Routing Table Basics
- A **routing table** contains paths to different networks.
- All network devices (workstations, servers, routers) maintain a routing table.
- **Routers** use this table to decide how to forward packets to their destination.

---

### 🧾 Routing Table Components
Each route entry contains:
- **Code**: Indicates source (e.g., `C` = Connected, `R` = RIP, `D` = EIGRP).
- **Destination Network**: Subnet (e.g., `10.0.30.0/24`).
- **Administrative Distance / Metric**: e.g., `120/1`
- **Next Hop IP**: Where to send packet (e.g., `via 10.10.50.2`)
- **Uptime**: How long the route has been known (e.g., `00:00:14`)
- **Outgoing Interface**: Which router interface to use (e.g., `Serial0/3/1`)

---

### 🧠 Route Selection Logic
1. **Longest Prefix Match Wins**:
   - /32 > /24 > /16 → More specific prefix is preferred.
   - Example:
     - Match IP: `192.168.1.6`
     - Routes:
       - `/32`: Most specific (exact match)
       - `/24`: More specific than `/16`
2. **If same prefix**: Choose based on **Administrative Distance**
3. **If same AD**: Choose based on **Routing Metric**

---

### 🪪 Administrative Distance (AD)
- Used to choose between **identical routes** from different sources.
- Lower AD = more preferred.
  
| Source                     | AD Value |
|---------------------------|----------|
| Directly Connected        | 0        |
| Static Route              | 1        |
| EIGRP                     | 90       |
| OSPF                      | 110      |
| RIP (v1/v2)               | 120      |
| External BGP              | 20       |
| Internal BGP              | 200      |

---

### 📊 Routing Metrics
- Internal values used **within routing protocols** to select best path.
- Not comparable **across protocols**.
  
**Examples:**
- **RIP**: Hop count (fewer = better)
- **EIGRP**: Bandwidth, delay, load, reliability
- **OSPF**: Cost (based on bandwidth)
- **BGP**: Path attributes, preference, etc.

---

### 🔁 FHRP (First Hop Redundancy Protocol)
**Problem**: Only 1 default gateway can be configured on a host  
**Solution**: Use a **Virtual IP (VIP)** shared between routers

- **Primary Router** = Active router associated with VIP
- **Backup Router** = Takes over VIP if primary fails
- **Protocols**: HSRP, VRRP, GLBP (examples of FHRP)
- **Failover is seamless** to the end-user

---

### 🔀 Subinterfaces
- Allows multiple **virtual interfaces** on a **single physical interface**
- Commonly used for **router-on-a-stick** inter-VLAN routing.

**Format**:  
`InterfaceName.SubinterfaceID`  
e.g. `GigabitEthernet0/0.10`, `0/0.20`, etc.

Each subinterface:
- Assigned to a specific **VLAN**
- Gets its own **IP address** and **subnet**
- Treated like a separate interface for routing

---

### 🧪 Example Scenario
**Three VLANs** (Red, Green, Blue) connected via one trunk to router:  
- Trunk link connects switch to router
- Router configures:
  - `G0/0.1` → VLAN 10 → IP/Subnet A
  - `G0/0.2` → VLAN 20 → IP/Subnet B
  - `G0/0.3` → VLAN 30 → IP/Subnet C

---
