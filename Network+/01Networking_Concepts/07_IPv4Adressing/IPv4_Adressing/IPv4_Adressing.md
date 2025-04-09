### IPv4 Addressing Overview (CompTIA Network+ N10-009 – 1.7)

#### Key Concepts:
- **IPv4 Addressing**: IPv4 addresses are unique identifiers for devices in a network, made up of 4 octets (32 bits) separated by periods (e.g., 192.168.1.165).
- **Subnet Mask**: A 4-octet value (e.g., 255.255.255.0) used to determine the subnet a device is on.
- **Default Gateway**: The device that allows communication between devices on different subnets. It must be within the same local subnet.
- **Loopback Address**: Used to test internal communication. The range is from **127.0.0.1 to 127.255.255.254**.
- **Reserved Addresses**: Reserved for future use or testing, within the range **240.0.0.1 to 254.255.255.254** (Class E).
- **Virtual IP (VIP)**: Assigned to devices like virtual machines for internal reference, not tied to a physical network adapter.

---

#### IPv4 Address Structure:
- **Format**: 4 octets (e.g., 192.168.1.131).
  - Each octet is 8 bits (1 byte), resulting in a 32-bit address.
  - Each octet value ranges from **0 to 255**.

#### IP Configuration Methods:
- **Static IP**: Manually configured on the device (rare in modern networks).
- **Dynamic IP (DHCP)**: Automatically assigned via **Dynamic Host Configuration Protocol** (DHCP) when a device joins the network.
- **Link-Local Address (APIPA)**: Auto-assigned address when DHCP is unavailable, within the range **169.254.0.1 to 169.254.255.254**.

---

#### Key Address Ranges:
- **Private IP Address Ranges**: Cannot be routed on the public internet.
  - **Class A**: 10.0.0.0 to 10.255.255.255 (over 16 million addresses) → **10.0.0.0/8**.
  - **Class B**: 172.16.0.0 to 172.31.255.255 (over 1 million addresses) → **172.16.0.0/12**.
  - **Class C**: 192.168.0.0 to 192.168.255.255 (over 65,000 addresses) → **192.168.0.0/16**.

---

#### Addressing Notes:
- **DHCP**: Automatically assigns IP configuration (address, subnet mask, gateway).
- **APIPA (Automatic Private IP Addressing)**: Assigned when no DHCP server is available (only local communication possible).
- **Network Address Translation (NAT)**: Used to allow devices with private IP addresses to communicate on the internet by translating them into a public IP address.

---

#### Reserved and Special Address Ranges:
- **Loopback Range**: 127.0.0.1 to 127.255.255.254 (Used for testing local device communication).
- **Reserved Range (Class E)**: 240.0.0.1 to 254.255.255.254 (Reserved for future use/testing).
- **APIPA Range**: 169.254.0.1 to 169.254.255.254 (Used when DHCP is unavailable).

---

### Summary of Private IP Ranges (RFC 1918):
1. **10.0.0.0 – 10.255.255.255** (Class A) → **10.0.0.0/8**
2. **172.16.0.0 – 172.31.255.255** (Class B) → **172.16.0.0/12**
3. **192.168.0.0 – 192.168.255.255** (Class C) → **192.168.0.0/16**

---
