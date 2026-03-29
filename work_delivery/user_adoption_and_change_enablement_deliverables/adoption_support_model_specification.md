# Adoption Support Model Specification

## 1. What This Artifact Is For

The Adoption Support Model defines how users receive help after go-live, how early adoption issues are handled, and what temporary or ongoing support arrangements are needed to protect outcomes.

It exists to make user support intentional rather than assumed. A useful model shows where users go for help, how support is triaged and escalated, what hypercare exists, and which adoption risks need targeted support.

The intended outcome is that users receive timely, structured help after go-live so adoption issues are resolved quickly and intended business outcomes are protected.

Intended readers include: Business Owner, Change or Communications Lead, support teams, Delivery Owner, and IT Operations / Service Owner where service support overlaps.

## 2. When to Use It

Use this artifact when user adoption risk, process change, or rollout complexity means post-launch support needs to be organized explicitly.

Use it before go-live and during transition. It is most useful where users need defined help channels and where early-adoption issues could affect business outcomes or operational stability.

It should align with ITIL 4 Service Desk, Incident Management, and organizational change management practice by making user-facing support entry points, escalation paths, and transition support explicit.

In the Work Delivery Framework lifecycle, this artifact is usually defined in Stage 4, activated during Stage 5 mobilization, operated in Stage 6, and confirmed as part of Stage 7 transition and closure.

## 3. Stage Fit and Handoffs

| Stage | Role of this artifact |
| --- | --- |
| Stage 4 – Work Definition Details | Defined once adoption risks and rollout approach are understood |
| Stage 5 – Delivery Mobilization | Activated; support channels and responsibilities confirmed |
| Stage 6 – Work Delivery | Operated through rollout and early adoption period |
| Stage 7 – Acceptance, Transition & Closure | Confirmed as part of transition and closure |

**Upstream inputs:**

- [User Impact Assessment](user_impact_assessment_specification.md) — provides adoption risk profile by user group
- [Change & Communication Plan](change_and_communication_plan_specification.md) — provides audience and channel context
- [Training & Enablement Materials Specification](training_and_enablement_materials_specification.md) — informs support gaps and help-path design

**Downstream outputs:**

- [Adoption Confirmation Record](adoption_confirmation_record_specification.md) — receives evidence of adoption support activity
- [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) — references confirmed support arrangements at closure

**Also relates to:**

- [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md)
- [Operational Readiness Confirmation Record Specification](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md)

## 4. Before You Start

Confirm the following before drafting:

- completed User Impact Assessment with known adoption risks by user group
- named change lead and Business Owner
- support teams identified and briefed
- hypercare period defined
- handoff point to steady-state support agreed

## 5. How to Draft It

1. Complete the support context header (§6.1).
2. Define support model channels, ownership, and transition (§6.2).
3. Document escalation and risk handling (§6.3).
4. Populate the summary table (§6.4).

## 6. Minimum Structure

### 6.1. Support Context

Must include:

- initiative or rollout name
- scope of adoption support
- owner
- support period or phase covered

This section identifies what support window and audience the model applies to.

### 6.2. Support Model

Must include:

- support channels and points of contact
- hypercare or transition assumptions where relevant
- ownership of support actions and decision-making
- how and when support responsibility shifts from hypercare or project-led support into steady-state support

This section shows how users access support and who is responsible for helping them.

### 6.3. Escalation and Risk Handling

Must include:

- issue triage expectations
- escalation routes
- known adoption risks and mitigation or support approach
- any user groups requiring targeted support because of higher change impact, lower readiness, or business criticality

This section ensures that user issues move predictably when they cannot be resolved at first contact.

### 6.4. Template Guide

Recommended summary columns:

| Support area | Channel or contact | Owner | Escalation path | Risk or note |
| --- | --- | --- | --- | --- |

Use short entries and reference technical support procedures elsewhere.

## 7. Writing Rules

Include enough detail to explain support channels, hypercare assumptions, escalation routes, and ownership of adoption issues. Do not turn it into a full incident management process.

Keep the following out of this artifact:

- full technical runbooks
- detailed defect registers
- generic IT support policies not specific to the adoption context

## 8. Traceability, Ownership, and Review

The change lead or Business Owner usually coordinates this artifact with support and operations teams.

Review should include the teams expected to receive user issues.

The Delivery Owner is accountable for ensuring adoption support arrangements are explicit before go-live and handover. The Support Owner and Business Owner should confirm that support responsibilities are clear before closure.

## 9. Maintenance Expectations

Update when rollout timing, hypercare coverage, support channels, or ownership changes.

## 10. Done When

- Support channels and points of contact are defined.
- Hypercare and transition assumptions are explicit.
- Escalation routes are visible.
- Adoption risks are reflected in the support approach.
- Handoff from project-led support to steady-state support is clear.
- Summary table is populated.

## 11. What Comes Next

1. Activate per rollout schedule.
2. Capture adoption support evidence for the [Adoption Confirmation Record](adoption_confirmation_record_specification.md).
3. Confirm alignment with the [Operations & Support Model](../operational_readiness_deliverables/operations_and_support_model_specification.md) for steady-state transition.
4. Reference in the [Formal Acceptance & Closure Record](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md).

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft an Adoption Support Model for this initiative.
Define how users receive help after go-live, what hypercare or transition support exists, how issues are escalated, and which adoption risks need focused support.
Keep it practical and user-facing.
```

### 12.2. Validation Prompt

```
Review this Adoption Support Model.
Check that: support channels and points of contact are defined; hypercare and transition assumptions are explicit; escalation routes are visible; adoption risks are reflected in the support approach; the handoff from project-led support to steady-state support is clear; and the summary table is populated.
Identify any gaps and suggest where support entry points or ownership need to be made clearer.
```
