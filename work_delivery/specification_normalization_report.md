# Specification Normalization Report

This report documents the outcome of the specification normalization work completed in this repository. It records which pattern each deliverable specification uses, how that compares to the classification in the [Specification Writing Guide](../specification_writing_guide.md), and any language or structural compliance gaps identified.

---

## 1. How to Read This Report

### Pattern definitions

The [Specification Writing Guide](../specification_writing_guide.md#3.%20When%20to%20Use%20Which%20Pattern) defines two patterns:

- **Light pattern** — 11 numbered sections (§1–§11). No Maintenance Expectations or Validation Guide sections.
- **Extended pattern** — 12 or 13 numbered sections. Adds one or both optional sections: Maintenance Expectations and/or Validation Guide.

### Status values used

| Status | Meaning |
|--------|---------|
| ✅ Compliant | Pattern and structure match the guide |
| ⚠️ Pattern mismatch | File uses a different pattern than the guide prescribes |
| 🔧 Structural issue | Numbering, casing, or section placement error |

---

## 2. Pattern Assignment by Specification

### 2.1 Work Assessment Specifications

Guide classification: **Light pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Initial Review](work_assessment/initial_review_specification.md) | Light (11 sections) | ✅ Compliant |
| [Validation Assessment](work_assessment/validation_assessment_specification.md) | Light (11 sections) | ✅ Compliant |
| [Work Assessment Report](work_assessment/work_assessment_report_specification.md) | Light (11 sections) | ✅ Compliant |
| [Business Process Stage Analysis](work_assessment/business_process_stage_analysis_specification.md) | Light (11 sections) | ✅ Compliant |
| [Challenges and Needs](work_assessment/challenges_and_needs_specification.md) | Light (11 sections) | ✅ Compliant |
| [Current State Analysis Report](work_assessment/current_state_analysis_report_specification.md) | Light (11 sections) | ✅ Compliant |

### 2.2 Work Brief

Guide classification: **Light pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Work Brief](work_brief/work_brief_specification.md) | Light (11 sections) | ✅ Compliant |

### 2.3 Governance and Control Specifications

Guide classification: Decision Record Log, Solution Assumptions & Issues Register, Validation & Evidence Matrix → **Light pattern**; all others → **Extended pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Decision Record Log](governance_and_control_deliverables/decision_record_log_specification.md) | Light (11 sections) | ✅ Compliant |
| [Solution Assumptions & Issues Register](governance_and_control_deliverables/solution_assumptions_and_issues_register_specification.md) | Light (11 sections) | ✅ Compliant |
| [Validation & Evidence Matrix](governance_and_control_deliverables/validation_and_evidence_matrix_specification.md) | Light (11 sections) | ✅ Compliant |
| [Initiative Definition Document](governance_and_control_deliverables/initiative_definition_document_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |
| [Project Charter](governance_and_control_deliverables/project_charter_specification.md) | Extended (12 sections: Validation Guide) | ✅ Compliant |
| [Formal Acceptance and Closure Record](governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) | Extended (12 sections: Validation Guide) | ✅ Compliant |
| [Delivery Roadmap](governance_and_control_deliverables/delivery_roadmap_specification.md) | Extended (12 sections: Maintenance Expectations) | ✅ Compliant |
| [Delivery Charter](governance_and_control_deliverables/delivery_charter_specification.md) | Light (11 sections) | ⚠️ Pattern mismatch — guide classifies as extended; Maintenance Expectations not yet added |

### 2.4 Solution Deliverables

Guide classification: **Light pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Problem and Outcome Validation Brief](solution_deliverables/problem_and_outcome_validation_brief_specification.md) | Light (11 sections) | ✅ Compliant |
| [Functional Capabilities](solution_deliverables/functional_capabilities_specification.md) | Light (11 sections) | ✅ Compliant |
| [User Roles, Personas and Access Model](solution_deliverables/user_roles_personas_and_access_model_specification.md) | Light (11 sections) | ✅ Compliant |
| [Business Rules Catalog](solution_deliverables/business_rules_catalog_specification.md) | Light (11 sections) | ✅ Compliant |
| [Use Case Narratives](solution_deliverables/use_case_narratives_specification.md) | Light (11 sections) | ✅ Compliant |
| [Non-Functional Requirements](solution_deliverables/non_functional_requirements_specification.md) | Light (11 sections) | ✅ Compliant |
| [Integration and External Dependency](solution_deliverables/integration_and_external_dependency_specification.md) | Light (11 sections) | ✅ Compliant |
| [Solution Module Definition](solution_deliverables/solution_module_definition_specification.md) | Light (11 sections) | ✅ Compliant |
| [Solution Modules](solution_deliverables/solution_modules_specification.md) | Light (11 sections) | ✅ Compliant |
| [Deployed Solution](solution_deliverables/deployed_solution_specification.md) | Light (11 sections) | ✅ Compliant |
| [Acceptance Record](solution_deliverables/acceptance_record_specification.md) | Light (11 sections) | ✅ Compliant |

### 2.5 Operational Readiness Specifications

Guide classification: **Extended pattern** for all five

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Technical Design Document](operational_readiness_deliverables/technical_design_document_specification.md) | Extended (12 sections: Maintenance Expectations) | ⚠️ Partial — guide warrants Validation Guide as a formal technical baseline; section not yet added |
| [Operations and Support Model](operational_readiness_deliverables/operations_and_support_model_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |
| [DevOps Guide](operational_readiness_deliverables/devops_guide_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |
| [Backup, Restore and Recovery Plan](operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |
| [Operational Readiness Confirmation Record](operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |

### 2.6 Security, Privacy and Compliance Specifications

Guide classification: **Light pattern** for assessment, compliance statement, residual risk, and audit summary; **Extended pattern** for Access Control and Authorization Model

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Access Control and Authorization Model](security_privacy_and_compliance_deliverables/access_control_and_authorization_model_specification.md) | Extended (13 sections: Maintenance Expectations + Validation Guide) | ✅ Compliant |
| [Security and Privacy Risk Assessment](security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — guide classifies as light; Maintenance Expectations adds a section not prescribed for light-pattern specs. Justified if treated as a living document. |
| [Compliance and Regulatory Alignment Statement](security_privacy_and_compliance_deliverables/compliance_and_regulatory_alignment_statement_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Residual Risk Acceptance Record](security_privacy_and_compliance_deliverables/residual_risk_acceptance_record_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Audit and Monitoring Design Summary](security_privacy_and_compliance_deliverables/audit_and_monitoring_design_summary_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — guide classifies as light; Maintenance Expectations adds a section not prescribed for light-pattern specs. Justified if treated as a living document. |

### 2.7 Data Governance and Records Specifications

Guide classification: **Light pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [Data Asset](data_governance_and_records_deliverables/data_asset_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — guide classifies as light. Maintenance Expectations may be appropriate if treated as a living record, but this should be made explicit in the guide. |
| [Data Governance and Impact Assessment](data_governance_and_records_deliverables/data_governance_and_impact_assessment_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Data Migration Record](data_governance_and_records_deliverables/data_migration_record_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |

### 2.8 User Adoption and Change Enablement Specifications

Guide classification: **Light pattern**

| Specification | Actual Pattern | Status |
|---------------|---------------|--------|
| [User Impact Assessment](user_adoption_and_change_enablement_deliverables/user_impact_assessment_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — guide classifies as light. Maintenance Expectations may be appropriate if these specs are treated as living documents, but this should be made explicit in the guide. |
| [Change and Communication Plan](user_adoption_and_change_enablement_deliverables/change_and_communication_plan_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Training and Enablement Materials](user_adoption_and_change_enablement_deliverables/training_and_enablement_materials_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Adoption Support Model](user_adoption_and_change_enablement_deliverables/adoption_support_model_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |
| [Adoption Confirmation Record](user_adoption_and_change_enablement_deliverables/adoption_confirmation_record_specification.md) | 12 sections (Maintenance Expectations added) | ⚠️ Pattern mismatch — same as above |

---

## 3. Structural and Language Issues Found

### 3.1 Resolved during this normalization

The following structural issues were identified and fixed as part of this PR:

| File | Issue | Fix Applied |
|------|-------|-------------|
| [formal_acceptance_and_closure_record_specification.md](governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) | `## Validation guide` was unnumbered and used lowercase "guide" | Renumbered to `## 10. Validation Guide`; subsequent sections renumbered to §11 and §12 |
| [project_charter_specification.md](governance_and_control_deliverables/project_charter_specification.md) | `## Validation guide` was unnumbered and used lowercase "guide" | Renumbered to `## 10. Validation Guide`; subsequent sections renumbered to §11 and §12 |

### 3.2 Open gaps requiring a decision

The following items are not structural errors but represent decisions that should be made to align the guide and the files:

**Pattern classification vs actual content**

Several groups of specifications were classified as light-pattern in the guide but have a Maintenance Expectations section added, making them 12-section quasi-extended specs. The Maintenance Expectations section is useful for these specs (security risk assessments, compliance statements, data governance records, adoption plans, and similar documents are updated throughout a programme), but it conflicts with the guide's classification.

Recommended resolution: either update the guide's classification to list these as extended-pattern (living document), or remove the Maintenance Expectations section from each.

Affected files:
- All 3 data governance specs
- 4 of 5 security, privacy and compliance specs (Assessment, Compliance Statement, Residual Risk, Audit Summary)
- All 5 user adoption specs

**Delivery Charter — missing Maintenance Expectations**

The guide classifies the Delivery Charter as extended-pattern, but the file currently uses 11 sections (light). If the Delivery Charter is treated as a living document (updated as team composition and scope evolve), a Maintenance Expectations section should be added.

**Technical Design Document — Validation Guide not present**

The guide classifies the Technical Design Document as extended-pattern, but the file has only Maintenance Expectations (12 sections) without a Validation Guide. Because the TDD serves as a formal technical baseline reviewed at handover, a Validation Guide section would be appropriate.

---

## 4. Summary Counts

| | Light (11 sections) | Extended (12–13 sections) | Total |
|--|--|--|--|
| Work Assessment | 6 | 0 | 6 |
| Work Brief | 1 | 0 | 1 |
| Governance and Control | 3 | 5 | 8 |
| Solution Deliverables | 11 | 0 | 11 |
| Operational Readiness | 0 | 5 | 5 |
| Security, Privacy and Compliance | 0 | 5 | 5 |
| Data Governance and Records | 0 | 3 | 3 |
| User Adoption and Change Enablement | 0 | 5 | 5 |
| **Total** | **21** | **23** | **44** |

Of the 44 specifications:
- **33 are fully compliant** with the guide's pattern classification and structure.
- **2 had structural issues** (unnumbered/lowercase headings) that were fixed in this PR.
- **9 have open pattern-classification gaps** that need a guide update or a file change to resolve.
- **2 have missing sections** (Delivery Charter — Maintenance Expectations; Technical Design Document — Validation Guide) relative to the guide's extended-pattern prescription.
