# Delivery Charter Specification

## 1. What This Artifact Is For

The Delivery Charter formally charters and mobilizes the delivery team after work authorization. It defines how the team will operate, communicate, govern execution, and prepare for acceptance readiness.

A useful delivery charter makes delivery expectations explicit before execution begins and keeps execution visible, governed, and acceptance-ready. It may also serve as the agenda and output record for the delivery team kickoff meeting.

Intended readers include: Delivery Owner, Project Manager (if assigned), delivery team members and team leads, Sponsor and governance stakeholders, Acceptance Authorities, and operations and support stakeholders.

## 2. When to Use It

This artifact is required when an initiative needs controlled delivery mobilization, cross-team coordination, or explicit execution governance.

It is primarily used in Stage 5 — Delivery Mobilization, though it may be drafted earlier and finalized at mobilization.

It does not replace the [Project Charter](project_charter_specification.md), detailed delivery plans, or active trackers.

## 3. Stage Fit and Handoffs

This artifact is produced in Stage 5 — Delivery Mobilization, once the [Project Charter](project_charter_specification.md) is in place.

**Upstream sources:**

- [Initiative Definition Document](initiative_definition_document_specification.md) — authorized scope baseline
- [Project Charter](project_charter_specification.md) — authorization, funding, and authority basis
- [Delivery Roadmap](delivery_roadmap_specification.md) — sequencing, milestones, and phase plan

**Downstream artifacts this charter activates:**

- [Decision Record Log](decision_record_log_specification.md) — decision tracking during execution
- [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md) — active RAID tracking during execution
- Delivery plans, acceptance trackers, and communication records

## 4. Before You Start

Before drafting, confirm you have:

- an authorized [Project Charter](project_charter_specification.md)
- a current [Initiative Definition Document](initiative_definition_document_specification.md) and at least a draft [Delivery Roadmap](delivery_roadmap_specification.md)
- a named Delivery Owner
- clarity on team structure and key roles
- the minimum Stage 5 trackers ready to stand up (RAID/dependency, decision, acceptance)

If the authorization basis is unclear or the delivery team is not yet assembled, label this document as a **working draft**.

## 5. How to Draft It

1. **State the mobilization intent and scope guardrails.** Reference the authorized baseline and make clear that scope changes require formal governance.
2. **Define team operating expectations.** Describe what is expected of delivery teams and role leads — accountability for deliverables, evidence readiness, and decision participation.
3. **Define the communication cadence.** Specify meeting rhythm, channels, escalation path, and stakeholder communication frequency.
4. **Document governance controls.** State how changes, risks, issues, and decisions will be handled and escalated during execution.
5. **Set up control trackers.** Identify which trackers are required (RAID/dependency, decision, acceptance), name the owner of each, and confirm they are active.
6. **If used as kickoff record:** capture the kickoff date, participants, decisions made, and open actions with owners.

## 6. Minimum Structure

### 6.1. Charter identity

Must include:

- initiative name
- charter version and date
- stage context (normally Stage 5)
- owner and preparing party

### 6.2. Mobilization intent and scope guardrails

Must include:

- short statement of delivery mobilization intent
- reference to authorized scope baseline
- explicit note that scope changes require formal governance

### 6.3. Team operating expectations

Must include:

- what is expected from delivery teams
- role responsibilities and decision participation expectations
- accountability for deliverables and evidence readiness

### 6.4. Communication methods and cadence

Must include:

- operating cadence (status, planning, risk/issue, and readiness reviews)
- communication channels and expected response norms
- stakeholder communication method and frequency

### 6.5. Governance controls during execution

Must include:

- change path and escalation path
- decision logging expectations
- issue, risk, and dependency handling expectations
- acceptance-readiness management expectations
- requirement to keep status visibility based on deliverables, evidence, and decision needs

### 6.6. Tracker and control setup

Must include:

- RAID and dependency log setup expectation
- decision log setup expectation
- acceptance tracker setup expectation
- owner for maintaining each control record

These controls should be practical and light, but they must be active before controlled execution begins.

### 6.7. Kickoff meeting record (where used)

If used as kickoff artifact, include:

- kickoff date and participants
- decisions made at kickoff
- open actions, owners, and due windows

### 6.8. Template guide

Recommended fields:

| Field | What to record |
| --- | --- |
| Delivery objective | Practical statement of what delivery is mobilizing to achieve |
| Team model | Roles, responsibilities, and reporting lines |
| Meeting rhythm | Recurring ceremonies and participants |
| Communication method | Channels, escalation path, and reporting expectations |
| Control rules | Change, risk, decision, and acceptance-readiness controls |
| Tracker ownership | Who maintains RAID/dependency, decision, and acceptance trackers |
| Kickoff outcomes | Confirmed decisions and follow-up actions |

## 7. Writing Rules

Keep the charter practical and execution-focused. Include enough detail so team members know how delivery will be run and governed, without duplicating day-to-day planning artifacts.

Keep the following out:

- duplicate copies of the Project Charter
- detailed backlog or task scheduling
- detailed technical design content
- unresolved scope proposals presented as agreed execution expectations

## 8. Traceability, Ownership, and Review

The Delivery Owner is accountable for producing and activating this artifact. The Project Manager (if assigned) supports coordination and maintenance.

The charter should be reviewed with team leads and Sponsor or governance stakeholders as needed for controlled mobilization.

This artifact traces back to the [Project Charter](project_charter_specification.md) and [Initiative Definition Document](initiative_definition_document_specification.md). It feeds forward to the active delivery governance trackers and, ultimately, to the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md).

Update when delivery operating expectations, communication methods, governance controls, or key roles change materially. Keep revision history concise and attributable.

## 9. Done When

The charter is ready to activate delivery when:

- mobilization intent and scope guardrails are explicit and reference the authorized baseline
- team operating expectations, communication methods, and escalation paths are defined
- minimum Stage 5 controls are active (RAID/dependency, decision, and acceptance tracking)
- owners are named for each control tracker
- the Delivery Owner has reviewed and confirmed the charter with team leads
- if used as kickoff record: decisions and follow-up actions are captured

## 10. What Comes Next

1. Activate all control trackers named in section 6.6 before execution begins.
2. Conduct or finalize the delivery team kickoff using this charter as the agenda.
3. Confirm the [Delivery Roadmap](delivery_roadmap_specification.md) with the assembled team.
4. Begin Stage 6 — Work Delivery with governance controls in place.

## 11. Prompt Guide

### Starter prompt

```
Draft a Delivery Charter for Stage 5 mobilization.
Define delivery team expectations, communication methods, governance controls, and acceptance-readiness management.
Keep it practical and suitable for use in a kickoff meeting.
```

### Validation prompt

```
Review this charter for missing accountability, unclear communication methods, or weak change and escalation controls.
Check whether any section duplicates project planning detail that should sit in delivery plans instead.
```
