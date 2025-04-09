
---

# 🌐 VLANs and Trunking – Network+ (N10-009) – Section 2.2

## 🧱 What is a VLAN?
- **VLAN (Virtual Local Area Network)** = Logically separates a physical switch into multiple broadcast domains.
- Devices in the same VLAN can communicate with each other, but not with devices in other VLANs (without routing).
- VLANs are defined by **numbers** (e.g., VLAN 1, VLAN 100, etc.).

---

## 🔁 Broadcast Domains and Switches
- All devices connected to a switch = same **broadcast domain**.
- Traditional setup: Separate switches for each domain.
- With VLANs: Use **one physical switch** for multiple logical networks.

---

## 🧷 Trunking and 802.1Q
- **Trunk Port**: Carries multiple VLANs between switches using a single connection.
- **802.1Q**: Industry standard for VLAN tagging on Ethernet frames.
- Tag is inserted after the **source MAC address** in the Ethernet frame.
- **12-bit VLAN ID** allows for **4,094 usable VLANs** (out of 4096 total).

### VLAN Tagging:
- Tags added to frames at the **egress** of the source switch.
- Tags removed at the **ingress** of the destination switch.

---

## 📦 Native VLAN
- **Native VLAN**: Untagged VLAN traffic on a trunk link.
- Used for legacy or management traffic that doesn’t support tagging.
- Must match on **both ends** of a trunk or errors will occur.

---

## 🔀 Layer 2 vs. Layer 3 Switching
- **Layer 2 Switch**: Uses MAC addresses (Data Link Layer).
- **Layer 3 Switch**: Adds routing capabilities using IP addresses (Network Layer).
- Enables **inter-VLAN routing** via **SVIs (Switched Virtual Interfaces)**.
- Often used in smaller sites or where simplicity is key.
- Routers still offer **more advanced routing features**.

---

## 📞 Voice and Data VLANs
- Modern enterprise setups use **VoIP phones + computers on the same Ethernet port**.
- One cable, but different VLANs:
  - **Voice VLAN** (e.g., VLAN 200) – For consistent, low-latency communication.
  - **Data VLAN** (e.g., VLAN 100) – For general computer network traffic.
- VoIP phones typically have a built-in switch to connect PCs.
- Switches must support and recognize **voice/data VLAN tagging**.

---

## 🧠 Key Takeaways
- VLANs = separate broadcast domains on the same switch.
- Trunks allow VLAN traffic to pass between switches over one cable.
- **802.1Q** is the tagging standard (not ISL).
- **SVIs** enable routing between VLANs (Layer 3).
- Native VLAN = Untagged traffic; must match on both sides.
- Voice and data can coexist on one cable using VLANs + trunking.

---
