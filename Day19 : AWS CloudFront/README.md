---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 19 Notes

# AWS CloudFront

## What is AWS CloudFront?

**Amazon CloudFront** is a **Content Delivery Network (CDN)** service provided by AWS.

It delivers content (websites, images, videos, APIs, etc.) to users with:

* Low latency
* High data transfer speed
* Improved performance

It works by caching content at **global Edge Locations** closer to users.

---

## Why We Use CloudFront

We use CloudFront for:

* Reduced latency
* Faster website performance
* Global content delivery
* High availability
* Enhanced security
* Reduced load on origin servers

---

## How CloudFront Works

1. A user requests content (website, image, API, video, etc.).
2. CloudFront checks the **nearest Edge Location**.
3. If the content is already cached:

   * It returns the content immediately.
4. If the content is NOT cached:

   * CloudFront fetches it from the **Origin** (S3, EC2, ALB, etc.).
   * Stores it in cache.
   * Delivers it to the user.
5. Future requests are served directly from the cache.

This process improves speed and reduces load on backend servers.

---

## Key Components of CloudFront

### 1. Edge Locations

* Global data centers.
* Cache content closer to users.
* Reduce latency.

---

### 2. Origin

The original source of content.

Examples:

* Amazon S3 Bucket
* EC2 Instance
* Application Load Balancer
* Custom Server

---

### 3. Distribution

A Distribution is the configuration that defines:

* Origin settings
* Cache behavior
* Security rules
* Routing rules

Types of Distributions:

* Web Distribution (for websites and APIs)
* RTMP Distribution (for media streaming – legacy)

---

## CloudFront + S3 Architecture Example

User → CloudFront → Edge Location → S3 (Origin)

This setup is commonly used for:

* Static websites
* Image hosting
* Frontend applications

---

## Benefits of AWS CloudFront

* High Performance
* Low Latency
* Scalability
* Security (HTTPS, WAF integration)
* DDoS protection (AWS Shield)
* Cost Optimization (Reduced origin load)

---

## Real-Time Example

If your website is hosted in Mumbai and a user from the US accesses it:

Without CloudFront:

* Request goes directly to Mumbai → Slow response.

With CloudFront:

* Request goes to nearest US Edge Location → Faster response.

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/b694577b7add429cf4c28c8d4a5896e078037de1/Day19%20%3A%20AWS%20CloudFront/Day19%2010.png)

---
