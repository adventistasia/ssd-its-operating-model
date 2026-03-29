# Security & Privacy Risk Assessment Specification

## 1. What This Artifact Is For

The Security & Privacy Risk Assessment identifies, evaluates, and records the security and privacy risks introduced or changed by the solution, along with the controls or treatment actions needed to reduce those risks.

It exists to make risk visible before it becomes an operational surprise. A useful assessment shows what could go wrong, what assets or data are affected, how serious the impact could be, what controls are already in place, and what residual risk remains.

The intended outcome is that material security and privacy risks are understood early, addressed deliberately, and carried forward into control decisions, readiness, and risk acceptance.

Intended readers include: Security / Data Protection Officer, Business Owner / Process Owner, Delivery Owner, solution and infrastructure leads, and Data Steward where data sensitivity is relevant.

## 2. When to Use It

This artifact is required when the initiative introduces or materially changes systems, data handling, integrations, access models, hosting arrangements, or user behaviors that affect security or privacy risk.

Use this artifact during design, before deployment, and whenever risk posture changes materially. It is most useful where the organization must decide what controls are needed and whether remaining risk is acceptable.

It should align with NIST SP 800-30 risk-assessment practice, NIST CSF 2.0, the NIST Privacy Framework, and ITIL 4 information security management thinking by framing risks, impacts, control needs, and residual exposure clearly.

## 3. Stage Fit and Handoffs

Initiated in Stage 2 at summary level, elaborated in Stage 4, updated in Stage 6 as risk conditions change, and used as evidence for Stage 7 acceptance and closure decisions.

Upstream inputs:

- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)

Downstream outputs inform:

- [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md)
- [Compliance & Regulatory Alignment Statement Specification](compliance_and_regulatory_alignment_statement_specification.md)
- [Residual Risk Acceptance Record Specification](residual_risk_acceptance_record_specification.md)

Also relates to:

- [Data Governance & Impact Assessment Specification](../data_governance_and_records_deliverables/data_governance_and_impact_assessment_specification.md)

## 4. Before You Start

Before drafting, confirm you have:

- confirmed initiative or solution scope
- known data types, access models, or integrations
- identified threat surface or known compliance obligations
- named security lead and Delivery Owner
- reference to the Initiative Definition Document or Work Brief

## 5. How to Draft It

1. Define assessment context — identify the scope, solution name, date, and owner (from 6.1).
2. Identify and describe risk scenarios — name threat, misuse, failure, or exposure scenarios with affected assets and why they matter (from 6.2).
3. Rate impact and severity — assess organizational, operational, legal, security, or privacy impacts and apply a risk rating (from 6.3).
4. Define control and treatment expectations — document controls in place and required, with named owners for each treatment action (from 6.4).
5. State residual risk — describe remaining exposure after planned controls and identify whether formal acceptance is required (from 6.5).
6. Review for hidden risk or vague statements and tighten ownership.

## 6. Minimum Structure

### 6.1. Assessment Context

Must include:

- scope of the assessment
- solution or service name
- date or version
- assessment owner

This section identifies what risk surface the assessment covers.

### 6.2. Risk Scenarios

Must include:

- threat, misuse, failure, or exposure scenarios
- assets, services, or data affected
- why the scenario matters
- source of exposure or threat path where that is needed to understand the risk realistically

This section makes the risks concrete enough to assess.

### 6.3. Impact and Severity View

Must include:

- likely organizational, operational, legal, security, or privacy impacts
- risk rating or prioritization method

This section shows how serious the risk is and why it needs attention.

### 6.4. Control and Treatment Expectations

Must include:

- controls already in place
- additional controls required
- owner for each required action or treatment

This section turns the assessment into a usable control-planning artifact.

### 6.5. Residual Risk Statement

Must include:

- remaining risk after planned controls
- whether formal residual risk acceptance is required
- trigger for escalation or re-assessment where the residual exposure cannot be accepted as-is

This section prevents silent risk acceptance.

## 7. Writing Rules

Include enough detail to describe the asset or process at risk, the threat or misuse scenario, the likely impact, existing or planned controls, and the residual exposure. Do not turn it into a generic policy restatement.

Keep the following out of this artifact:

- vague risk statements with no scenario or impact basis
- full control procedure text copied from standards
- hidden residual risk inside narrative paragraphs

## 8. Traceability, Ownership, and Review

The security lead or reviewer usually coordinates the assessment with business, delivery, privacy, and technical stakeholders.

Material risks should be reviewed by the Security / Data Protection Officer and relevant decision authorities.

The Delivery Owner is accountable for ensuring this artifact is kept current through design and delivery. Where residual risk remains material, a named risk acceptance authority must make an explicit acceptance decision before closure.

## 9. Maintenance Expectations

Update when design, access, data handling, threat exposure, hosting, or regulatory obligations change. Revisit after material incidents or control failures.

## 10. Done When

- The assessment explains what could go wrong and why it matters.
- Required controls and treatment owners are explicit.
- Residual risk is visible after mitigation rather than assumed away.
- A decision-maker can tell which risks still need explicit acceptance, redesign, or control strengthening.
- A decision-maker can understand what action or acceptance is required.

## 11. What Comes Next

1. Review with Security / Data Protection Officer.
2. Use outputs to inform the [Access Control & Authorization Model Specification](access_control_and_authorization_model_specification.md).
3. Record unresolved exposure in the [Residual Risk Acceptance Record Specification](residual_risk_acceptance_record_specification.md).
4. Keep current through delivery and update at Stage 7 acceptance.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Security & Privacy Risk Assessment for this solution.
Identify the main threat or misuse scenarios, the assets or data affected, the likely impact, the controls already in place or still required, and the residual risk after treatment.
Keep it practical and decision-ready.
```

### 12.2. Validation Prompt

```
Review this Security & Privacy Risk Assessment.
Check that each risk scenario has a clear description, named assets or data, an impact statement, named controls and owners, and an explicit residual risk position.
Flag any vague risk statements, missing treatment owners, or hidden residual exposure.
```
