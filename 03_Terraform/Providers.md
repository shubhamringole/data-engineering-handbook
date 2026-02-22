# Terraform Providers

## What is a Provider?

A provider is a plugin that allows Terraform to interact with cloud
platforms.

Example: - Google Cloud - AWS - Azure

------------------------------------------------------------------------

## GCP Provider Example

provider "google" { project = var.project_id region = var.region }

This tells Terraform to use Google Cloud APIs.

------------------------------------------------------------------------

## Why Providers Are Important

Without provider: Terraform does not know where to create resources.

Provider handles: - Authentication - API communication - Resource
management

------------------------------------------------------------------------

## Interview Questions

Q: What is a provider in Terraform?\
A: It connects Terraform with external platforms like GCP or AWS.
