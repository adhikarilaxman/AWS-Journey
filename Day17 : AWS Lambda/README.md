---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 17 Notes

## AWS Lambda

---

## What is AWS Lambda?

AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers.

You upload your code → Lambda runs it automatically when triggered → You pay only for execution time.

---

## How AWS Lambda Works

1. You create a function (Python, Node.js, Java, etc.)
2. Configure a trigger (API Gateway, S3 upload, CloudWatch event, etc.)
3. When the event happens → Lambda executes the code
4. It automatically scales based on request volume

---

## Advantages of AWS Lambda

### 1. No Server Management

No need to manage EC2, OS updates, or scaling.

### 2. Automatic Scaling

Lambda automatically scales up or down based on traffic.

### 3. Pay Per Use

You pay only for:

* Number of requests
* Execution time (milliseconds)

### 4. High Availability

Built-in fault tolerance and availability.

### 5. Easy Integration

Works with:

* S3
* DynamoDB
* API Gateway
* CloudWatch
* SNS/SQS

### 6. Faster Development

Developers focus only on code, not infrastructure.

---

## AWS Lambda vs EC2

| Feature           | AWS Lambda                 | Amazon EC2                |
| ----------------- | -------------------------- | ------------------------- |
| Server Management | No                         | Yes                       |
| Scaling           | Automatic                  | Manual / Auto Scaling     |
| Pricing           | Pay per execution          | Pay per hour/second       |
| Use Case          | Event-driven apps          | Long-running applications |
| Control           | Limited OS access          | Full OS control           |
| Startup Time      | Fast (cold start possible) | Instance boot time        |

---

Lambda = Serverless, event-driven, pay per use
EC2 = Virtual server, full control, pay for uptime

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/2b341b179d8fe3c40df25f183a80f87dd1a3acf7/Day17%20%3A%20AWS%20Lambda/Day17%2001%20.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/2b341b179d8fe3c40df25f183a80f87dd1a3acf7/Day17%20%3A%20AWS%20Lambda/Day17%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/2b341b179d8fe3c40df25f183a80f87dd1a3acf7/Day17%20%3A%20AWS%20Lambda/Day17%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/2b341b179d8fe3c40df25f183a80f87dd1a3acf7/Day17%20%3A%20AWS%20Lambda/Day17%2004.png)

---
