# Day 5: Create an Amazon EBS gp3 Volume

## Overview

On Day 5 of my **100 Days of Cloud** journey, I learned how to create an **Amazon Elastic Block Store (Amazon EBS) gp3 volume**. Amazon EBS provides persistent block storage for Amazon EC2 instances, making it suitable for operating systems, applications, and databases.

The **gp3** volume type is the latest generation of General Purpose SSD storage, offering high performance and cost efficiency.

---

## Objective

- Understand the purpose of Amazon EBS.
- Create a General Purpose SSD (gp3) volume.
- Learn the characteristics and use cases of gp3 volumes.
- Prepare the volume for attachment to an EC2 instance.

---

## Prerequisites

- AWS Account
- Appropriate IAM permissions
- Access to the Amazon EC2 Console

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **EC2 Dashboard**.
3. Selected **Elastic Block Store** → **Volumes**.
4. Clicked **Create Volume**.
5. Configured the volume with the following settings:
   - **Volume Type:** General Purpose SSD (gp3)
   - **Size:** 8 GiB
   - **Availability Zone:** `us-east-1a` (or the same AZ as the EC2 instance)
6. Reviewed the configuration.
7. Clicked **Create Volume**.
8. Verified that the volume was successfully created.

---

## Volume Configuration

| Setting | Value |
|---------|-------|
| Volume Type | gp3 |
| Size | 8 GiB |
| Availability Zone | us-east-1a |
| Encryption | Default AWS-managed key (optional) |
| Status | Available |

---

## What I Learned

- Amazon EBS provides persistent block storage for EC2 instances.
- A gp3 volume delivers SSD performance for a wide range of workloads.
- EBS volumes must be created in the same Availability Zone as the EC2 instance they will be attached to.
- A newly created EBS volume is empty until it is attached, partitioned, formatted, and mounted.

---

## Why gp3?

Compared to gp2, gp3 offers:

- Better price-to-performance ratio.
- Independent configuration of storage size and performance.
- Consistent baseline performance.
- Suitable for most production workloads.

---

## Best Practices

- Create EBS volumes in the same Availability Zone as the target EC2 instance.
- Enable encryption for sensitive data.
- Take regular snapshots for backup and disaster recovery.
- Delete unused volumes to avoid unnecessary costs.

---

## Key Takeaways

- Amazon EBS provides durable block storage for EC2 instances.
- gp3 is the recommended General Purpose SSD volume type for most workloads.
- EBS volumes are Availability Zone-specific.
- A volume must be attached to an EC2 instance before it can be used.

---
