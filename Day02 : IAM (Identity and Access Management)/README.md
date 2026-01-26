---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 02 Notes

## IAM (Identity and Access Management)

### What is IAM?

**AWS IAM (Identity and Access Management)** is a service that enables you to **securely control access to AWS resources**.

IAM helps answer two important questions:

* **Authentication** – Who are you?
* **Authorization** – What are you allowed to do?

IAM allows you to manage **users, permissions, and access** to AWS services in a secure way.

> IAM is a **global service** and is **free of cost**.

---

### IAM Core Components

IAM mainly consists of the following components:

1. Users
2. Groups
3. Policies
4. Roles

![IAM Architecture Diagram](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/AWS%20IAM%20Authentication%20and%20Authorization.png)

---

## 1. IAM Users

An **IAM User** represents a **person or an application** that interacts with AWS.

### Key Points:

* Each user has a **unique username**
* Users are assigned **credentials** to access AWS

### Types of Credentials:

* **Password** → For AWS Management Console access
* **Access Key & Secret Key** → For programmatic access (CLI, SDK, APIs)

### Example:

* A developer logging into AWS Console
* An application accessing S3 using access keys

---

## 2. IAM Groups

An **IAM Group** is a **collection of IAM users**.

Instead of assigning permissions to each user individually, permissions are assigned to the group, and users inherit those permissions.

### Key Points:

* Groups contain users
* Policies are attached to groups
* A user can belong to **multiple groups**

### Example:

* `AdminGroup` → Full access
* `DeveloperGroup` → EC2 and S3 access
* `ReadOnlyGroup` → View-only access

---

## 3. IAM Policies

An **IAM Policy** is a **JSON document** that defines permissions.

A policy specifies:

* What actions are **allowed or denied**
* On which **AWS resources**
* Under what **conditions** (optional)

---

### Types of IAM Policies

#### 1. AWS Managed Policies

* Created and maintained by AWS
* Ready to use

**Example:**

* `AmazonS3ReadOnlyAccess`

---

#### 2. Customer Managed Policies

* Created and managed by users
* Can be reused across users, groups, and roles

---

#### 3. Inline Policies

* Attached directly to a single user, group, or role
* Not reusable
* Used for specific or temporary permissions

---

## 4. IAM Roles

An **IAM Role** is an AWS identity that **does not have permanent credentials**.

Roles are **assumed temporarily** and provide **temporary security credentials**.

### Roles can be assumed by:

* AWS services (EC2, Lambda, etc.)
* IAM users
* Applications
* External users or accounts

### Why IAM Roles Are Important:

* More secure than access keys
* Used for cross-account access
* Best practice for AWS services

### Example:

* EC2 instance accessing S3 using a role
* Lambda accessing DynamoDB

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2010.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2011.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2012.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2013.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2014.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/5f23a9dd236e7ef33336f70e8474a673dd861f91/Day02%20%3A%20IAM%20(Identity%20and%20Access%20Management)/Day02%2015.png)

---
