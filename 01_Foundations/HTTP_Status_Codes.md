# HTTP Status Codes

## What Are HTTP Status Codes?

HTTP status codes are standard response codes returned by servers when a
client makes a request.

They tell us whether the request was successful or failed.

------------------------------------------------------------------------

## Categories of Status Codes

  Range   Meaning
  ------- ---------------
  1xx     Informational
  2xx     Success
  3xx     Redirection
  4xx     Client Error
  5xx     Server Error

------------------------------------------------------------------------

## Commonly Used Status Codes

### 200 -- OK

Request successful.

### 201 -- Created

Resource successfully created.

### 400 -- Bad Request

Client sent invalid request.

### 401 -- Unauthorized

Authentication required or missing.

### 403 -- Forbidden

Authenticated but not allowed.

### 404 -- Not Found

Resource does not exist.

### 500 -- Internal Server Error

Server-side failure.

------------------------------------------------------------------------

## 401 vs 403 (Important)

401 → Who are you?\
403 → I know you, but you are not allowed.

------------------------------------------------------------------------

## Real Project Usage

-   YouTube API disabled → 403 error\
-   Missing credentials → 401 error\
-   Wrong endpoint → 404 error

------------------------------------------------------------------------

## Interview Questions

Q: What is difference between 401 and 403?\
A: 401 means not authenticated, 403 means not authorized.

Q: What does 500 indicate?\
A: Server-side failure.
