### IPv4 Subnet Masks Cheat Sheet – CompTIA Network+ (N10-009)

#### **Key Concepts:**
- **Classless Subnetting (CIDR):** 
  - Since 1993, class-based subnetting is no longer used. Now, we use **CIDR** (Classless Interdomain Routing) for more flexible IP addressing.
  - **CIDR Notation:** Represents the subnet mask as the number of 1's in the mask, e.g., `/24` instead of `255.255.255.0`.
  - Example: `192.168.1.44/24` means a subnet mask of `255.255.255.0`.

- **Subnet Mask Representation:**
  - **Binary:** A series of 1's followed by 0's, indicating the network portion and host portion of an IP.
  - **CIDR Notation:** The number of 1's in the subnet mask.
  - **Decimal:** The traditional dotted-decimal format, e.g., `255.255.255.0`.

#### **Examples:**
1. **/24 (255.255.255.0):**
   - **CIDR Block Notation:** `/24` (24 bits for the network, 8 bits for hosts).
   - **Decimal Mask:** `255.255.255.0`.

2. **/16 (255.255.0.0):**
   - **CIDR Block Notation:** `/16` (16 bits for the network, 16 bits for hosts).
   - **Decimal Mask:** `255.255.0.0`.

3. **/26 (255.255.255.192):**
   - **CIDR Block Notation:** `/26` (26 bits for the network, 6 bits for hosts).
   - **Decimal Mask:** `255.255.255.192`.

4. **/12 (255.240.0.0):**
   - **CIDR Block Notation:** `/12` (12 bits for the network, 20 bits for hosts).
   - **Decimal Mask:** `255.240.0.0`.

5. **/19 (255.255.224.0):**
   - **CIDR Block Notation:** `/19` (19 bits for the network, 13 bits for hosts).
   - **Decimal Mask:** `255.255.224.0`.

#### **Converting Subnet Masks:**

- **Binary to CIDR:**
  - Count the number of consecutive 1's in the subnet mask.
  - Example: `11111111.11111111.11100000.00000000` → 19 1's → `/19`.

- **CIDR to Decimal:**
  - Break down the CIDR into 8-bit sections (octets), then convert each to decimal.
  - Example: `/26` → `11111111.11111111.11111111.11000000` → `255.255.255.192`.

#### **Subnet Mask to CIDR Notation Conversion Chart:**

| Binary Octet        | Decimal Equivalent |
|---------------------|--------------------|
| 11111111 (8 ones)   | 255                |
| 11111110 (7 ones)   | 254                |
| 11111100 (6 ones)   | 252                |
| 11111000 (5 ones)   | 248                |
| 11110000 (4 ones)   | 240                |
| 11100000 (3 ones)   | 224                |
| 11000000 (2 ones)   | 192                |
| 10000000 (1 one)    | 128                |
| 00000000 (0 ones)   | 0                  |

#### **Subnet Mask Examples in Binary, CIDR, and Decimal:**

- **Example 1:** `255.240.0.0`
  - **Binary:** `11111111.11110000.00000000.00000000`
  - **CIDR:** `/12`
  - **Network Bits:** 12
  - **Host Bits:** 20
  
- **Example 2:** `255.255.224.0`
  - **Binary:** `11111111.11111111.11100000.00000000`
  - **CIDR:** `/19`
  - **Network Bits:** 19
  - **Host Bits:** 13

#### **Subnetting Summary:**

- **CIDR Notation:** `/X`, where `X` is the number of 1's in the subnet mask.
- **Decimal Notation:** Commonly used in configurations (e.g., Windows or routers).
- **Network Portion:** Defined by the 1's in the subnet mask.
- **Host Portion:** Defined by the 0's in the subnet mask.

#### **Quick Tips:**
- Always check the device documentation for preferred notation.
- **CIDR Block:** `/X` (X = number of network bits).
- **Decimal Mask:** Traditional subnet mask format (e.g., `255.255.255.0`).
