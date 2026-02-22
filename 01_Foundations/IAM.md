# IAM (Identity and Access Management)

## What is IAM?

IAM stands for Identity and Access Management.

It controls: - Who can access resources - What actions they can perform

------------------------------------------------------------------------

## Core Components

### 1. Identity

Who is accessing? - User - Service Account - Group

### 2. Role

What permissions are granted?

Example: - roles/viewer - roles/editor - roles/owner -
roles/dataflow.admin

### 3. Policy

Binding between identity and role.

------------------------------------------------------------------------

## Why IAM Is Important

Even if API is enabled: Without proper IAM roles → You get 403 error.

------------------------------------------------------------------------

## Real Project Example

If Dataflow job fails with 403: It means service account does not have
required role like:

roles/dataflow.admin

------------------------------------------------------------------------

## Principle of Least Privilege

Give minimum permissions required. Never give Owner role in production.

------------------------------------------------------------------------

## Interview Questions

Q: What causes 403 error in GCP?\
A: Missing IAM permission.

Q: What is service account?\
A: Identity used by applications instead of humans.
