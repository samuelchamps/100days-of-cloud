# Day 11: Attach an Elastic Network Interface to an EC2 Instance

## Overview

On Day 11 of my **100 Days of Cloud** journey, I learned how to create and attach an **Elastic Network Interface (ENI)** to an Amazon EC2 instance.

An Elastic Network Interface is a virtual network interface that allows an EC2 instance to communicate within a VPC. An ENI can have its own private IPv4 address, security groups, and other network attributes.

---

## Objective

- Understand what an Elastic Network Interface (ENI) is.
- Create an additional ENI in a VPC subnet.
- Attach the ENI to an existing EC2 instance.
- Understand how multiple network interfaces can be used with EC2.

---

## Prerequisites

- AWS Account
- Existing VPC
- Existing subnet
- Running EC2 instance
- Existing Security Group
- Appropriate IAM permissions

---

## Steps Performed

1. Logged in to the **AWS Management Console**.
2. Navigated to the **EC2 Dashboard**.
3. Selected **Network Interfaces** under **Network & Security**.
4. Clicked **Create network interface**.
5. Configured the network interface:
   - **Description:** `day11-eni`
   - **Subnet:** Selected the target subnet.
   - **Private IPv4 address:** Automatic
   - **Security Group:** Selected the existing Security Group.
6. Clicked **Create network interface**.
7. Selected the newly created ENI.
8. Clicked **Actions** → **Attach**.
9. Selected the target EC2 instance.
10. Confirmed the attachment.
11. Verified that the ENI was attached successfully to the EC2 instance.

---

## ENI Configuration

| Setting | Value |
|---|---|
| Network Interface | `day11-eni` |
| VPC | Existing VPC |
| Subnet | Existing Subnet |
| Private IPv4 | Automatically assigned |
| Security Group | Existing Security Group |
| Attachment | EC2 Instance |

> **Note:** Replace the example values above with the actual values used during the lab.

---

## What I Learned

- An **Elastic Network Interface (ENI)** is a virtual network interface in an AWS VPC.
- An ENI can have one or more private IPv4 addresses.
- ENIs can be associated with Security Groups.
- An ENI can be attached to an EC2 instance.
- EC2 instances can have multiple network interfaces, depending on the instance type.
- ENIs are associated with a specific Availability Zone through their subnet.

---

## Primary vs Secondary Network Interface

The first network interface attached to an EC2 instance is typically the **primary network interface (eth0)**.

Additional network interfaces are called **secondary network interfaces**.

Example:

```text
EC2 Instance
     |
     +--- eth0 → Primary ENI
     |
     +--- eth1 → Secondary ENI
```

The secondary ENI can provide an additional private IP address and network connectivity.

---

## Use Cases for ENIs

Elastic Network Interfaces can be useful for:

- Separating network traffic
- Running network appliances
- Connecting applications to different networks
- Failover configurations
- Assigning additional private IP addresses
- Supporting workloads that require multiple network interfaces

---

## Best Practices

- Attach ENIs only when additional network connectivity is required.
- Use appropriate Security Groups for each network interface.
- Keep track of unused ENIs and remove them when they are no longer needed.
- Ensure the ENI and EC2 instance are in compatible Availability Zones.
- Follow the principle of least privilege when configuring network access.

---

## Key Takeaways

- An ENI is a virtual network interface within an AWS VPC.
- EC2 instances can have multiple network interfaces.
- Each ENI can have its own private IP addresses and Security Groups.
- ENIs provide flexibility when designing AWS network architectures.
- Understanding ENIs is important for designing advanced VPC and EC2 architectures.

---
