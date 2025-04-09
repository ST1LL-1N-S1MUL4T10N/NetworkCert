### **Binary Math – CompTIA Network+ N10-009 (1.7)**

Understanding binary math is crucial, especially when calculating IP subnets. The ability to convert between **binary** and **decimal** IP addresses is fundamental for network professionals. This section breaks down the basics of binary math and how to perform these conversions.

---

### **Binary Number System**

- **Binary** is a numbering system that uses **only two digits**: 0 and 1. 
- Each 0 or 1 is referred to as a **bit**.
- **8 bits** together form a **byte** (also called an **octet**).

### **Conversion Chart**

To convert between **binary** and **decimal**, you can use the following binary place value chart:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----|----|----|----|---|---|---|---|
  
This chart helps us determine the decimal value corresponding to each binary bit. For example, if you have a binary value like `10101000`, you can determine its decimal value by mapping the ones to the appropriate place values.

---

### **Binary to Decimal Conversion**

Let’s go through a few examples to understand how to convert binary numbers to decimal:

1. **Binary 00000010**:
    - Binary number: `00000010`
    - Use the conversion chart:  
      128, 64, 32, 16, 8, 4, 2, 1  
      Start from the right:
      - 0 * 128 = 0
      - 0 * 64 = 0
      - 0 * 32 = 0
      - 0 * 16 = 0
      - 0 * 8 = 0
      - 0 * 4 = 0
      - 1 * 2 = 2
      - 0 * 1 = 0  
      **Total**: `2` in decimal.

2. **Binary 10000010**:
    - Binary number: `10000010`
    - Conversion chart:  
      128, 64, 32, 16, 8, 4, 2, 1  
      - 1 * 128 = 128
      - 0 * 64 = 0
      - 0 * 32 = 0
      - 0 * 16 = 0
      - 0 * 8 = 0
      - 0 * 4 = 0
      - 1 * 2 = 2
      - 0 * 1 = 0  
      **Total**: `128 + 2 = 130` in decimal.

3. **Binary 11111111**:
    - Binary number: `11111111`
    - Conversion chart:  
      128, 64, 32, 16, 8, 4, 2, 1  
      - 1 * 128 = 128
      - 1 * 64 = 64
      - 1 * 32 = 32
      - 1 * 16 = 16
      - 1 * 8 = 8
      - 1 * 4 = 4
      - 1 * 2 = 2
      - 1 * 1 = 1  
      **Total**: `128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255` in decimal.

---

### **Decimal to Binary Conversion**

Now let’s look at how to convert decimal numbers back to binary.

1. **Convert 154 decimal to binary**:
    - Start with 154 and compare it to the powers of 2.
    - Use the conversion chart for powers of 2:  
      128, 64, 32, 16, 8, 4, 2, 1.
    - 154 is greater than 128 but less than 192, so place a `1` under 128.
    - Subtract 128 from 154: 154 - 128 = 26.
    - 26 is greater than 16 but less than 32, so place a `1` under 16.
    - Subtract 16 from 26: 26 - 16 = 10.
    - 10 is greater than 8 but less than 16, so place a `1` under 8.
    - Subtract 8 from 10: 10 - 8 = 2.
    - 2 is greater than 1, so place a `1` under 2.
    - Subtract 2 from 2: 2 - 2 = 0.
    - All other powers of 2 (64, 32, 4, 1) are skipped, as 0 is left.
    - **Result**: The binary value for 154 decimal is `10011010`.

---

### **General Process for Decimal to Binary Conversion**

1. Start with the decimal number.
2. Compare the decimal number with the largest power of 2 less than or equal to the number.
3. Place a `1` in the corresponding binary place and subtract that power of 2 from the decimal number.
4. Repeat the process with the remaining number, moving to the next smaller power of 2.
5. If the power of 2 is larger than the remaining decimal value, place a `0` in that place.

---

### **Understanding Powers of 2**

The **powers of 2** increase exponentially as you move left in the binary number. For example:
- **2^0** = 1
- **2^1** = 2
- **2^2** = 4
- **2^3** = 8
- **2^4** = 16
- **2^5** = 32
- **2^6** = 64
- **2^7** = 128
- And so on...

The more bits you have, the higher the number you can represent. For instance:
- **2 bits**: 4 possibilities (00, 01, 10, 11)
- **3 bits**: 8 possibilities (000, 001, 010, 011, 100, 101, 110, 111)
- **8 bits (1 byte)**: 256 possibilities (0 to 255 in decimal)

---

### **Summary**

- **Binary to Decimal**: You sum the corresponding place values of the bits that are `1`.
- **Decimal to Binary**: Break the decimal number down using powers of 2 to determine the binary representation.
- The process of converting between binary and decimal allows for better understanding of IP subnetting, a critical skill in network design.
