# Decision Record Log Specification

## 1. Purpose and Intended Outcome

The Decision Record Log maintains an attributable history of material decisions affecting scope, funding, sequencing, risk treatment, architecture direction, compliance position, acceptance, or other governed baselines.

It exists to make important decisions visible after the meeting or conversation where they were made. A useful Decision Record Log helps delivery teams, reviewers, and future maintainers understand what was decided, why, by whom, what changed as a result, and how those decisions align with other core deliverables.

The intended outcome is that material decisions remain traceable, do not need to be rediscovered or re-litigated, and can be followed through into delivery, governance, and acceptance actions across all domains.

## 2. When It Is Required

This artifact is required when the initiative involves material governance, scope, risk, acceptance, or design decisions that should remain reviewable over time.

It is strongly recommended for initiatives with multiple authorities, material risk, cross-domain impacts, or likely audit needs.

## 3. Stage Fit

Start the log in **Stage 2 – Work Definition** when the initiative begins to make decisions about scope, funding, approach, or design. Use it throughout all stages to log decisions as they arise. The log remains active until the initiative is formally closed.

- **Stage 2 – Work Definition:** log early decisions about problem, outcomes, scope boundaries, funding, or delivery approach.
- **Stage 3 – Work Authorization:** log authorization decisions, conditions, and risk acceptance.
- **Stage 4 – Work Definition Details:** log design-level decisions about modules, quality attributes, integration approach, business rules, or data handling.
- **Stage 5 – Delivery Mobilization:** log mobilization and execution decisions, changes, and risk responses.
- **Stage 6 – Work Delivery:** log decisions on implementation, evidence, or material changes.
- **Stage 7 – Acceptance, Transition & Closure:** log final acceptance decisions and closure decisions.

## 4. Intended Readers and Users

- Sponsor and Decision Authorities
- Delivery Owner
- governance and audit reviewers
- future maintainers
- leads affected by recorded decisions
- domain owners for assumptions, quality attributes, business rules, integration dependencies, or other deliverables referenced in the log

## 5. Intended Project Context

Use this artifact from definition through closure. It should align with PMI governance and integrated change-control discipline by making material decisions attributable and easy to review without searching across email, meeting notes, or chat history.

Decisions should also be cross-referenced to assumptions and issues (`AI-###`), quality attributes (`QA-###`), validation and evidence matrix entries (`VE-###`), business rules (`BR-###`), integration and external dependency entries (`INT-###`), and other governed artifacts where the decision materially affects them.

## 6. How Much Detail to Include

Keep each entry short but decision-useful. Include enough context that another reader can understand the decision, the rationale, the decision-maker, and the impact on delivery or governance. When cross-referencing other artifacts, include the IDs (e.g., `AI-001`, `BR-002`) rather than restating their content.

## 7. Required Content or Minimum Structure

This artifact should be table-driven.

### 7.1. Log context

Must include:

- initiative or solution name
- log owner
- current version or last updated date

### 7.2. Required content for each decision row

Each decision row must include:

- Decision ID (`DR-###`)
- decision date
- decision title
- decision category
- decision taken
- decision maker or approving authority
- artifact or evidence basis used for the decision
- rationale or basis
- impacted artifacts or deliverables
- baseline impact or change implication where the decision alters approved scope, cost, authority, risk position, or acceptance approach
- conditions or follow-up actions where applicable
- follow-up owner where action is required
- related assumptions & issues (`AI-###`) where the decision resolves or introduces assumptions or issues
- related quality attributes / NFRs (`QA-###`) where the decision affects non-functional qualities
- related business rules (`BR-###`) affected by the decision
- related integration & external dependency entries (`INT-###`) where the decision introduces or changes dependencies
- current status

Recommended columns:

| DR-### | Date | Title | Category | Decision Taken | Authority | Evidence Basis | Rationale | Impacted Artifacts | Baseline Impact | Related AI-### | Related QA-### | Related BR-### | Related INT-### | Conditions / Follow-Up | Follow-Up Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Use controlled status values such as:

- `Proposed`
- `Approved`
- `Superseded`
- `Withdrawn`

**Mandatory columns for all entries:** DR-###, Date, Title, Category, Decision Taken, Authority, Rationale, Impacted Artifacts, Status.

**Add cross-domain reference columns (AI-###, QA-###, BR-###, INT-###) only where the decision materially affects those artifacts.** Leave unused cross-domain columns blank rather than adding them to every row.

For simple initiatives with few cross-domain dependencies, a narrower table (mandatory columns only) is sufficient.

### 7.3. Decision logging rules

- Log only material decisions: those affecting scope, funding, risk position, architecture direction, compliance, quality commitments, acceptance approach, or approved baselines.
- Superseded decisions remain visible rather than deleted — mark them `Superseded` and add the new entry.
- Routine low-impact operational choices should not overload the log.
- Decisions requiring artifact updates, re-approval, or new acceptance conditions must identify the affected baseline or record explicitly.
- Each decision with conditions records a named owner for each follow-up action.
- Any decision materially affecting assumptions, quality attributes, business rules, or integration dependencies must record the related IDs so traceability and updates are triggered.

### 7.4. Template guide

Use short entries:

- `Category`: scope, funding, risk, architecture, privacy, acceptance, quality attribute, integration, business rule, or other defined category
- `Decision`: the conclusion, not the meeting discussion
- `Evidence basis`: the artifact, analysis, or record used to support the decision
- `Rationale`: a short reason, not full minutes
- `Impacted artifacts`: name the records or specifications that must align to the decision
- `Baseline impact`: state whether the decision confirms the current baseline, changes it, or creates a follow-up action to revise it

## 8. What to Keep Out

Keep the following out of this artifact:

- full meeting minutes
- raw discussion history
- large attachments copied into the log
- routine operational choices that do not affect governance or delivery direction

## 9. Relationships to Other Artifacts

The log should reference the Initiative Definition Document, Project Charter, major scope baselines, risk acceptance records, and closure records. Link to the [Solution Assumptions & Issues Register](solution_assumptions_and_issues_register_specification.md), [Quality Attributes / NFR Specification](../solution_deliverables/quality_attributes_specification.md), [Validation & Evidence Matrix](validation_and_evidence_matrix_specification.md), [Business Rules Catalog](../solution_deliverables/business_rules_catalog_specification.md), and [Integration & External Dependency Specification](../solution_deliverables/integration_and_external_dependency_specification.md) where applicable. Linking to these artifacts ensures that decisions requiring changes or confirmations in those areas are visible and traceable.

## 10. Ownership, Review, and Acceptance Expectations

The Delivery Owner or governance coordinator usually maintains the log. Decision makers remain accountable for the recorded decision itself. Domain owners for assumptions, quality attributes, rules, or dependencies should review entries that reference their deliverables to confirm alignment or identify required follow-up actions.

## 11. Recommended Acceptance Evidence

- Updated Decision Record Log showing all material decisions with authority, rationale, impacted artifacts, cross-domain references, and current status.
- Confirmation by the Delivery Owner that the log is complete and accurate up to the acceptance point.

## 12. Recommended Acceptance Authority

- **Sponsor or Decision Authority** for governance-level and authorization decisions.
- **Delivery Owner** for design-level and execution decisions.

## 13. Maintenance Expectations

Update the log as decisions occur. If a decision changes, mark the original entry as superseded and add the new one rather than overwriting history. When a decision affects assumptions, quality attributes, rules, or dependencies, update or cross-reference the respective artifacts accordingly and record the follow-up ownership.

## 14. Validation Guide

- Does each entry identify the decision, authority, rationale, and impacted artifacts clearly?
- Are related assumptions, quality attributes, business rules, or integration dependencies referenced where the decision materially affects them?
- Can a reader tell whether the decision changed an approved baseline or only clarified it?
- Can a reader tell which decisions are still current?
- Is the log short enough to scan and strong enough to support audit or future change review?
- Does the log avoid becoming a copy of meeting minutes?

If weak, shorten entries, improve status handling, and make impacts on artifacts and cross-references more explicit.

## 15. Prompt Guide for Drafting the Artifact

### 15.1. Starter prompt

> Create or update a Decision Record Log for this initiative.
> Capture only material decisions, with clear DR-### IDs, authority, rationale, impacted artifacts, follow-up ownership, and current status.
> Include related AI-###, QA-###, BR-###, and INT-### references where the decision affects assumptions, quality attributes, business rules, or external dependencies.
> Keep each entry short enough to scan quickly.

### 15.2. Section prompts

> Convert these meeting outcomes into Decision Record Log entries using the required row fields in this specification, including related cross-domain IDs where applicable.

> Review the log and mark any entries that should be superseded, withdrawn, or removed because they are not material enough for this artifact.

### 15.3. Validation prompts

> Check whether this log distinguishes clearly between decisions, rationale, related cross-domain IDs, and follow-up actions.

> Check whether any current decision affecting scope, funding, acceptance, quality attributes, rules, or integration dependencies is missing from the log.
