---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 16 Notes

## AWS CloudWatch

---

## What is AWS CloudWatch?

Amazon CloudWatch is a monitoring and observability service in AWS that helps you track, analyze, and respond to system performance, logs, and events.

CloudWatch helps you see what is happening in your AWS environment in real time.

---

## Core Concepts

1. Monitoring
2. Alerting
3. Reporting
4. Logging

---

## Important Features

### 1. Monitoring

* Real-time infrastructure monitoring
* Automatic metric collection
* Custom dashboards

---

### 2. Real-Life Metrics (Examples)

#### For EC2:

* CPU Utilization
* Network Traffic
* Status Check Failed

#### For RDS:

* DB Connections
* Read/Write IOPS

#### For Lambda:

* Invocations
* Errors
* Duration

---

### 3. Alarms

* Threshold-based alerts
* Email notifications
* Auto-scaling triggers
* Automated recovery actions

---

### 4. Log Insights

CloudWatch Log Insights allows you to:

* Run queries on logs
* Filter error messages
* Analyze application failures
* Troubleshoot quickly

It works like a log search engine.

---

### 5. Custom Metrics

You can push your own metrics to CloudWatch.

Examples:

* Application response time
* Number of active users
* Custom business KPIs

This is useful for monitoring application-level performance.

---

### 6. Cost Optimization

CloudWatch helps in:

* Identifying underutilized EC2 instances
* Detecting idle resources
* Monitoring usage patterns
* Optimizing Auto Scaling

This reduces unnecessary AWS costs.

---

### 7. Scaling

CloudWatch integrates with:

* Auto Scaling Groups

If CPU > 80% → Launch new EC2
If CPU < 20% → Terminate EC2

This ensures:

* High availability
* Performance stability
* Cost efficiency

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2010.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2011.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2012.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2013.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2014.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2015.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/a25c262640be8eadddfbbf98b9c7b7bfbc4cf79f/Day16%20%3A%20AWS%20CLOUD%20WATCH/Day16%2016.png)

---
