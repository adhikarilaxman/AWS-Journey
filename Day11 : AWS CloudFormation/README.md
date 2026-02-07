Here’s a **clean, structured, and GitHub-ready version of your Day 11 notes**, with clear sections, corrected formatting, and no extra fluff—perfect for revision and interviews.

---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 11 Notes

## AWS CloudFormation

---

## AWS CFT (CloudFormation Template)

### What is AWS CloudFormation?

**AWS CloudFormation** is an **Infrastructure as Code (IaC)** service that allows you to **create, update, and manage AWS resources using templates** instead of manual configuration.

Templates are written in:

* **YAML** (most commonly used)
* **JSON**

CloudFormation automatically handles:

* Resource creation
* Dependency management
* Updates and rollback

---

## Why AWS CloudFormation?

* Automates infrastructure provisioning
* Ensures **consistent and repeatable deployments**
* Reduces manual errors
* Supports **automatic rollback** on failure
* Infrastructure can be **version-controlled**

---

## AWS CloudFormation Architecture

![image]()

---

## Difference: AWS CLI vs CloudFormation vs Terraform

| Feature          | AWS CLI           | CloudFormation   | Terraform              |
| ---------------- | ----------------- | ---------------- | ---------------------- |
| Type             | Command-line tool | IaC (AWS native) | IaC (Multi-cloud)      |
| State Management | No                | Managed by AWS   | Managed via state file |
| Cloud Support    | AWS only          | AWS only         | Multi-cloud            |
| Rollback         | Manual            | Automatic        | Manual / Controlled    |
| Version Control  | No                | Yes              | Yes                    |
| Declarative      | No                | Yes              | Yes                    |

---

## Drift Detection

### What is Drift?

**Drift** occurs when the **actual AWS infrastructure differs from the CloudFormation template**.

### Example:

* Resource created using CloudFormation
* Resource modified manually from AWS Console
* Template state ≠ actual infrastructure state

### Drift Detection:

* CloudFormation can detect:

  * Modified resources
  * Deleted resources
  * Configuration changes

This helps maintain infrastructure consistency.

---

## Declarative Infrastructure

### What does Declarative Mean?

You define **WHAT you want**, not **HOW to create it**.

### Example:

```
I want 2 EC2 instances
```

CloudFormation decides:

* Resource creation order
* Dependencies
* Required updates

### Declarative Tools:

* AWS CloudFormation
* Terraform

### Imperative (Non-declarative) Tools:

* AWS CLI
* Manual AWS Console actions

---

## Versioned Infrastructure

### What is Versioned Infrastructure?

Infrastructure code is stored in **version control systems (Git)**.

### Benefits:

* Track infrastructure changes
* Easy rollback
* Team collaboration
* Auditable change history

### Example:

* `v1.0` → 1 EC2 instance
* `v2.0` → 2 EC2 instances
* Roll back anytime if required

CloudFormation templates and Terraform files are **fully versionable**.

---

## Screenshots

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
![image]()

![image]()
![image]()
![image]()


![image]()

---
