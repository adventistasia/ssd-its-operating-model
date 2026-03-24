# Operations & Support Model Specification

## 1. Purpose and Intended Outcome

The Operations & Support Model defines who owns the live service, how support is structured, where escalation occurs, and what operating assumptions govern steady-state service.

It exists to make long-term accountability explicit and to prevent unsupported handover. A useful model shows who owns the service, who supports it, how incidents and escalations move, and what constraints or dependencies affect support.

The intended outcome is that the live service remains supportable beyond the delivery team, with clear ownership, support boundaries, escalation paths, and sustainable operating responsibilities.

## 2. When It Is Required

This artifact is required when the initiative creates or changes a service, application, integration, or platform component that must be operated after delivery.

## 3. Stage Fit and Handoffs

- Stage 4: define the target support model and ownership boundaries early enough to influence design.
- Stage 6: confirm the model against real deployment and support arrangements.
- Stage 7: use this model as part of operational acceptance and transition evidence.

Upstream sources:

- [Technical Design Document Specification](technical_design_document_specification.md)
- [DevOps Guide Specification](devops_guide_specification.md)
- [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md)

Downstream artifacts:

- [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)
- [Formal Acceptance and Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

## 4. Intended Readers and Users

- IT Operations / Service Owner
- Support Owner and support teams
- Delivery Owner
- Business Owner where service outcomes matter

## 5. Intended Project Context

Use this artifact during solution design, before go-live, and at formal handover. It is most useful where support must continue beyond the delivery team and where boundaries between teams, vendors, or service tiers must be explicit.

It should align with ITIL 4 Service Desk, Incident Management, Monitoring and Event Management, and Relationship Management practices by making service accountability, support channels, and escalation paths clear.

## 6. How Much Detail to Include

Include enough detail to show ownership, support boundaries, escalation paths, monitoring expectations, and transition assumptions. Do not turn it into a full runbook.

## 7. Required Content or Minimum Structure

### 7.1. Service ownership

Must include:

- named Service Owner
- named Support Owner
- short statement of what each is accountable for

This section shows who is responsible for the live service.

### 7.2. Support structure

Must include:

- support tiers or equivalent responsibility split
- internal and external support boundaries
- vendor or partner dependencies where relevant
- note of any known concentration risk, such as reliance on one specialist, one vendor path, or one team for critical support knowledge

This section defines how support is organized.

### 7.3. Escalation and response model

Must include:

- escalation paths
- escalation triggers or conditions
- incident or support response expectations where relevant
- decision points for when issues must be transferred from delivery or hypercare into steady-state support ownership

This section shows how issues move when they cannot be resolved at the first point of contact.

### 7.4. Monitoring and operating assumptions

Must include:

- monitoring expectations
- support coverage or service hours where relevant
- hypercare, transition, and steady-state assumptions
- operational constraints or risks that affect supportability
- any service-level assumptions, priority handling rules, or dependency obligations that materially affect support expectations

This section connects support ownership to the real operating model.

### 7.5. Template guide

Recommended summary table:

| Area | Owner | Boundary or responsibility | Escalation path | Notes |
| --- | --- | --- | --- | --- |

Use short entries and point to detailed procedures elsewhere.

## 8. What to Keep Out

Keep the following out of this artifact:

- full troubleshooting procedures
- detailed deployment steps
- deep technical design
- project task assignments

## 9. Relationships to Other Artifacts

This artifact should align with the Technical Design Document, Solution Module Definitions, DevOps Guide, Backup, Restore & Recovery Plan, Operational Readiness Confirmation Record, and monitoring or audit designs where applicable.

It should also align with the Initiative Definition Document or Work Brief so the named run/support ownership in operations matches the ownership model approved earlier in the work lifecycle.

## 10. Ownership, Review, and Acceptance Expectations

The Service Owner or operational lead usually owns this artifact with support from the Delivery Owner and support leads.

It should be reviewed as part of solution design where operational impact exists, and again as part of operational readiness and handover.

## 11. Maintenance Expectations

Keep it current when ownership, support coverage, escalation, vendor dependencies, or operating assumptions change.

## 12. Traceability and Ownership Minimum

Minimum traceability expectation:

- support boundaries and escalation paths align with the deployed scope
- ownership fields are consistent with readiness and acceptance records
- known support risks and constraints are visible and assigned

Minimum ownership expectation:

- Service Owner is accountable for live-service continuity.
- Support Owner is accountable for support execution clarity.
- Delivery Owner ensures the transition is complete before closure.

## 13. Validation Guide

- Are service and support ownership explicit?
- Can a reviewer see who supports what and when escalation happens?
- Are concentration risks, dependency assumptions, and transition-to-steady-state expectations visible?
- Are transition assumptions and known operational constraints visible?
- Does the artifact define the operating model without drifting into runbook detail?

If weak, clarify the responsibility split and make escalation routes easier to follow.

## 14. Prompt Guide for Drafting the Artifact

### 14.1. Starter prompt

> Draft an Operations & Support Model for this solution.
> Define service ownership, support ownership, support tiers or boundaries, escalation paths, monitoring expectations, support coverage, and the transition or steady-state assumptions that matter after go-live.

