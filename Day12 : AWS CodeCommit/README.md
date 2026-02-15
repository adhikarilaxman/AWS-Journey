---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 12 Notes

# AWS CI/CD | AWS CodeCommit

---

## What is AWS CodeCommit?

**AWS CodeCommit** is a **fully managed source control service** provided by AWS that allows you to securely store and manage **Git repositories in the cloud**.

It is similar to:

* GitHub
* GitLab

But it is fully managed inside AWS infrastructure.

---

## Key Features of AWS CodeCommit

1. Fully managed Git repository (no server management required)
2. Highly available and automatically scalable
3. Integrated with **IAM** for secure access control
4. Encryption at rest and in transit
5. Seamless integration with AWS CI/CD services

Works well with:

* AWS CodeBuild
* AWS CodeDeploy
* AWS CodePipeline

---

## Advantages of AWS CodeCommit

### 1. Fully Managed

No need to maintain Git servers.

### 2. High Security

* IAM-based authentication
* Fine-grained access control
* Encrypted by default

### 3. Scalable

Supports growing repositories and teams.

### 4. High Availability

Data is replicated across multiple Availability Zones.

### 5. Easy AWS Integration

Works seamlessly within AWS DevOps ecosystem.

---

## Disadvantages of AWS CodeCommit

### 1. AWS-Only

Limited to AWS ecosystem.

### 2. Limited Community Features

Fewer collaboration features compared to GitHub or GitLab.

### 3. Smaller Community Support

Less third-party integration and marketplace tools.

### 4. Vendor Lock-in

Migration required if moving to another cloud.

---

# Why Do We Use IAM Accounts for CodeCommit?

When using **AWS CodeCommit**, we use **IAM users or IAM roles** to control:

* Who can access the repository
* What actions they can perform

Unlike GitHub, CodeCommit does **not use traditional username/password authentication**.
It uses **AWS IAM for authentication and authorization**.

---

## Reasons for Using IAM with CodeCommit

### 1. Authentication (Who are you?)

IAM verifies the identity of users accessing repositories.

### 2. Authorization (What can you do?)

IAM policies control actions like:

* `GitPull`
* `GitPush`
* Create branches
* Delete repositories

### 3. Fine-Grained Access Control

You can:

* Grant access to specific repositories
* Allow read-only or full access
* Restrict actions based on roles

### 4. Security Best Practice

* Never use the root account
* Use IAM users with limited permissions
* Enable MFA
* Follow Principle of Least Privilege

### 5. Service-to-Service Access

If:

* EC2 pulls code
* CodePipeline accesses repository

We use **IAM Roles**, not IAM users.

---

# CI/CD Flow with CodeCommit

Developer → Push Code → CodeCommit → CodePipeline → CodeBuild → CodeDeploy → Application Deployment

This creates a fully automated CI/CD pipeline.

---

## Screenshots

(Add your console screenshots below)

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
