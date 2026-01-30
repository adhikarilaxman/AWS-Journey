---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 04 Notes

## VPC (Virtual Private Cloud)

---

## What is VPC?

**Amazon VPC (Virtual Private Cloud)** is a **logically isolated private network** within AWS where you can launch and manage AWS resources such as **EC2, RDS, and Load Balancers**.

In simple terms, a VPC is **your own private data center in the AWS cloud**.

### You control:

* IP address range (CIDR block)
* Subnets
* Routing
* Network security

---

### VPC Architecture Diagram

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/dda34cf4fd0dfc832157021309079340aab6bee5/Day04%20%3A%20AWS%20Networking%20(VPC)/Day04%2001%20VPC%20Diagram.png)

---

## Why VPC?

VPC is used to achieve the following:

### 1. Network Isolation

* Resources are isolated from other AWS customers

### 2. Security

* Full control over inbound and outbound traffic
* Multiple layers of security using **Security Groups** and **Network ACLs (NACLs)**

### 3. Custom Networking

* Ability to choose your own IP address range
* Design **public and private subnets**

### 4. Scalability and Availability

* Easily expand subnets
* Deploy resources across multiple **Availability Zones**

---

## Internet Gateway (IGW)

### What is an Internet Gateway?

An **Internet Gateway (IGW)** is a VPC component that enables **communication between resources in your VPC and the Internet**.

---

### Why Internet Gateway?

* Provides internet access to resources in **public subnets**
* Required for EC2 instances to be reachable from the internet

---

### Key Points:

* Internet Gateway is attached to a VPC
* Supports both IPv4 and IPv6 traffic
* Works together with route tables

---

## Subnets

### What is a Subnet?

A **Subnet** is a **smaller network inside a VPC** used to organize resources and control traffic.

### Key Points:

* Each subnet belongs to **one Availability Zone**
* Subnets cannot span multiple AZs

---

## Public Subnets

### What is a Public Subnet?

A **Public Subnet** is a subnet that has **a route to the Internet Gateway** in its route table.

### Common Use Cases:

* Web servers
* Load balancers
* Bastion hosts

---

## Load Balancers

### What is a Load Balancer?

A **Load Balancer** distributes incoming network traffic across multiple targets such as **EC2 instances, containers, or IP addresses**.

---

### Why Load Balancers?

* High availability
* Fault tolerance
* Improved application performance

---

## Route Tables

### What is a Route Table?

A **Route Table** contains a set of rules (routes) that determine **where network traffic is directed**.

---

### Key Points:

* Every subnet must be associated with a route table
* Routes define traffic destinations

### Example:

* `0.0.0.0/0 → Internet Gateway` (for internet access)

---

## Summary

* VPC provides a secure and isolated network in AWS
* Internet Gateway enables internet connectivity
* Subnets divide the VPC into smaller networks
* Public subnets allow internet-facing resources
* Load balancers distribute traffic efficiently
* Route tables control traffic flow

---

Just tell me.
