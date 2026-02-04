---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 08 Notes

## AWS Scenario-Based Interview Questions

**Topics: EC2, IAM, VPC**

---

## 1. Designing a Highly Available and Scalable 2-Tier Application

### Question

You have been assigned to design a VPC architecture for a 2-tier application. The application needs to be highly available and scalable. How would you design the VPC architecture?

### Answer

To design a highly available and scalable 2-tier application, I would follow this approach:

* Create a **VPC** with a suitable CIDR block
* Create **two types of subnets**:

  * **Public Subnets** for Load Balancers
  * **Private Subnets** for application servers
* Distribute subnets across **multiple Availability Zones** for high availability
* Place **Application Load Balancers** in public subnets
* Deploy EC2 instances in private subnets using an **Auto Scaling Group**
* Configure **Security Groups** to allow only required traffic

This design ensures scalability, fault tolerance, and security.

---

## 2. Controlling Outbound Internet Access Per Subnet

### Question

Your organization has a VPC with multiple subnets. You want to restrict outbound internet access for one subnet while allowing it for another. How would you achieve this?

### Answer

This can be achieved using **route tables**:

* For the subnet where internet access is **not required**:

  * Remove the default route `0.0.0.0/0` pointing to the Internet Gateway
* For the subnet where internet access **is required**:

  * Keep the default route `0.0.0.0/0` pointing to the Internet Gateway

Route tables control outbound traffic at the subnet level.

---

## 3. Internet Access for Private Subnet Instances

### Question

Instances in a private subnet need internet access for software updates. How would you allow this?

### Answer

To provide outbound internet access to private subnet instances:

* Create a **NAT Gateway** (recommended) or **NAT Instance**
* Place the NAT Gateway/Instance in a **public subnet**
* Update the **private subnet route table** to send `0.0.0.0/0` traffic to the NAT Gateway

This allows outbound internet access while preventing inbound access from the internet.

---

## 4. Private Communication Between EC2 Instances

### Question

You want EC2 instances to communicate using private IP addresses. What steps are required?

### Answer

By default, EC2 instances within the **same VPC** can communicate using private IPs.

Ensure the following:

* Instances are launched in the **same VPC**
* Subnets are connected (default VPC routing or VPC peering if needed)
* **Security Groups** allow required inbound and outbound traffic

No additional configuration is needed beyond security rules.

---

## 5. Implementing Strict Network Access Control

### Question

How would you implement strict network access control for VPC resources?

### Answer

To enforce strict network access control:

* Use **Network Access Control Lists (NACLs)** at the subnet level
* Define **inbound and outbound rules** based on:

  * IP address
  * Port
  * Protocol
* Since NACLs are **stateless**, explicitly allow return traffic

NACLs provide an additional security layer at the subnet boundary.

---

## 6. Creating an Isolated Environment for Sensitive Workloads

### Question

How would you set up an isolated environment inside a VPC?

### Answer

To create an isolated environment:

* Create a **subnet with no route to an Internet Gateway**
* Do not attach a default route (`0.0.0.0/0`)
* Deploy sensitive workloads in this subnet

If outbound internet access is required:

* Use a **NAT Gateway** in a separate subnet
* Route outbound traffic through the NAT Gateway

This ensures isolation while maintaining flexibility.

---

## 7. Secure Access to AWS Services from a VPC

### Question

How would your application securely access AWS services like S3 from within a VPC?

### Answer

Use **VPC Endpoints**:

* Create a **VPC Endpoint** for services such as:

  * Amazon S3
  * DynamoDB
* This allows private communication without:

  * Internet Gateway
  * NAT Gateway

VPC Endpoints improve security and reduce latency.

---

## 8. Difference Between Security Groups and NACLs (With Use Case)

### Question

Explain the difference between NACLs and Security Groups with a use case.

### Answer

**NACLs:**

* Operate at **subnet level**
* **Stateless**
* Support **ALLOW and DENY**
* Used for coarse-grained network filtering

**Security Groups:**

* Operate at **instance level**
* **Stateful**
* Allow rules only (implicit deny)
* Used for fine-grained access control

**Use Case:**
For a sensitive application:

* Use **NACLs** to restrict traffic at subnet boundaries
* Use **Security Groups** to control traffic to individual EC2 instances

This provides **defense in depth**.

---

## 9. Difference Between IAM Users, Groups, Roles, and Policies

### Answer

**IAM User**

* Represents an individual or application
* Has long-term credentials
* Assigned permissions directly or via groups

**IAM Group**

* Collection of IAM users
* Permissions are assigned at group level
* Simplifies user management

**IAM Role**

* Not tied to a specific user
* Provides **temporary credentials**
* Assumed by services, users, or external accounts

**IAM Policy**

* JSON document defining permissions
* Attached to users, groups, or roles
* Specifies actions, resources, and conditions

---

## 10. Secure Access to Private Subnet Using Bastion Host

### Question

How would you securely access private subnet instances without exposing them to the internet?

### Answer

Set up a **Bastion Host**:

1. Launch an EC2 instance in a **public subnet**
2. Assign a public or Elastic IP
3. Configure its security group to allow SSH/RDP only from trusted IPs
4. Place application instances in **private subnets**
5. Allow SSH/RDP from the bastion host security group to private instances
6. Access flow:

   * Local machine → Bastion Host → Private EC2 (using private IP)

This ensures secure administrative access without exposing private instances.

---
