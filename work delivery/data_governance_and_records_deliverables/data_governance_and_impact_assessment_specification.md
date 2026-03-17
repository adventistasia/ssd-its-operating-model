# Data Governance & Impact Assessment Specification

## 1. Purpose and Intended Outcome

The Data Governance & Impact Assessment identifies the data categories handled by the initiative, the governance implications they create, and the operational, privacy, or compliance impacts that must be managed.

It exists to make data accountability visible before implementation is finalized. A useful assessment tells the organization what data is in play, how sensitive it is, who is accountable, what obligations are triggered, and what impacts require action.

The intended outcome is that data-related obligations, sensitivities, and required actions are identified early enough to shape design, controls, approvals, and operational readiness.

## 2. When It Is Required

This artifact is required when the initiative creates, collects, stores, processes, shares, or materially changes organizational data.

## 3. Intended Readers and Users

- Data Steward
- Data Governance Officer
- Business Owner / Process Owner
- security and privacy reviewers
- Delivery Owner
- operations and support stakeholders where data handling affects service

## 4. Intended Project Context

Use this artifact during design and governance review before implementation is finalized. It is most useful where data sensitivity, stewardship, retention, privacy, or operational impact must be made explicit.

It should align with the NIST Privacy Framework by identifying data categories, privacy implications, and governance actions early. It should also align with NIST CSF governance and identification outcomes by making stewardship, sensitivity, and obligations explicit.

In the Work Delivery Framework lifecycle, this artifact is usually identified at summary level in Stage 2, elaborated in Stage 4, and kept current through Stage 6 when data-handling decisions change. It supports Stage 7 acceptance and closure by showing that data obligations were identified and handled.

## 5. How Much Detail to Include

Include enough detail to explain data categories, sensitivity, obligations, stewardship, and material impacts. Do not turn it into a full data model or a legal opinion.

## 6. Required Content or Minimum Structure

### 6.1. Assessment context

Must include:

- initiative or solution name
- scope of data handling being assessed
- date or version
- assessment owner

This section identifies what data-handling context the assessment covers.

### 6.2. Data categories and sensitivity

Must include:

- categories of data produced, stored, processed, or shared
- sensitivity or classification of those categories
- whether personal, confidential, regulated, or operationally critical data is involved

This section makes the data exposure visible in practical terms.

### 6.3. Governance and obligation impacts

Must include:

- internal policy implications
- regulatory, contractual, or privacy implications where relevant
- operational or lifecycle impacts that require governance attention
- retention, archival, disposal, backup, or recovery obligations where the data creates those requirements

This section shows why the data matters beyond implementation.

### 6.4. Accountability and stewardship

Must include:

- named Data Steward
- other governance or privacy contacts where relevant
- ownership assumptions that affect data quality, retention, or access
- any authority split between business ownership, stewardship, operational custody, or vendor custody where relevant

This section makes accountability explicit.

### 6.5. Risks, issues, and required actions

Should include:

- material governance, privacy, or operational risks
- known gaps or unresolved issues
- required actions and owners where the assessment reveals control needs

This section turns the assessment into a usable governance tool.

## 7. What to Keep Out

Keep the following out of this artifact:

- full field-by-field data dictionaries
- detailed schema design
- full migration procedure detail
- lengthy legal analysis copied from other sources

## 8. Relationships to Other Artifacts

This artifact should align with and inform:

- [Work Delivery Framework](../work_delivery_framework.md)
- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)
- [Data Asset Specification](data_asset_specification.md)
- [Security & Privacy Risk Assessment Specification](../security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md)
- [Compliance & Regulatory Alignment Statement Specification](../security_privacy_and_compliance_deliverables/compliance_and_regulatory_alignment_statement_specification.md)
- [Backup, Restore & Recovery Plan Specification](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md)
- [Operations & Support Model Specification](../operational_readiness_deliverables/operations_and_support_model_specification.md)
- [Operational Readiness Confirmation Record Specification](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md)

## 9. Ownership, Review, and Acceptance Expectations

The Data Steward or analyst responsible for data governance usually coordinates this artifact with security, privacy, and business input.

Review should include the Data Governance Officer where governance exposure is material.

The Delivery Owner is accountable for ensuring this artifact is produced and kept aligned with scope and design decisions. The relevant Acceptance Authority for data-governance outcomes should confirm that material data obligations and actions are visible before acceptance and closure.

## 10. Maintenance Expectations

Update when data categories, sensitivity, stewardship, storage patterns, or triggered obligations change.

## 11. Validation Guide

- Does the assessment make the handled data and its sensitivity clear?
- Are stewardship and governance accountability explicit?
- Are material compliance, privacy, or operational impacts visible?
- Does the assessment make lifecycle and custody obligations visible enough for later operational and security planning?
- Does the artifact show what action is required where risk or obligation exists?

If weak, sharpen the data categories, add accountability, and state the triggered obligations more plainly.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Data Governance & Impact Assessment for this initiative.
> Identify the categories of data involved, their sensitivity, the main governance or compliance implications, the named Data Steward, and the operational or privacy impacts that must be managed.
> Keep it practical and action-oriented.
