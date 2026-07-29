# Day 6: Launch an Amazon EC2 Instance

## Overview

On Day 6 of my **100 Days of Cloud** journey, I launched my first Amazon Elastic Compute Cloud (Amazon EC2) instance. EC2 provides secure, scalable virtual servers in the cloud, allowing users to deploy applications without managing physical hardware.

This exercise helped me understand the basic components required to launch an EC2 instance, including Amazon Machine Images (AMIs), instance types, key pairs, security groups, and storage.

---

## Objective

- Launch an Amazon EC2 instance.
- Understand the components involved in launching an EC2 instance.
- Configure networking, storage, and security settings.
- Verify that the instance is running successfully.

---

## Prerequisites

- AWS Account
- Existing EC2 Key Pair
- Security Group
- Amazon VPC and Subnet
- Appropriate IAM permissions

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **EC2 Dashboard**.
3. Clicked **Launch Instance**.
4. Configured the instance:
   - **Name:** `day6-ec2-instance`
   - **Amazon Machine Image (AMI):** Amazon Linux 2023
   - **Instance Type:** `t2.micro` (Free Tier Eligible)
5. Selected the previously created **Key Pair**.
6. Selected the existing **Security Group**.
7. Selected the appropriate **VPC** and **Subnet**.
8. Verified the default **8 GiB gp3** root volume.
9. Reviewed the configuration.
10. Clicked **Launch Instance**.
11. Confirmed that the instance entered the **Running** state.

---

## EC2 Configuration

| Setting | Value |
|---------|-------|
| Name | day6-ec2-instance |
| AMI | Amazon Linux 2023 |
| Instance Type | t2.micro |
| Key Pair | Existing Key Pair |
| Security Group | Existing Security Group |
| Storage | 8 GiB gp3 |
| State | Running |

---

## What I Learned

- Amazon EC2 allows users to provision virtual servers on demand.
- An Amazon Machine Image (AMI) contains the operating system and software required to launch an instance.
- A Security Group controls inbound and outbound traffic to the instance.
- A Key Pair is required for secure SSH access to Linux instances.
- Every EC2 instance requires an Amazon EBS root volume for storage.

---

## Best Practices

- Use the principle of least privilege when configuring Security Groups.
- Restrict SSH (Port 22) access to your IP address.
- Stop or terminate unused EC2 instances to avoid unnecessary charges.
- Tag AWS resources for easier management and cost tracking.

---

## Key Takeaways

- Amazon EC2 provides scalable and flexible cloud computing resources.
- Launching an EC2 instance requires an AMI, instance type, networking configuration, storage, and security settings.
- Security Groups and Key Pairs are essential for securing EC2 instances.
- Monitoring the instance state ensures that it is successfully provisioned and ready for use.

---
