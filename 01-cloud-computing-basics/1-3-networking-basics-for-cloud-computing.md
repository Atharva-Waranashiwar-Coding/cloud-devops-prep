# 📌 Networking Basics for Cloud Computing

## **1️⃣ CIDR (Classless Inter-Domain Routing)**
### 📌 Definition
CIDR (Classless Inter-Domain Routing) is a method for efficiently allocating and managing IP addresses. It defines IP address ranges using a combination of an IP address and a subnet mask in the format **`<IP address>/<prefix length>`**.

### 📌 Key Points
✅ **IP Address Range:** Defines the number of usable IP addresses.  
✅ **Prefix Length:** Determines the subnet size (e.g., `/24` represents 256 IPs).  
✅ **Efficient Addressing:** Eliminates wasteful IP allocation compared to the older class-based system.  

### 📌 Examples
| CIDR Notation | Total IPs | Usable IPs |
|---------------|-----------|------------|
| **/32**       | 1         | 1          |
| **/24**       | 256       | 254        |
| **/16**       | 65,536    | 65,534     |

---

## **2️⃣ Subnets**
### 📌 Definition
Subnets (short for sub-networks) divide a larger network into smaller, more manageable segments. This improves network efficiency, enhances security, and simplifies traffic management.

### 📌 Key Points
✅ **Public Subnet:** Exposes resources (e.g., web servers) to the internet.  
✅ **Private Subnet:** Restricts access to internal resources (e.g., databases).  
✅ **Subnet Mask:** Determines the network's size by specifying the portion of the IP reserved for the network vs hosts.

### 📌 Examples
| Subnet Mask | CIDR Notation | Total IPs | Usable IPs |
|-------------|---------------|-----------|------------|
| 255.255.255.0 | **/24**       | 256       | 254        |
| 255.255.0.0   | **/16**       | 65,536    | 65,534     |

---

## **3️⃣ Firewalls & Security Groups**
### 📌 Firewalls
Firewalls are network security systems that monitor and control incoming and outgoing traffic based on predefined security rules.

### 📌 Security Groups
Security groups act as **virtual firewalls** for cloud resources like EC2 instances (AWS) or virtual machines (Azure/GCP).

### 📌 Key Features
✅ Control **inbound and outbound traffic**.  
✅ Allow or deny access based on **IP addresses, protocols, and ports**.  
✅ Operate at the instance or network level.

### 📌 Examples
| Cloud Provider | Security Feature            | Purpose                      |
|----------------|-----------------------------|------------------------------|
| **AWS**        | Security Groups & NACLs    | Protect EC2 instances        |
| **Azure**      | Network Security Groups     | Control VM network access    |
| **GCP**        | Firewall Rules             | Manage traffic to resources  |

---

## **4️⃣ Practical Examples**
### **1. CIDR Example**
- **`192.168.1.0/24`:** Provides 256 total IPs, with 254 usable for hosts.  
- **Use Case:** Allocating IP addresses for a small office or cloud network.

### **2. Subnet Design Example**
- **Scenario:** A VPC with 2 public and 2 private subnets.  
  - Public Subnet: **10.0.0.0/24**  
  - Private Subnet: **10.0.1.0/24**

### **3. Firewall Configuration**
- **Inbound Rule:** Allow HTTP (port 80) from all IPs (0.0.0.0/0).  
- **Outbound Rule:** Allow all traffic to external internet (0.0.0.0/0).

---

## 🚀 Summary
- CIDR simplifies IP address allocation and reduces waste.  
- Subnets segment networks for better security and management.  
- Firewalls and security groups ensure resource security by controlling traffic.  

---

## **5️⃣ Next Steps**
💻 **Hands-On Tasks:**  
✅ Design a VPC with **CIDR allocation** and **subnets**.  
✅ Configure **firewalls and security groups** in AWS/GCP/Azure.  
✅ Test connectivity between public and private subnets.

---
