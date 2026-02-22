# Terraform Backends

## What is a Backend?

Backend defines where Terraform stores state file.

------------------------------------------------------------------------

## Default Backend

Local backend: Stores state in local file.

------------------------------------------------------------------------

## Remote Backend Example (GCS)

terraform { backend "gcs" { bucket = "my-terraform-state" prefix = "dev"
} }

------------------------------------------------------------------------

## Why Remote Backend Is Important

-   Team collaboration
-   State locking
-   Secure storage
-   Prevents accidental deletion

------------------------------------------------------------------------

## State Locking

Prevents multiple users from modifying infrastructure at same time.

------------------------------------------------------------------------

## Interview Questions

Q: Why use remote backend?\
A: To securely store and share state file.

Q: What is state locking?\
A: Prevents concurrent infrastructure changes.
