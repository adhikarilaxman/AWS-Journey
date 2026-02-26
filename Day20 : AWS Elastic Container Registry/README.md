---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 20 – AWS Elastic Container Registry (ECR)

## What is AWS ECR?

Amazon Elastic Container Registry (ECR) is a **fully managed Docker container registry** provided by AWS.

It is used to:

* Store Docker container images
* Manage container image versions
* Securely push and pull images
* Integrate with AWS container services

In simple words:

> ECR is a private Docker image storage service inside AWS.

---

## Why We Use ECR

ECR helps in managing containerized applications efficiently.

### Key Benefits:

* Store container images securely
* Integrate with container services like:

  * Amazon ECS
  * Amazon EKS
  * AWS Lambda
* Control access using IAM roles and policies
* Automate CI/CD pipelines
* Enable image vulnerability scanning
* Apply lifecycle policies to manage old images

---

# ECR vs Docker Hub

Docker Hub is Docker’s public container registry used worldwide.

Below is the comparison:

| Feature            | AWS ECR                | Docker Hub           |
| ------------------ | ---------------------- | -------------------- |
| Ownership          | AWS                    | Docker Inc.          |
| Default Visibility | Private                | Public               |
| Integration        | Native AWS integration | General use          |
| Security           | IAM-based access       | Username/password    |
| Image Scanning     | Built-in               | Limited (paid plans) |
| Pricing            | Pay-as-you-go          | Free + Paid plans    |
| CI/CD Integration  | Strong with AWS        | Works with any CI/CD |

---

## Key Differences Explained

### 1. Integration

* ECR is tightly integrated with AWS ecosystem.
* Docker Hub works across all platforms and clouds.

---

### 2. Security

* ECR uses IAM roles and policies for fine-grained access control.
* Docker Hub uses account-based authentication.

---

### 3. Use Case

Use **ECR** when:

* Your infrastructure is inside AWS
* You use ECS or EKS
* You want private repositories by default

Use **Docker Hub** when:

* You want public image sharing
* You work in multi-cloud or local environments
* You maintain open-source projects

---

## Summary

* Amazon ECR is a secure, scalable, and fully managed container registry inside AWS.
* Docker Hub is a public container registry widely used for sharing container images.
* ECR is best for AWS-based production workloads.

---

# Screenshots

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

---
