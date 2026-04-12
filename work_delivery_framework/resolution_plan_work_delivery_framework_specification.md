# Resolution Plan for Specification Ambiguities

## 1. Executive Summary

The specification is directionally strong but operationally underdefined. It clearly states the intended outcomes of the framework, but many of the decisions needed to make the framework repeatable, enforceable, and scalable are still unresolved.

The main risks created by the current ambiguity level are:
- inconsistent implementation by different teams
- invented stage gates, artifacts, and review criteria
- false readiness signals caused by documents that look complete but are not executable
- over-documentation for small work and under-specification for complex or AI-assisted work
- unclear authority to stop progression when blockers remain

Recommended high-level order of resolution:
1. Define scope, framework form, governance, and decision rights.
2. Define minimum intake requirements, lifecycle stages, and artifact model.
3. Define completeness criteria, scaling rules, and framework boundary to technical specification work.
4. Define domain-specific expectations for acceptance, supportability, external handoff, and AI-consumable precision.
5. Define review, audit, and blocker-handling mechanics.

## 2. Ambiguity Register

- [x] **A01 - In-scope and out-of-scope work types are not fully defined**
  - Relevant section(s): Section 1 System Overview; Section 5.1; Section 5.6; Section 6.4
  - Description: The specification referenced greenfield and brownfield software initiatives, but did not clearly define whether the framework also applies to operational changes, internal process changes, research spikes, support work, non-software initiatives, or minor enhancements.
  - Why it matters: Scope determines who must use the framework, which paths need to exist, and which artifacts are required.
  - Dependencies: Blocks or materially affects A04, A05, A06, A09, A12.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The framework is optimized for software initiatives. It is in scope for greenfield and brownfield software projects; out of scope for minor low-risk changes, research spikes, support work, and small internal process changes; and conditionally in scope for complex operational changes affecting multiple organizations, complex internal process changes affecting the whole organization, and non-software initiatives that can use the framework with minimum changes.

- [x] **A02 - Framework form and publication model are undefined**
  - Relevant section(s): Section 4.2; Section 6.1
  - Description: It is unclear whether the framework is a policy, playbook, workflow, template library, knowledge base structure, operating model, or a combination. This leaves the primary deliverable shape unresolved.
  - Why it matters: The form determines how teams consume the framework, how guidance is organized, and how compliance is checked.
  - Dependencies: Blocks or materially affects A05, A06, A13, A16.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: This framework is a full operating model for work definition and delivery readiness. The canonical source of truth is Markdown-first (`work_delivery_framework_specification.md`) and it must embed machine-consumable YAML blocks (with stable IDs) for stages, artifacts, and gates so both humans and AI agents can apply the framework consistently.
- [x] **A03 - Governance, ownership, and decision rights are underdefined**
  - Relevant section(s): Section 1 System Overview; Section 2.2; Section 6.7
  - Description: The specification names internal teams, PMO, delivery managers, and engineers, but does not define who owns the framework, who maintains it, who approves outputs, who can reject work as incomplete, and who arbitrates disputes.
  - Why it matters: Without clear authority, gating rules may be ignored or applied inconsistently.
  - Dependencies: Blocks or materially affects A05, A13, A14.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: PMO owns the framework. Every gate requires a single named Gate Decision Owner (assigned by PMO or Delivery Owner at Intake and recorded in the Initiative Definition / Project Brief; also in the Project Charter for large projects). No role has veto power; the Decision Owner is accountable, and substantive disagreements must have a documented plan of action forward recorded in the project Decision Log.
- [x] **A04 - Minimum intake inputs and entry readiness are not operationalized**
  - Relevant section(s): Section 2.1.1; Section 2.2.1-3; Section 4.3; Section 4.5
  - Description: The specification lists input categories such as business rules, constraints, dependencies, and acceptance criteria, but does not define the minimum information required before a request may enter the framework or proceed past intake.
  - Why it matters: Intake quality affects every downstream artifact and determines whether teams stop early or proceed with hidden gaps.
  - Dependencies: Depends on A01 and A03; blocks or materially affects A05, A06, A08, A14.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The minimum entry payload to allow a request to enter Intake is: requester name; and a short description that includes background/problem/opportunity, desired outcome, success measures, and affected systems/processes. Success measures and affected systems/processes are allowed to be explicitly "Unknown/TBD" at entry. Requests may enter Intake even when in-scope is not yet confirmed. A triage owner is assigned immediately (provisional ownership allowed), and an initial clarification session is expected as part of the initial assessment.
- [x] **A05 - Lifecycle stages, progression gates, and exit criteria are not explicit**
  - Relevant section(s): Section 2.1.1-10; Section 2.2.1-7; Section 5.1-5.5; Section 6.3
  - Description: The specification implies a staged flow from intake through documentation and readiness evaluation, but does not define the formal stages, gate names, required evidence, or completion conditions for each stage.
  - Why it matters: Teams will otherwise invent their own process steps and gate logic.
  - Dependencies: Depends on A02, A03, A04; blocks or materially affects A06, A08, A13, A14.
  - Estimated complexity: High
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The framework lifecycle is now explicitly defined as formal stages with explicit progression gates and gate decision owners. Stages (in order): Intake; Assessment/Qualification; Discovery/Initiative Definition; Authorization (conditional); Solution Definition; Planning/Mobilization/MVP Plan; Delivery/Execution; Handoff/Transition; Closure. Gates (in order): Qualified Request; Initiative Defined (for Authorization decision); Authorized (conditional); Specification Complete; MVP Identified (MVP scope + MVP success/acceptance criteria approved); All Deliverables Accepted (Acceptance Owner accepts delivered solution against specified acceptance criteria); Transition Complete (supported operating state accepted); Closure Complete (ITS Director or PMO depending on project). Authorization applicability is explicitly conditional and must be declared at Gate 2 until scaling thresholds are resolved in A09.
- [x] **A06 - Required artifact taxonomy is incomplete**
  - Relevant section(s): Section 2.1.2-9; Section 4.4; Section 5.1-5.3; Section 6.2
  - Description: The specification refers to project documentation, solution definition artifacts, delivery approach documentation, support documentation, and external handoff packs, but does not define the canonical artifact set, the contents of each artifact, or which outputs are mandatory versus conditional.
  - Why it matters: The framework cannot be executed consistently until teams know what outputs are expected.
  - Dependencies: Depends on A01, A02, A05; blocks or materially affects A07, A08, A09, A10, A11, A12, A16.
  - Estimated complexity: High
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The canonical artifact taxonomy is now defined in `work_delivery_framework_specification.md` Section 2.5, including packaging modes (Work Brief packet for small work; separate artifacts for large work), the always-required artifacts (Project Brief or Work Brief; Decision Log), conditional artifacts with triggers (Project Charter, Delivery Charter, TDD, API/Contract Spec, Deployment Guide, User Adoption Plan, Data Asset Spec, Data Migration Plan, Access Model, Security/Privacy RIA), and gate timing expectations. RAID is optional at Delivery Owner discretion. Canonical artifact names are defined, with filenames strongly recommended but not strictly enforced.
- [x] **A07 - Boundary between framework outputs and technical specification work is unclear**
  - Relevant section(s): Section 2.1.8-10; Section 4.4.6; Section 5.1.3; Section 6.8
  - Description: The specification says the framework should enable technical specifications to be derived, but does not state whether technical specifications are outside the framework, standardized by it, or partially included.
  - Why it matters: This boundary determines where the framework ends and where engineering planning begins.
  - Dependencies: Depends on A05 and A06; materially affects A08, A10, A15.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The framework includes business and system-level documentation sufficient to derive downstream technical specifications without foundational clarification (including architecture, major system components, and data flows when needed), but explicitly excludes downstream engineering planning and code-level technical specifications (task breakdown, code-level design, per-endpoint acceptance test suites). Acceptance criteria and behavior-level tests derived from use cases remain in-framework; detailed engineering test plans/cases are generally downstream. The boundary does not shift by delivery mode; AI may require a higher “good/completeness” standard (tracked separately as A15).
- [x] **A08 - Completeness and delivery-readiness criteria are not operationalized**
  - Relevant section(s): Section 1; Section 2.1.9-10; Section 2.2.5-6; Section 3.4-8; Section 5.3-5.5; Section 6.5
  - Description: The specification defines completeness directionally but does not provide a formal rubric, checklist, scorecard, or pass/fail criteria for determining when outputs are sufficiently buildable, supportable, and unambiguous.
  - Why it matters: This is the core acceptance standard of the framework. Without it, all gates and reviews remain subjective.
  - Dependencies: Depends on A05, A06, A07; blocks or materially affects A09, A10, A11, A13, A15.
  - Estimated complexity: High
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: Completeness is now defined as a hybrid model with immediate-fail mandatory criteria plus qualitative ratings (`weak`, `adequate`, `strong`). The model applies at both artifact and gate level. Every artifact definition must include purpose, required contents, artifact-specific completeness rules, and common failure conditions, with a shared review core of clarity, internal consistency, decision/assumption visibility, and actionability for the next consumer. Every gate definition must include mandatory pass conditions, immediate fail conditions, a minimum qualitative threshold, and a critical-artifact field. Gates 1-3 and 5-8 require at least `adequate`; Gate 4 requires `strong`. Open issues may remain only when explicit, owned, actionable, and non-blocking for downstream work. Reviewers may not use undocumented context to upgrade ratings, document presence is not evidence of completeness, failed reviews require a written deficiency list tied to criteria, and there is no conditional progression for completeness failure.
- [ ] **A17 - Critical stage-defining artifact mapping is deferred**
  - Relevant section(s): Section 2.6.4; gate YAML definitions; Section 6.13
  - Description: The completeness model now requires each gate to identify its critical stage-defining artifacts, but the exact mapping between gates and critical artifacts has not yet been defined.
  - Why it matters: The gate-level qualitative model, especially the rule for when a gate can be rated `strong`, depends on knowing which artifacts are stage-defining rather than merely present.
  - Dependencies: Depends on A05, A06, A08; materially affects A09, A13, A15.
  - Estimated complexity: Medium
  - Risk if unresolved: Medium
  - Status: Unresolved
- [x] **A09 - Scaling rules for simple versus complex work are resolved**
  - Relevant section(s): Section 2.3.1-3; Section 5.6-5.7; Section 6.6; Section 8
  - Description: The specification states that the framework must avoid bureaucracy for simple work and scale up for complex work, but it does not define classification criteria, path variants, or thresholds for selecting a lighter or heavier path.
  - Why it matters: This is the main control for balancing rigor with usability.
  - Dependencies: Depends on A01, A06, A08; materially affects A11, A12, A16.
  - Estimated complexity: High
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: Two tiers: small-work (Work Brief packet) and large-work (separate artifact set). Single-factor trigger (OR logic): any one of scope (multi-team, multi-system, multi-component, or greenfield), business impact (cross-department, material impact, or requires approved budget), or effort/complexity (Delivery Owner judgment; default to large-work when uncertain) forces large-work. External involvement is context, not a forcing factor. Small-work quick-passes Gates 1, 3, 5, 7, 8; substantive review at Gates 2, 4, 6. Small-work requires only Work Brief; conditional artifacts at Delivery Owner discretion. Classification declared by Gate 2. Reclassification required if thresholds exceeded; recorded in Decision Log. No intermediate tier.
- [x] **A10 - Acceptance criteria and observable validation model are underdefined**
  - Relevant section(s): Section 2.1.9; Section 2.3.6; Section 5.1.1; Section 5.3.2; Section 6.9; new Section 2.8
  - Description: Acceptance criteria are required, but the required syntax, level of rigor, and meaning of terms such as testable acceptance patterns and holdout patterns are not defined.
  - Why it matters: Acceptance structure determines whether outputs can be validated objectively by humans, vendors, or AI agents.
  - Dependencies: Depends on A06, A07, A08.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: Hybrid Gherkin (Given/When/Then + quantifiable metrics, validation method, holdout examples). Observable/quantifiable principle enforced. Embedded in primary artifacts. Updated YAML for ARTIFACT-ACCEPTANCE-CRITERIA (embedded), gates, scaling rules, and examples added in new Section 2.8. Gate 4 requires `strong` rating on acceptance quality.
- [x] **A11 - Minimum supportability and maintainability definition is missing**
  - Relevant section(s): Section 2.1.6; Section 2.3.3; Section 3.7; Section 5.2.1; Section 5.7.2; Section 6.11; new Section 2.9
  - Description: The specification requires supportability and maintainability but does not decompose them into minimum required information, such as ownership, support model, incident expectations, transition needs, or maintenance responsibilities.
  - Why it matters: The framework could otherwise produce delivery-ready documents that are operationally incomplete.
  - Dependencies: Depends on A06, A08, A09.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: Minimum 5 fields required (ownership, support model, observability, maintainability commitments, transition checklist). Embedded in Deployment Guide / Work Brief and TDD. Updated YAML for affected artifacts and GATE-TRANSITION-COMPLETE. Scaling rules defined. Gate 7 enforces supported operating state. New Section 2.9 added.
- [ ] **A12 - External engagement modes and handoff variants are underspecified**
  - Relevant section(s): Section 2.1.7; Section 4.3.10; Section 4.4.5; Section 5.2; Section 6.10
  - Description: The specification mentions external development teams but does not distinguish among full outsourced delivery, co-delivery, staff augmentation, implementation partners, or advisory vendors, nor define how handoff expectations change by engagement model.
  - Why it matters: Different external delivery modes require different artifact depth, assumptions, controls, and acceptance framing.
  - Dependencies: Depends on A01, A06, A09.
  - Estimated complexity: Medium
  - Risk if unresolved: Medium
  - Status: Unresolved
- [x] **A13 - Review, assurance, and audit mechanism is unclear**
  - Relevant section(s): Section 5; Section 6.12
  - Description: The specification uses reviewers, evaluators, and independent reviewers in scenarios, but does not define the official review process, review timing, required reviewers, approval model, or evidence retention expectations.
  - Why it matters: The framework depends on independent evaluation, but the method for that evaluation is not standardized.
  - Dependencies: Depends on A03, A05, A08.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The default model is Delivery Owner-led review with PMO assurance oversight. PMO defines the standard, assigns the Gate Decision Owner, checks evidence completeness, attends every substantive gate, audits samples, and intervenes on escalation, non-compliance, or dispute. Review mode follows the existing gate profile (small-work substantive at Gates 2/4/6 and quick-pass elsewhere; large-work substantive at all gates). Substantive gates require live meetings and committee-action style review records; quick-pass gates require a Decision Log entry only. Independent review is trigger-based only (architecture, security/privacy, external vendor handoff, material business/regulatory risk) and requires explicit domain signoff when triggered. PMO audits may reopen a passed gate only for material completeness or control failure.
- [x] **A14 - Blocker, risk, and open-issue handling model is incomplete**
  - Relevant section(s): Section 2.2.1-7; Section 2.3.7; Section 4.5.3-4; Section 5.4-5.5
  - Description: The specification requires missing information, dependencies, risks, and open questions to be documented, but it does not define the taxonomy, recording method, ownership, escalation path, or closure criteria for those items.
  - Why it matters: The framework cannot reliably stop work on unresolved ambiguity unless unresolved items are managed in a standard way.
  - Dependencies: Depends on A03, A04, A05, A13.
  - Estimated complexity: Medium
  - Risk if unresolved: High
  - Status: Resolved
  - Resolution note: The framework now mandates a single Open Items Register for every initiative by Gate 2. It uses one typed-entry model (`blocker`, `risk`, `issue`, `assumption`, `dependency`) across the full lifecycle, with standard statuses (`open`, `in progress`, `monitoring`, `resolved`, `closed`), mandatory minimum fields, one named item owner per entry, explicit blocker reclassification when a non-blocker becomes gate-disqualifying, mandatory escalation triggers, Gate Decision Owner confirmation for blocker closure, and strict separation from the Decision Log, which records formal decisions rather than item lifecycle updates.
- [ ] **A15 - AI-agent sufficiency standard is implied but not concretely defined**
  - Relevant section(s): Section 1; Section 2.1.8-10; Section 2.3.5; Section 3.8; Section 5.3
  - Description: The specification requires outputs to be precise enough for AI-assisted delivery, but it does not define what additional structure, explicitness, or machine-readable discipline is required beyond what would satisfy a human team.
  - Why it matters: The framework may under-specify requirements for AI use while falsely claiming AI readiness.
  - Dependencies: Depends on A07, A08, A10.
  - Estimated complexity: Medium
  - Risk if unresolved: Medium
  - Status: Unresolved
- [ ] **A16 - Anti-bureaucracy guardrails are stated but not enforceable**
  - Relevant section(s): Section 1; Section 2.3.1; Section 3.1-2; Section 5.6; Section 7.1; Section 8
  - Description: The specification repeatedly says the framework must avoid unnecessary process, but it does not define how to judge whether an artifact, review step, or requirement adds delivery value or may be omitted. Possible interpretations range from strict minimalism to broad mandatory documentation with discretionary waivers.
  - Why it matters: Without an enforceable guardrail, teams may either over-document or bypass rigor under the banner of speed.
  - Dependencies: Depends on A02, A06, A08, A09.
  - Estimated complexity: Medium
  - Risk if unresolved: Medium
  - Status: Unresolved
## 3. Dependency and Sequencing Analysis

### Foundational
- **A01 - In-scope and out-of-scope work types**
- **A02 - Framework form and publication model**
- **A03 - Governance, ownership, and decision rights**
- **A04 - Minimum intake inputs and entry readiness**
- **A05 - Lifecycle stages, progression gates, and exit criteria**
- **A06 - Required artifact taxonomy**
- **A07 - Boundary to technical specification work**
- **A08 - Completeness and delivery-readiness criteria**
- **A09 - Scaling rules for simple versus complex work**

These items are foundational because they define the framework's basic operating model: what work it governs, what form it takes, who owns it, how work enters it, how teams move through it, what outputs it produces, where it stops, how readiness is judged, and how rigor scales.

### Dependent
- **A10 - Acceptance criteria and observable validation model**
- **A11 - Minimum supportability and maintainability definition**
- **A14 - Blocker, risk, and open-issue handling model**
- **A15 - AI-agent sufficiency standard**
- **A17 - Critical stage-defining artifact mapping**

These items depend on the foundational model because they rely on defined artifacts, gates, readiness criteria, and framework boundaries.

### Optional / lower-impact
- **A12 - External engagement modes and handoff variants**
- **A16 - Anti-bureaucracy guardrails**

These are not unimportant, but they are either conditional by delivery mode or easier to finalize once the core operating model already exists.

### Proposed sequence rationale
1. **Resolve scope, form, and authority first** so the framework has a stable identity and owner.
2. **Resolve intake, stages, and artifacts next** because these define how the framework operates day to day.
3. **Resolve boundary, completeness, and scaling** because these determine where the framework ends and how rigor is applied.
4. **Resolve validation-specific topics** such as acceptance, supportability, review, and blocker handling once the core structure exists.
5. **Resolve conditional or optimization topics last** such as external engagement variants and anti-bureaucracy guardrails.

## 4. Prioritized Resolution Plan

| Done | Priority order | Ambiguity ID and title | Why it is in this position | Expected outcome of resolving it | Recommended stakeholders or decision owners | Suggested method to resolve it | Status |
|---|---:|---|---|---|---|---|---|
| [x] | 1 | **A01 - In-scope and out-of-scope work types** | Scope must be fixed before paths, artifacts, and controls can be defined. | A clear applicability statement and exclusions list. | Framework sponsor, PMO lead, delivery leadership | Scope decision with explicit inclusion/exclusion rules and examples. | Resolved |
| [x] | 2 | **A02 - Framework form and publication model** | The team must know what it is actually building before detailing mechanics. | A defined framework packaging model, such as operating model plus templates and workflow. | Framework sponsor, knowledge owner, PMO | Decision on deliverable form, structure, and publishing approach. | Resolved |
| [x] | 3 | **A03 - Governance, ownership, and decision rights** | Enforcement cannot work without named owners and escalation authority. | A RACI-like ownership model and formal stop/proceed authority. | PMO, delivery leadership, framework owner | Governance decision with named roles and approval rights. | Resolved |
| [x] | 4 | **A04 - Minimum intake inputs and entry readiness** | Intake quality determines whether the process starts with enough signal. | A minimum required input set and intake gate definition. | Request owners, PMO, delivery managers | Clarification plus intake checklist and blocker rules. | Resolved |
| [x] | 5 | **A05 - Lifecycle stages, progression gates, and exit criteria** | Stages and gates operationalize the framework and unlock artifact design. | A formal staged flow with evidence required at each gate. | Framework owner, delivery managers, PMO | Workflow definition with gate criteria and examples. | Resolved |
| [x] | 6 | **A06 - Required artifact taxonomy** | Once stages exist, outputs can be assigned to the correct points and conditions. | A canonical artifact set with core and conditional outputs. | Framework owner, delivery managers, engineering representatives | Artifact matrix with purpose, required contents, and applicability rules. | Resolved |
| [x] | 7 | **A07 - Boundary between framework outputs and technical specification work** | The handoff line must be clear before readiness can be measured. | A defined boundary between framework deliverables and downstream engineering specs. | Engineering leadership, architects, PMO | Scope boundary decision supported by examples of in-framework vs downstream artifacts. | Resolved |
| [x] | 8 | **A08 - Completeness and delivery-readiness criteria** | This is the core pass/fail rule for the entire framework. | A reusable completeness rubric and readiness checklist. | PMO, engineering reviewers, framework owner | Decision plus rubric, checklist, and fail conditions. | Resolved |
| [x] | 9 | **A09 - Scaling rules for simple versus complex work** | Scaling should be defined after artifacts and readiness criteria exist. | A tiering model or decision rule for path selection and artifact depth. | PMO, delivery managers, framework owner | Complexity classification model with thresholds and examples. | Resolved |
| [x] | 10 | **A10 - Acceptance criteria and observable validation model** | Acceptance design depends on artifacts, boundary, and completeness rules already being known. | A standard acceptance format and definition of observable validation. | Product or business leads, QA or validation stakeholders, engineering | Rule definition plus examples or acceptance-writing pattern. | Resolved |
| [x] | 11 | **A11 - Minimum supportability and maintainability definition** | Operational readiness content can be specified after artifact structure and scaling are known. | A minimum operational-readiness content standard. | Support owner, operations lead, delivery manager | Clarification of required support fields, responsibilities, and transition expectations. | Resolved |
| [x] | 12 | **A13 - Review, assurance, and audit mechanism** | Review design depends on governance, stages, and readiness criteria. | A standard review model with reviewer roles, checkpoints, and evidence. | PMO, framework owner, engineering review leads | Review workflow definition and approval policy. | Resolved |
| [x] | 13 | **A14 - Blocker, risk, and open-issue handling model** | Blocker handling should align to the approved workflow and governance model. | A standard issue register model and stop/proceed rules. | Delivery managers, PMO, framework owner | Decision on taxonomy, ownership, escalation, and closure rules. | Resolved |
| [ ] | 14 | **A15 - AI-agent sufficiency standard** | AI-readiness should be calibrated after the human baseline is explicit. | A defined precision standard for AI-consumable documentation. | Framework owner, engineering, AI delivery stakeholders | Clarification of additional structure, explicitness, and prohibited ambiguity. | Unresolved |
| [ ] | 15 | **A12 - External engagement modes and handoff variants** | External variants should be derived from the core framework rather than invented upfront. | A handoff model adjusted by vendor engagement type. | Vendor management, PMO, delivery leadership | Scope decision plus conditional handoff requirements by engagement model. | Unresolved |
| [ ] | 16 | **A16 - Anti-bureaucracy guardrails** | Guardrails are most credible once the full framework exists and can be pruned deliberately. | A clear rule for omitting low-value steps without weakening readiness. | Framework owner, PMO, delivery leadership | Principle-to-rule conversion using omission criteria, waiver rules, and examples. | Unresolved |
| [ ] | 17 | **A17 - Critical stage-defining artifact mapping** | The completeness model now depends on identifying which artifacts are truly stage-defining at each gate. | A canonical gate-to-critical-artifact mapping, including packaging-mode and conditional-artifact rules. | Framework owner, PMO, delivery managers, engineering reviewers | Mapping decision with examples for packet mode, large-work mode, and conditional artifacts. | Unresolved |

## 5. Progress Tracking Summary

- **Total ambiguities identified:** 17
- **Resolved ambiguities:** 13
- **Remaining unresolved ambiguities:** 4
- **Foundational items:** 9
- **Dependent items:** 5
- **Optional / lower-impact items:** 2
- **Tracking note:** A01-A11 and A13-A14 have been resolved (13 of 17). A17 remains deferred. Next active ambiguity is now A15 (AI-agent sufficiency standard).
