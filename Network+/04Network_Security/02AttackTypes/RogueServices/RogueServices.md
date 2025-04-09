
---

# 🛡️ **Rogue Services – CompTIA Network+ N10-009 – Section 4.2**

### 🚨 **What Are Rogue Services?**
- **Rogue services** are unauthorized devices or services on the network that can lead to security vulnerabilities.
  
  Examples:
  - **Rogue DHCP Server**: A device that pretends to be a legitimate DHCP server and hands out incorrect IP addresses.
  - **Rogue Access Point**: An unauthorized wireless access point installed in the network.

---

### 📡 **Rogue DHCP Server**:
- **DHCP (Dynamic Host Configuration Protocol)** assigns IP addresses to devices on the network. However, the protocol has no inherent security, allowing attackers to set up rogue DHCP servers.
  
  #### **How a Rogue DHCP Server Works**:
  - It can issue **incorrect IP addresses** (e.g., duplicates or invalid addresses), causing network issues like outages or preventing internet access.
  - **Security risk**: Devices may be misconfigured or fail to communicate properly.

  #### **Defenses**:
  - **DHCP Snooping**: Feature on enterprise switches that ensures DHCP responses come only from legitimate servers.
  - **Active Directory**: In Microsoft environments, this feature identifies **authorized DHCP servers**, ensuring only trusted servers can assign IP addresses.
  - **Action**: If you detect a rogue DHCP server, remove it, and renew IP addresses on the network.

---

### 🌐 **Rogue Access Point**:
- **Rogue access points** are unauthorized devices that connect to the network and provide wireless access.
  - These may be installed by well-meaning employees, but they can create security holes by exposing the network to unauthorized users.
  
  #### **How Rogue Access Points Work**:
  - Can be plugged into any Ethernet port, often with weak or no security.
  - Can be created using wireless sharing features in operating systems, turning a computer into an access point.

  #### **Defenses**:
  - **Periodic Network Scans**: Regularly check for unauthorized access points using wireless analyzers.
  - **802.1X (Network Access Control)**: This requires **authentication** before granting network access, preventing unauthorized devices from connecting.
  
---

### 🔴 **Wireless Evil Twin**:
- A **Wireless Evil Twin** is a rogue access point designed to mimic a legitimate access point.
  - Uses the **same SSID (network name)** as the legitimate network, tricking users into connecting to it.
  - **Increased Signal Strength**: The attacker might boost the signal power to outshine the legitimate access points, forcing users to connect to the rogue one.
  
  #### **How It Works**:
  - The attacker sets up the evil twin to look like a trusted network, perhaps even replicating the **captive portal**.
  - Once connected, all **unencrypted traffic** can be intercepted and manipulated by the attacker.

  #### **Defenses**:
  - Always use **VPN** (Virtual Private Network) or **HTTPS** to encrypt communication, ensuring that even if traffic is intercepted, it cannot be read.
  
---

### 🕵️‍♂️ **On-Path (Man-in-the-Middle) Attacks**:
- **On-path attacks** (formerly known as **Man-in-the-Middle**) occur when an attacker intercepts or alters communications between two parties, without their knowledge.
  
  #### **How It Works**:
  - The attacker sits between the source and destination devices, intercepting and potentially modifying the data.
  - Common on-path attacks include:
    - **ARP Poisoning**: An attacker uses ARP to spoof a device’s IP and MAC addresses, sitting in the middle of the traffic.
    - **Session Hijacking**: Taking control of an active session between two devices.
    - **HTTPS Spoofing**: Intercepting or redirecting HTTPS traffic.
    - **Wi-Fi Eavesdropping**: Intercepting wireless communications.

  #### **Defenses**:
  - **Encryption**: Encrypt all data (using **VPN** or **HTTPS**) to prevent attackers from reading or altering intercepted traffic.
  
---

### 🛡️ **Key Takeaways**:
1. **Rogue DHCP Server**:
   - A malicious or misconfigured server can issue bad IP addresses, causing network disruptions. Use **DHCP Snooping** and **Active Directory** to prevent this.
  
2. **Rogue Access Points**:
   - Unauthorized access points can expose the network to security risks. Use **802.1X** for authentication and perform regular scans to detect rogue access points.
  
3. **Wireless Evil Twin**:
   - An attacker mimics a legitimate access point, tricking users into connecting and intercepting unencrypted data. Always use encryption like **VPN** or **HTTPS** to protect data.

4. **On-Path Attacks**:
   - Attackers sit between communication channels, intercepting or modifying traffic. Prevent this by encrypting traffic to maintain confidentiality and integrity.

---
