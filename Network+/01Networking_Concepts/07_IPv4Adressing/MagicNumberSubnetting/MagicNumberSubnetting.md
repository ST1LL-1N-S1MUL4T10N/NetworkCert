
---

## 🔮 **The Magic Number Method (Quick Ref Guide)**

### 🧠 **Goal:**  
Find **Subnet ID**, **Broadcast**, **First Host**, and **Last Host** — **without binary conversions**.

---

### 🔢 Step-by-Step Breakdown:

#### 1. **Identify the Interesting Octet**
- Look at the **subnet mask**.
- The **first octet** that is *not* 255 or 0 is your **interesting octet**.

#### 2. **Calculate the Magic Number**
- **Magic Number = 256 - (Interesting Octet Mask Value)**  
  e.g., if subnet mask is `255.255.255.224`, interesting octet is 224 → `256 - 224 = 32`.

#### 3. **Find the Subnet Block**
- Use the **magic number** to divide the range (0–255) into blocks.  
  E.g., with 32 → blocks: 0–31, 32–63, 64–95, etc.
- Find which block your IP address falls into.
- The **start** of that block = **Subnet ID**.

#### 4. **Broadcast Address**
- **Broadcast = Subnet ID + Magic Number - 1**  
  (In the interesting octet)

#### 5. **First and Last Usable Hosts**
- **First Host = Subnet ID + 1**
- **Last Host = Broadcast - 1**

---

### 📝 Example:
IP: `172.16.242.133/27`  
Mask: `/27 = 255.255.255.224` → Interesting octet: 224 → Magic Number: **32**

- IP (last octet) = 133 → Falls in block **128–159**
- Subnet ID = `172.16.242.128`
- Broadcast = `128 + 32 - 1 = 159` → `172.16.242.159`
- First host = `172.16.242.129`
- Last host = `172.16.242.158`

---

### ✨ Pro Tips:
- Memorize the **CIDR ↔ Decimal ↔ Magic Number** chart for common masks (`/25` to `/30` especially).
- **Magic Number also = block size** in the interesting octet.
- Always remember: **First address = Network**, **Last = Broadcast**, rest are usable.

---


