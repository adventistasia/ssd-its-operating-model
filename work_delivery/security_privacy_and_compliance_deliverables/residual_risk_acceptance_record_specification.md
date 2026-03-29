# Residual Risk Acceptance Record Specification

## 1. What This Artifact Is For

The Residual Risk Acceptance Record documents the formal acknowledgment and acceptance of material risk that remains after planned controls or mitigations have been applied.

It exists to keep risk acceptance explicit, attributable, and reviewable rather than silent or assumed. A useful record shows what risk remains, why it remains, what controls are in place, and who accepted the exposure.

The intended outcome is that material residual risk is consciously accepted by the right authority with a clear record of the remaining exposure, its basis, and any conditions attached to that acceptance.

Intended readers include: Sponsor or delegated risk owner, Security / Data Protection Officer, Business Owner / Process Owner, Delivery Owner, and audit and governance reviewers.

## 2. When to Use It

This artifact is required when material security, privacy, operational, or compliance risk remains and a responsible authority must decide whether to accept it.

Use this artifact after risk treatment decisions are understood and before the residual risk is allowed to remain in operation. It is most useful where formal risk acceptance authority must be clear and where time-bound acceptance or conditions may apply.

It should align with NIST risk-management practice by making residual exposure, approving authority, review timing, and acceptance conditions explicit and reviewable.

## 3. Stage Fit and Handoffs

Typically prepared in late Stage 6 or Stage 7 when unresolved material risk requires an explicit human decision before final acceptance and closure.

Upstream inputs:

- [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md)
- [Compliance & Regulatory Alignment Statement Specification](compliance_and_regulatory_alignment_statement_specification.md)

Downstream outputs inform:

- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)
- [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)
- [Decision Record Log Specification](../governance_and_control_deliverables/decision_record_log_specification.md)

## 4. Before You Start

Before drafting, confirm you have:

- completed risk assessment with residual risks identified
- named accepting authority empowered for the specific class of risk
- controls applied or confirmed in place
- review date and any conditions agreed
- reference to the underlying risk assessment

## 5. How to Draft It

1. Complete record identity — record the ID, date, linked risk assessment reference, and owner (from 6.1).
2. Populate accepted risk rows — for each residual risk document the description, controls applied, impact summary, basis for acceptance, review date, accepting authority, and conditions (from 6.2).
3. Write the formal acceptance statement — state what is being accepted, the scope, and any time limit, condition, or required follow-up (from 6.3).
4. Review for vague approval wording and unclear conditions.

## 6. Minimum Structure

### 6.1. Record Identity

Must include:

- record ID
- date
- linked risk assessment reference
- owner or preparer

This section identifies the acceptance record and its source risk context.

### 6.2. Required Content for Each Accepted Risk Row

Each row must include:

- risk ID
- residual risk description
- controls applied
- impact summary
- basis for acceptance, such as business necessity, implementation timing, or compensating control position
- review date
- accepting authority
- conditions

Recommended columns:

| Risk ID | Residual risk | Controls applied | Impact summary | Basis for acceptance | Review date | Accepting authority | Conditions |
| --- | --- | --- | --- | --- | --- | --- | --- |

This row structure ensures the decision basis is explicit rather than implied.

### 6.3. Acceptance Statement

Must include:

- formal statement that the residual risk is being accepted
- scope or environment the acceptance applies to
- any time limit, condition, or required follow-up action

This section is the actual acceptance act and must not be vague.

## 7. Writing Rules

Keep it concise and decision-focused. Include enough detail to identify the residual risk, why it remains, what controls exist, the impact if realized, and who accepted it.

Keep the following out of this artifact:

- the entire underlying risk register
- vague approval wording such as `noted` or `aware`
- hidden conditions that are not stated clearly

## 8. Traceability, Ownership, and Review

The security or governance lead usually prepares the record. The accepting authority must be the person or body empowered to accept the specific class of risk.

The Delivery Owner is accountable for ensuring residual risk decisions are visible, attributable, and reflected in acceptance and closure records. Risk acceptance authority must not be assumed or delegated informally.

## 9. Maintenance Expectations

Review the record at the stated review date, when controls change, or when the residual risk changes materially. Supersede rather than overwrite accepted records.

## 10. Done When

- The residual risk is described clearly enough for a decision-maker to understand it.
- The accepting authority is explicit and appropriate.
- Any conditions or review dates are visible.
- The record explains why acceptance was chosen instead of further treatment or rejection.
- The record distinguishes clearly between risk description and formal acceptance.

## 11. What Comes Next

1. Confirm with Delivery Owner that acceptance is reflected in closure documentation.
2. Reference in the [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md).
3. Schedule review at the stated review dates.
4. Issue a superseding version when residual risk changes or conditions are resolved.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Residual Risk Acceptance Record for this initiative.
Summarize the residual risk, the controls already applied, the impact if the risk is realized, any review date or conditions, and the formal acceptance by the appropriate authority.
Keep it concise, explicit, and attributable.
```

### 12.2. Validation Prompt

```
Review this Residual Risk Acceptance Record.
Check that each accepted risk has a clear residual description, named controls, an impact summary, an explicit basis for acceptance, a named accepting authority, and any conditions or review dates.
Flag any vague approval wording, missing acceptance authority, or hidden conditions.
```
