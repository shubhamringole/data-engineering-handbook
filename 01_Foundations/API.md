# API (Application Programming Interface)

## 1️⃣ What is an API?

API stands for **Application Programming Interface**.

An API allows one software system to communicate with another software
system.

In simple words:

> API is a messenger that takes your request to another service and
> brings back the response.

------------------------------------------------------------------------

## 2️⃣ Real-Life Analogy

Imagine you are in a restaurant:

-   You = Client\
-   Kitchen = Server\
-   Waiter = API

You tell the waiter what you want.\
The waiter takes your order to the kitchen.\
The kitchen prepares the food.\
The waiter brings it back.

You never go inside the kitchen.

Similarly:

Your application never directly controls Google Cloud services.\
It sends requests through APIs.

------------------------------------------------------------------------

## 3️⃣ What is an API in Google Cloud?

In Google Cloud, every service works through APIs.

Examples: - Cloud Functions API - Dataflow API - BigQuery API - Pub/Sub
API - Cloud Natural Language API - YouTube Data API

When we "Enable API" in GCP, we are telling Google:

> "Allow this project to use this service programmatically."

Without enabling API: - Terraform cannot create resources - gcloud CLI
commands fail - Python code fails - Deployment fails

------------------------------------------------------------------------

## 4️⃣ How API Works (Technically)

Most cloud APIs use HTTP requests.

Example:

POST https://dataflow.googleapis.com/v1/projects/project-id/jobs

Client sends request → Google processes → Returns response (JSON)

Common HTTP Status Codes:

-   200 → Success
-   400 → Bad request
-   401 → Unauthorized (No authentication)
-   403 → Forbidden (No permission)
-   404 → Not found
-   500 → Server error

------------------------------------------------------------------------

## 5️⃣ Types of APIs in My Projects

### Infrastructure APIs

Used by Terraform or CLI to create resources.

Examples: - Dataflow API - Cloud Functions API - Cloud Composer API -
Cloud Run Admin API

If disabled → Terraform apply fails.

### Business Logic APIs

Used by application code.

Examples: - YouTube Data API v3 - Cloud Natural Language API

If disabled → Python script returns 403 error.

------------------------------------------------------------------------

## 6️⃣ Why APIs Must Be Enabled in GCP

Google Cloud services are isolated microservices.

If API is not enabled: - You cannot use that service. - Requests are
rejected. - You get HTTP 403 error.

Example Error:

403: Access Not Configured. API has not been used in project before.

------------------------------------------------------------------------

## 7️⃣ Difference Between 401 and 403

  Error Code   Meaning
  ------------ ----------------------------------
  401          Not authenticated
  403          Authenticated but not authorized
  404          Resource not found

401 = Who are you?\
403 = I know who you are, but you are not allowed.

------------------------------------------------------------------------

## 8️⃣ How APIs Are Used in My Terraform Project

In my YouTube Sentiment Pipeline:

-   Terraform calls Dataflow API to start streaming jobs.
-   Terraform calls BigQuery API to create datasets.
-   Terraform calls Pub/Sub API to create topics.
-   Python code calls YouTube Data API to fetch comments.
-   ML script calls Natural Language API for sentiment scoring.

Everything depends on APIs.

------------------------------------------------------------------------

## 9️⃣ How to Enable an API in GCP

Using gcloud CLI:

gcloud services enable dataflow.googleapis.com

Using Terraform:

resource "google_project_service" "dataflow" { service =
"dataflow.googleapis.com" }

------------------------------------------------------------------------

## 🔟 Key Takeaways

-   API allows communication between software systems.
-   Google Cloud services are accessed via APIs.
-   APIs must be enabled per project.
-   403 error usually means permission issue or API not enabled.
-   Terraform, gcloud, and Python scripts all use APIs behind the
    scenes.

------------------------------------------------------------------------

## 🎯 Interview Questions

**Q1: What happens if Dataflow API is disabled?**\
Terraform apply fails with API not enabled error.

**Q2: What is difference between 401 and 403?**\
401 = Not authenticated\
403 = Not authorized

**Q3: Why do we need to enable APIs in GCP?**\
Because GCP services are isolated microservices and must be activated
before use.

**Q4: How does Terraform create GCP resources?**\
Terraform calls GCP service APIs behind the scenes.

------------------------------------------------------------------------

## 📌 Final Understanding

API is the foundation of: - Cloud computing - Microservices
architecture - Infrastructure as Code - Modern application development

Without APIs, cloud systems cannot function.
