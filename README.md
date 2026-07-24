# Day 1: Create an AWS EC2 Key Pair

## Overview

Today, I completed the first task in my **100 Days of Cloud** journey by creating an EC2 Key Pair in AWS. A key pair is used to securely connect to EC2 instances using SSH authentication instead of passwords.

---

## Objective

- Understand what an EC2 Key Pair is.
- Create a new Key Pair in the AWS Management Console.
- Download and securely store the private key.

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to **EC2 Dashboard**.
3. Selected **Key Pairs** under **Network & Security**.
4. Clicked **Create Key Pair**.
5. Configured the Key Pair:
   - **Name:** `100days-keypair`
   - **Key Pair Type:** RSA
   - **Private Key Format:** `.pem`
6. Created the Key Pair.
7. Downloaded the private key (`100days-keypair.pem`) and stored it securely.

---

## What I Learned

- An EC2 Key Pair consists of a **public key** stored by AWS and a **private key** downloaded by the user.
- The private key is required to securely connect to Linux EC2 instances using SSH.
- AWS does not allow the private key to be downloaded again after creation, so it must be stored safely.

---

## Key Takeaways

- Password authentication is disabled by default for many EC2 instances.
- SSH Key Pairs provide a more secure authentication method.
- Losing the private key means you may lose SSH access to your EC2 instance.

---

## Progress

- ✅ Day 1 Completed
