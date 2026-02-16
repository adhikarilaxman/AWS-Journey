---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 13 Notes

## AWS CodePipeline

### What is AWS CodePipeline?

--> AWS CodePipeline is a fully managed Continuous Integration and Continuous Delivery (CI/CD) service that automates the build, test, and deployment phases of your application release process.

In simple words:
It automates the flow — **Source → Build → Test → Deploy**.

Whenever code changes → Pipeline automatically triggers.

---

## How CodePipeline Works

A pipeline consists of stages:

### 1. Source Stage

Code from:

* AWS CodeCommit
* GitHub
* S3

### 2. Build Stage

Uses:

* AWS CodeBuild

### 3. Deploy Stage

Uses:

* AWS CodeDeploy
* EC2
* Elastic Beanstalk
* ECS

---

## Jenkins vs AWS CodePipeline

### What is Jenkins?

--> Jenkins is an open-source automation server used to build CI/CD pipelines.

It is self-hosted and highly customizable.

---

## When to Use Jenkins

* Multi-cloud or hybrid environment
* Need advanced customization
* Complex workflows
* Large plugin ecosystem required

---

## When to Use AWS CodePipeline

* Fully AWS-based project
* Want minimal maintenance
* Prefer managed services
* Small to medium CI/CD pipelines

---

## Simple Difference

Jenkins = More control, more maintenance
CodePipeline = Less control, less maintenance

---

## Jenkins

![image]()

## AWS CodePipeline

![image]()
