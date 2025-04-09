### **Classful Subnetting Overview (CompTIA Network+ N10-009 - 1.7)**

**What is Classful Subnetting?**
Classful subnetting refers to the traditional way of dividing IP addresses into five classes (A, B, C, D, E) based on the first octet of the address. Though this method is outdated and rarely used today, it serves as a foundational concept for understanding IP address structure and subnetting.

---

### **IP Address Classes**

| **Class** | **Range of First Octet** | **Default Subnet Mask** | **Use Case** |
|-----------|--------------------------|-------------------------|--------------|
| **Class A** | 0 - 127 | 255.0.0.0 | Large networks |
| **Class B** | 128 - 191 | 255.255.0.0 | Medium-sized networks |
| **Class C** | 192 - 223 | 255.255.255.0 | Small networks |
| **Class D** | 224 - 239 | N/A | Multicast (no host assignment) |
| **Class E** | 240 - 255 | N/A | Reserved for experimental use |

---

### **How to Identify the Class of an IP Address**
1. **Look at the first octet** (the first number in the IP address).
2. **Class A**: 0-127 (First bit: `0`)
3. **Class B**: 128-191 (First bits: `10`)
4. **Class C**: 192-223 (First bits: `110`)
5. **Class D**: 224-239 (First bits: `1110`)
6. **Class E**: 240-255 (First bits: `1111`)

---

### **Example IP Classifications**
- **17.22.90.7**: First octet is 17 → **Class A**
- **220.10.77.40**: First octet is 220 → **Class C**
- **165.245.0.1**: First octet is 165 → **Class B**
- **191.77.24.250**: First octet is 191 → **Class B**
- **192.1.12.5**: First octet is 192 → **Class C**

---

### **Subnetting Key Values**
When subnetting an IP address, there are four key values to calculate:
1. **Network Address**: Set all host bits to 0.
2. **First Usable Host Address**: One more than the network address.
3. **Broadcast Address**: Set all host bits to 1.
4. **Last Usable Host Address**: One less than the broadcast address.

---

### **Step-by-Step Example: Subnet Calculation**

**IP Address:** 10.74.222.11 (Class A)
- **Default Subnet Mask:** 255.0.0.0
- **Network Address:** Set all host bits to 0 → **10.0.0.0**
- **First Usable Host:** 10.0.0.1
- **Broadcast Address:** Set all host bits to 1 → **10.255.255.255**
- **Last Usable Host:** 10.255.255.254

---

**IP Address:** 172.16.88.200 (Class B)
- **Default Subnet Mask:** 255.255.0.0
- **Network Address:** 172.16.0.0
- **First Usable Host:** 172.16.0.1
- **Broadcast Address:** 172.16.255.255
- **Last Usable Host:** 172.16.255.254

---

**IP Address:** 192.168.4.77 (Class C)
- **Default Subnet Mask:** 255.255.255.0
- **Network Address:** 192.168.4.0
- **First Usable Host:** 192.168.4.1
- **Broadcast Address:** 192.168.4.255
- **Last Usable Host:** 192.168.4.254

---

### **Summary of Classful Subnetting**
- The concept of IP address classes (A, B, C, D, E) is based on the first octet of the address.
- Although classful subnetting is outdated, understanding the classes helps you determine the default subnet mask and provides a starting point for subnetting networks.
- Key calculations (network address, usable host range, and broadcast address) apply to both classful and modern subnetting methods.

---
