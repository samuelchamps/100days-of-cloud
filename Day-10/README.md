# Day 10: Attach an Elastic IP to an Amazon EC2 Instance

## Overview

On Day 10 of my **100 Days of Cloud** journey, I learned how to allocate and associate an **Elastic IP (EIP)** with an Amazon EC2 instance. An Elastic IP is a static public IPv4 address designed for dynamic cloud computing, allowing an instance to retain the same public IP address even after it is stopped and started.

This is especially useful for hosting websites, applications, or services that require a consistent public IP address.

---

## Objective

- Understand the purpose of an Elastic IP.
- Allocate a new Elastic IP address.
- Associate the Elastic IP with an existing EC2 instance.
- Verify that the instance is accessible using the Elastic IP.

---

## Prerequisites

- AWS Account
- A running Amazon EC2 instance
- Appropriate IAM permissions to manage Elastic IPs

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **EC2 Dashboard**.
3. Selected **Elastic IPs** under **Network & Security**.
4. Clicked **Allocate Elastic IP Address**.
5. Accepted the default settings and allocated the address.
6. Selected the newly created Elastic IP.
7. Clicked **Actions** → **Associate Elastic IP Address**.
8. Selected the target EC2 instance.
9. Confirmed the association.
10. Verified that the EC2 instance was assigned the new Elastic IP address.

---

## Configuration

| Setting | Value |
|---------|-------|
| Resource | Amazon EC2 |
| Elastic IP | Allocated |
| Association | Existing EC2 Instance |
| Status | Associated |

---

## What I Learned

- An Elastic IP is a static public IPv4 address provided by AWS.
- Unlike a standard public IP, an Elastic IP remains the same even if the EC2 instance is stopped and started.
- An Elastic IP can be disassociated from one instance and reassociated with another if needed.
- AWS charges for unused Elastic IPs that are allocated but not associated with a running resource.

---

## Why Use an Elastic IP?

Elastic IPs are useful for:

- Hosting web servers
- Running production applications
- Providing a fixed IP for DNS records
- Simplifying disaster recovery and failover

---

## Best Practices

- Release Elastic IPs that are no longer in use to avoid unnecessary charges.
- Associate Elastic IPs only with resources that require a static public IP.
- Use Route 53 with Elastic IPs for easier DNS management.
- Monitor your Elastic IP usage through AWS Cost Explorer or Billing Dashboard.

---

## Key Takeaways

- Elastic IPs provide a persistent public IP address for EC2 instances.
- They help ensure applications remain reachable even after instance restarts.
- Unused Elastic IPs can incur charges, so they should be released when no longer needed.
- Elastic IPs improve flexibility by allowing IP addresses to be quickly reassigned between instances.

---
