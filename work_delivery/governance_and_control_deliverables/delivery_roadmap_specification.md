# Delivery Roadmap Specification

## 1. What This Artifact Is For

The Delivery Roadmap defines the planned path for delivering the authorized initiative from mobilization through acceptance and closure. It makes sequencing, milestones, dependencies, and control points visible so delivery progress can be managed and governed.

A useful roadmap is drafted early enough to support authorization-level visibility, elaborated before delivery starts, confirmed with the mobilized delivery team, and kept current through controlled updates as delivery changes.

Intended readers include: Delivery Owner, Project Manager (if assigned), Sponsor and Decision Authority, delivery team leads and domain owners, and governance, portfolio, and risk stakeholders.

## 2. When to Use It

This artifact is recommended for governed initiatives and required where controlled mobilization, cross-team dependencies, or milestone-based governance visibility are needed.

Use it progressively across stages:

- Stage 2 — Work Definition: draft a high-level roadmap with phases, key milestones, and major dependencies
- Stage 4 — Work Definition Details: elaborate to a delivery-ready baseline with releases, control checkpoints, and domain deliverables
- Stage 5 — Delivery Mobilization: confirm the roadmap with the delivery team and key stakeholders before execution begins

Use it when the initiative requires structured coordination and clear progress visibility beyond ad hoc task tracking.

It should align with the [Work Delivery Framework](../work_delivery_framework.md) and the governance and control section of the [Standard Deliverables Guide](../standard_deliverables_guide.md).

## 3. Stage Fit and Handoffs

This artifact spans Stages 2 through 7 and is updated progressively at each stage gate.

**Upstream sources:**

- [Initiative Definition Document](initiative_definition_document_specification.md) — authorized scope baseline that defines what is in scope by phase
- [Project Charter](project_charter_specification.md) — funding, authority, and authorization conditions that constrain the roadmap

**Downstream artifacts this roadmap feeds:**

- [Delivery Charter](delivery_charter_specification.md) — mobilization operating agreement aligned to roadmap phases
- [Decision Record Log](decision_record_log_specification.md) — change records tied to material roadmap revisions
- Domain deliverables planned and tracked against roadmap phases

## 4. Before You Start

Before drafting, confirm you have:

- a current [Initiative Definition Document](initiative_definition_document_specification.md) with approved scope boundaries
- understanding of the major delivery phases or waves at minimum
- awareness of material dependencies (internal and external)
- named Delivery Owner accountable for roadmap integrity

For a Stage 2 draft, high-level phase and milestone intent is sufficient. For a Stage 4 elaboration, confirm you also have:

- elaborated functional capabilities and domain deliverables
- confirmed team structure and domain owners
- a working [Delivery Charter](delivery_charter_specification.md)

If key inputs are missing, label the roadmap as a **working draft** and state what needs confirmation.

## 5. How to Draft It

1. **Define delivery phases or waves.** Name the major segments of delivery and their purpose. Align them to authorized scope boundaries.
2. **Identify milestones and governance checkpoints.** For each phase, name observable milestones and the governance review or decision points that mark readiness to proceed.
3. **Map dependencies and assumptions.** Record material internal and external dependencies. State critical assumptions that affect sequence or timing.
4. **Align to scope and deliverables.** Map key in-scope deliverables or Deliverable Domains to phases. Note explicitly that unapproved scope is excluded.
5. **Record major risks and change markers.** Identify sequencing constraints and state the conditions that would trigger a formal roadmap update.
6. **Confirm with the delivery team at Stage 5.** Record who confirmed the roadmap, when, and what unresolved concerns remain with follow-up owners.

## 6. Minimum Structure

### 6.1. Roadmap identity

Must include:

- initiative name
- roadmap version and date
- stage context (Stage 2, Stage 4, or Stage 5+ baseline)
- owner and preparing party

### 6.2. Delivery phases and milestones

Must include:

- named delivery phases or waves
- major milestones per phase
- target timing window (date or period)
- key governance checkpoints (for example: readiness review, acceptance review)

### 6.3. Dependencies and assumptions

Must include:

- material dependencies (internal and external)
- critical assumptions that affect sequence or timing
- dependency owner or coordinating owner where known

### 6.4. Scope and deliverable alignment

Must include:

- mapping to authorized scope baseline (for example Initiative Definition Document version)
- key in-scope deliverables or domains by phase
- explicit note that unapproved scope is excluded

### 6.5. Risks and change markers

Must include:

- major roadmap risks and sequencing constraints
- conditions that trigger escalation or formal roadmap update
- links to decision or change records for material revisions

### 6.6. Confirmation and communication record

Must include:

- date and method used to confirm roadmap with delivery team (Stage 5)
- confirming participants and roles
- unresolved concerns and follow-up owners

### 6.7. Template guide

Recommended fields:

| Field | What to record |
| --- | --- |
| Phase / Wave | Planned segment of delivery |
| Milestone | Observable checkpoint or outcome |
| Planned window | Date or period |
| In-scope deliverables | Relevant domain deliverables or artifacts |
| Dependency | Precondition or external input |
| Dependency owner | Owner accountable for coordination |
| Risk note | Material delivery risk affecting roadmap |
| Governance checkpoint | Review or decision point |
| Update reference | Linked decision or change record ID |

## 7. Writing Rules

Include enough detail to guide execution and governance without turning the roadmap into a full task plan.

- Stage 2: phases, key milestones, major dependencies, key risks
- Stage 4: releases or waves, control checkpoints, domain deliverables, planned acceptance points
- Stage 5 onward: confirmed ownership, cadence dates, and controlled updates

Keep the following out:

- detailed day-to-day task assignments
- low-level technical implementation steps
- unapproved scope proposals presented as committed work
- duplicate copies of full project plans or RAID logs

## 8. Traceability, Ownership, and Review

The Delivery Owner is accountable for roadmap integrity and update discipline. The Project Manager (if assigned) typically coordinates updates and publication.

Roadmap acceptance normally sits with the Delivery Owner and is reviewed with the Sponsor or Decision Authority where milestone governance requires it.

This artifact traces back to the [Initiative Definition Document](initiative_definition_document_specification.md) and [Project Charter](project_charter_specification.md). Material revisions should link to records in the [Decision Record Log](decision_record_log_specification.md).

## 9. Maintenance Expectations

Update the roadmap whenever material sequence, milestone, dependency, or scope-aligned delivery assumptions change.

Each material revision should include:

- what changed
- why it changed
- decision or change reference
- impact on milestones, dependencies, or acceptance timing

The roadmap is a living document from Stage 2 through Stage 7. Each stage gate (Stage 4 elaboration, Stage 5 confirmation) produces a new baseline version.

## 10. Done When

The roadmap is ready to use when:

- phases, milestones, and governance checkpoints are visible and aligned to authorized scope
- material dependencies and assumptions are explicit with owners named where known
- scope alignment is confirmed and unapproved scope is excluded
- major risks and conditions for escalation are recorded
- at Stage 5: the roadmap has been confirmed with the delivery team and unresolved concerns have owners

## 11. What Comes Next

1. Use the confirmed roadmap to set up delivery cadence in the [Delivery Charter](delivery_charter_specification.md).
2. Track material roadmap changes in the [Decision Record Log](decision_record_log_specification.md).
3. Update the roadmap at each significant stage gate or when material assumptions change.
4. Use the roadmap to monitor progress against milestones during Stage 6 — Work Delivery.
5. Reference the roadmap in the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md) to confirm what was delivered against the plan.

## 12. Prompt Guide

### Starter prompt

```
Draft a Delivery Roadmap for a governed initiative.
Show phases, milestones, dependencies, risks, and governance checkpoints.
Keep it aligned to authorized scope and suitable for stage-gated governance review.
```

### Validation prompt

```
Check whether any roadmap element implies new scope not found in the authorized baseline.
Identify unclear dependencies, missing owners, or milestone entries that are not governance-testable.
```
