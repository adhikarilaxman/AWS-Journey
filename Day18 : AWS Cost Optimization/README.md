---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 18 Notes

# AWS Cost Optimization

---

## AWS Cost Optimization

AWS Cost Optimization means reducing unnecessary AWS spending while maintaining performance and availability.

It focuses on:

* Removing unused resources
* Right-sizing instances
* Using proper pricing models
* Automating cleanup

### Monitoring Tools

* AWS Cost Explorer
* CloudWatch
* Trusted Advisor

---

# Amazon EBS Volume

## What is EBS?

Amazon Elastic Block Store (EBS) is a block storage service used with EC2 instances.

EBS is like a hard disk attached to an EC2 server.

---

# EBS Snapshot

## What is a Snapshot?

An EBS Snapshot is a backup of an EBS volume stored in Amazon S3.

It is:

* Used for backup
* Used for disaster recovery
* Used for cloning volumes
* Incremental in nature

Snapshots also cost money based on storage used.

---

# What is Stale?

Stale means data or resources that are outdated or no longer actively used.

### Examples in AWS Context

* Stale EBS snapshot → A snapshot not used anymore
* Stale volume → Volume not attached to any instance
* Stale DNS cache → Old DNS records
* Stale credentials → Expired access keys

---

# Identifying Stale EBS Snapshots

## Problem

Sometimes:

* EC2 instance is deleted
* EBS volume is deleted
* But snapshot remains

These unused snapshots are called stale snapshots.

They increase storage cost unnecessarily.

---

# Solution Using AWS Lambda

We can create a Lambda function that:

* Fetches all EBS snapshots owned by the account (`self`)
* Fetches all active EC2 instances (running)
* Checks whether snapshot’s volume is attached to any active instance
* If not → Deletes the snapshot
* Saves storage cost automatically

---

# How It Works (Architecture Flow)

EC2 → EBS Volume → Snapshot →
Lambda checks usage → Deletes stale snapshot → Cost optimized

---

# ebs_stale-snapshots.py

```python
import boto3

def lambda_handler(event, context):
    ec2 = boto3.client('ec2')

    # Get all EBS snapshots
    response = ec2.describe_snapshots(OwnerIds=['self'])

    # Get all active EC2 instance IDs
    instances_response = ec2.describe_instances(
        Filters=[{'Name': 'instance-state-name', 'Values': ['running']}]
    )
    active_instance_ids = set()

    for reservation in instances_response['Reservations']:
        for instance in reservation['Instances']:
            active_instance_ids.add(instance['InstanceId'])

    # Iterate through each snapshot
    for snapshot in response['Snapshots']:
        snapshot_id = snapshot['SnapshotId']
        volume_id = snapshot.get('VolumeId')

        if not volume_id:
            # Delete snapshot if not attached to any volume
            ec2.delete_snapshot(SnapshotId=snapshot_id)
            print(f"Deleted EBS snapshot {snapshot_id} as it was not attached to any volume.")
        else:
            try:
                volume_response = ec2.describe_volumes(VolumeIds=[volume_id])
                if not volume_response['Volumes'][0]['Attachments']:
                    ec2.delete_snapshot(SnapshotId=snapshot_id)
                    print(f"Deleted EBS snapshot {snapshot_id} as it was taken from a volume not attached to any running instance.")
            except ec2.exceptions.ClientError as e:
                if e.response['Error']['Code'] == 'InvalidVolume.NotFound':
                    ec2.delete_snapshot(SnapshotId=snapshot_id)
                    print(f"Deleted EBS snapshot {snapshot_id} as its associated volume was not found.")
```

---

# Screenshots

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
