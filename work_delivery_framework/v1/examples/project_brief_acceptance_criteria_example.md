# Project Brief Acceptance Criteria Example

## 1. Example Purpose

This example shows the expected hybrid Gherkin shape for embedded acceptance criteria in the `Initiative Definition / Project Brief`.

## 2. Example Criteria

### 2.1 AC-001 Order Creation

Given a registered user with valid credentials
When they submit a valid order request
Then the system creates the order with status `pending`
  - Metric: HTTP 201 and response time less than 300ms at p95
  - Validation method: API response inspection plus order-record query
  - Holdout example: Input `{"item":"widget","qty":2}` produces an order ID and `status=pending`

### 2.2 AC-002 Duplicate Submission Handling

Given a user submits the same idempotent request twice within the permitted retry window
When the second request is received
Then the system returns the original successful result without creating a duplicate order
  - Metric: exactly one order record exists for the request key
  - Validation method: request replay test plus database query
  - Holdout example: two identical requests with the same idempotency key return one created order and no duplicate record
