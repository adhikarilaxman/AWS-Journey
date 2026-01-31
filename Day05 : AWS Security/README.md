---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 05 Notes

## AWS Security

### Security Group and NACL (Network Access Control List)

---

## 1. Security Group

### What is a Security Group?

A **Security Group** is a **virtual firewall** that controls **inbound and outbound traffic** for AWS resources such as **EC2 instances**.

In simple terms, a **Security Group protects an EC2 instance**.

---

### Inbound Rules (Incoming Traffic)

Inbound rules define:

* Who can access your instance
* Which **port** and **protocol** are allowed

#### Examples:

* Allow **HTTP** → Port 80
* Allow **HTTPS** → Port 443
* Allow **SSH** → Port 22 (only from your IP address)

---

### Outbound Rules (Outgoing Traffic)

Outbound rules define:

* Where your instance can send traffic

#### Default Behavior:

* All outbound traffic is **allowed**

---

### Key Characteristics of Security Groups:

* Operate at **instance level**
* Support **ALLOW rules only**
* Are **stateful** (return traffic is automatically allowed)

---

### Security Group Diagram

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Security%20Group%20Inbound%20and%20Outbound%20Rules.png)

---

## 2. NACL (Network Access Control List)

### What is a NACL?

A **Network Access Control List (NACL)** is a **firewall that controls traffic at the subnet level**.

In simple terms, a **NACL protects the subnet**.

---

### Key Characteristics of NACL:

* Operates at **subnet level**
* Supports both **ALLOW and DENY rules**
* Is **stateless** (return traffic must be explicitly allowed)
* Rules are evaluated in **number order** (lowest to highest)

---

### Example Use Cases:

* Block a specific IP address
* Add an extra security layer for compliance

---

## Security Group vs NACL (Quick Comparison)

| Feature          | Security Group               | NACL                       |
| ---------------- | ---------------------------- | -------------------------- |
| Level            | Instance                     | Subnet                     |
| Rules            | Allow only                   | Allow and Deny             |
| Stateful         | Yes                          | No                         |
| Rule Evaluation  | All rules                    | Ordered rules              |
| Default Behavior | Deny inbound, allow outbound | Allow inbound and outbound |

---

## Screenshots
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2001%20VPC.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2002.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2003.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2004.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2005.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2006.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2007.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2008.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2009.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2010.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2011.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2012.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2013.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2014.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b98cb15fe8336f34bc431f548a912c5c8704fcd4/Day05%20%3A%20AWS%20Security/Day05%2015.png)

---

## Summary

* Security Groups protect individual EC2 instances
* NACLs protect entire subnets
* Security Groups are stateful and simpler to manage
* NACLs provide an additional security layer

---
