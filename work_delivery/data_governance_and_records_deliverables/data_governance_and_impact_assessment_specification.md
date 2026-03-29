# Data Governance & Impact Assessment Specification

## 1. What This Artifact Is For

The Data Governance & Impact Assessment identifies the data categories handled by the initiative, the governance implications they create, and the operational, privacy, or compliance impacts that must be managed.

It exists to make data accountability visible before implementation is finalized. A useful assessment tells the organization what data is in play, how sensitive it is, who is accountable, what obligations are triggered, and what impacts require action.

The intended outcome is that data-related obligations, sensitivities, and required actions are identified early enough to shape design, controls, approvals, and operational readiness.

Intended readers include: Data Steward, Data Governance Officer, Business Owner / Process Owner, security and privacy reviewers, Delivery Owner, and operations and support stakeholders where data handling affects service.

## 2. When to Use It

This artifact is required when the initiative creates, collects, stores, processes, shares, or materially changes organizational data.

Use this artifact during design and governance review before implementation is finalized. It is most useful where data sensitivity, stewardship, retention, privacy, or operational impact must be made explicit.

It should align with the NIST Privacy Framework by identifying data categories, privacy implications, and governance actions early. It should also align with NIST CSF governance and identification outcomes by making stewardship, sensitivity, and obligations explicit.

In the Work Delivery Framework lifecycle, this artifact is usually identified at summary level in Stage 2, elaborated in Stage 4, and kept current through Stage 6 when data-handling decisions change. It supports Stage 7 acceptance and closure by showing that data obligations were identified and handled.

## 3. Stage Fit and Handoffs

**Upstream inputs:**

- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md) — provides the approved scope and data categories that bound the assessment

**Downstream consumers:**

- [Data Asset Specification](data_asset_specification.md) — receives data structure and stewardship details identified in this assessment
- [Security & Privacy Risk Assessment](../security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md) — uses data sensitivity and obligation findings from this assessment to identify and rate security and privacy risks
- [Compliance & Regulatory Alignment Statement](../security_privacy_and_compliance_deliverables/compliance_and_regulatory_alignment_statement_specification.md) — draws on identified regulatory and contractual obligations from this assessment
- [Operational Readiness Confirmation Record](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) — requires confirmation that data obligations have been addressed before closure

**Also relates to:**

- [Backup, Restore & Recovery Plan Specification](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) — uses lifecycle and recovery obligations identified in this assessment
- [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md) — uses data handling and custodial accountability from this assessment

## 4. Before You Start

Confirm the following inputs are available before drafting:

- known initiative scope and the data categories being created, collected, stored, processed, or shared
- identified or proposed Data Steward and Data Governance Officer
- known privacy or regulatory obligations that apply to the data categories in scope
- reference to the [Initiative Definition Document](../governance_and_control_deliverables/initiative_definition_document_specification.md) that authorized the work

## 5. How to Draft It

1. **Complete assessment context** (§6.1) — record the initiative or solution name, scope, date or version, and assessment owner.
2. **Describe data categories and sensitivity** (§6.2) — list the categories of data in play, their sensitivity or classification, and whether personal, confidential, regulated, or operationally critical data is involved.
3. **Document governance and obligation impacts** (§6.3) — identify internal policy implications, regulatory or privacy obligations, and lifecycle impacts such as retention, archival, disposal, backup, or recovery requirements.
4. **Record accountability and stewardship** (§6.4) — name the Data Steward and governance or privacy contacts, and make ownership assumptions explicit.
5. **Identify risks, issues, and required actions** (§6.5) — surface material governance, privacy, or operational risks; note gaps; and assign required actions to owners.

## 6. Minimum Structure

### 6.1. Assessment Context

Must include:

- initiative or solution name
- scope of data handling being assessed
- date or version
- assessment owner

This section identifies what data-handling context the assessment covers.

### 6.2. Data Categories and Sensitivity

Must include:

- categories of data produced, stored, processed, or shared
- sensitivity or classification of those categories
- whether personal, confidential, regulated, or operationally critical data is involved

This section makes the data exposure visible in practical terms.

### 6.3. Governance and Obligation Impacts

Must include:

- internal policy implications
- regulatory, contractual, or privacy implications where relevant
- operational or lifecycle impacts that require governance attention
- retention, archival, disposal, backup, or recovery obligations where the data creates those requirements

This section shows why the data matters beyond implementation.

### 6.4. Accountability and Stewardship

Must include:

- named Data Steward
- other governance or privacy contacts where relevant
- ownership assumptions that affect data quality, retention, or access
- any authority split between business ownership, stewardship, operational custody, or vendor custody where relevant

This section makes accountability explicit.

### 6.5. Risks, Issues, and Required Actions

Should include:

- material governance, privacy, or operational risks
- known gaps or unresolved issues
- required actions and owners where the assessment reveals control needs

This section turns the assessment into a usable governance tool.

## 7. Writing Rules

Include enough detail to explain data categories, sensitivity, obligations, stewardship, and material impacts. Do not turn it into a full data model or a legal opinion.

Keep the following out of this artifact:

- full field-by-field data dictionaries
- detailed schema design
- full migration procedure detail
- lengthy legal analysis copied from other sources

## 8. Traceability, Ownership, and Review

The Data Steward or analyst responsible for data governance usually coordinates this artifact with security, privacy, and business input.

Review should include the Data Governance Officer where governance exposure is material.

The Delivery Owner is accountable for ensuring this artifact is produced and kept aligned with scope and design decisions. The relevant Acceptance Authority for data-governance outcomes should confirm that material data obligations and actions are visible before acceptance and closure.

## 9. Maintenance Expectations

Update when data categories, sensitivity, stewardship, storage patterns, or triggered obligations change.

## 10. Done When

- Data categories and sensitivity are described
- Named Data Steward and governance contacts are visible
- Governance, privacy, and compliance implications are stated
- Material impacts requiring action are identified with owners
- Lifecycle and custody obligations are visible

## 11. What Comes Next

1. Inform the [Data Asset Specification](data_asset_specification.md) with data structure and stewardship details identified in this assessment.
2. Feed identified obligations into the [Compliance & Regulatory Alignment Statement](../security_privacy_and_compliance_deliverables/compliance_and_regulatory_alignment_statement_specification.md).
3. Flag data risks to the [Security & Privacy Risk Assessment](../security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md) for rating and control assignment.
4. Reference when preparing the [Operational Readiness Confirmation Record](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) to confirm data obligations have been handled.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Data Governance & Impact Assessment for this initiative.
Identify the categories of data involved, their sensitivity, the main governance or compliance implications, the named Data Steward, and the operational or privacy impacts that must be managed.
Keep it practical and action-oriented.
```

### 12.2. Validation Prompt

```
Review this Data Governance & Impact Assessment.
Check that data categories and sensitivity are described; named Data Steward and governance contacts are visible; governance, privacy, and compliance implications are stated; material impacts requiring action are identified with owners; and lifecycle and custody obligations are visible.
Note any gaps in accountability, obligation coverage, or required actions.
```
