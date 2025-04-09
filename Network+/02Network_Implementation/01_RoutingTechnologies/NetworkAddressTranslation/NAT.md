
---

# 🌐 Network Address Translation (NAT) – CompTIA Network+ (2.1)

### 🧠 Purpose of NAT:
- **NAT modifies IP addresses in real time** to allow devices with **private IP addresses** to access the **public internet**.
- Enables communication despite IPv4 address exhaustion (only ~4.29 billion addresses vs. billions of devices).

---

## 📦 Types of IP Addresses (per **RFC 1918**):
| Address Range              | Use Case             |
|---------------------------|----------------------|
| 10.0.0.0 – 10.255.255.255 | Large enterprise     |
| 172.16.0.0 – 172.31.255.255 | Mid-size networks    |
| 192.168.0.0 – 192.168.255.255 | Home networks        |

> ⚠️ **Private IPs** are **not routable on the internet**.

---

## 🔁 Standard NAT (One-to-One Translation)
**Goal**: Translate a private IP ➝ public IP (and vice versa)

### Example:
- **Vala (Private IP)**: `10.10.20.50`  
- **Public Web Server (Professor Messer)**: `104.20.19.63`  
- **NAT Router translates Vala's IP to**: `94.1.1.1` (public IP)

### Packet Flow:
1. **Outgoing**:
   - Source IP: `10.10.20.50` ➝ translated to `94.1.1.1`
   - Dest IP: `104.20.19.63`
2. **Incoming**:
   - Source IP: `104.20.19.63`
   - Dest IP: `94.1.1.1` ➝ translated back to `10.10.20.50`

---

## 🔄 NAT Overload (PAT – Port Address Translation)
**Goal**: Allow **multiple private IPs** to share a **single public IP**  
→ Accomplished by translating **IP addresses + port numbers**

### How It Works:
- Each internal device gets a unique **port number** mapped to the **same public IP**.
- Translation is stored in a **NAT table** (IP + port ↔ IP + port)

---

### PAT Example:

#### Vala:
- Private: `10.10.20.50:3233`  
- Public: `94.1.1.1:1055`

#### Jonas:
- Private: `10.10.20.70:5782`  
- Public: `94.1.1.1:1056`

> ✅ Both Vala and Jonas use **94.1.1.1** but have **different port numbers**, enabling simultaneous connections.

---

## 📌 Key Terms:
- **NAT**: Network Address Translation
- **PAT**: Port Address Translation / NAT Overload
- **Public IP**: Routable on the internet
- **Private IP**: Non-routable, defined in RFC 1918
- **NAT Table**: Stores private↔public IP and port mappings

---

## 🧩 Summary:
| NAT Type     | Translates        | Use Case                     |
|--------------|-------------------|------------------------------|
| Static NAT   | 1 private ↔ 1 public | One-to-one mapping (rare)     |
| Dynamic NAT  | Many private ↔ pool of public | Limited scale translation |
| PAT (NAT Overload) | Many private ↔ 1 public (diff ports) | Most common method |

---
