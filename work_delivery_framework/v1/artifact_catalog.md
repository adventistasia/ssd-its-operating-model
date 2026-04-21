# Artifact Catalog

## 1. Purpose

This catalog defines the canonical artifact set for the Work Delivery Framework `v1` pack.

Use it to answer:

1. which artifacts always exist
2. which artifacts are conditional
3. what triggers a conditional artifact
4. which gate each artifact is required by
5. whether the artifact is standalone or embedded

## 2. Category Labels vs Artifacts

The following are category labels, not standalone artifacts:

1. Project Governance
2. Solution Design
3. DevOps and Support
4. User Adoption

These labels help organize thinking. They do not themselves create mandatory files.

## 3. Primary Definition Artifact

Every in-scope initiative must have one canonical primary definition artifact:

1. `Initiative Definition / Project Brief`

Conditional artifacts add detail when triggered. They do not replace the Project Brief.

## 4. Always-Required Artifacts

| Artifact | Packaging | Required By |
| --- | --- | --- |
| Request Intake Record | Standalone | Gate 1 |
| Initiative Definition / Project Brief | Standalone | Gate 2 |
| Decision Log | Standalone | No later than Gate 2 |
| Open Items Register | Standalone | No later than Gate 2 |
| Closure Record | Standalone | Gate 8 |

## 5. Conditional Artifacts

| Trigger Condition | Artifact | Required By |
| --- | --- | --- |
| Authorization is required | Project Charter (Approved) | Gate 3 |
| Co-delivery or Full External Delivery | Delivery Charter | Gate 4 by default; sometimes Gate 3 |
| Material ops/support impact | Technical Design Document (TDD) | Gate 4 |
| Material ops/support impact | Deployment Guide | Gate 6 |
| Data migration | Data Asset Specification | Gate 4 |
| Data migration | Data Migration Plan | Gate 4 |
| Security/compliance impact | Access Model | Gate 4 |
| Security/compliance impact | Security/Privacy Risk Impact Assessment | Gate 4 |
| New integration or API change | API/Contract Specification | Gate 4 |
| Customer-facing change | User Adoption Plan | Start between Gate 4 and Gate 6; complete by Gate 6 |

## 6. Embedded Artifact Rule

`Acceptance Criteria` is a canonical embedded artifact rather than a required standalone document.

It must be embedded in the `Initiative Definition / Project Brief` and must be present by Gate 4.

## 7. Artifact Summary Table

| Artifact | ID | Packaging | Notes |
| --- | --- | --- | --- |
| Request Intake Record | `ARTIFACT-REQUEST-INTAKE-RECORD` | Standalone | Entry and qualification record |
| Initiative Definition / Project Brief | `ARTIFACT-PROJECT-BRIEF` | Standalone | Primary definition artifact |
| Decision Log | `ARTIFACT-DECISION-LOG` | Standalone | Durable record of material decisions |
| Open Items Register | `ARTIFACT-OPEN-ITEMS-REGISTER` | Standalone | Canonical unresolved-items register |
| Closure Record | `ARTIFACT-CLOSURE-RECORD` | Standalone | Formal closure artifact |
| Project Charter (Approved) | `ARTIFACT-PROJECT-CHARTER` | Standalone | Required only when authorization is required |
| Delivery Charter | `ARTIFACT-DELIVERY-CHARTER` | Standalone | Required for co-delivery or full external delivery |
| Technical Design Document (TDD) | `ARTIFACT-TDD` | Standalone | Required when material ops/support impact exists |
| API/Contract Specification | `ARTIFACT-API-CONTRACT-SPEC` | Standalone | Required when new integration or API change exists |
| Deployment Guide | `ARTIFACT-DEPLOYMENT-GUIDE` | Standalone | Required when material ops/support impact exists |
| User Adoption Plan | `ARTIFACT-USER-ADOPTION-PLAN` | Standalone | Required when change is customer-facing |
| Data Asset Specification | `ARTIFACT-DATA-ASSET-SPEC` | Standalone | Required when data migration exists |
| Data Migration Plan | `ARTIFACT-DATA-MIGRATION-PLAN` | Standalone | Required when data migration exists |
| Access Model | `ARTIFACT-ACCESS-MODEL` | Standalone | Required when security/compliance impact exists |
| Security/Privacy Risk Impact Assessment | `ARTIFACT-SECURITY-PRIVACY-RIA` | Standalone | Required when security/compliance impact exists |
| Acceptance Criteria | `ARTIFACT-ACCEPTANCE-CRITERIA` | Embedded | Embedded in the Project Brief |

## 8. External Engagement Modes

### 8.1 Staff Augmentation

External personnel work within the internal team's delivery model.

This mode does not by itself trigger a `Delivery Charter`.

### 8.2 Co-delivery

Internal and external teams share delivery responsibility.

This mode triggers a `Delivery Charter` and explicit coordination, decision-interface, and responsibility rules.

### 8.3 Full External Delivery

The external team executes from the approved package with minimal reliance on recurring requirement clarification.

This mode triggers a `Delivery Charter` and the strongest handoff completeness standard.

## 9. Filename Guidance

Canonical artifact names are normative. Exact filenames are not mandatory, but teams should strongly prefer canonical filenames for consistency, discovery, and auditability.

## 10. How to Use This Catalog

1. Confirm the initiative is in scope.
2. Start with the always-required artifacts.
3. Check the trigger conditions for each conditional artifact.
4. Confirm the required-by gate.
5. Open the matching file in `artifact_specifications/`.
6. Draft using the matching template in `templates/`.
