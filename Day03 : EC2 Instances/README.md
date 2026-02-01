---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 03 Notes

## Amazon EC2 (Elastic Compute Cloud)

---

## What is EC2?

**Amazon EC2 (Elastic Compute Cloud)** is an AWS service that provides **resizable virtual servers** in the cloud.

It allows users to:

* Launch virtual machines within minutes
* Choose CPU, memory, storage, and operating system
* Scale resources up or down based on workload

---

## Why EC2?

### (Why Cloud Servers Instead of Physical Servers?)

---

### 1. Timely Upgrade

**Traditional Servers:**

* Hardware upgrades take weeks or months
* High cost for new hardware
* Downtime during upgrades

**With EC2:**

* Upgrade CPU, RAM, or instance type in minutes
* No need to purchase new hardware
* Easy and fast scaling based on workload demand

---

### 2. Security Issues

**Physical Servers:**

* Organization must manage physical security
* Manual patching and monitoring
* Higher risk if security is misconfigured

**With EC2:**

* AWS provides highly secure data centers
* Security Groups act as virtual firewalls
* IAM controls user and service access
* Regular security updates managed by AWS

---

### 3. Server Management Problems

**Traditional Servers Require:**

* Power supply and cooling systems
* Physical space
* Hardware maintenance
* Backup and disaster recovery planning

**With EC2:**

* No physical infrastructure management
* Pay only for what you use
* Easy backups using snapshots
* High availability using AWS infrastructure

---

## Types of EC2 Instances

AWS provides different EC2 instance types based on application requirements.

1. **General Purpose Instances**
2. **Compute Optimized Instances**
3. **Memory Optimized Instances**
4. **Storage Optimized Instances**
5. **Accelerated Computing Instances**

---

## Global Infrastructure in AWS

---

## AWS Regions

### What is an AWS Region?

An **AWS Region** is a **geographical location** where AWS operates multiple data centers.

### Characteristics:

* Each region is independent
* Regions are isolated from one another
* Designed for fault tolerance and compliance

### Examples:

* Asia Pacific (Mumbai)
* US East (N. Virginia)
* Europe (Frankfurt)

---

## Availability Zones (AZs)

### What is an Availability Zone?

An **Availability Zone (AZ)** consists of **one or more physically separate data centers** within a region.

### Key Points:

* Each region has multiple AZs (usually 2 to 6)
* AZs are isolated from each other
* Connected using high-speed, low-latency links
* Used to achieve high availability and fault tolerance

### Example:

**Region:** Asia Pacific (Mumbai)

* AZ-1: ap-south-1a
* AZ-2: ap-south-1b
* AZ-3: ap-south-1c

---

## Screenshots


![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2001%20Regions.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2002.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2003.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2004.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2005.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2006.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2007.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2008.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2009.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2010.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2011.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2012.png)
![image](https://github.com/adhikarilaxman/AWS-Journey/blob/81a6899466cc4b18ff47420b89d59127d9399eac/Day03%20%3A%20EC2%20Instances/Day03%2013.png)

---

## Summary

* EC2 provides scalable virtual servers in AWS
* Cloud servers eliminate hardware and maintenance overhead
* Different EC2 instance types support different workloads
* Regions provide geographical isolation
* Availability Zones ensure high availability and fault tolerance
