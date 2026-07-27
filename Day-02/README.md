# Day 2: Create an AWS Security Group

## Overview

On Day 2 of my **100 Days of Cloud** journey, I learned how to create and configure an AWS Security Group. Security Groups act as virtual firewalls that control inbound and outbound traffic for AWS resources such as EC2 instances.

---

## Objective

- Understand the purpose of Security Groups.
- Create a new Security Group in AWS.
- Configure inbound and outbound rules.
- Learn the principle of least privilege when granting network access.

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **VPC** → **Security Groups**.
3. Clicked **Create Security Group**.
4. Configured the following:
   - **Security Group Name:** `day2-security-group`
   - **Description:** Security Group for Day 2 Cloud Lab
   - **VPC:** Selected the target VPC.
5. Added inbound rules:
   - SSH (TCP Port 22) from **My IP**
   - HTTP (TCP Port 80) from **0.0.0.0/0**
6. Left the default outbound rule:
   - Allow all outbound traffic.
7. Created the Security Group successfully.

---

## Inbound Rules

| Type | Protocol | Port | Source | Purpose |
|------|----------|------|--------|---------|
| SSH | TCP | 22 | My IP | Secure remote access |
| HTTP | TCP | 80 | 0.0.0.0/0 | Allow web traffic |

---

## Outbound Rules

| Type | Protocol | Destination | Purpose |
|------|----------|-------------|---------|
| All Traffic | All | 0.0.0.0/0 | Allow outbound communication |

---

## What I Learned

- Security Groups are **stateful**, meaning return traffic is automatically allowed.
- Inbound rules control incoming traffic, while outbound rules control outgoing traffic.
- Restricting SSH access to **My IP** improves security.
- Security Groups can be attached to multiple EC2 instances.

---

## Best Practices

- Never allow SSH (Port 22) from `0.0.0.0/0` in production.
- Grant only the permissions that are required.
- Use descriptive names and descriptions for Security Groups.
- Regularly review and remove unused rules.

---

## Screenshot

> Add screenshots of:
>
> - The Security Group details
> - The inbound rules
> - The outbound rules

## Key Takeaways

- Security Groups serve as the first line of defense for EC2 instances.
- They are stateful firewalls that protect AWS resources.
- Properly configured Security Groups are essential for securing cloud infrastructure.

---

## Progress

- ✅ Day 2 Completed
