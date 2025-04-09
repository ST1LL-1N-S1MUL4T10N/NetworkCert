
---

## 🔮 **Magic Number Subnetting Cheat Sheet**

### 🎯 Quick Reference Steps:

1. **Find the Interesting Octet**  
   - First octet in the subnet mask ≠ 255 or 0  
2. **Magic Number = 256 - Value in Interesting Octet**
3. **Find Subnet Block**  
   - Which multiple of the magic number does your IP fall into?  
4. **Subnet ID = Start of that block**
5. **Broadcast = Subnet ID + Magic Number - 1**
6. **First Host = Subnet ID + 1**
7. **Last Host = Broadcast - 1**

---

## 📊 **CIDR Block / Subnet Mask / Magic Number / Hosts Chart**

| CIDR | Subnet Mask         | Interesting Octet | Magic Number | Hosts per Subnet* |
|------|----------------------|-------------------|---------------|--------------------|
| /25  | 255.255.255.128      | 4th               | 128           | 126                |
| /26  | 255.255.255.192      | 4th               | 64            | 62                 |
| /27  | 255.255.255.224      | 4th               | 32            | 30                 |
| /28  | 255.255.255.240      | 4th               | 16            | 14                 |
| /29  | 255.255.255.248      | 4th               | 8             | 6                  |
| /30  | 255.255.255.252      | 4th               | 4             | 2                  |
| /24  | 255.255.255.0        | 3rd               | 256           | 254                |
| /23  | 255.255.254.0        | 3rd               | 2             | 510                |
| /22  | 255.255.252.0        | 3rd               | 4             | 1022               |
| /21  | 255.255.248.0        | 3rd               | 8             | 2046               |
| /20  | 255.255.240.0        | 3rd               | 16            | 4094               |
| /19  | 255.255.224.0        | 3rd               | 32            | 8190               |
| /18  | 255.255.192.0        | 3rd               | 64            | 16,382             |
| /17  | 255.255.128.0        | 3rd               | 128           | 32,766             |
| /16  | 255.255.0.0          | 2nd               | 256           | 65,534             |

> 📝 *Hosts per subnet = (2^host bits) - 2 (for Network & Broadcast)*

---

## 📌 Optional: Pre-built Subnet Ranges (Helpful for /27 example)

With a magic number of 32 (from a /27), your fourth octet subnet blocks look like:

```
0–31
32–63
64–95
96–127
128–159
160–191
192–223
224–255
```

You’d pick the range that your IP’s last octet falls into, then:
- **Subnet ID = First number in range**
- **Broadcast = Last number**
- **First/Last Host = in between those two**

---
