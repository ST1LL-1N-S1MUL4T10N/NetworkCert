
---

# **Security Concepts – CompTIA Network+ N10-009 – Section 4.1**

### 🛡 **Overview of IT Security**

Security in IT involves a range of concepts that protect data and systems. Key topics covered include data states, encryption, certificates, Identity and Access Management (IAM), and more.

---

### **Data States**

1. **Data in Transit (Data in Motion)**:
   - **Definition**: Data being transferred across a network (wired or wireless).
   - **Security Concerns**: Network devices like switches or routers don't inherently secure data; security mechanisms (e.g., firewalls, encryption) must be added.
   - **Encryption Protocols**: **TLS** (Transport Layer Security) and **IPsec** (Internet Protocol Security) are commonly used for encrypting data in transit.

2. **Data at Rest**:
   - **Definition**: Data stored on a physical medium like a hard drive or SSD.
   - **Encryption**: Methods like **full disk encryption**, database encryption, or file-level encryption are applied to protect data at rest.
   - **Access Control**: **Access Control Lists (ACLs)** are used to determine which users can access specific data.

---

### **Public Key Infrastructure (PKI)**

- **Definition**: A framework for managing encryption keys and digital certificates.
- **Function**: PKI helps secure communication, manage certificates, and ensure data integrity.
- **Digital Certificates**: Used to authenticate users, devices, and applications. These certificates are issued by a **Certificate Authority (CA)**.

---

### **Certificate Authorities (CA)**

1. **Role of CA**:
   - **Definition**: A CA signs digital certificates, providing trust to the certificates.
   - **Internal vs. External CA**: Some organizations set up their own internal CA, while others rely on third-party CAs.
   - **Web of Trust**: A decentralized trust model where trust is passed through mutual associations (e.g., If A trusts B, and B trusts C, then A can trust C).

2. **Self-Signed Certificates**: 
   - **Definition**: Organizations can create their own CA to issue and sign certificates for internal use.

---

### **Identity and Access Management (IAM)**

- **Definition**: A framework for ensuring only authorized users can access specific data.
- **Key Components**:
  1. **Authentication**: Verifying the identity of users accessing the system.
  2. **Authorization**: Granting access to data based on authentication.
  3. **Tracking and Auditing**: Monitoring access to data and maintaining logs.

---

### **Security Principles**

1. **Least Privilege**:
   - **Definition**: Users are given only the minimum access necessary for their roles.
   - **Goal**: Prevent unauthorized access and limit the potential impact of any breach.

2. **Role-Based Access Control (RBAC)**:
   - **Definition**: Users are assigned roles, and each role has a specific set of permissions.
   - **Example**: Shipping and receiving employees might have different access levels than managers or executives.

3. **Geofencing**:
   - **Definition**: Restricting or granting access to data based on a user’s physical location (e.g., IP address, GPS coordinates).
   - **Use Case**: Users accessing sensitive data may be restricted based on their geographic location (e.g., only accessible inside the corporate building).

---

### **Physical Security**

1. **CCTV (Closed Circuit Television)**:
   - **Use**: Surveillance cameras are used for monitoring and recording physical security within an organization.
   - **Modern Features**: Motion detection, license plate recognition, facial recognition.

2. **Door Locks and Access Control**:
   - **Traditional Locks**: Physical key-based systems.
   - **Electronic Access**: Personal identification codes, RFID badges, and biometric methods (fingerprints, retina scans) for controlling access.
   - **Multi-Factor Authentication (MFA)**: Combines multiple security measures, such as using both a badge and a PIN, for stronger access control.

---
