
---

# Cloud Models Cheat Sheet  
**CompTIA Network+ N10-009 – Video 1.3**

---

## Overview  
- **Cloud Computing Impact:**  
  - Provides on-demand resources with rapid scalability and global access.  
  - Supports both public and private (or hybrid) deployments based on user needs.  
- **Key Consideration:**  
  - Choice of cloud model depends on who will access your application (public vs. internal) and the level of control/responsibility your organization wants.

---

## Cloud Service Models

### 1. Software as a Service (SaaS)  
- **Definition:**  
  - Fully managed applications delivered over the Internet.  
- **User Experience:**  
  - Access via a web browser, login, and use—no installation, upgrades, or maintenance by you.  
- **Responsibility:**  
  - **Provider:** Manages the infrastructure, application, and underlying data.
  - **Customer:** Manages only user-specific settings and data.  
- **Examples:**  
  - Google Mail, Office 365.

---

### 2. Platform as a Service (PaaS)  
- **Definition:**  
  - Cloud platforms offering a suite of tools and services for developing, deploying, and managing applications.  
- **User Experience:**  
  - Build and customize applications using provided “building blocks” without managing the underlying infrastructure.  
- **Responsibility:**  
  - **Provider:** Manages the underlying infrastructure (servers, network, storage) and platform-level services.
  - **Customer:** Handles application development, configuration, and data.  
- **Examples:**  
  - Salesforce platform, Google App Engine.

---

### 3. Infrastructure as a Service (IaaS)  
- **Definition:**  
  - Provides virtualized computing resources over the Internet.  
- **User Experience:**  
  - Rent computing hardware (servers, storage, networks) and deploy your own software and operating systems.  
- **Responsibility:**  
  - **Provider:** Supplies the physical infrastructure (data center, network, hosts).  
  - **Customer:** Installs and manages the OS, applications, middleware, and security of deployed workloads.  
- **Alternate Name:**  
  - Sometimes called Hardware as a Service (HaaS).  
- **Examples:**  
  - Web hosting services that offer virtual servers.

---

## Cloud Deployment Scenarios  
- **Public Cloud:**  
  - Applications accessible to anyone over the internet (e.g., SaaS for general consumers).  
- **Private Cloud:**  
  - Applications deployed on your own virtualized infrastructure for internal use only.  
- **Hybrid Cloud:**  
  - Combines public and private clouds to meet varied needs and maintain flexibility.

---

## Cloud Responsibility Matrix  
Visualize a continuum of responsibilities between the provider and the customer:  

| Model     | Provider’s Responsibility                       | Customer’s Responsibility                |
|-----------|-------------------------------------------------|------------------------------------------|
| **On-Prem** | Everything (physical data center, network, security, apps, data) | All aspects of management and maintenance  |
| **IaaS**    | Physical data center, physical network & hosts | OS, middleware, applications, and data    |
| **PaaS**    | Infrastructure, platform services (network, runtime) | Application development and data           |
| **SaaS**    | Infrastructure, platform, application, data   | User-specific settings and data management  |

- **Key Point:**  
  - As you move from on-prem to SaaS, the provider takes on more responsibilities, reducing the customer’s management overhead.

---

## Summary Points  
- **SaaS:** Complete, ready-to-use applications with minimal customer management.  
- **PaaS:** Development platforms with tools for customized apps, balancing management between provider and customer.  
- **IaaS:** Raw virtual hardware giving maximum control to the customer while the provider handles physical infrastructure.  
- **Cloud Deployment Choice:**  
  - Public clouds allow broad accessibility.
  - Private clouds offer more control for internal applications.
  - Hybrid setups blend both to meet diverse organizational needs.

---
