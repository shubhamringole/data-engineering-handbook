# Networking Basics for Cloud

## What is Networking?

Networking allows systems to communicate over a network.

In cloud, networking controls how services talk to each other.

------------------------------------------------------------------------

## Key Concepts

### 1. IP Address

Unique address of a machine.

### 2. DNS

Translates domain name into IP address.

### 3. Port

Logical communication endpoint. Example: - 80 → HTTP - 443 → HTTPS

### 4. VPC (Virtual Private Cloud)

Private network inside cloud.

### 5. Firewall

Controls incoming and outgoing traffic.

------------------------------------------------------------------------

## Public vs Private

Public IP → Accessible from internet\
Private IP → Internal communication only

------------------------------------------------------------------------

## In GCP Context

-   Dataflow runs inside VPC
-   Cloud Functions may use public endpoints
-   Firewalls control traffic rules

------------------------------------------------------------------------

## Interview Questions

Q: What is difference between public and private IP?\
A: Public accessible from internet, private only internal.

Q: Why is VPC important?\
A: It isolates and secures cloud resources.
