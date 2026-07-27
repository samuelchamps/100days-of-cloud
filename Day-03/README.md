# Day 3: Create an AWS Subnet

## Overview

On Day 3 of my **100 Days of Cloud** journey, I learned how to create a subnet within an Amazon Virtual Private Cloud (VPC). Subnets allow you to divide a VPC into smaller, isolated networks, making it easier to organize resources and control network traffic.

---

## Objective

- Understand the purpose of subnets in AWS.
- Create a subnet within a VPC.
- Learn the difference between public and private subnets.
- Understand CIDR block allocation and subnet sizing.

---

## Prerequisites

- AWS Account
- An existing VPC
- Appropriate IAM permissions to manage VPC resources

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **VPC Dashboard**.
3. Selected **Subnets**.
4. Clicked **Create Subnet**.
5. Selected the target VPC.
6. Entered the subnet details:
   - **Subnet Name:** `day3-public-subnet`
   - **Availability Zone:** `us-east-1a`
   - **IPv4 CIDR Block:** `10.0.1.0/24`
7. Reviewed the configuration.
8. Clicked **Create Subnet**.

---

## Subnet Configuration

| Setting | Value |
|----------|-------|
| VPC CIDR | `10.0.0.0/16` |
| Subnet Name | `day3-public-subnet` |
| Availability Zone | `us-east-1a` |
| Subnet CIDR | `10.0.1.0/24` |

---

## What I Learned

- A subnet is a smaller network within a VPC.
- Every subnet must have a unique CIDR block that does not overlap with other subnets in the same VPC.
- Public subnets are typically used for internet-facing resources, while private subnets host internal services such as databases and application servers.
- AWS reserves the first four IP addresses and the last IP address in every subnet.

---

## Challenges Encountered

While creating the subnet, I initially received the following error:

```
CIDR Address overlaps with existing Subnet CIDR.
```

This happened because the subnet CIDR block I selected overlapped with an existing subnet in the VPC. I resolved the issue by choosing a non-overlapping CIDR block within the VPC's address range.

---

## Best Practices

- Plan your VPC and subnet CIDR ranges before deployment.
- Avoid overlapping CIDR blocks.
- Separate public and private resources into different subnets.
- Use multiple Availability Zones for high availability.

---

## Key Takeaways

- Subnets improve network organization and security.
- Careful CIDR planning prevents address conflicts.
- Public and private subnet design is a fundamental concept in AWS networking.

---

