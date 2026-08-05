# Day 9: Enable Termination Protection for an Amazon EC2 Instance

## Overview

On Day 9 of my **100 Days of Cloud** journey, I learned how to enable **Termination Protection** for an Amazon EC2 instance. This feature helps prevent accidental deletion of an EC2 instance by blocking termination requests through the AWS Management Console, AWS CLI, and API.

Termination Protection is an important safeguard for production workloads where accidental deletion could result in downtime or data loss.

---

## Objective

- Understand the purpose of EC2 Termination Protection.
- Enable Termination Protection on an existing EC2 instance.
- Verify that the protection is enabled.
- Learn the difference between Stop Protection and Termination Protection.

---

## Prerequisites

- AWS Account
- An existing EC2 instance
- Appropriate IAM permissions to modify EC2 instance settings

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to the **EC2 Dashboard**.
3. Selected the EC2 instance.
4. Clicked **Actions** → **Instance settings** → **Change termination protection**.
5. Selected **Enable**.
6. Saved the changes.
7. Verified that Termination Protection was successfully enabled.

---

## Configuration

| Setting | Value |
|---------|-------|
| EC2 Instance | day6-ec2-instance *(Example)* |
| Termination Protection | Enabled |
| Status | Active |

> **Note:** Replace the instance name above with the one you used.

---

## What I Learned

- Termination Protection prevents accidental deletion of an EC2 instance.
- It is enabled by setting the **DisableApiTermination** attribute to **True**.
- If someone attempts to terminate the instance while protection is enabled, AWS blocks the request.
- To terminate the instance, Termination Protection must first be disabled.

---

## Stop Protection vs Termination Protection

| Feature | Stop Protection | Termination Protection |
|---------|-----------------|-------------------------|
| Prevents accidental stop | ✅ Yes | ❌ No |
| Prevents accidental termination | ❌ No | ✅ Yes |
| Protects against downtime | ✅ Yes | Indirectly |
| Protects against accidental deletion | ❌ No | ✅ Yes |

---

## Why Use Termination Protection?

Termination Protection is useful for:

- Production web servers
- Critical application servers
- Database servers
- Long-running workloads
- Infrastructure that should not be accidentally removed

---

## Best Practices

- Enable Termination Protection for production EC2 instances.
- Combine it with Stop Protection for additional safeguards.
- Restrict termination permissions using IAM policies.
- Regularly review EC2 protection settings during infrastructure audits.

---

## Key Takeaways

- Termination Protection helps prevent accidental deletion of EC2 instances.
- It is a simple but effective feature for improving infrastructure reliability.
- Combining Stop Protection, Termination Protection, and IAM permissions provides stronger operational security.

