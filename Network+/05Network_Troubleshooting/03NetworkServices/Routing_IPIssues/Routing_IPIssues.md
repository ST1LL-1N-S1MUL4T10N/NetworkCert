
---

# 🖧 Routing and IP Issues – CompTIA Network+ (5.3)

### ⚡ **Routing Table Issues**:
- **Problem**: Incorrect routing tables can cause data to be dropped or misrouted.
- **Solution**: Always verify the **routing table** on each router along the path to ensure proper routes are in place for both outgoing and return traffic.
  
  **Steps**:
  1. Check the routing table of the router to confirm it has a route to the destination network.
  2. If no route exists, the router will drop the traffic or respond with an ICMP "host unreachable" message.

---

## 🌐 **Default Gateway (Gateway of Last Resort)**:
- **Problem**: If no specific route matches in the routing table, traffic may be dropped.
- **Solution**: Configure a **gateway of last resort** by adding a **static default route** (0.0.0.0/0), which sends traffic to the next router if no other route exists.

  **Example**:
  - **Default Route**: `0.0.0.0/0 → 10.10.50.2`
  - If there’s no other route to the destination, the router forwards traffic to **10.10.50.2**.

---

### 🛠️ **Routing Table Example**:
- **Direct Routes**: Routes directly connected to the router (e.g., 10.10.10.0/24, 10.10.40.0/24).
- **Static Routes**: Manually added routes (e.g., 10.10.20.0/24).
- **Dynamic Routes**: Learned through routing protocols like RIP (e.g., 10.10.30.0/24).

---

### 🔄 **DHCP and IP Address Pool Exhaustion**:
- **Problem**: **DHCP address pool exhaustion** causes devices to receive **APIPA addresses** (Automatic Private IP Addressing), which are **non-routable**.
- **Solution**: 
  1. Check the **DHCP server** for available IP addresses.
  2. Consider using **IP Address Management (IPAM)** to monitor and manage DHCP pools.
  3. **Reduce DHCP lease times** to free up IP addresses quicker.

---

### 📡 **DHCP Configuration and Troubleshooting**:
- **Problem**: Incorrect **DHCP** settings, such as wrong IP address, subnet mask, or default gateway.
- **Solution**:
  1. Verify that the **IP address** provided by DHCP is correct for the network interface.
  2. Check **subnet mask** and **default gateway** values to ensure they match the network's configuration.
  3. Use tools like **ping** and **traceroute** to confirm connectivity and troubleshoot where traffic is failing.

---

### 🚨 **Duplicate IP Address Issues**:
- **Problem**: **Duplicate IP addresses** on the network can cause conflicts and communication failures.
- **Cause**: 
  - A device manually configured with an IP address that overlaps with a DHCP-assigned address.
  - Multiple **DHCP servers** distributing overlapping IP address ranges.
  - A device with **DHCP enabled** giving out IPs, causing conflicts with the designated DHCP server.

  **Troubleshooting Steps**:
  1. **Ping** the suspected IP address and check if it’s already in use.
  2. If a response is received, use the **ARP table** to find the **MAC address** of the device.
  3. Trace the MAC address through the **switch’s MAC address table** to locate the connected device.
  4. If multiple DHCP servers are in use, **capture DHCP traffic** to see what IP addresses each server is assigning.

---

## 🔑 **Key Terms**:
- **Routing Table**: A data structure in a router that defines where to forward packets based on destination IP addresses.
- **Gateway of Last Resort**: A default route used when no specific route is found for traffic.
- **Static Route**: A manually configured route that dictates how packets should be forwarded to a destination network.
- **DHCP (Dynamic Host Configuration Protocol)**: A network protocol used to automatically assign IP addresses to devices on a network.
- **APIPA (Automatic Private IP Addressing)**: A fallback mechanism where devices self-assign a non-routable IP address when the DHCP server is unavailable.
- **IPAM (IP Address Management)**: A system used to manage and monitor IP address usage across a network.
- **ARP (Address Resolution Protocol)**: A protocol used to map IP addresses to MAC addresses in a local network.

---

## 🛠️ **Troubleshooting Checklist**:
| **Issue**                        | **Solution**                                          |
|-----------------------------------|-------------------------------------------------------|
| **Routing Table Problems**        | Check all routers along the path for correct routes. |
| **No Route Found**                | Add a **default route** (0.0.0.0/0) as a **gateway of last resort**. |
| **DHCP Address Pool Exhaustion**  | Check the **DHCP server**, reduce lease time, or increase the address pool. |
| **Incorrect DHCP Configurations** | Verify IP address, subnet mask, and gateway settings. |
| **Duplicate IP Addresses**        | Ping and check the **ARP table** for duplicate IPs. Use **packet capture** for DHCP conflicts. |

---
