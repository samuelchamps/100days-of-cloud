# Day 4: Enable Versioning for an Amazon S3 Bucket

## Overview

On Day 4 of my **100 Days of Cloud** journey, I enabled versioning on an existing Amazon S3 bucket. S3 Versioning allows multiple versions of an object to be stored in the same bucket, helping to protect files from accidental deletion or unintended changes.

---

## Objective

- Understand the purpose of Amazon S3 Versioning.
- Enable versioning on an existing S3 bucket.
- Upload multiple versions of the same object.
- Learn how versioning helps with data protection and recovery.

---

## Prerequisites

- An AWS account
- An existing Amazon S3 bucket
- Appropriate IAM permissions to manage S3 bucket properties

---

## Steps Performed

1. Logged in to the AWS Management Console.
2. Navigated to the **Amazon S3 Console**.
3. Selected the existing S3 bucket.
4. Opened the **Properties** tab.
5. Scrolled to the **Bucket Versioning** section.
6. Clicked **Edit**.
7. Selected **Enable**.
8. Clicked **Save changes**.

---

## Configuration

| Setting | Value |
|---|---|
| AWS Service | Amazon S3 |
| Feature | Bucket Versioning |
| Status | Enabled |
| Purpose | Preserve multiple versions of objects |

---

## Testing Versioning

After enabling versioning, I tested the feature by:

1. Uploading a file to the S3 bucket.
2. Modifying the file locally.
3. Uploading the updated file using the same object name.
4. Opening the **Versions** section in the S3 bucket.
5. Confirming that multiple versions of the object were available.

---

## What I Learned

- S3 Versioning preserves multiple versions of an object in the same bucket.
- Uploading a new file with the same object name creates a new version instead of permanently replacing the previous version.
- Previous versions can be viewed and restored when needed.
- When an object is deleted from a version-enabled bucket, Amazon S3 adds a **delete marker** instead of immediately removing the previous object versions.
- S3 Versioning can help protect data from accidental deletion and unintended changes.

---

## Important Notes

- Once enabled, S3 Versioning cannot be completely disabled; it can only be suspended.
- Suspending versioning does not delete existing object versions.
- Each object version consumes storage and may increase S3 storage costs.
- Lifecycle rules can be used to manage or remove noncurrent object versions.

---

## Key Takeaways

- S3 Versioning improves data protection and recovery.
- Previous versions of objects can be retained after files are updated or deleted.
- Versioning is useful for protecting important data against accidental changes.
- Lifecycle rules can help control the storage costs associated with multiple object versions.

---
