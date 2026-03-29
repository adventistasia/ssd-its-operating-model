# Decision Record Log Specification

## 1. What This Artifact Is For

The Decision Record Log keeps a traceable record of material decisions made during an initiative. It prevents decisions from being lost, forgotten, or re-litigated by making them visible with a clear owner, rationale, and current status.

Intended readers include the Delivery Owner, governance coordinator, delivery team, and any reviewer or auditor who needs to understand why key choices were made.

## 2. When to Use It

Start the log in Stage 2 — Work Definition when the initiative begins making decisions about scope, funding, approach, or design. Keep it active until the initiative closes.

Use it whenever a decision could affect:

- scope, funding, or approved baselines
- risk position, security, or compliance
- architecture, module design, or integration approach
- acceptance approach or conditions

Do not use it for routine operational choices, meeting discussion notes, or minor day-to-day decisions that do not affect governance or delivery.

This log is required for all governed initiatives. It is most valuable when decisions are numerous, cross-team, or when accountability and audit trail matter.

## 3. Stage Fit and Handoffs

**Upstream sources:**

- [Initiative Definition Document](initiative_definition_document_specification.md) — scope, deliverables, and ownership decisions that anchor the log
- [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md) — resolved assumptions and issues that become decisions

**Downstream artifacts this log feeds:**

- [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md) — closure and exception decisions
- [Delivery Roadmap](delivery_roadmap_specification.md) — material changes to sequence or milestones linked from decision records
- Domain deliverables that are affected by logged decisions (NFRs, business rules, integrations)

| Stage | What to log |
| --- | --- |
| Work Definition (Stage 2) | Early decisions on problem, scope, funding, or delivery approach |
| Work Authorization (Stage 3) | Authorization decisions, conditions, and risk acceptance |
| Work Definition Details (Stage 4) | Design decisions on modules, NFRs, integrations, or business rules |
| Delivery Mobilization (Stage 5) | Mobilization, risk response, and execution decisions |
| Work Delivery (Stage 6) | Decisions on implementation, evidence, or material changes |
| Acceptance, Transition & Closure (Stage 7) | Acceptance decisions and closure decisions |

## 4. Before You Start

Before creating the log, confirm you have:

- a named log owner (usually the Delivery Owner or governance coordinator)
- agreement on which categories of decision are material enough to log
- a naming convention using `DR-###` identifiers for stable traceability
- a shared location where the log is visible to the delivery team and reviewers

## 5. How to Draft It

1. **Assign a log owner.** The owner is accountable for maintaining currency and completeness.
2. **Add a row immediately when a material decision is made** — while context is fresh.
3. **Keep each entry short.** Record the decision and rationale, not the meeting discussion.
4. **Choose the right log format.** Use the baseline form for simple initiatives. Use the extended form when cross-domain traceability is needed.
5. **If a decision changes, mark the original row `Superseded` and add a new row.** Never overwrite history.
6. **Share the log** with the delivery team and reviewers so it is visible, not buried.

## 6. Minimum Structure

### 6.1. Baseline — simplest form

Use the baseline log when the initiative is small, has few cross-team dependencies, and does not need detailed traceability to other artifacts.

| DR-### | Date | Decision | Authority | Rationale | Status |
| --- | --- | --- | --- | --- | --- |

**Example:**

| DR-### | Date | Decision | Authority | Rationale | Status |
| --- | --- | --- | --- | --- | --- |
| DR-001 | 2026-01-15 | Use Azure for hosting | IT Director | Best fit for existing licensing and support capability | Approved |
| DR-002 | 2026-01-22 | Defer mobile app to Phase 2 | Sponsor | Budget constraint; core web functionality is sufficient for Phase 1 | Approved |
| DR-003 | 2026-02-10 | Increase data retention from 3 to 7 years | Compliance Officer | New regulatory requirement effective July 2026 | Approved |

### 6.2. Extended — with cross-domain traceability

Use the extended log when the initiative is large, has multiple teams or authorities, or needs traceability to other deliverables such as NFRs, business rules, integrations, or assumptions.

Add cross-domain columns only when they apply to the initiative. Leave unused columns out of the table.

| DR-### | Date | Title | Category | Decision | Authority | Rationale | Impacted Artifacts | Baseline Impact | Related AI-### | Related QA-### | Related BR-### | Related INT-### | Conditions / Follow-Up | Follow-Up Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

**Example:**

| DR-### | Date | Title | Category | Decision | Authority | Rationale | Impacted Artifacts | Baseline Impact | Related AI-### | Related BR-### | Conditions / Follow-Up | Follow-Up Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DR-001 | 2026-01-15 | Hosting platform selection | Architecture | Use Azure for hosting | IT Director | Best fit for existing licensing and support | Technical Design Document | Confirms baseline | AI-003 | | IT to confirm DR-compliant region by Jan 30 | Infrastructure Lead | Approved |
| DR-002 | 2026-01-22 | Mobile app deferred | Scope | Defer mobile app to Phase 2 | Sponsor | Budget constraint; core web sufficient for Phase 1 | Functional Capabilities (FC-007 deferred) | Scope change | | | Update FC register to mark FC-007 deferred | Delivery Owner | Approved |
| DR-003 | 2026-02-10 | Data retention extension | Compliance | Extend retention from 3 to 7 years | Compliance Officer | New regulatory requirement | Data Governance Spec, DevOps Guide | Baseline change — storage sizing update required | AI-007 | BR-004 | Update storage estimate and DR design before Delivery Mobilization (Stage 5) | Delivery Owner | Approved |

### 6.3. Status values

Use these status values consistently:

| Status | Meaning |
| --- | --- |
| `Proposed` | Under review, not yet approved |
| `Approved` | Decision accepted and in effect |
| `Superseded` | Replaced by a later decision — keep row visible |
| `Withdrawn` | No longer applicable |

## 7. Writing Rules

Each entry should record what was decided, not the deliberation that led to it. Keep entries short enough to scan but complete enough to understand without needing to trace back to meeting minutes.

Keep the following out:

- meeting discussion summaries or minutes
- draft proposals that were not approved (record as `Withdrawn` if they were formally considered)
- operational instructions or how-to guidance
- content that belongs in the [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md) until a decision is actually reached

## 8. Traceability, Ownership, and Review

The Delivery Owner or designated governance coordinator owns the log. They are accountable for its completeness, currency, and accessibility to the delivery team.

This artifact traces back to the [Initiative Definition Document](initiative_definition_document_specification.md) and the [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md). It feeds forward to domain deliverables affected by decisions and to the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md).

Decisions may affect and should link to:

- [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md) (`AI-###`) — when a decision resolves an assumption or opens a new issue
- [Non-Functional Requirements Specification](../solution_deliverables/non_functional_requirements_specification.md) (`QA-###`) — when a decision affects a quality target
- [Business Rules Catalog](../solution_deliverables/business_rules_catalog_specification.md) (`BR-###`) — when a decision adds or changes a rule
- [Integration & External Dependency Specification](../solution_deliverables/integration_and_external_dependency_specification.md) (`INT-###`) — when a decision introduces or changes an integration

Acceptance evidence: updated Decision Record Log showing all material decisions with authority, rationale, and current status, plus confirmation by the Delivery Owner that the log is complete up to the acceptance point.

## 9. Maintenance Expectations

This is a living document. Update the log as decisions are made throughout delivery. Add each new material decision promptly so the log remains the authoritative record for the initiative.

Do not archive or stop maintaining the log until the initiative reaches formal closure.

## 10. Done When

The log is ready for review or acceptance when:

- all material decisions made to date are logged with DR-### identifiers
- each entry has a named authority, a rationale, and a current status
- superseded decisions are marked `Superseded` and the replacement decision is referenced
- any decision affecting scope, funding, or acceptance is included
- the log owner has confirmed it is current and complete

## 11. What Comes Next
2. Reference decision IDs in affected domain artifacts (NFRs, business rules, integrations) for traceability.
3. Include the completed log in the acceptance package for Stage 7 — Acceptance, Transition & Closure.
4. Reference the log in the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md) for any conditions or exceptions.

## 12. Prompt Guide

### Starter prompt

```
Create a Decision Record Log for this initiative.
Add a row for each material decision made so far, with a DR-### ID, date, decision statement, authority, rationale, and status.
Use the baseline structure for simple initiatives or the extended structure when cross-domain traceability is needed.
Keep entries short — record the conclusion, not the discussion.
```

### Validation prompt

```
Review this Decision Record Log. Check that:
- each entry records what was decided (not the discussion)
- each entry has a named authority and a current status
- superseded decisions are marked Superseded, not deleted
- any decision affecting scope, funding, or acceptance is included
```
