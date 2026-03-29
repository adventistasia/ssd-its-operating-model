# Compliance & Regulatory Alignment Statement Specification

## 1. What This Artifact Is For

The Compliance & Regulatory Alignment Statement documents how the initiative aligns with applicable internal policies, contractual obligations, regulatory requirements, and data protection expectations.

It exists to make compliance exposure visible, interpreted, and attributable before and after implementation. A useful statement shows what obligations apply, why they apply, how they are being addressed, and what gaps or dependencies remain.

The intended outcome is that applicable obligations are translated into clear accountability, visible alignment decisions, and understood gaps that can be acted on before they become audit or operational issues.

Intended readers include: Security / Data Protection Officer, compliance and governance reviewers, Sponsor and Business Owner, Delivery Owner, and audit reviewers.

## 2. When to Use It

This artifact is required when the initiative is subject to internal policy, regulatory, contractual, sectoral, privacy, or audit obligations that materially affect solution design, operation, or acceptance.

Use this artifact when the initiative needs a formal statement of how obligations were considered and addressed. It is most useful where multiple policy, privacy, or regulatory requirements must be interpreted into practical delivery and control actions.

It should align with NIST CSF governance outcomes and the NIST Privacy Framework by translating obligations into accountable controls, decisions, and actions.

## 3. Stage Fit and Handoffs

Outlined in Stage 2 when obligations materially affect authorization decisions, elaborated in Stage 4, updated through Stage 6 as controls are implemented, and used in Stage 7 acceptance and closure reviews.

Upstream inputs:

- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md)

Downstream outputs inform:

- [Residual Risk Acceptance Record Specification](residual_risk_acceptance_record_specification.md)
- [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

Also relates to:

- [Data Governance & Impact Assessment Specification](../data_governance_and_records_deliverables/data_governance_and_impact_assessment_specification.md)
- [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md)
- [Audit & Monitoring Design Summary Specification](audit_and_monitoring_design_summary_specification.md)

## 4. Before You Start

Before drafting, confirm you have:

- identified applicable obligations (policy, regulatory, contractual, privacy)
- named compliance lead
- initiative scope confirmed
- reference to the Initiative Definition Document or Work Brief
- known waivers or exceptions already identified

## 5. How to Draft It

1. Complete statement context header — identify the initiative, scope, date, and owner (from 6.1).
2. Populate obligation rows — for each obligation record applicability, treatment, evidence, owner, status, and any gap or note (from 6.2).
3. Identify and document open gaps and dependencies — list unresolved gaps, required waivers, and dependencies that affect compliance alignment (from 6.3).
4. Review for vague alignment claims and hidden non-compliance.

## 6. Minimum Structure

### 6.1. Statement Context

Must include:

- initiative or solution name
- scope of the statement
- date or version
- owner

This section identifies what the alignment statement covers.

### 6.2. Required Content for Each Obligation Row

Each obligation row must include:

- obligation or requirement
- why it applies
- how it is addressed
- evidence or authoritative reference showing where alignment is implemented or recorded
- owner
- status
- gap or note

Recommended table:

| Obligation | Why it applies | How it is addressed | Evidence or reference | Owner | Status | Gap or note |
| --- | --- | --- | --- | --- | --- | --- |

Use controlled status values where helpful, such as `addressed`, `in progress`, `gap`, or `waiver required`.

This row structure turns the statement into a usable control-mapping tool.

### 6.3. Open Gaps and Dependencies

Must include:

- unresolved gaps
- required waivers or exceptions
- dependencies that affect compliance alignment

This section makes unresolved exposure visible.

## 7. Writing Rules

Include enough detail to identify the applicable obligation, what it means for the initiative, how it is addressed, and what remains open. Do not turn it into a legal treatise.

Keep the following out of this artifact:

- full copies of policies or regulations
- unsupported legal conclusions
- hidden non-compliance in vague notes

## 8. Traceability, Ownership, and Review

The compliance lead, security lead, or governance reviewer usually coordinates this artifact with business and legal or privacy input where needed.

Formal review should be completed by the relevant compliance or protection authority.

The Delivery Owner is accountable for ensuring open compliance gaps are visible and tracked to decision or treatment. The relevant Acceptance Authority should confirm that material obligations are addressed or explicitly conditionally accepted.

## 9. Maintenance Expectations

Update when obligations change, solution scope changes, or compliance gaps are discovered or resolved.

## 10. Done When

- The statement shows clearly what obligations apply and why.
- A reviewer can see how each obligation is being addressed.
- There is enough evidence or reference detail to verify the claimed alignment.
- Unresolved gaps, waivers, or dependencies are explicit.
- Ownership is assigned for material obligations.

## 11. What Comes Next

1. Review with compliance or governance authority.
2. Feed open gaps into the [Residual Risk Acceptance Record Specification](residual_risk_acceptance_record_specification.md) where needed.
3. Reference in the [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md).

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Compliance & Regulatory Alignment Statement for this initiative.
List the applicable obligations, explain briefly why each applies, state how each is being addressed, identify owners, and record any open gaps or waivers.
Keep it practical and table-driven.
```

### 12.2. Validation Prompt

```
Review this Compliance & Regulatory Alignment Statement.
Check that each obligation has a clear applicability reason, a stated treatment approach, an evidence or reference pointer, a named owner, and a status.
Flag any vague alignment claims, hidden non-compliance, or obligations without an owner or gap note.
```
