# Terraform State File

## What is Terraform State?

Terraform stores information about managed infrastructure in a file
called:

terraform.tfstate

------------------------------------------------------------------------

## Why State File Is Important

It keeps track of: - Resource IDs - Dependencies - Current
infrastructure status

Without state: Terraform cannot determine what to update.

------------------------------------------------------------------------

## Local vs Remote State

Local State: Stored on your machine.

Remote State: Stored in remote storage like GCS bucket. Used in
production.

------------------------------------------------------------------------

## What Happens If State Is Deleted?

Terraform may: - Recreate resources - Lose track of infrastructure

------------------------------------------------------------------------

## Interview Questions

Q: Why is remote state preferred?\
A: For collaboration and safety.

Q: What happens if state file is corrupted?\
A: Infrastructure management becomes inconsistent.
