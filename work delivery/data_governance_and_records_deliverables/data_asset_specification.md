# Data Asset Specification

## 1. Purpose and Intended Outcome

The Data Asset Specification provides authoritative documentation of the key data handled by the initiative so that ownership, structure, storage, lifecycle, and recoverability are clear.

It exists to make the data understandable and governable beyond the original designer. A useful specification helps operations, support, security, governance, and future change teams understand what the asset is, where it lives, who owns it, and how it should be managed over time.

The intended outcome is that the data asset can be governed, protected, supported, and changed with clear ownership and without needing to rediscover core facts about the data.

## 2. When It Is Required

This artifact is required when the initiative introduces, changes, or depends materially on governed data assets.

## 3. Intended Readers and Users

- Data Steward
- data analysts and designers
- security and privacy reviewers
- IT Operations / Service Owner
- support teams
- audit reviewers

## 4. Intended Project Context

Use this artifact when the organization needs a practical, authoritative view of the data asset beyond a generic project description. It is most useful where data ownership, system of record, retention, storage, and recovery treatment must be explicit.

It should align with NIST planning and privacy-management guidance by making inventory, stewardship, storage, and lifecycle expectations visible. It should also support recovery and control planning by showing what data exists and where it is authoritative.

## 5. How Much Detail to Include

Include enough detail to describe the key entities, attributes, ownership, storage, system of record, retention, and recovery relevance. Do not try to replace a full enterprise data catalog or every physical schema artifact.

## 6. Required Content or Minimum Structure

### 6.1. Data asset context

Must include:

- data asset name
- business purpose
- scope of the asset
- version or status

This section identifies the governed asset and why it exists.

### 6.2. Structure and content view

Must include:

- key entities and relationships, or a reference to them
- data dictionary for important fields or attributes

This section makes the asset understandable to readers other than the original designer.

### 6.3. Ownership and authority

Must include:

- system of record declaration
- responsible owner
- Data Steward
- note of any other system that republishes, caches, or derives the data where that affects authority or reconciliation

This section makes governance and correctness accountability explicit.

### 6.4. Storage and lifecycle treatment

Must include:

- storage locations and environments
- retention rules
- lifecycle or archival treatment
- backup or recovery inclusion status where applicable
- disposal or decommissioning treatment where relevant

This section shows how the asset is managed over time.

### 6.5. Optional supporting notes

Should include when useful:

- downstream usage or interface notes
- known data-quality constraints
- operational notes that materially affect support or recovery

This section adds practical context without expanding the artifact into a full design pack.

## 7. What to Keep Out

Keep the following out of this artifact:

- every physical table, column, or ETL detail unless essential
- full migration execution content
- lengthy legal text
- unrelated business-process instructions

## 8. Relationships to Other Artifacts

This artifact should align with the Data Governance & Impact Assessment, Technical Design Document, Backup, Restore & Recovery Plan, Security & Privacy Risk Assessment, and Data Migration Record where applicable.

## 9. Ownership, Review, and Acceptance Expectations

The Data Steward or data design lead usually owns this artifact with delivery and operations input.

Review should include relevant governance, security, and support stakeholders.

## 10. Maintenance Expectations

Update when data structure, ownership, system of record, storage, retention, or recovery treatment changes materially.

## 11. Validation Guide

- Does it make the data asset understandable to someone other than the original designer?
- Are ownership, system of record, and storage locations clear?
- Are lifecycle and recoverability expectations visible?
- Is the system-of-record boundary clear enough to support reconciliation, migration, and audit?
- Does it stay focused on the governed asset rather than drifting into full technical schema detail?

If weak, add stewardship clarity, simplify the structure description, and make the lifecycle rules easier to find.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Data Asset Specification for this initiative.
> Describe the asset's purpose, key entities or structures, important attributes, system of record, storage locations, ownership, lifecycle rules, and backup or recovery relevance.
> Keep it authoritative, practical, and maintainable.
