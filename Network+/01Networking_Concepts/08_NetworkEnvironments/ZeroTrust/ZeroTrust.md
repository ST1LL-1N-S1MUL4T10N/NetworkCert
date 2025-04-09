
---

## 🛡️ **Zero Trust – CompTIA Network+ N10-009 (1.8)**

### 🔍 **What Is Zero Trust?**
- **Traditional model:** Trust was granted once someone got past the **perimeter defenses**.
- **Zero Trust model:** **No one** is trusted by default—**not even internal users, devices, or applications**.
- Assumes **breach is inevitable** and constantly verifies access.

> **Core Principle:** *"Never trust, always verify."*

---

### 🧩 **Key Elements of Zero Trust**

| Element                       | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| **Continuous Verification**  | Authentication isn't one-and-done—it’s **ongoing** and contextual.         |
| **Least Privilege Access**   | Users/devices only get the **minimal access** they need.                   |
| **Micro-Segmentation**       | Networks are divided into **smaller zones** to limit lateral movement.     |
| **Policy-Based Access**      | Access decisions based on **identity, device type, location, etc.**       |

---

### 👤 **Adaptive Identity & Authentication**

| Factor                       | Evaluated During Authentication                                             |
|-----------------------------|------------------------------------------------------------------------------|
| **User identity**           | Who is this? How long have they been with the company?                     |
| **Device trust**            | Is this a **known device** (e.g. corporate laptop with a valid cert)?       |
| **Geolocation/IP**          | Are they connecting from a **recognized region** or suspicious location?    |
| **Time of access**          | Unusual login times might trigger extra verification.                      |
| **Network/Connection type** | Public Wi-Fi? VPN? Secure corporate LAN?                                    |

> 📌 *Risky logins (e.g., unknown IP or device) may trigger Multi-Factor Authentication (MFA), or even a denial.*

---

### 🔐 **Least Privilege**

- Users should **only** have access necessary for their job function.
- **Avoid giving admin rights** unless absolutely needed.
- Reduces damage from **malware, data breaches, insider threats**.

> ✅ Example: A Help Desk tech may view records but not modify them. A manager might have edit rights.

---

### 🌍 **Challenges in a Modern Network**

- Users are **everywhere**: home, office, field, etc.
- Applications live **everywhere**: on-premises, in the cloud, SaaS, etc.
- **Need a secure, scalable solution** that works across all locations and devices.

---

### ☁️ **SASE – Secure Access Service Edge**

| Component                     | What It Does                                                               |
|------------------------------|-----------------------------------------------------------------------------|
| **SASE (pronounced “sassy”)**| Moves security services to the cloud **near the application**.             |
| **SASE client**              | Installed on user devices; **automatically** connects to secure resources. |
| **Integrated security**      | Zero trust network access (ZTNA), firewall-as-a-service, DNS security, etc.|
| **Network as a Service**     | Adds routing, QoS, and optimization features.                              |

> 💡 Think of SASE as a **modern VPN**, but smarter, cloud-native, and way more integrated.

---

### 📈 **Why Zero Trust Matters**
- Prevents **lateral movement** of attackers inside the network.
- Protects **sensitive data**, even if someone’s inside your network perimeter.
- Reduces **attack surface**, improves **visibility**, and **centralizes control**.

---

### 🧠 Exam Tip:
> **Zero Trust = verify every time + enforce least privilege.**  
> Pair this with **SASE** for cloud-era security across remote users and distributed apps.

---
