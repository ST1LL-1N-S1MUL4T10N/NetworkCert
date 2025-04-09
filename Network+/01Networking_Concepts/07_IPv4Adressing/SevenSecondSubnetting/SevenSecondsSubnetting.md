
---

### ✅ **Seven Second Subnetting Summary**

#### 🎯 **Goal**:
Quickly determine:
- **Subnet mask**
- **Network address**
- **Broadcast address**
- **First and last usable IPs**

---

### 🧠 **What You Need: THE CHART**

You build this once (on paper or whiteboard):

| CIDR | Subnet Mask | # of Subnets | Addresses per Subnet | Magic Number |
|------|--------------|--------------|------------------------|----------------|
| /24  | 255.255.255.0 | 1            | 256 (254 usable)       | 256            |
| /25  | 255.255.255.128 | 2         | 128                    | 128            |
| /26  | 255.255.255.192 | 4         | 64                     | 64             |
| /27  | 255.255.255.224 | 8         | 32                     | 32             |
| /28  | 255.255.255.240 | 16        | 16                     | 16             |
| /29  | 255.255.255.248 | 32        | 8                      | 8              |
| /30  | 255.255.255.252 | 64        | 4                      | 4              |
| /31  | 255.255.255.254 | —         | 2 (point-to-point)     | 2              |
| /32  | 255.255.255.255 | —         | 1                      | —              |

Build out more as needed (/20, /17, etc.)—you’re mostly using:
- **Power of twos** (for address count)
- Magic Number = **256 - subnet mask value** (in the varying octet)

---

### 🧮 **Steps (The Four-Part Process)**

1. **Convert CIDR to Decimal Mask**  
   Use your chart to convert `/x` to 255.xxx.xxx.xxx format.

2. **Find the Network Address**  
   - Find where the IP falls in the **block ranges** based on magic number.
   - Example: If block size is 64, your subnets start at 0, 64, 128, etc.
   - Find the **block start** that your IP belongs to.

3. **Find the Broadcast Address**  
   - Next block start - 1  
   - Or: **Network address + block size - 1**

4. **Find the Usable IPs**  
   - First IP = Network address + 1  
   - Last IP = Broadcast address - 1  

---

### ✍️ **Example** (like one from above)

**IP**: `165.245.12.88/26`

- `/26` = `255.255.255.192` → block size = **64**
- IP 88 falls in the **64-127** range
- **Network address** = `165.245.12.64`
- **Broadcast** = `165.245.12.127`
- **First usable** = `165.245.12.65`
- **Last usable** = `165.245.12.126`

Done in seconds if your chart is ready.

---
