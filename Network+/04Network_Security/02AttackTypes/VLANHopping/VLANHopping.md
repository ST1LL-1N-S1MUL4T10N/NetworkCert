
---

# 🔄 **VLAN Hopping – CompTIA Network+ N10-009 – Section 4.2**

### 📝 **What is VLAN Hopping?**
**VLANs (Virtual Local Area Networks)** are used to separate different parts of a network, such as separating devices into different VLANs for security and organizational reasons. However, **VLAN hopping** is a security issue where an attacker can gain access to a VLAN they shouldn't have access to, even without a router between VLANs. This can occur through **switch spoofing** or **double tagging**.

---

### 💻 **VLAN Hopping Methods:**

1. **Switch Spoofing**:
   - **Autonegotiation Issue**: Switches can automatically configure an interface to act as a device or another switch. If a switch believes it's connected to another switch, it can establish a trunk connection, allowing VLAN traffic to pass between them.
   - **Attack Scenario**: By "spoofing" a switch, an attacker can trick the network into thinking they are another switch, allowing them to send traffic to any VLAN through the trunk. This allows VLAN hopping without the need for a router.
   - **Prevention**: To avoid this, network administrators should disable **autonegotiation** and manually configure trunk interfaces. Additionally, VLANs should be specifically allowed between switches.

2. **Double Tagging**:
   - **VLAN Tagging**: VLANs use tags in frames to indicate which VLAN the traffic belongs to. In **double tagging**, two VLAN tags are added to a frame.
   - **Attack Scenario**: The first VLAN tag is removed by the first switch, and the second tag is processed by the second switch, allowing the attacker to send traffic to a different VLAN than intended.
   - **Native VLAN Exploitation**: This method relies on the **native VLAN** configuration, which is often set to VLAN 1 by default. By adding a second tag (for a different VLAN) to the frame, an attacker can "hop" to another VLAN.
   - **Prevention**: To defend against double tagging:
     - Change the **native VLAN** to a non-default value.
     - Ensure **tagging** of the native VLAN for all traffic across switches.

---

### 🛡️ **Example of Double Tagging Attack**:
1. **Network Setup**:
   - Attacker is on **VLAN 10 (green)**, and there is a trunk between two switches that supports **VLANs 10 and 20**.
   - The victim device is on **VLAN 20 (red)**.

2. **Attack Process**:
   - The attacker sends a frame with **two VLAN tags**: one for VLAN 10 and another for VLAN 20.
   - **First switch** processes the **VLAN 10 tag** and removes it, forwarding the frame to the second switch.
   - **Second switch** processes the remaining **VLAN 20 tag** and sends the frame to the victim device on **VLAN 20**.

---

### 🔧 **Preventing VLAN Hopping**:
- **Disable autonegotiation** and manually configure **trunk interfaces**.
- **Change the native VLAN ID** to something other than the default (VLAN 1).
- Ensure **proper tagging** of the native VLAN traffic across the trunk links.

---

### 📝 **Key Takeaways**:
- **VLAN Hopping** allows attackers to bypass VLAN separation and gain unauthorized access to other VLANs.
- **Switch Spoofing** and **Double Tagging** are two common methods used for VLAN hopping.
- Proper switch configurations and security measures, like disabling autonegotiation and changing native VLAN settings, can mitigate these attacks.

---
