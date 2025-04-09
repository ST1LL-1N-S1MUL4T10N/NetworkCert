
---

### ✅ **ICMP (Internet Control Message Protocol)**
- Used for diagnostic and error reporting (e.g., `ping` and `traceroute`).
- **Does not use TCP/UDP** – it’s its own Layer 3 protocol.
- Common messages:
  - **Echo request/reply** (ping)
  - **Destination unreachable**
  - **Time exceeded** (TTL expired)

---

### ✅ **GRE (Generic Routing Encapsulation)**
- Used to create **tunnels** for carrying different types of traffic.
- **Encapsulates packets**, but **does not encrypt** them.
- Commonly used with **VPNs** to move data between endpoints.

---

### ✅ **VPN and VPN Concentrators**
- A **VPN (Virtual Private Network)** allows secure communication over untrusted networks like the internet.
- **VPN concentrator**: A dedicated device or software that handles VPN connections (often built into firewalls or routers).
- Used in **site-to-site VPNs** to connect remote locations.

---

### ✅ **IPSec (Internet Protocol Security)**
- Provides **encryption, authentication, and integrity** for VPN traffic.
- Works across devices from different manufacturers.
- Two key IPSec protocols:
  - **AH (Authentication Header)** – Validates the sender, ensures integrity (no encryption).
  - **ESP (Encapsulation Security Payload)** – **Encrypts** data and also provides authentication.

---

### 🔐 **IKE (Internet Key Exchange)**
- Used to **establish Security Associations (SAs)** for IPSec.
- Two phases:
  - **Phase 1**: Establishes ISAKMP (UDP 500), uses **Diffie-Hellman** to share keys.
  - **Phase 2**: Negotiates the encryption method, key sizes, and SAs for secure data transfer.

---

### 🔄 **IPSec Modes**
- **Transport Mode**:
  - Encrypts only the data payload.
  - Leaves original IP header **visible**.
  - Useful for **end-to-end encryption** within a trusted network.
- **Tunnel Mode**:
  - Encrypts **entire original IP packet** (header + data).
  - Adds **new outer IP header**.
  - Commonly used for **site-to-site VPNs** (most secure).

---
