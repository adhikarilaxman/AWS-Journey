---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 06 Notes

## AWS Route 53

---

## What is Amazon Route 53?

**Amazon Route 53** is AWS’s **DNS (Domain Name System) web service** used to **convert human-readable domain names into IP addresses**.

### Meaning of the Name:

* **Route** → Routes internet traffic
* **53** → DNS operates on **port 53**

---

## Why Route 53?

Amazon Route 53 is used because it provides:

### 1. Domain Name Resolution

* Converts domain names into IP addresses

### 2. High Availability

* Routes traffic only to **healthy resources**

### 3. Scalability

* Handles a very large number of DNS queries

### 4. Low Latency

* Routes users to the **nearest AWS resource**

### 5. Tight AWS Integration

* Works seamlessly with:

  * EC2
  * Elastic Load Balancer (ELB)
  * S3
  * CloudFront

---

## Main Components of Route 53

---

## 1. Domain Registration

* Buy and manage domain names directly from AWS
* AWS acts as the domain registrar

**Example:**
`mywebsite.com`

---

## 2. Hosted Zones

A **Hosted Zone** is a container that holds **DNS records** for a domain.

### Types of Hosted Zones:

* **Public Hosted Zone**

  * Used for internet-facing domains

* **Private Hosted Zone**

  * Used for internal domains within a VPC

---

## 3. DNS Records

DNS records define **how traffic is routed** to resources.

### Common DNS Record Types:

| Record Type | Purpose                                         |
| ----------- | ----------------------------------------------- |
| A           | Maps domain name to IPv4 address                |
| AAAA        | Maps domain name to IPv6 address                |
| CNAME       | Maps one domain name to another                 |
| Alias       | AWS-specific DNS routing (free and recommended) |
| MX          | Mail server configuration                       |
| TXT         | Domain verification and security                |

---

## Summary

* Route 53 is AWS’s DNS service
* Converts domain names into IP addresses
* Provides high availability and low latency
* Supports domain registration and DNS management
* Integrates tightly with AWS services

---

Just tell me.
