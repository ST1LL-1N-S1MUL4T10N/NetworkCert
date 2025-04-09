
---

## 🧠 IPv4 Subnet & Host Calculations – Cheat Sheet  
**CompTIA Network+ (N10-009) – Section 1.7**  
*Topic: Variable Length Subnet Masks (VLSM) & IP Calculations*

---

### 🔧 Why Subnet?
- **Routers** connect smaller networks to route traffic efficiently.
- Subnetting breaks a large network into **smaller, manageable networks**.
- **VLSM** (Variable Length Subnet Masking) allows flexibility in defining subnet sizes per need.

---

### 📐 VLSM Basics
- You can **"borrow" bits** from the host portion of an address to create more subnets.
- More subnet bits = **More subnets, fewer hosts**
- Fewer subnet bits = **Fewer subnets, more hosts**

---

### 📊 Subnet & Host Formulas

| What            | Formula                                |
|-----------------|-----------------------------------------|
| **# of Subnets**| `2^n` ← where **n** = # of **borrowed subnet bits** |
| **Hosts/Subnet**| `2^h - 2` ← where **h** = # of **host bits**<br>(minus 2 for Network + Broadcast) |

---

### ⚡ Powers of 2 (Quick Reference)

| Power | Value |
|-------|-------|
| 2^1   | 2     |
| 2^2   | 4     |
| 2^3   | 8     |
| 2^4   | 16    |
| 2^5   | 32    |
| 2^6   | 64    |
| 2^7   | 128   |
| 2^8   | 256   |
| 2^9   | 512   |
| 2^10  | 1024  |
| 2^11  | 2048  |
| 2^12  | 4096  |
| ...   | ...   |

---

### 📌 Examples

#### 1️⃣ `10.1.1.0/24`
- Class A default: `/8`, but we're using `/24`
- **Borrowed Subnet Bits:** 16 (`24 - 8`)
- **Remaining Host Bits:** 8

🧮
- Subnets: `2^16 = 65,536`  
- Hosts/Subnet: `2^8 - 2 = 254`

---

#### 2️⃣ `192.168.11.0/26`
- Class C default: `/24`
- **Borrowed Bits:** 2 (`26 - 24`)
- **Host Bits:** 6

🧮
- Subnets: `2^2 = 4`  
- Hosts/Subnet: `2^6 - 2 = 62`

---

#### 3️⃣ `172.16.55.0/21`
- Class B default: `/16`
- **Borrowed Bits:** 5 (`21 - 16`)
- **Host Bits:** 11

🧮
- Subnets: `2^5 = 32`  
- Hosts/Subnet: `2^11 - 2 = 2046`

---

### 🎯 Key Takeaways
- **Use the class of the IP** to determine default subnet mask:
  - Class A → /8
  - Class B → /16
  - Class C → /24
- **Borrow bits** from the host portion to increase subnet count.
- **Subtract 2 hosts** per subnet for network + broadcast addresses.

---

### 🧭 Analogy: Subnetting is like slicing a pizza 🍕

- You start with a full pizza (a full network).
- Slice it depending on how many groups (subnets) you need.
- Each slice has only so many bites (hosts).
- You control the slice size with **subnet masks**.

---
