# Day 7: Change an Amazon EC2 Instance Type

## Overview

On Day 7 of my **100 Days of Cloud** journey, I learned how to change the instance type of an existing Amazon EC2 instance. Changing the instance type allows you to scale your compute resources up or down based on your application's performance requirements without creating a new instance.

---

## Objective

- Learn how to modify an EC2 instance type.
- Understand when and why to resize an EC2 instance.
- Stop, modify, and restart an EC2 instance safely.
- Verify that the instance is running with the new instance type.

---

## Prerequisites

- AWS Account
- An existing EC2 instance
- Appropriate IAM permissions

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **EC2 Dashboard**.
3. Selected the existing EC2 instance.
4. Stopped the instance.
5. Waited for the instance state to change to **Stopped**.
6. Clicked **Actions** → **Instance settings** → **Change instance type**.
7. Selected the desired instance type (e.g., `t2.small`).
8. Saved the changes.
9. Started the EC2 instance.
10. Verified that the instance was running with the new instance type.

---

## Instance Configuration

| Setting | Before | After |
|---------|--------|-------|
| Instance Type | t2.micro | t2.small *(Example)* |
| Instance State | Running | Running |
| Availability Zone | us-east-1a | us-east-1a |

> **Note:** Replace the example instance types above with the ones you actually used.

---

## What I Learned

- EC2 instance types determine the amount of CPU, memory, networking, and storage performance available to an instance.
- Most instance type changes require the instance to be stopped before modification.
- Changing the instance type does not affect the data stored on the attached Amazon EBS volumes.
- Selecting the appropriate instance type helps optimize both performance and cost.

---

## Why Change an Instance Type?

Common reasons include:

- Improve application performance.
- Increase CPU or memory resources.
- Reduce infrastructure costs by downsizing.
- Support changing workload requirements.

---

## Best Practices

- Stop the instance before changing its instance type.
- Verify that the selected instance type is supported in your Availability Zone.
- Monitor CPU and memory utilization before resizing.
- Choose the smallest instance type that meets your workload requirements to optimize costs.

---
## Key Takeaways

- EC2 instances can be resized to match application requirements.
- Stopping an instance is generally required before changing its instance type.
- Amazon EBS volumes remain attached after the instance type is changed.
- Proper instance sizing helps balance performance and cost.

---
