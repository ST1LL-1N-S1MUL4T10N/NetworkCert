
---

# 🖧 Hardware Issues – CompTIA Network+ (5.2)

### ⚡ **Power over Ethernet (PoE) Standards**
- **PoE**: Power and data over the same Ethernet cable.
- **Power Sources**:
  - **Endspan**: Power provided directly by a **PoE switch**.
  - **Midspan**: Power injected by a separate **PoE injector**.

---

## 💡 **PoE Standards Overview**:
1. **PoE (IEEE 802.3af)**:  
   - **Power**: 15.4 watts  
   - **Current**: 350 milliamps  
   - **Used for**: Small devices (e.g., telephones, basic access points).

2. **PoE+ (IEEE 802.3at)**:  
   - **Power**: 25.5 watts  
   - **Current**: 600 milliamps  
   - **Used for**: Larger devices (e.g., cameras, larger access points).

3. **PoE++ (IEEE 802.3bt)**:  
   - **Power**:  
     - Type 3: 51 watts, 600 milliamps  
     - Type 4: 71.3 watts, 960 milliamps  
   - **Used for**: High-powered devices (e.g., laptops, PTZ cameras, and 2.5-10 gigabit connections).

---

## 🛠️ **Important PoE Switch Compatibility Considerations**:
- **Device-Switch Compatibility**: Ensure the **PoE standard** of your device matches the switch’s supported PoE standard (PoE, PoE+, or PoE++).
  - **Example**: A **PoE+ switch** can’t power a **PoE++ device**.
  
- **Total Power Capacity**: Ensure the total power requirement of connected devices is under the switch’s PoE power capacity (e.g., 200 watts, 720 watts).

---

## 🖧 **Transceiver Mismatches & Signal Loss**:
- **Transceivers**: Essential for modular connections in Ethernet. They must match fiber type and wavelength:
  - **Wavelength Marks**: Look for markings like **850 nm** or **1310 nm** to ensure compatibility.
  - **Signal Loss**: Using mismatched transceivers or cables leads to **signal loss** and **errors**.

---

### **Calculating Signal Strength**:
1. **Transmit Power**: The power the transmitting device sends (in **decibels per milliwatt**, dBm).
2. **Signal Loss**: Factor in:
   - **Distance**
   - **Connectors/splices**
3. **Received Power**: Subtract signal loss from transmitted power.
4. **Sensitivity Value**: Compare received power to the **transceiver’s sensitivity**.
   - If received power ≥ sensitivity, the connection works.
   - If received power < sensitivity, the signal is too weak.

---

## 📊 **Example: Power Budget Calculation**
- **Transceiver Sensitivity**: A typical **SFP transceiver** may have a receiver sensitivity of **-17 dBm**.
- **Power Budget Calculation**:  
   - **Example**: If the calculated received power is **-20 dBm**, this is **too weak** for the transceiver to function properly.

---

## ⚠️ **Transceiver Types and Fiber Compatibility**:
- **Fiber Compatibility**: Always ensure the **fiber type** and **transceiver wavelength** match to prevent signal loss.
  - Common wavelengths: **850 nm** (short-range) and **1310 nm** (long-range).
  
- **Warning**: Mismatched transceivers may cause **signal loss**, leading to **network slowdowns** and **errors**.

---

## 📋 **Hardware Issue Checklist**:
| **Issue**                      | **Solution**                                        |
|---------------------------------|-----------------------------------------------------|
| **PoE Power Mismatch**          | Ensure the device and switch support the same PoE standard (PoE, PoE+, PoE++). |
| **Transceiver Mismatch**        | Check wavelength and fiber type compatibility.     |
| **Insufficient Signal Strength**| Calculate the power budget; ensure received power meets sensitivity. |
| **Signal Loss**                 | Verify fiber length, number of connectors, and loss factors. |

---
