# Compliance & Regulatory Alignment Statement Specification

## 1. Purpose and Intended Outcome

The Compliance & Regulatory Alignment Statement documents how the initiative aligns with applicable internal policies, contractual obligations, regulatory requirements, and data protection expectations.

It exists to make compliance exposure visible, interpreted, and attributable before and after implementation. A useful statement shows what obligations apply, why they apply, how they are being addressed, and what gaps or dependencies remain.

The intended outcome is that applicable obligations are translated into clear accountability, visible alignment decisions, and understood gaps that can be acted on before they become audit or operational issues.

## 2. When It Is Required

This artifact is required when the initiative is subject to internal policy, regulatory, contractual, sectoral, privacy, or audit obligations that materially affect solution design, operation, or acceptance.

## 3. Intended Readers and Users

- Security / Data Protection Officer
- compliance and governance reviewers
- Sponsor and Business Owner
- Delivery Owner
- audit reviewers

## 4. Intended Project Context

Use this artifact when the initiative needs a formal statement of how obligations were considered and addressed. It is most useful where multiple policy, privacy, or regulatory requirements must be interpreted into practical delivery and control actions.

It should align with NIST CSF governance outcomes and the NIST Privacy Framework by translating obligations into accountable controls, decisions, and actions.

In the Work Delivery Framework lifecycle, this artifact is typically outlined in Stage 2 when obligations materially affect authorization decisions, elaborated in Stage 4, updated through Stage 6 as controls are implemented, and used in Stage 7 acceptance and closure reviews.

## 5. How Much Detail to Include

Include enough detail to identify the applicable obligation, what it means for the initiative, how it is addressed, and what remains open. Do not turn it into a legal treatise.

## 6. Required Content or Minimum Structure

### 6.1. Statement context

Must include:

- initiative or solution name
- scope of the statement
- date or version
- owner

This section identifies what the alignment statement covers.

### 6.2. Required content for each obligation row

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

### 6.3. Open gaps and dependencies

Must include:

- unresolved gaps
- required waivers or exceptions
- dependencies that affect compliance alignment

This section makes unresolved exposure visible.

## 7. What to Keep Out

Keep the following out of this artifact:

- full copies of policies or regulations
- unsupported legal conclusions
- hidden non-compliance in vague notes

## 8. Relationships to Other Artifacts

This artifact should align with:

- [Work Delivery Framework](../work_delivery_framework.md)
- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Security & Privacy Risk Assessment Specification](security_and_privacy_risk_assessment_specification.md)
- [Data Governance & Impact Assessment Specification](../data_governance_and_records_deliverables/data_governance_and_impact_assessment_specification.md)
- [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md)
- [Audit & Monitoring Design Summary Specification](audit_and_monitoring_design_summary_specification.md)
- [Residual Risk Acceptance Record Specification](residual_risk_acceptance_record_specification.md)
- [Formal Acceptance & Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

## 9. Ownership, Review, and Acceptance Expectations

The compliance lead, security lead, or governance reviewer usually coordinates this artifact with business and legal or privacy input where needed.

Formal review should be completed by the relevant compliance or protection authority.

The Delivery Owner is accountable for ensuring open compliance gaps are visible and tracked to decision or treatment. The relevant Acceptance Authority should confirm that material obligations are addressed or explicitly conditionally accepted.

## 10. Maintenance Expectations

Update when obligations change, solution scope changes, or compliance gaps are discovered or resolved.

## 11. Validation Guide

- Does the statement show clearly what obligations apply and why?
- Can a reviewer see how each obligation is being addressed?
- Is there enough evidence or reference detail to verify the claimed alignment?
- Are unresolved gaps, waivers, or dependencies explicit?
- Is ownership assigned for material obligations?

If weak, make the applicability reasoning clearer and tighten ownership of open actions.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Compliance & Regulatory Alignment Statement for this initiative.
> List the applicable obligations, explain briefly why each applies, state how each is being addressed, identify owners, and record any open gaps or waivers.
> Keep it practical and table-driven.
