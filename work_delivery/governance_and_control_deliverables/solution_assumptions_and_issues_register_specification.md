# Solution Assumptions & Issues Register Specification

## 1. What This Artifact Is For

The Solution Assumptions & Issues Register is a living log of unresolved design assumptions, open questions, issues, and risks that emerge during solution definition and delivery. It provides transparency into uncertainties and design dependencies and helps ensure they are tracked to resolution rather than buried in scattered notes.

It answers: What assumptions is the solution relying on? What design issues or open questions still need resolution? How might unresolved items affect scope, cost, quality, or timeline? Who owns each assumption or issue and when will it be resolved?

The register complements the [Decision Record Log](decision_record_log_specification.md) by making assumptions and issues visible before they become decisions. When assumptions are confirmed or issues are resolved, the outcomes should be captured as decisions in the Decision Record Log.

Intended readers include the Delivery Owner, domain designers, solution architects, and any reviewer or acceptance authority who needs confidence that unknowns are being actively managed.

## 2. When to Use It

Use this register from Stage 2 — Work Definition through Stage 7 — Acceptance, Transition & Closure. It is most helpful when:

- there are multiple unknowns, dependencies, or unanswered questions that could affect design or acceptance
- design assumptions could significantly change cost, timeline, quality, or scope if invalidated
- there is a risk that unresolved issues will be forgotten or rediscovered late in delivery

Maintain it throughout the initiative and review it regularly. Items that turn into decisions should cross-reference the [Decision Record Log](decision_record_log_specification.md).

## 3. Stage Fit and Handoffs

**Upstream sources:**

- [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md)
- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md)
- [Non-Functional Requirements Specification](../solution_deliverables/non_functional_requirements_specification.md)
- Team workshops, risk assessments, and design reviews

**Downstream artifacts:**

- [Decision Record Log](decision_record_log_specification.md) — receives resolved assumptions and issues as formal decisions
- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md) — remaining open items visible at acceptance

| Stage | How the register is used |
| --- | --- |
| Work Definition (Stage 2) | Capture early assumptions and open questions before Functional Capabilities are approved |
| Work Definition Details (Stage 4) | Update during module definition and use case drafting; assign owners and resolution targets |
| Delivery Mobilization (Stage 5) | Update during mobilization planning and risk assessment |
| Work Delivery (Stage 6) | Track resolution; record outcomes and reference the Decision Record Log for decisions made |
| Acceptance, Transition & Closure (Stage 7) | Highlight remaining assumptions or unresolved issues that affect acceptance |

## 4. Before You Start

Before creating the register, confirm you have:

- a mechanism for capturing assumptions, questions, and issues as they arise (workshops, design sessions, comments)
- agreement on the `AI-###` naming convention for stable traceability
- agreement on how often the register will be reviewed and updated
- a named owner and reviewer for the register

## 5. How to Draft It

1. **Create an entry for each assumption or issue.** Include the type (assumption, issue, open question, risk), a description, and context.
2. **Identify the impact.** Describe how the assumption or issue could affect scope, cost, timeline, quality, compliance, or operations if not addressed.
3. **Link to related artifacts.** Reference the `FC-###`, `SM-###`, or `UC-###` that the assumption or issue touches. If it relates to a rule (`BR-###`), integration (`INT-###`), or a quality attribute (`QA-###`), note that too.
4. **Assign an owner.** Specify who is responsible for resolving the assumption or issue.
5. **Set a target resolution date or stage.** Provide an expected timeframe for resolution.
6. **Track status.** Use: Open, Under Investigation, Resolved, Deferred, or Closed. Update status as work progresses.
7. **Record the resolution.** When resolved, summarize the outcome, any decisions made, implications for scope or design, and reference the Decision Record Log entry if appropriate.

## 6. Minimum Structure

Use a table like this:

| Item ID | Type (Assumption/Issue/Risk) | Description | Impact | Related artifacts | Owner | Status | Target resolution | Resolution summary / Decision reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AI-001 | Assumption | API provider will deliver v2 endpoints by Q3 | Could delay integration if API is late | SM-003, UC-010 | Delivery owner | Open | Delivery Mobilization (Stage 5) | |
| AI-002 | Issue | Unclear whether finance approval is needed for small purchases | Could change approval flow in UC-003 | BR-002, UC-003 | SME for Finance | Under investigation | Work Definition Details (Stage 4) | |

## 7. Writing Rules

Each entry should be specific enough to act on. Vague entries like "requirements unclear" are not useful — state what exactly is unknown and why it matters.

Keep entries current. A stale register with unresolved items from early stages and no status updates is a governance gap.

Keep the following out:

- meeting minutes or discussion summaries (record the assumption or issue, not the conversation)
- items that have already been formally decided (move those to the [Decision Record Log](decision_record_log_specification.md))
- general risk register content that does not relate to solution design or delivery assumptions

## 8. Traceability, Ownership, and Review

The Delivery Owner is accountable for completeness and management oversight of the register. The Outcome Owner or Sponsor should review where assumptions or issues materially affect business outcomes.

This artifact traces back to the solution definition artifacts (functional capabilities, modules, use cases). Resolved items feed forward to the [Decision Record Log](decision_record_log_specification.md). Remaining open items at acceptance are visible in the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md).

Acceptance evidence: completed register showing all open and resolved items, with resolution summaries and references to the Decision Record Log, plus endorsement from the Delivery Owner that all critical assumptions and issues have been managed appropriately.

## 9. Maintenance Expectations

This is a living document. Update the register throughout delivery as new assumptions are identified, new issues arise, and existing items are resolved.

Keep item status, owners, and resolution summaries current. Do not close the register until all critical items are resolved or explicitly carried into closure records.

## 10. Done When

The register is ready for acceptance review when:

- all material assumptions and issues identified during design and delivery are logged with `AI-###` identifiers
- each entry describes the potential impact and references related artifacts
- owners and target resolution timelines are defined for all open items
- status updates and resolution summaries are maintained and current
- decisions arising from resolved items are captured in the [Decision Record Log](decision_record_log_specification.md)
- remaining open items at acceptance are explicitly flagged with handling instructions

## 11. What Comes Next
2. Link resolved items to their corresponding `DR-###` entries in the [Decision Record Log](decision_record_log_specification.md).
3. Include the register in the acceptance package for Stage 7 — Acceptance, Transition & Closure.
4. Flag any items that remain open at closure in the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md).

## 12. Prompt Guide

### Starter prompt

```
Create a Solution Assumptions & Issues Register.
List all assumptions, open questions, issues, and risks identified during solution design. Include the type, description, potential impact, related artifacts (FC-###, SM-###, UC-###, BR-###, INT-###, QA-###), owner, status, and target resolution.
Use a table format with AI-### identifiers and leave the resolution summary blank until resolution.
```

### Validation prompt

```
Check whether all assumptions and issues are logged with clear descriptions, impacts, related artifacts, owners, statuses, and target resolution dates, and that resolved items reference decisions or outcomes in the Decision Record Log.
```
