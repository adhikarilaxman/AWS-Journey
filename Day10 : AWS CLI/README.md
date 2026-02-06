---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 10 Notes

## AWS CLI & AWS API

---

## AWS CLI (Command Line Interface)

### What is AWS CLI?

**AWS CLI (Command Line Interface)** is a command-line tool that allows you to **manage and interact with AWS services using commands**, instead of using the AWS Management Console.

In simple words:
AWS CLI helps you control AWS resources directly from the terminal.

---

### Why AWS CLI?

* Faster than using the AWS Console
* Automates repetitive tasks
* Useful for scripting and DevOps
* Works with almost all AWS services (EC2, S3, IAM, VPC, etc.)

---

### How AWS CLI Works

AWS CLI communicates with AWS services using **AWS APIs**.

Flow:

```
User / Script
     ↓
AWS CLI
     ↓
AWS APIs
     ↓
AWS Services
```

---

### AWS CLI Setup Steps

1. Install AWS CLI
2. Configure AWS CLI using:

   ```
   aws configure
   ```
3. Provide the following details:

   * Access Key ID
   * Secret Access Key
   * Default Region
   * Output Format

---

## Installing AWS CLI on Ubuntu (Linux)

### Step 1: Update Package Index

```
sudo apt update
```

### Step 2: Install Required Dependencies

```
sudo apt install -y unzip curl
```

### Step 3: Download AWS CLI Installer

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
```

### Step 4: Extract the Installer

```
unzip awscliv2.zip
```

### Step 5: Run the Installer

```
sudo ./aws/install
```

### Step 6: Verify Installation

```
aws --version
```

### Step 7: Clean Up

```
rm -rf awscliv2.zip aws
```

### Step 8: Configure AWS CLI

```
aws configure
```

You will be prompted to enter:

* Access Key ID
* Secret Access Key
* Default region (example: us-east-1)
* Output format (json / text / table)

---

## Example AWS CLI Commands

### List S3 Buckets

```
aws s3 ls
```

### Upload a File to S3

```
aws s3 cp file.txt s3://my-bucket/
```

### List EC2 Instances

```
aws ec2 describe-instances
```

---

## AWS API (Application Programming Interface)

### What is AWS API?

An **AWS API** is a set of endpoints that allows **applications, tools, and services** to communicate with AWS programmatically.

In simple words:
AWS APIs are the backend interfaces used by:

* AWS Console
* AWS CLI
* AWS SDKs

---

### Key Points About AWS API

* Uses **HTTPS**
* Authenticated using **IAM credentials**
* Uses **JSON** for request and response
* Each AWS service has its own APIs

Examples:

* EC2 → `RunInstances`
* S3 → `PutObject`
* IAM → `CreateUser`

---

### AWS API Diagram

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%20Digram%20API.png)

---

## Command to Create an EC2 Instance Using AWS CLI

```
aws ec2 run-instances \
  --region YOUR_REGION \
  --image-id YOUR_AMI_ID \
  --instance-type YOUR_INSTANCE_TYPE \
  --key-name YOUR_KEY_PAIR_NAME \
  --subnet-id YOUR_SUBNET_ID \
  --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=YOUR_INSTANCE_NAME}]'
```

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2002%20AWS%20CLI%20Installation.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/432157689cc5cb0024dfd6075a91063acdcc0821/Day10%20%3A%20AWS%20CLI/Day10%2010.png)

---
