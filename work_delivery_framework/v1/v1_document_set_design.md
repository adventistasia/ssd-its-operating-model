# Work Delivery Framework v1 Document Set Design

## 1. Role

Information architecture and operating model documentation design.

## 2. Objective

Convert the canonical specification in `../work_delivery_framework_specification.md` into a usable, publishable `v1` document set that:

1. preserves the specification as the canonical source of truth
2. makes the framework easy for human teams to navigate and apply
3. exposes machine-readable framework definitions cleanly
4. includes ready-to-use templates for the canonical artifacts

## 3. Approach

Use a lean split-document model.

This model keeps the `v1` pack operational and discoverable without recreating the larger, more fragmented structure under the legacy `work_delivery/` framework.

The split is based on durable operating concerns:

1. framework navigation and lifecycle control
2. artifact taxonomy and usage rules
3. completeness, review, and governance controls
4. artifact-level specifications
5. ready-to-use templates
6. machine-readable framework definitions

## 4. Output

The `work_delivery_framework/v1` folder will contain the following structure.

```text
work_delivery_framework/v1/
  README.md
  framework_overview.md
  artifact_catalog.md
  completeness_and_review_model.md
  machine_readable/
  artifact_specifications/
  templates/
  examples/
```

## 5. Folder Design

### 5.1 README.md

Purpose:

1. provide the start-here entry point
2. define reading order
3. explain what is canonical versus derived
4. point readers to the right document for common tasks

### 5.2 framework_overview.md

Purpose:

1. define scope and applicability
2. explain the lifecycle stages and gates
3. summarize entry and exit logic
4. explain scaling and control boundaries

### 5.3 artifact_catalog.md

Purpose:

1. define canonical artifacts
2. show artifact triggers and gate requirements
3. explain packaging rules
4. define external engagement modes

### 5.4 completeness_and_review_model.md

Purpose:

1. define artifact- and gate-level completeness
2. define AI sufficiency rules
3. define blocker and open-item handling
4. define review, assurance, and audit model
5. define anti-bureaucracy controls

### 5.5 machine_readable/

Purpose:

1. provide extracted YAML definitions for stages, gates, artifacts, mappings, and control models
2. preserve stable identifiers from the canonical specification
3. support direct AI-agent or tooling consumption without scraping long prose files

Expected contents:

1. `stages.yaml`
2. `gates.yaml`
3. `artifacts.yaml`
4. `gate_mappings.yaml`
5. `control_models.yaml`
6. `quality_and_policy_models.yaml`

### 5.6 artifact_specifications/

Purpose:

Provide one specification file per canonical artifact so teams can draft or review artifacts directly.

Expected files:

1. `request_intake_record_specification.md`
2. `initiative_definition_project_brief_specification.md`
3. `decision_log_specification.md`
4. `open_items_register_specification.md`
5. `closure_record_specification.md`
6. `project_charter_approved_specification.md`
7. `delivery_charter_specification.md`
8. `technical_design_document_specification.md`
9. `api_contract_specification.md`
10. `deployment_guide_specification.md`
11. `user_adoption_plan_specification.md`
12. `data_asset_specification.md`
13. `data_migration_plan_specification.md`
14. `access_model_specification.md`
15. `security_privacy_risk_impact_assessment_specification.md`

Design rule:

Acceptance Criteria remains an embedded artifact inside the Project Brief rather than becoming a standalone specification file.

### 5.7 templates/

Purpose:

Provide ready-to-use Markdown templates/forms matching the canonical artifact set.

Expected files:

1. `request_intake_record_template.md`
2. `initiative_definition_project_brief_template.md`
3. `decision_log_template.md`
4. `open_items_register_template.md`
5. `closure_record_template.md`
6. `project_charter_approved_template.md`
7. `delivery_charter_template.md`
8. `technical_design_document_template.md`
9. `api_contract_specification_template.md`
10. `deployment_guide_template.md`
11. `user_adoption_plan_template.md`
12. `data_asset_specification_template.md`
13. `data_migration_plan_template.md`
14. `access_model_template.md`
15. `security_privacy_risk_impact_assessment_template.md`

Template design rules:

1. templates must be directly usable by human teams without extra interpretation
2. templates must preserve numbering and traceability where the framework depends on exact referenceability
3. templates must make controlled unknowns explicit rather than encouraging placeholders
4. templates must align terminology exactly to the canonical specification

### 5.8 examples/

Purpose:

Provide a very small number of examples only where they materially improve adoption.

Expected scope:

1. one example Project Brief section showing hybrid Gherkin acceptance criteria
2. one example Open Items Register
3. one example Decision Log

The examples folder is intentionally small so `v1` remains lean.

## 6. Key Design Decisions

1. The canonical source remains `work_delivery_framework_specification.md` outside `v1`.
2. The `v1` pack is a derived operating artifact set, not a replacement source.
3. The document set uses fewer top-level files than the legacy `work_delivery/` model.
4. Artifact specifications are split per artifact for drafting and review convenience.
5. Templates are included because the user explicitly requested ready-to-use forms.
6. Acceptance Criteria is treated as an embedded artifact and will be surfaced inside the Project Brief spec and template.
7. Machine-readable YAML is published as first-class output rather than remaining buried in prose.

## 7. Out of Scope for This v1 Pack

1. code generation
2. software integrations
3. service management tooling implementation
4. recreating the full legacy framework taxonomy where the new specification has simplified it

## 8. Execution Note

Once this design is accepted, implementation means authoring the complete `v1` Markdown document set, templates, and machine-readable files under this folder.
