
---

# 🛑 **MAC Flooding – CompTIA Network+ N10-009 – Section 4.2**

### 📝 **What is a MAC Address?**
- **MAC (Media Access Control) Address**: A unique hardware identifier assigned to network interfaces, used to direct network traffic.
- **Format**: 48 bits long, displayed in hexadecimal (e.g., `00:14:22:01:23:45`).
  - **OUI (Organizationally Unique Identifier)**: The first 3 bytes identifying the manufacturer.
  - **NIC-specific value**: The last 3 bytes, acting as the serial number of the device.

---

### 🖧 **Switch Operation with MAC Addresses**
- Switches build a **MAC address table** to efficiently direct traffic between devices. The table stores **source MAC addresses** and maps them to switch interfaces (ports).
- **Learning Process**: Switches learn MAC addresses from incoming traffic and record which interface it came from.
  
---

### 🌀 **What Happens During MAC Flooding?**
- **MAC Address Table**: Switches store a limited number of MAC addresses. Once the table is full, the switch will flood traffic to all ports (like a hub).
- **MAC Flooding Attack**: 
  - **Attackers** send many frames with random, forged source MAC addresses, filling up the table.
  - Once the table is full, the switch can no longer make specific forwarding decisions and floods all traffic to all ports.
  - **Result**: The switch becomes like a **hub**, sending data to all devices on the network. This allows attackers to intercept data not originally intended for them.

---

### 🔐 **How to Defend Against MAC Flooding**
- **Port Security**: Modern switches offer **port security** features to limit the number of MAC addresses learned on each port.
- **Limiting the Table Size**: With security settings in place, switches become much harder to flood, thus protecting the network from becoming vulnerable to attacks.

---

### 🛡️ **Key Takeaways**
- **MAC Flooding** turns a switch into a hub, allowing attackers to intercept all traffic on the network.
- It's a **denial of service** type of attack, relying on overloading the MAC address table.
- **Port security** is crucial in preventing or mitigating this attack, as it limits the number of addresses that can be learned per port.

---
