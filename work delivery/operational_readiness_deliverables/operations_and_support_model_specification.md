# Operations & Support Model Specification

## 1. Purpose and Intended Outcome

The Operations & Support Model defines who owns the live service, how support is structured, where escalation occurs, and what operating assumptions govern steady-state service.

It exists to make long-term accountability explicit and to prevent unsupported handover. A useful model shows who owns the service, who supports it, how incidents and escalations move, and what constraints or dependencies affect support.

The intended outcome is that the live service remains supportable beyond the delivery team, with clear ownership, support boundaries, escalation paths, and sustainable operating responsibilities.

## 2. When It Is Required

This artifact is required when the initiative creates or changes a service, application, integration, or platform component that must be operated after delivery.

## 3. Intended Readers and Users

- IT Operations / Service Owner
- Support Owner and support teams
- Delivery Owner
- Business Owner where service outcomes matter

## 4. Intended Project Context

Use this artifact before go-live or formal handover. It is most useful where support must continue beyond the delivery team and where boundaries between teams, vendors, or service tiers must be explicit.

It should align with ITIL 4 Service Desk, Incident Management, Monitoring and Event Management, and Relationship Management practices by making service accountability, support channels, and escalation paths clear.

## 5. How Much Detail to Include

Include enough detail to show ownership, support boundaries, escalation paths, monitoring expectations, and transition assumptions. Do not turn it into a full runbook.

## 6. Required Content or Minimum Structure

### 6.1. Service ownership

Must include:

- named Service Owner
- named Support Owner
- short statement of what each is accountable for

This section shows who is responsible for the live service.

### 6.2. Support structure

Must include:

- support tiers or equivalent responsibility split
- internal and external support boundaries
- vendor or partner dependencies where relevant
- note of any known concentration risk, such as reliance on one specialist, one vendor path, or one team for critical support knowledge

This section defines how support is organized.

### 6.3. Escalation and response model

Must include:

- escalation paths
- escalation triggers or conditions
- incident or support response expectations where relevant
- decision points for when issues must be transferred from delivery or hypercare into steady-state support ownership

This section shows how issues move when they cannot be resolved at the first point of contact.

### 6.4. Monitoring and operating assumptions

Must include:

- monitoring expectations
- support coverage or service hours where relevant
- hypercare, transition, and steady-state assumptions
- operational constraints or risks that affect supportability
- any service-level assumptions, priority handling rules, or dependency obligations that materially affect support expectations

This section connects support ownership to the real operating model.

### 6.5. Template guide

Recommended summary table:

| Area | Owner | Boundary or responsibility | Escalation path | Notes |
| --- | --- | --- | --- | --- |

Use short entries and point to detailed procedures elsewhere.

## 7. What to Keep Out

Keep the following out of this artifact:

- full troubleshooting procedures
- detailed deployment steps
- deep technical design
- project task assignments

## 8. Relationships to Other Artifacts

This artifact should align with the Technical Design Document, System Administration Guide, Backup, Restore & Recovery Plan, Operational Readiness Confirmation Record, and monitoring or audit designs where applicable.

## 9. Ownership, Review, and Acceptance Expectations

The Service Owner or operational lead usually owns this artifact with support from the Delivery Owner and support leads.

It should be reviewed as part of operational readiness and handover.

## 10. Maintenance Expectations

Keep it current when ownership, support coverage, escalation, vendor dependencies, or operating assumptions change.

## 11. Validation Guide

- Are service and support ownership explicit?
- Can a reviewer see who supports what and when escalation happens?
- Are concentration risks, dependency assumptions, and transition-to-steady-state expectations visible?
- Are transition assumptions and known operational constraints visible?
- Does the artifact define the operating model without drifting into runbook detail?

If weak, clarify the responsibility split and make escalation routes easier to follow.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft an Operations & Support Model for this solution.
> Define service ownership, support ownership, support tiers or boundaries, escalation paths, monitoring expectations, support coverage, and the transition or steady-state assumptions that matter after go-live.
