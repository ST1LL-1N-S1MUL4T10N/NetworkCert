
---

# 🖥️ **Basic Network Device Commands – CompTIA Network+ (5.5)**

### 1. **`show mac-address-table`**  
- **Purpose**: Displays the MAC address table on a switch.
- **How it Works**: Lists all MAC addresses learned by the switch and the ports where they were learned.
- **Use Case**: 
  - Troubleshooting: If traffic is being sent out of every interface, check the MAC address table to ensure correct mappings.
  - Diagnosing Full Table: Identifies if the switch has hit its MAC address table capacity.

---

### 2. **`show route`**  
- **Purpose**: Displays the routing table of a router.
- **How it Works**: Shows all routes that the router knows about, including connected and dynamically learned routes (like RIP, OSPF).
- **Example**:
  - **R (RIP route)**: Indicates a route learned via RIP.
  - **C (Connected route)**: Indicates a directly connected network.
- **Use Case**: 
  - Determine where specific traffic is routed across the network.
  - Track a route from source to destination by checking all routers in the path.

---

### 3. **`show interface`**  
- **Purpose**: Displays detailed information about a specific network interface.
- **How it Works**: Provides interface status (up/down), speed, MTU, duplex, errors (e.g., CRC, input/output errors).
- **Example**:
  - Interface is up: Means it's physically connected.
  - Line protocol is up: The interface is actively transmitting data.
  - Errors: Helps identify issues with packet loss or performance degradation.
- **Use Case**: 
  - Troubleshooting network performance.
  - Check interface configuration and identify errors (e.g., CRC errors or frame drops).

---

### 4. **`show config`** or **`show running-config`**  
- **Purpose**: Displays the active configuration of the device.
- **How it Works**: Shows current settings, such as IP configurations, routing protocols, security settings, and more.
- **Example**: For a router, the config might include IP addresses, subnet masks, routing protocols (e.g., OSPF, RIP).
- **Use Case**: 
  - Quickly view or verify device settings.
  - Troubleshoot configuration issues.
  - Make and confirm changes to device settings.

---

### 5. **`show arp`**  
- **Purpose**: Displays the Address Resolution Protocol (ARP) cache.
- **How it Works**: Shows the mapping between IP addresses and MAC addresses.
- **Use Case**: 
  - Verify which MAC addresses correspond to specific IP addresses.
  - Diagnose ARP-related issues, such as IP-to-MAC address mismatches.

---

### 6. **`show vlan`**  
- **Purpose**: Displays VLAN configuration on a switch.
- **How it Works**: Shows the VLANs configured on the switch and which interfaces are assigned to each VLAN.
- **Use Case**: 
  - View VLAN assignments for switch ports.
  - Diagnose VLAN misconfigurations or ensure correct port assignments.

---

### 7. **`show power`**  
- **Purpose**: Displays Power over Ethernet (PoE) status and power consumption.
- **How it Works**: Shows the power usage for each interface and the overall power budget for PoE-enabled devices.
- **Use Case**: 
  - Monitor PoE status to ensure sufficient power for devices like IP phones or access points.
  - Check if additional devices can be supported by the switch’s remaining power.

---

### 8. **Example Use of Commands**:
- **`show route`**:  
  - Look at the **routing table** on a router to track traffic across the network.
  - Check if a route is dynamically learned (e.g., RIP, OSPF) or manually configured.
  
- **`show interface`**:  
  - Use this command to check if an interface is physically up, configured correctly, or experiencing issues (e.g., CRC errors).

- **`show vlan`**:  
  - For VLAN troubleshooting, ensure the correct ports are assigned to the appropriate VLAN.

---

### 🔧 **Summary of Commands and Their Use Cases**:

| **Command**              | **Purpose**                                             | **Use Case**                                          |
|--------------------------|---------------------------------------------------------|-------------------------------------------------------|
| **`show mac-address-table`** | View MAC address table in a switch.                    | Troubleshoot MAC address learning issues.            |
| **`show route`**          | View routing table in a router.                        | Track network traffic paths across routers.           |
| **`show interface`**      | View interface status and details.                     | Troubleshoot interface issues (errors, speed, duplex).|
| **`show config`**         | View active device configuration.                      | Verify and modify device settings.                    |
| **`show arp`**            | View ARP cache for IP-MAC address mappings.            | Diagnose ARP issues and IP-to-MAC mapping problems.   |
| **`show vlan`**           | View VLANs and their port assignments.                 | Confirm correct VLAN configurations.                  |
| **`show power`**          | View PoE status and power usage.                       | Monitor PoE usage and available power for devices.    |

---

## **Best Practices**:
- **Network Troubleshooting**: Use `show interface` to check for errors, `show route` to trace traffic paths, and `show mac-address-table` for troubleshooting switching issues.
- **Configuration Review**: Use `show config` or `show running-config` to view and modify device configurations.
- **PoE Monitoring**: If using PoE switches, regularly check the power usage with `show power` to ensure all devices are powered properly.

---
