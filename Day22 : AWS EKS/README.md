Here is your **Day 22 Notes** properly formatted, clean, and professional — ready for GitHub.

---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 22 – AWS Elastic Kubernetes Service (EKS)

## What is AWS EKS?

Amazon Elastic Kubernetes Service (EKS) is a **fully managed Kubernetes service** provided by AWS.

It allows you to:

* Run Kubernetes clusters without managing the control plane
* Deploy and manage containerized applications
* Scale applications automatically
* Integrate with AWS services

In simple words:

> EKS lets you run Kubernetes on AWS without managing Kubernetes master nodes.

---

## What is Kubernetes?

Kubernetes is an open-source container orchestration platform used to:

* Deploy containers
* Manage scaling
* Handle networking
* Perform rolling updates

EKS is AWS’s managed version of Kubernetes.

---

## How AWS EKS Works

1. AWS manages the Kubernetes control plane (Master nodes).
2. You manage worker nodes (EC2 or Fargate).
3. Applications run inside **Pods** on worker nodes.
4. EKS integrates with AWS services like VPC, ALB, IAM, and CloudWatch.

---

## Key Components of EKS

### 1. Cluster

The main Kubernetes environment where applications run.

### 2. Control Plane

Managed by AWS and includes:

* API Server
* Scheduler
* etcd

### 3. Worker Nodes

Run your applications. These can be:

* Amazon EC2 instances
* AWS Fargate (serverless option)

### 4. Node Groups

A group of worker nodes with the same configuration and scaling settings.

---

## Advantages of AWS EKS

### High Availability

The control plane runs across multiple Availability Zones.

### Managed Kubernetes

No need to maintain or patch master nodes.

### Deep AWS Integration

Works seamlessly with:

* IAM
* CloudWatch
* Application Load Balancer (ALB)
* Amazon Elastic Container Registry

### Scalability

Supports auto scaling for both pods and worker nodes.

### Security

Supports IAM Roles for Service Accounts (IRSA) for fine-grained access control.

---

## Disadvantages of AWS EKS

### More Complex than ECS

Requires knowledge of Kubernetes concepts and architecture.

### Higher Cost

EKS control plane has a fixed hourly cost.

### Steep Learning Curve

Kubernetes concepts can be advanced for beginners.

---

# Summary

* Amazon EKS is a managed Kubernetes service in AWS.
* AWS manages the control plane, and you manage worker nodes.
* It provides high availability, scalability, and deep AWS integration.
* Best suited for teams already familiar with Kubernetes.

---

# Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/12b9173713cdf07421c69de35b01ad0c1dee57ae/Day22%20%3A%20AWS%20EKS/Day22%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/12b9173713cdf07421c69de35b01ad0c1dee57ae/Day22%20%3A%20AWS%20EKS/Day22%2002.png)

---
