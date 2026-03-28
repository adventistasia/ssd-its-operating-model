# Branch Comparison Report: solution-design-updates vs expand-work-delivery-artifacts

**Status:** Working draft  
**Prepared:** 2026-03-28  
**Purpose:** Compare the two branches and record the rationale for how their content is combined into the `expand-work-delivery-artifacts` branch.

---

## 1. Scope of Comparison

Both branches diverge from the same common ancestor commit (`d1f4ea2`) after the Work Brief framing update. Each branch independently added a set of new specification files and modified the Decision Record Log.

This report covers every file changed or added in either branch.

---

## 2. File Inventory by Branch

### 2.1. expand-work-delivery-artifacts (only)

| File | Location | Status |
| --- | --- | --- |
| `problem_outcome_validation_brief_specification.md` | `governance_and_control_deliverables/` | Added |
| `integration_and_external_dependency_specification.md` | `operational_readiness_deliverables/` | Added |

### 2.2. solution-design-updates (only)

| File | Location | Status |
| --- | --- | --- |
| `problem_and_outcome_validation_brief_specification.md` | `solution_deliverables/` | Added |
| `integration_and_external_dependency_specification.md` | `solution_deliverables/` | Added |
| `validation_and_evidence_matrix_specification.md` | `governance_and_control_deliverables/` | Added |

### 2.3. Both branches (diverged versions)

| File | Location (both) | Status |
| --- | --- | --- |
| `decision_record_log_specification.md` | `governance_and_control_deliverables/` | Modified (different in each branch) |
| `solution_assumptions_and_issues_register_specification.md` | `governance_and_control_deliverables/` | Added (different in each branch) |
| `business_rules_catalog_specification.md` | `solution_deliverables/` | Added (different in each branch) |
| `quality_attributes_specification.md` | `solution_deliverables/` | Added (different in each branch) |
| `validation_and_evidence_matrix_specification.md` | `solution_deliverables/` (expand) | Added – location differs |

---

## 3. File-by-File Analysis

### 3.1. Decision Record Log Specification

**Location:** `governance_and_control_deliverables/` (both agree)

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Title | Decision Record Log Specification (Extended) | Decision Record Log Specification (Broadened) |
| Architecture | Separate artifact for decisions only | Unified: decisions + assumptions + issues merged into one log using a Type field (DR-###) |
| Structure | 12 numbered sections, detailed per-row requirements | Shorter; stage-fit section, prompt guide, acceptance evidence/authority |
| Cross-domain IDs | Yes — SI-###, QA-###, BR-###, IE-### references | No cross-domain IDs |
| Stage Fit section | No explicit per-stage guidance | Yes — per-stage description (Stages 2–7) |
| Acceptance evidence / authority | No | Yes |
| ID convention | No explicit prefix stated | DR-### |

**Recommendation:** Keep the `expand` version's 12-section structure, separate-artifact architecture, and cross-domain ID references. Add:
- A Stage Fit section from `sol`
- Recommended acceptance evidence and acceptance authority sections
- Explicit DR-### ID convention

**Key architectural note:** The `sol` version merges decisions, assumptions, and issues into one log. This simplifies tooling but blurs an important distinction — decisions are governance events, while assumptions and issues are design-time uncertainties. Keeping them separate (the `expand` architecture) preserves clearer governance. The `sol` Stage Fit section is the most valuable element to carry forward.

---

### 3.2. Solution Assumptions & Issues Register Specification

**Location:** `governance_and_control_deliverables/` (both agree)

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| ID convention | SI-### | AI-### |
| Stage range | Stages 2–6 | Stages 4–7 |
| Upstream/downstream links | No | Yes (explicit file links to related specs) |
| Acceptance evidence / authority | No | Yes |
| Table structure | 7 columns | 9 columns (adds Related artifacts, Target resolution) |
| "Why it exists" framing | Paragraph description | Bullet-question format (more scannable) |

**Recommendation:** Use the `sol` version as the base (richer structure, upstream/downstream links, acceptance evidence/authority, better table). Adjust stage range to start from Stage 2 (matching `expand`) since early assumptions in Stage 2 work definition are important to capture. Use `AI-###` (more intuitive than `SI-###`). Update decision log cross-references to match.

---

### 3.3. Problem & Outcome Validation Brief Specification

**Branches disagree on both location and filename:**

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Location | `governance_and_control_deliverables/` | `solution_deliverables/` |
| Filename | `problem_outcome_validation_brief_specification.md` | `problem_and_outcome_validation_brief_specification.md` |
| Sections | 9 | 10 |
| Upstream/downstream links | No | Yes |
| Acceptance evidence / authority | No | Yes |
| Affected user groups section | No | Yes (Section 5.2) |
| Roles and ownership section | No | Yes (Section 6.7) |
| Validation sign-off section | Yes (Section 6.6) | No separate section |

**Location recommendation:** `solution_deliverables/`. This artifact is a solution design precursor — it establishes what problem the solution should solve. It feeds downstream into Functional Capabilities, Quality Attributes, and Module Definitions. Governance and control deliverables are for cross-stage governance artifacts; problem validation is design-stage content.

**Filename recommendation:** `problem_and_outcome_validation_brief_specification.md` (include "and"; both words belong in the name).

**Content recommendation:** Use the `sol` version. It is richer, adds upstream/downstream links, an affected user groups step, a roles/ownership section, and acceptance evidence/authority. Carry forward the explicit validation sign-off field from `expand` Section 6.6 by noting it within Section 6.7 (Roles and ownership) of the combined version.

---

### 3.4. Business Rules Catalog Specification

**Location:** `solution_deliverables/` (both agree)

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Sections | 9 | 10 |
| Table columns | 6 | 7 (adds Validation & evidence column) |
| Upstream/downstream links | No | Yes |
| Acceptance evidence / authority | No | Yes |
| Stage fit | Stages 4, 6 | Stages 4–7 (more explicit) |

**Recommendation:** Use the `sol` version. The additional Validation & evidence column in the table is a clear improvement — it keeps traceability to the Validation & Evidence Matrix explicit at the rule level. Upstream/downstream links and acceptance evidence/authority are consistent with other improved specs.

---

### 3.5. Quality Attributes / Non-Functional Requirements Specification

**Location:** `solution_deliverables/` (both agree)

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Sections | 9 | 10 |
| Table | 6-column summary table | 4-column summary table + attribute details + measurement/monitoring section + assumptions/constraints section |
| Upstream/downstream links | No | Yes |
| Acceptance evidence / authority | No | Yes |
| Problem & Outcome Brief link | No | Yes (upstream source) |

**Recommendation:** Use the `sol` version. The dedicated Measurement and Monitoring Expectations section (6.4) and Assumptions and Constraints section (6.5) are meaningful additions. These ensure quality attributes are operational, not just aspirational. The 6-column `expand` table (with QA-### IDs and Applies to FC/SM/UC IDs) should be carried forward by incorporating those columns into the `sol` version's table.

---

### 3.6. Integration & External Dependency Specification

**Branches disagree on location:**

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Location | `operational_readiness_deliverables/` | `solution_deliverables/` |
| Sections | 9 | 10 |
| INT-### ID convention | Yes | No |
| Upstream/downstream links | No | Yes |
| Overall considerations section | No | Yes (Section 6.4) |
| Acceptance evidence / authority | No | Yes |
| Stage fit | Stages 4, 6 | Stages 4–7 |

**Location recommendation:** `solution_deliverables/`. This specification primarily concerns solution design decisions — what external dependencies exist, their contracts and data flows. It is most valuable during Stages 4 and 5 when design is being defined. Operational readiness artifacts (DevOps Guide, Operations & Support Model) are downstream consumers. The `sol` branch correctly treats this as a solution deliverable.

**Content recommendation:** Use the `sol` version as the base. Add the `INT-###` ID convention from `expand` — stable identifiers per integration entry improve traceability to the Decision Record Log and Assumptions Register.

---

### 3.7. Validation & Evidence Matrix Specification

**Branches disagree on location:**

| Dimension | expand-work-delivery-artifacts | solution-design-updates |
| --- | --- | --- |
| Location | `solution_deliverables/` | `governance_and_control_deliverables/` |
| Sections | 9 | 10 |
| Table | 7 columns | 7 columns (minor variation) |
| Upstream/downstream links | No | Yes |
| Acceptance evidence / authority | No | Yes |
| Additional column notes | Notes | Priority, risk, or notes as optional extra columns |

**Location recommendation:** `governance_and_control_deliverables/`. The Validation & Evidence Matrix exists to support governance decisions at acceptance. Its primary consumer is the Acceptance Authority reviewing evidence before formal acceptance. This puts it firmly in the governance and control domain. Upstream sources (FC, SM, UC specifications) live in `solution_deliverables/`, and the downstream Acceptance Record also uses it.

**Content recommendation:** Use the `sol` version.

---

## 4. Structural Observations

### 4.1. Artifact ID conventions

The two branches developed independently and do not always agree on ID prefixes:

| Artifact | expand prefix | sol prefix | Recommended |
| --- | --- | --- | --- |
| Decision Record | (none stated) | DR-### | DR-### |
| Assumptions & Issues | SI-### | AI-### | AI-### |
| Business Rules | BR-### | BR-### | BR-### (no conflict) |
| Quality Attributes | QA-### | QA-### | QA-### (no conflict) |
| Integration entries | INT-### | (none stated) | INT-### |
| Validation & Evidence | VE-### (referenced in decision log) | (none stated) | VE-### |

The combined specification set uses these prefixes consistently.

### 4.2. Template consistency pattern

The `sol` branch uses a more consistent per-specification pattern:
- "It answers questions like:" bullet format for What This Artifact Is For
- Upstream sources and downstream artifacts with relative links
- Recommended Acceptance Evidence section
- Recommended Acceptance Authority section
- 10-section structure

The `expand` branch uses a richer numbered-section governance structure with stronger cross-domain traceability (section-level requirements, detailed rows, template guides with multiple prompt types).

The combined version preserves the `expand` numbered section structure for the Decision Record Log (because its governance complexity justifies it) and adopts the `sol` pattern for all other specifications (because it is more consistent with the rest of the repository's specification style).

### 4.3. Separation of decision log vs assumptions register

The `sol` branch merged decisions, assumptions, and issues into one log. The `expand` branch kept them separate. The combined version keeps them separate because:

1. The Decision Record Log is a governance artifact — it records settled, attributable outcomes.
2. The Assumptions & Issues Register is a working artifact — it tracks live uncertainties until they are resolved.
3. Mixing the two makes the log harder to use for audit and acceptance purposes.
4. Resolution of an assumption or issue can then be promoted into the Decision Record Log as an explicit decision.

---

## 5. Summary of Recommended Placements

| Specification | Location | Filename |
| --- | --- | --- |
| Decision Record Log | `governance_and_control_deliverables/` | `decision_record_log_specification.md` |
| Solution Assumptions & Issues Register | `governance_and_control_deliverables/` | `solution_assumptions_and_issues_register_specification.md` |
| Validation & Evidence Matrix | `governance_and_control_deliverables/` | `validation_and_evidence_matrix_specification.md` |
| Problem & Outcome Validation Brief | `solution_deliverables/` | `problem_and_outcome_validation_brief_specification.md` |
| Business Rules Catalog | `solution_deliverables/` | `business_rules_catalog_specification.md` |
| Quality Attributes / NFR Specification | `solution_deliverables/` | `quality_attributes_specification.md` |
| Integration & External Dependency Specification | `solution_deliverables/` | `integration_and_external_dependency_specification.md` |

---

## 6. Open Questions for Review

1. **ID prefix for Assumptions & Issues register:** Should the combined spec use `AI-###` (from `sol`, more intuitive) or `SI-###` (from `expand`, already referenced in the expand decision log)? This report recommends `AI-###`.

2. **Problem & Outcome Validation Brief location:** Placed in `solution_deliverables/` in the combined version. The `expand` branch put it in `governance_and_control_deliverables/`. Confirm whether this is acceptable.

3. **Integration spec location:** Placed in `solution_deliverables/` in the combined version. The `expand` branch put it in `operational_readiness_deliverables/`. Confirm.

4. **Validation & Evidence Matrix location:** Placed in `governance_and_control_deliverables/` in the combined version. The `expand` branch put it in `solution_deliverables/`. Confirm.

5. **Decision Record Log architecture:** The combined version maintains separate Decision Log and Assumptions Register. The `sol` approach of combining them may be preferable for smaller initiatives. Consider whether a note should be added in the Decision Record Log specification permitting simplified use in smaller initiatives.

6. **Standard Deliverables Guide and Deliverables Index:** Neither branch updated these to reflect the new specifications. The combined version will update both to make the new specs discoverable.
