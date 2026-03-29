# Specification Normalization Report

This report documents the outcome of the specification normalization work completed in this repository. It records which pattern each deliverable specification uses, how it applies the pattern criteria from the [Specification Writing Guide](../specification_writing_guide.md), and any language or structural compliance gaps identified.

---

## 1. How to Read This Report

### Pattern definitions

The [Specification Writing Guide](../specification_writing_guide.md#3.%20When%20to%20Use%20Which%20Pattern) defines two patterns. The choice is based on the properties of the artifact, not a fixed assignment:

- **Light pattern** — 11 numbered sections (§1–§11). Use when the artifact is produced once, primarily enables a decision or records an outcome, and is unlikely to need formal ongoing maintenance after acceptance.
- **Extended pattern** — 12 or 13 numbered sections. Adds one or both optional sections: Maintenance Expectations (for living documents) and/or Validation Guide (for formal governance baselines requiring sign-off or complex technical control documents).

### Status values used

| Status | Meaning |
|--------|---------|
| ✅ Compliant | Pattern and structure match the guide criteria |
| ⚠️ Pattern mismatch | Sections present do not align with artifact properties |
| 🔧 Structural issue | Numbering, casing, or section placement error |

---

## 2. Pattern Assignment by Specification

### 2.1 Work Assessment Specifications

Work assessment specs are produced once per assessment engagement. They record findings and recommendations but are not maintained beyond the assessment stage.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Initial Review](work_assessment/initial_review_specification.md) | Light | 11 | Once-produced assessment output | ✅ Compliant |
| [Validation Assessment](work_assessment/validation_assessment_specification.md) | Light | 11 | Once-produced assessment output | ✅ Compliant |
| [Work Assessment Report](work_assessment/work_assessment_report_specification.md) | Light | 11 | Once-produced decision-enabling output | ✅ Compliant |
| [Business Process Stage Analysis](work_assessment/business_process_stage_analysis_specification.md) | Light | 11 | Once-produced analysis artifact | ✅ Compliant |
| [Challenges and Needs](work_assessment/challenges_and_needs_specification.md) | Light | 11 | Once-produced assessment output | ✅ Compliant |
| [Current State Analysis Report](work_assessment/current_state_analysis_report_specification.md) | Light | 11 | Once-produced analysis artifact | ✅ Compliant |

### 2.2 Work Brief

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Work Brief](work_brief/work_brief_specification.md) | Light | 11 | Once-produced decision artifact; not a living document | ✅ Compliant |

### 2.3 Governance and Control Specifications

Logs and registers are inherently living documents that must be kept current throughout delivery — they receive Maintenance Expectations. Approval-bearing records receive a Validation Guide.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Decision Record Log](governance_and_control_deliverables/decision_record_log_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living log — updated as decisions are made throughout delivery | ✅ Compliant |
| [Solution Assumptions & Issues Register](governance_and_control_deliverables/solution_assumptions_and_issues_register_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living register — updated as assumptions and issues are identified and resolved | ✅ Compliant |
| [Validation & Evidence Matrix](governance_and_control_deliverables/validation_and_evidence_matrix_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living tracking artifact — updated as evidence is collected and items validated | ✅ Compliant |
| [Initiative Definition Document](governance_and_control_deliverables/initiative_definition_document_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Living governance baseline subject to formal sign-off | ✅ Compliant |
| [Project Charter](governance_and_control_deliverables/project_charter_specification.md) | Extended | 12 (+ Validation Guide) | Formal governance baseline requiring authorization | ✅ Compliant |
| [Formal Acceptance and Closure Record](governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) | Extended | 12 (+ Validation Guide) | Approval-bearing closure record requiring formal sign-off | ✅ Compliant |
| [Delivery Roadmap](governance_and_control_deliverables/delivery_roadmap_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated at each stage gate | ✅ Compliant |
| [Delivery Charter](governance_and_control_deliverables/delivery_charter_specification.md) | Light | 11 | Produced once at Stage 5 mobilization; not a living document | ✅ Compliant |

### 2.4 Solution Deliverables

Solution deliverables are produced once during Work Definition Details (Stage 4). They enable design and delivery decisions but are not maintained as living documents after acceptance.

| Specification | Pattern | Sections | Status |
|---------------|---------|----------|--------|
| [Problem and Outcome Validation Brief](solution_deliverables/problem_and_outcome_validation_brief_specification.md) | Light | 11 | ✅ Compliant |
| [Functional Capabilities](solution_deliverables/functional_capabilities_specification.md) | Light | 11 | ✅ Compliant |
| [User Roles, Personas and Access Model](solution_deliverables/user_roles_personas_and_access_model_specification.md) | Light | 11 | ✅ Compliant |
| [Business Rules Catalog](solution_deliverables/business_rules_catalog_specification.md) | Light | 11 | ✅ Compliant |
| [Use Case Narratives](solution_deliverables/use_case_narratives_specification.md) | Light | 11 | ✅ Compliant |
| [Non-Functional Requirements](solution_deliverables/non_functional_requirements_specification.md) | Light | 11 | ✅ Compliant |
| [Integration and External Dependency](solution_deliverables/integration_and_external_dependency_specification.md) | Light | 11 | ✅ Compliant |
| [Solution Module Definition](solution_deliverables/solution_module_definition_specification.md) | Light | 11 | ✅ Compliant |
| [Solution Modules](solution_deliverables/solution_modules_specification.md) | Light | 11 | ✅ Compliant |
| [Deployed Solution](solution_deliverables/deployed_solution_specification.md) | Light | 11 | ✅ Compliant |
| [Acceptance Record](solution_deliverables/acceptance_record_specification.md) | Light | 11 | ✅ Compliant |

### 2.5 Operational Readiness Specifications

Operational artifacts are either formal technical baselines reviewed at handover (Validation Guide), living reference documents kept current after go-live (Maintenance Expectations), or both.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Technical Design Document](operational_readiness_deliverables/technical_design_document_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Formal technical baseline; living reference updated when design changes materially | ✅ Compliant |
| [Operations and Support Model](operational_readiness_deliverables/operations_and_support_model_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Living operating model; formal baseline reviewed at handover | ✅ Compliant |
| [DevOps Guide](operational_readiness_deliverables/devops_guide_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Living operational guide; reviewed at handover | ✅ Compliant |
| [Backup, Restore and Recovery Plan](operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Living plan; formal baseline reviewed at operational readiness | ✅ Compliant |
| [Operational Readiness Confirmation Record](operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Approval-bearing readiness record | ✅ Compliant |

### 2.6 Security, Privacy and Compliance Specifications

Security and compliance artifacts are living documents updated as threat landscapes, controls, and regulatory requirements change.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Access Control and Authorization Model](security_privacy_and_compliance_deliverables/access_control_and_authorization_model_specification.md) | Extended | 13 (+ Maintenance Expectations + Validation Guide) | Living control document; formal baseline reviewed at each access review | ✅ Compliant |
| [Security and Privacy Risk Assessment](security_privacy_and_compliance_deliverables/security_and_privacy_risk_assessment_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated as risk profile changes | ✅ Compliant |
| [Compliance and Regulatory Alignment Statement](security_privacy_and_compliance_deliverables/compliance_and_regulatory_alignment_statement_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated as regulatory requirements change | ✅ Compliant |
| [Residual Risk Acceptance Record](security_privacy_and_compliance_deliverables/residual_risk_acceptance_record_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living record updated as residual risk items are revisited | ✅ Compliant |
| [Audit and Monitoring Design Summary](security_privacy_and_compliance_deliverables/audit_and_monitoring_design_summary_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated as monitoring design evolves | ✅ Compliant |

### 2.7 Data Governance and Records Specifications

Data governance artifacts are living records maintained throughout the life of the service or dataset.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [Data Asset](data_governance_and_records_deliverables/data_asset_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living record maintained as data asset properties change | ✅ Compliant |
| [Data Governance and Impact Assessment](data_governance_and_records_deliverables/data_governance_and_impact_assessment_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated as data governance obligations evolve | ✅ Compliant |
| [Data Migration Record](data_governance_and_records_deliverables/data_migration_record_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living record updated as migration activity progresses | ✅ Compliant |

### 2.8 User Adoption and Change Enablement Specifications

Adoption and change enablement artifacts are living documents maintained throughout delivery and transition as the change programme evolves.

| Specification | Pattern | Sections | Rationale | Status |
|---------------|---------|----------|-----------|--------|
| [User Impact Assessment](user_adoption_and_change_enablement_deliverables/user_impact_assessment_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living document updated as scope and impact change | ✅ Compliant |
| [Change and Communication Plan](user_adoption_and_change_enablement_deliverables/change_and_communication_plan_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living plan updated as communication needs evolve | ✅ Compliant |
| [Training and Enablement Materials](user_adoption_and_change_enablement_deliverables/training_and_enablement_materials_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living materials updated as capabilities and users change | ✅ Compliant |
| [Adoption Support Model](user_adoption_and_change_enablement_deliverables/adoption_support_model_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living model updated as adoption support evolves | ✅ Compliant |
| [Adoption Confirmation Record](user_adoption_and_change_enablement_deliverables/adoption_confirmation_record_specification.md) | Extended | 12 (+ Maintenance Expectations) | Living record updated as adoption milestones are confirmed | ✅ Compliant |

---

## 3. Structural Issues Resolved in This PR

| File | Issue | Fix Applied |
|------|-------|-------------|
| [formal_acceptance_and_closure_record_specification.md](governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) | `## Validation guide` was unnumbered and lowercase | Renumbered to `## 10. Validation Guide`; §11 and §12 renumbered |
| [project_charter_specification.md](governance_and_control_deliverables/project_charter_specification.md) | `## Validation guide` was unnumbered and lowercase | Renumbered to `## 10. Validation Guide`; §11 and §12 renumbered |
| [decision_record_log_specification.md](governance_and_control_deliverables/decision_record_log_specification.md) | Missing Maintenance Expectations (logs are living documents) | Added `## 9. Maintenance Expectations`; §9→§10→§11→§12 renumbered |
| [solution_assumptions_and_issues_register_specification.md](governance_and_control_deliverables/solution_assumptions_and_issues_register_specification.md) | Missing Maintenance Expectations (registers are living documents) | Added `## 9. Maintenance Expectations`; §9→§10→§11→§12 renumbered |
| [validation_and_evidence_matrix_specification.md](governance_and_control_deliverables/validation_and_evidence_matrix_specification.md) | Missing Maintenance Expectations (tracking matrix is a living document) | Added `## 9. Maintenance Expectations`; §9→§10→§11→§12 renumbered |
| [technical_design_document_specification.md](operational_readiness_deliverables/technical_design_document_specification.md) | Missing Validation Guide (TDD is a formal technical baseline) | Added `## 10. Validation Guide`; §10→§11→§12→§13 renumbered |

---

## 4. Summary Counts

| | Light (11 sections) | Extended (12–13 sections) | Total |
|--|--|--|--|
| Work Assessment | 6 | 0 | 6 |
| Work Brief | 1 | 0 | 1 |
| Governance and Control | 1 | 7 | 8 |
| Solution Deliverables | 11 | 0 | 11 |
| Operational Readiness | 0 | 5 | 5 |
| Security, Privacy and Compliance | 0 | 5 | 5 |
| Data Governance and Records | 0 | 3 | 3 |
| User Adoption and Change Enablement | 0 | 5 | 5 |
| **Total** | **19** | **25** | **44** |

All 44 specifications are compliant. No open structural or pattern-classification gaps remain.

