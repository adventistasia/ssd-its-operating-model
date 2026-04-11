# Security And Privacy Risk Assessment - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 - Work Definition Details
Reference baseline: [Functional Capabilities](10_functional_capabilities.md)

## 1. Assessment context

- Scope of the assessment: availability view, HR leave data visibility, itinerary approval visibility, and access boundaries
- Solution or service name: SSD staff itinerary tracker
- Date or version: 2026-04-10 / working draft
- Assessment owner: Delivery Owner / Project Manager

## 2. Risk scenarios

### 2.1. Unauthorized exposure of leave data

- **Threat / misuse / failure scenario:** a user sees more leave detail than they should.
- **Assets or data affected:** leave status, leave date range, identity data.
- **Why it matters:** leave data is controlled HR information and may be personal.
- **Source of exposure:** too-broad access to the combined visibility layer.

### 2.2. Stale or conflicting status shown as truth

- **Threat / misuse / failure scenario:** the tracker shows outdated itinerary or leave status.
- **Assets or data affected:** itinerary approval state, revision metadata, freshness indicators.
- **Why it matters:** staff may make decisions on the wrong availability assumption.
- **Source of exposure:** source refresh failure, mapping error, or revision logic defect.

### 2.3. Shadow copy becomes a false system of record

- **Threat / misuse / failure scenario:** users start editing the tracker as if it were the authoritative record.
- **Assets or data affected:** status records, approvals, revision metadata.
- **Why it matters:** the tracker would undermine the source owners and create governance confusion.
- **Source of exposure:** poor wording, bad permissions, or unclear ownership.

## 3. Impact and severity view

- unauthorized leave exposure: moderate
- stale or conflicting status: moderate
- shadow system of record: high for governance, moderate for technical impact

The overall risk profile is moderate because the data is not highly regulated in the abstract, but it is sensitive enough to require discipline.

## 4. Control and treatment expectations

| Risk | Existing controls | Required controls | Owner |
| --- | --- | --- | --- |
| Unauthorized exposure of leave data | HR ownership and role separation | Role-based access, least privilege, and limited display detail | HR Leave Records Owner |
| Stale or conflicting status shown as truth | Source ownership and revision history | Freshness flag, source refresh checks, and clear stale-state wording | Delivery Owner / Technical SME |
| Shadow copy becomes a false system of record | Formal source ownership | Read-only or controlled update boundaries, source labeling, and user guidance | Angie and Delivery Owner |

## 5. Residual risk statement

Residual risk remains after treatment because the tracker still aggregates information from multiple controlled sources.

This residual risk should be explicitly accepted by the sponsor and domain owners before closure, but it can be managed to a low-to-moderate level if access and source rules stay clear.
