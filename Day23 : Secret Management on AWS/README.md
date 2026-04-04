---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 23 Notes

## Secret Management on AWS 

---

## What is Secret Management?

Secret Management is the process of securely storing, managing, and accessing sensitive information such as:

* API keys
* Database passwords
* Access tokens
* Encryption keys

In simple words:

> It ensures that sensitive data is not hardcoded in applications and is accessed securely when needed.

---

## Why Secret Management is Important

* Prevents data breaches
* Improves security
* Avoids hardcoding credentials in code
* Enables controlled access using IAM
* Supports auditing and compliance

---

## Secret Management Options on AWS

### 1. AWS Systems Manager Parameter Store

#### What is Parameter Store?

A service used to store configuration data and secrets as key-value pairs.

---

#### Features

* Store plain text and encrypted values
* Integration with IAM
* Uses AWS KMS for encryption
* Supports hierarchical structure (e.g., `/app/dev/db-password`)
* Cost-effective (free tier available)

---

#### Use Cases

* Storing environment variables
* Application configuration
* Basic secret storage

---

#### Limitations

* No automatic secret rotation
* Basic functionality compared to Secrets Manager

---

### 2. AWS Secrets Manager

#### What is Secrets Manager?

A fully managed service designed specifically for storing and managing secrets securely.

---

#### Features

* Automatic secret rotation
* Fine-grained access control using IAM
* Encrypted using AWS KMS
* Versioning of secrets
* Integration with RDS, Lambda, and other AWS services

---

#### Use Cases

* Database credentials
* API keys
* Third-party integrations

---

#### Advantages over Parameter Store

* Built-in rotation
* More suitable for production environments
* Advanced security features

---

#### Limitations

* More expensive than Parameter Store

---

### 3. HashiCorp Vault

#### What is Vault?

An open-source tool used for managing secrets across multi-cloud and on-premises environments.

---

#### Features

* Dynamic secrets (temporary credentials)
* Secret leasing and expiration
* Encryption as a service
* Fine-grained access control
* Multi-cloud support

---

#### Use Cases

* Multi-cloud environments
* Advanced security setups
* Enterprise-level secret management

---

#### Limitations

* Requires setup and maintenance
* More complex than AWS-native services

---

## Comparison

| Feature         | Parameter Store | Secrets Manager    | HashiCorp Vault          |
| --------------- | --------------- | ------------------ | ------------------------ |
| Managed Service | Yes             | Yes                | No (self-managed)        |
| Cost            | Low / Free      | Paid               | Infrastructure cost      |
| Secret Rotation | No              | Yes                | Yes                      |
| Multi-cloud     | No              | No                 | Yes                      |
| Complexity      | Low             | Medium             | High                     |
| Best For        | Basic configs   | Production secrets | Enterprise / multi-cloud |

---

## When to Use What

### Use Parameter Store if:

* You need simple configuration storage
* Cost is a concern
* No need for automatic rotation

---

### Use Secrets Manager if:

* You need secure secret storage
* You want automatic rotation
* You are building production applications

---

### Use HashiCorp Vault if:

* You need multi-cloud or hybrid setup
* You need dynamic secrets
* You want advanced security control

---

## Summary

* Secret Management is essential for securing sensitive data in AWS.
* Parameter Store is best for basic configurations.
* Secrets Manager is ideal for production-level secret management.
* HashiCorp Vault is suitable for advanced, multi-cloud environments.

---
