# Data Asset Specification

## 1. What This Artifact Is For

The Data Asset Specification provides authoritative documentation of the key data handled by the initiative so that ownership, structure, storage, lifecycle, and recoverability are clear.

It exists to make the data understandable and governable beyond the original designer. A useful specification helps operations, support, security, governance, and future change teams understand what the asset is, where it lives, who owns it, and how it should be managed over time.

The intended outcome is that the data asset can be governed, protected, supported, and changed with clear ownership and without needing to rediscover core facts about the data.

Intended readers include: Data Steward, data analysts and designers, security and privacy reviewers, IT Operations / Service Owner, support teams, and audit reviewers.

## 2. When to Use It

This artifact is required when the initiative introduces, changes, or depends materially on governed data assets.

Use this artifact when the organization needs a practical, authoritative view of the data asset beyond a generic project description. It is most useful where data ownership, system of record, retention, storage, and recovery treatment must be explicit.

It should align with NIST planning and privacy-management guidance by making inventory, stewardship, storage, and lifecycle expectations visible. It should also support recovery and control planning by showing what data exists and where it is authoritative.

In the Work Delivery Framework lifecycle, this artifact is usually identified at summary level in Stage 2, elaborated in Stage 4, and validated as delivery evidence in Stage 6. It supports Stage 7 by providing a clear, supportable record of data ownership and lifecycle treatment.

## 3. Stage Fit and Handoffs

**Upstream inputs:**

- [Initiative Definition Document Specification](../governance_and_control_deliverables/initiative_definition_document_specification.md) — confirms the approved scope and data categories the specification must cover
- [Data Governance & Impact Assessment](data_governance_and_impact_assessment_specification.md) — identifies data sensitivity, obligations, and stewardship context that inform this specification

**Downstream consumers:**

- [Backup, Restore & Recovery Plan](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) — uses storage locations, lifecycle, and recovery status from this specification
- [Data Migration Record](data_migration_record_specification.md) — references this specification for source and target asset context and must be updated after cutover
- [Operational Readiness Confirmation Record](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) — requires a current data asset record before closure is confirmed

**Also relates to:**

- [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md) — shares structural context; this specification focuses on governance rather than design
- [Security & Privacy Risk Assessment Specification](../security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md) — uses sensitivity and storage information from this specification to assess risk

## 4. Before You Start

Confirm the following inputs are available before drafting:

- confirmed initiative scope and data categories in scope
- named Data Steward
- known storage locations and environments
- understanding of retention obligations and recovery requirements
- reference to the [Initiative Definition Document](../governance_and_control_deliverables/initiative_definition_document_specification.md) or Work Brief that authorized the work

## 5. How to Draft It

1. **Document data asset context** (§6.1) — name the asset, state its business purpose, define its scope, and record the version or status.
2. **Describe structure and content** (§6.2) — identify key entities and relationships, and capture a data dictionary for important fields or attributes.
3. **Record ownership and authority** (§6.3) — declare the system of record, name the responsible owner and Data Steward, and note any systems that republish or derive the data.
4. **Document storage and lifecycle treatment** (§6.4) — record storage locations, retention rules, archival treatment, backup or recovery inclusion status, and disposal approach.
5. **Add supporting notes for recovery, quality, or interface context** (§6.5) — note downstream usage, known data-quality constraints, and operational notes that affect support or recovery.

## 6. Minimum Structure

### 6.1. Data Asset Context

Must include:

- data asset name
- business purpose
- scope of the asset
- version or status

This section identifies the governed asset and why it exists.

### 6.2. Structure and Content View

Must include:

- key entities and relationships, or a reference to them
- data dictionary for important fields or attributes

This section makes the asset understandable to readers other than the original designer.

### 6.3. Ownership and Authority

Must include:

- system of record declaration
- responsible owner
- Data Steward
- note of any other system that republishes, caches, or derives the data where that affects authority or reconciliation

This section makes governance and correctness accountability explicit.

### 6.4. Storage and Lifecycle Treatment

Must include:

- storage locations and environments
- retention rules
- lifecycle or archival treatment
- backup or recovery inclusion status where applicable
- disposal or decommissioning treatment where relevant

This section shows how the asset is managed over time.

### 6.5. Optional Supporting Notes

Should include when useful:

- downstream usage or interface notes
- known data-quality constraints
- operational notes that materially affect support or recovery

This section adds practical context without expanding the artifact into a full design pack.

## 7. Writing Rules

Include enough detail to describe the key entities, attributes, ownership, storage, system of record, retention, and recovery relevance. Do not try to replace a full enterprise data catalog or every physical schema artifact.

Keep the following out of this artifact:

- every physical table, column, or ETL detail unless essential
- full migration execution content
- lengthy legal text
- unrelated business-process instructions

## 8. Traceability, Ownership, and Review

The Data Steward or data design lead usually owns this artifact with delivery and operations input.

Review should include relevant governance, security, and support stakeholders.

The Delivery Owner is accountable for ensuring this artifact stays aligned with authorized scope and implemented behavior. The relevant Acceptance Authority should confirm the data-asset record is complete enough for ongoing support and governance before closure.

## 9. Maintenance Expectations

Update when data structure, ownership, system of record, storage, retention, or recovery treatment changes materially.

## 10. Done When

- Data asset name, purpose, and scope are documented
- Key entities, relationships, and important attributes are described
- Data Steward and system of record are named
- Storage locations, retention rules, and lifecycle treatment are recorded
- Backup or recovery inclusion status is stated
- A reviewer other than the original designer can understand and use the record

## 11. What Comes Next

1. Reference this specification in the [Data Governance & Impact Assessment](data_governance_and_impact_assessment_specification.md) to align data structure and stewardship details.
2. Use as input to the [Backup, Restore & Recovery Plan](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) when defining recovery scope for this asset.
3. Reference when planning a [Data Migration Record](data_migration_record_specification.md) if data is moving, and update after cutover to reflect the new authoritative location.
4. Confirm the record is current before the [Operational Readiness Confirmation Record](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) is finalized.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Data Asset Specification for this initiative.
Describe the asset's purpose, key entities or structures, important attributes, system of record, storage locations, ownership, lifecycle rules, and backup or recovery relevance.
Keep it authoritative, practical, and maintainable.
```

### 12.2. Validation Prompt

```
Review this Data Asset Specification.
Check that the data asset name, purpose, and scope are documented; key entities and attributes are described; Data Steward and system of record are named; storage locations, retention rules, and lifecycle treatment are recorded; and backup or recovery inclusion status is stated.
Confirm that a reviewer other than the original designer can understand and use the record.
Note any gaps in stewardship clarity, lifecycle rules, or system-of-record boundaries.
```
