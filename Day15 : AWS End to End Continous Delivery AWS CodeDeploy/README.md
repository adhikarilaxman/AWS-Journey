---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 15 Notes

## AWS End-to-End Continuous Delivery – AWS CodeDeploy

---

## AWS CodeDeploy

AWS CodeDeploy is a fully managed **Continuous Deployment (CD)** service that automates application deployments to:

* Amazon EC2
* Amazon ECS
* AWS Lambda
* On-premises servers

---

## Why We Use CodeDeploy

* Automates deployments
* Reduces human errors
* Supports zero-downtime deployment
* Enables automatic rollback on failure
* Improves release reliability

---

## How AWS CodeDeploy Works

1. Developer pushes code
2. CodeBuild builds the application
3. CodeDeploy receives the build artifact
4. Deploys it to target instances
5. Monitors deployment health
6. Rolls back automatically if deployment fails

---

## Important Components

### 1. Application

A logical name that represents your application in CodeDeploy.

---

### 2. Deployment Group

Defines:

* Target EC2 instances (using tags or Auto Scaling groups)
* Deployment type (In-place or Blue/Green)
* Rollback settings

---

### 3. appspec.yml

A configuration file that tells CodeDeploy:

* Which files to copy
* Where to copy them
* Which scripts to run

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2010.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2011.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2012.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2013.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2014.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2015.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2016.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2017.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2018.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2019.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2020.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/0cc4841c791691a67ba867e0d95df17bc274a7b8/Day15%20%3A%20AWS%20End%20to%20End%20Continous%20Delivery%20AWS%20CodeDeploy/Day15%2021.png)

---
