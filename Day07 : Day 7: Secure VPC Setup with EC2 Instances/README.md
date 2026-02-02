---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 07 Notes

## Secure VPC Setup with EC2 Instances

---

## 1. Auto Scaling Group (ASG)

### What is Auto Scaling Group?

An **Auto Scaling Group (ASG)** is an AWS service that **automatically increases or decreases the number of EC2 instances** based on traffic or system load.

### Why Auto Scaling?

* Handles traffic spikes automatically
* Optimizes cost by terminating unused instances
* Ensures high availability by maintaining the required number of instances

### Key Points:

* Define **Minimum**, **Maximum**, and **Desired** instance count
* Automatically launches or terminates EC2 instances
* Commonly used with **Load Balancers**

---

## 2. Load Balancer (ELB)

### What is a Load Balancer?

A **Load Balancer (ELB)** distributes incoming application traffic across **multiple EC2 instances**.

### Why Load Balancer?

* Prevents overloading a single server
* Improves availability and fault tolerance
* Enhances application performance

### Note:

* Works closely with **Target Groups** and **Auto Scaling Groups**

---

## 3. Target Group

### What is a Target Group?

A **Target Group** is a logical group of **registered targets** such as:

* EC2 instances
* IP addresses
* Lambda functions

These targets receive traffic from a **Load Balancer**.

### Key Points:

* Load Balancer forwards traffic to the Target Group
* Performs **health checks** on instances
* Traffic is sent only to **healthy targets**

---

## 4. Bastion Host / Jump Server

### What is a Bastion Host?

A **Bastion Host (Jump Server)** is a **secure EC2 instance** used to access **private EC2 instances** inside a VPC.

### Why Bastion Host?

* Improves security
* Prevents direct internet access to private EC2 instances

### How it works:

* Bastion Host is placed in a **Public Subnet**
* Application EC2 instances are placed in **Private Subnets**

```
Your Laptop
     ↓
Bastion Host (Public Subnet)
     ↓
Private EC2 (Private Subnet)
```

### Access Method:

* SSH into the Bastion Host
* From Bastion Host, SSH into private EC2 instances

---

## Overall Architecture Flow

```
Users
  ↓
Load Balancer
  ↓
Target Group
  ↓
Auto Scaling Group (EC2 Instances)
```

* **Auto Scaling Group** manages EC2 scaling
* **Load Balancer** distributes traffic
* **Target Group** performs health checks
* **Bastion Host** provides secure administrative access

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day%2007%20vpc-example-private-subnets.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2001.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2002.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2003%20Resource%20Map.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2004%20Launch%20Template.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2005%20Creating%20Launch%20Template.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2006%20Creating%20Launch%20Template.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2007%20Creating%20Launch%20Template.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2008%20Creating%20Launch%20Template%20Network%20Settings.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2009.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2010.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2011.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2012.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2013%20Bastion.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/f58dbc99c471f46cd68fd2034b55df685d8470ef/Day07%20%3A%20Day%207%3A%20Secure%20VPC%20Setup%20with%20EC2%20Instances/Day07%2014.png)

---
