# Operations and Support Model Specification

## 1. What This Artifact Is For

The Operations and Support Model defines who owns the live service, how support is structured, where escalation occurs, and what operating assumptions govern steady-state service.

It exists to make long-term accountability explicit and to prevent unsupported handover. A useful model shows who owns the service, who supports it, how incidents and escalations move, and what constraints or dependencies affect support. The intended outcome is that the live service remains supportable beyond the delivery team, with clear ownership, support boundaries, escalation paths, and sustainable operating responsibilities.

Intended readers include: IT Operations / Service Owner, Support Owner and support teams, Delivery Owner, and Business Owner where service outcomes are significant.

## 2. When to Use It

This artifact is required when the initiative creates or changes a service, application, integration, or platform component that must be operated after delivery.

For small, contained changes with an established and well-understood support arrangement, a brief support summary within the Work Brief or Deployed Solution record may be sufficient. A fuller Operations and Support Model is needed when:

- support crosses team, vendor, or partner boundaries
- ownership must be made explicit for handover
- service-level assumptions, priority handling, or dependency obligations materially affect support expectations

Use this artifact during solution design, before go-live, and at formal handover. It should align with ITIL 4 Service Desk, Incident Management, Monitoring and Event Management, and Relationship Management practices by making service accountability, support channels, and escalation paths clear.

## 3. Stage Fit and Handoffs

- **Stage 4:** define the target support model and ownership boundaries early enough to influence design decisions.
- **Stage 6:** confirm the model against real deployment and support arrangements.
- **Stage 7:** use this model as part of operational acceptance and transition evidence.

**Upstream sources:**

- [Technical Design Document Specification](technical_design_document_specification.md)
- [DevOps Guide Specification](devops_guide_specification.md)
- [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md)

**Downstream artifacts:**

- [Operational Readiness Confirmation Record Specification](operational_readiness_confirmation_record_specification.md)
- [Formal Acceptance and Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

This artifact should also align with the Initiative Definition Document or Work Brief so that named run and support ownership in operations is consistent with the ownership model approved earlier in the work lifecycle. It should be consistent with the [Backup, Restore and Recovery Plan Specification](backup_restore_and_recovery_plan_specification.md) and any monitoring or audit designs.

## 4. Before You Start

Before drafting, confirm you have:

- a technical design or deployment configuration reference from the [Technical Design Document](technical_design_document_specification.md) or equivalent
- confirmed service ownership: who will own the live service after handover
- support boundaries established: internal tiers, vendor dependencies, and partner arrangements
- SLA, SLO, or service-level assumptions applicable to this service where relevant
- hypercare and transition-to-steady-state plan where applicable

If service ownership is not yet confirmed or support boundaries are still being negotiated, label the output as a **working draft** and identify the missing inputs explicitly.

## 5. How to Draft It

1. **Confirm scope.** Identify the service, integration, or platform component this model covers and the delivery boundary it reflects.
2. **Name service and support ownership.** Identify the Service Owner and Support Owner; state what each is accountable for.
3. **Map the support structure.** Identify support tiers or equivalent responsibility splits, internal and external boundaries, vendor and partner dependencies, and any known concentration risks such as reliance on a single specialist or vendor path.
4. **Define escalation and response.** Document escalation paths, triggers, and incident or support response expectations. Note decision points for when issues move from delivery or hypercare into steady-state support ownership.
5. **Set monitoring and operating assumptions.** List monitoring expectations, support coverage or service hours, hypercare and transition assumptions, and operational constraints or risks that affect supportability.
6. **Draft the summary table.** Populate the recommended summary table with key areas, owners, boundaries, escalation paths, and notes.
7. **Review for completeness.** Confirm that ownership, support boundaries, escalation, and operating assumptions are explicit enough for someone not on the delivery team to understand and act on.

## 6. Minimum Structure

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

### 6.5. Summary table

Recommended summary table:

| Area | Owner | Boundary or responsibility | Escalation path | Notes |
| --- | --- | --- | --- | --- |

Use short entries and point to detailed procedures elsewhere.

## 7. Writing Rules

Include enough detail to show ownership, support boundaries, escalation paths, monitoring expectations, and transition assumptions. Do not turn it into a full runbook.

Keep the following out:

- full troubleshooting procedures
- detailed deployment steps
- deep technical design
- project task assignments

## 8. Traceability, Ownership, and Review

The Service Owner or operational lead usually owns this artifact, with input from the Delivery Owner and support leads.

It should be reviewed as part of solution design where operational impact exists, and again as part of operational readiness and handover.

Minimum traceability expectation:

- support boundaries and escalation paths align with the deployed scope
- ownership fields are consistent with readiness and acceptance records
- known support risks and constraints are visible and assigned

Minimum ownership expectation:

- Service Owner is accountable for live-service continuity
- Support Owner is accountable for support execution clarity
- Delivery Owner ensures the transition is complete before closure

## 9. Maintenance Expectations

This is a living document. Keep it current when ownership, support coverage, escalation paths, vendor dependencies, or operating assumptions change.

The model should reflect the actual operating arrangements in place, not the arrangements planned at initial handover.

## 10. Validation Guide

Before treating this artifact as ready for operational acceptance, confirm:

1. Are service and support ownership named with explicit accountabilities?
2. Can a reviewer see who supports what and when escalation happens?
3. Are concentration risks, vendor dependencies, and transition-to-steady-state expectations visible?
4. Are operational constraints and known support risks recorded?
5. Does the artifact define the operating model without drifting into runbook detail?

If weak, clarify the responsibility split and make escalation routes easier to follow.

## 11. Done When

- Service Owner and Support Owner are named with explicit accountabilities.
- Support tiers, boundaries, and vendor or partner dependencies are documented.
- Escalation paths and triggers are defined.
- Monitoring expectations and operational constraints are recorded.
- Transition and steady-state assumptions are visible.
- The summary table is populated and reflects the agreed operating model.

## 12. What Comes Next

1. Validate the model with the Service Owner and Support Owner before handover.
2. Reference this model in the [Operational Readiness Confirmation Record](operational_readiness_confirmation_record_specification.md).
3. Confirm the model is consistent with the [Technical Design Document](technical_design_document_specification.md) and [DevOps Guide](devops_guide_specification.md).
4. Update before formal operational acceptance as part of Stage 7.
5. Keep current after go-live when ownership, escalation, or operating assumptions change.

## 13. Prompt Guide

### Starter prompt

```
Draft an Operations and Support Model for this solution.
Define service ownership, support ownership, support tiers or boundaries, escalation paths, monitoring expectations, support coverage, and the transition and steady-state assumptions that matter after go-live.
Use the recommended summary table and keep it concise — point to detailed procedures rather than repeating them.
```

### Validation prompt

```
Review this Operations and Support Model against its specification.
Check: Are service and support owners named with clear accountabilities? Are support boundaries, escalation paths, and operating assumptions explicit? Are concentration risks and vendor dependencies visible? Does it stay at the operating-model level without drifting into runbook detail?
Identify gaps, missing inputs, and anything that would make the model unclear to a reviewer or incoming support team.
```

