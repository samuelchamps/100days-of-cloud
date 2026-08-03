# Day 8: Enable Stop Protection for an Amazon EC2 Instance

## Overview

On Day 8 of my **100 Days of Cloud** journey, I learned how to enable **Stop Protection** for an Amazon EC2 instance. Stop Protection helps prevent an EC2 instance from being accidentally stopped through the AWS Management Console, AWS CLI, or API calls.

This feature is useful for protecting critical workloads from unintended downtime caused by human error.

---

## Objective

- Understand the purpose of EC2 Stop Protection.
- Enable Stop Protection on an existing EC2 instance.
- Verify that the protection is enabled.
- Learn when Stop Protection should be used.

---

## Prerequisites

- AWS Account
- An existing EC2 instance
- Appropriate IAM permissions to modify instance settings

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to the **EC2 Dashboard**.
3. Selected the EC2 instance.
4. Clicked **Actions** → **Instance settings** → **Change stop protection**.
5. Selected **Enable**.
6. Saved the changes.
7. Verified that Stop Protection was successfully enabled.

---

## Configuration

| Setting | Value |
|---------|-------|
| EC2 Instance | day6-ec2-instance *(Example)* |
| Stop Protection | Enabled |
| Status | Active |

> **Note:** Replace the instance name above with the one you used.

---

## What I Learned

- Stop Protection prevents an EC2 instance from being accidentally stopped.
- It helps improve the availability of critical workloads.
- Stop Protection does **not** prevent an instance from being terminated.
- To stop a protected instance, Stop Protection must first be disabled.

---

## Stop Protection vs Termination Protection

| Feature | Stop Protection | Termination Protection |
|---------|-----------------|-------------------------|
| Prevents accidental stop | ✅ Yes | ❌ No |
| Prevents accidental termination | ❌ No | ✅ Yes |
| Can be disabled | ✅ Yes | ✅ Yes |

---

## Use Cases

- Production web servers
- Application servers
- Database servers
- Critical business workloads
- Long-running batch processing jobs

---

## Best Practices

- Enable Stop Protection for critical production instances.
- Combine Stop Protection with Termination Protection for maximum safety.
- Use IAM policies to restrict who can modify instance settings.
- Regularly review protection settings as part of infrastructure management.

---

## Key Takeaways

- Stop Protection reduces the risk of accidental service interruptions.
- It is an important safeguard for production environments.
- Stop Protection and Termination Protection serve different purposes and can be used together for enhanced protection.

---
