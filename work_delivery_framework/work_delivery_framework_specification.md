# Work Delivery Framework Specification

## 1. System Overview

This framework defines how internal teams, the PMO, delivery managers, and internal engineers turn a new business request into delivery-ready project documentation. Its purpose is to produce complete, unambiguous, buildable, supportable specifications that are sufficient for internal human teams, external development teams, or AI agents to deliver work without redefining the problem during execution.

The framework exists to make “good” and “complete” explicit while avoiding unnecessary process overhead for its own sake.

### 1.1 Scope of applicability

The framework is defined for planned software initiatives.

**In scope**
1. Greenfield software projects
2. Brownfield software projects

**Out of scope**
1. Minor low-risk changes
2. Research spikes
3. Support work
4. Small internal process changes

**Conditionally in scope**
1. Complex operational changes affecting multiple organizations when the work is still primarily a software initiative
2. Complex internal process changes affecting the whole organization when the work is still primarily a software initiative

Conditional use does not make this a general enterprise change framework. The default and intended design target is planned software initiative delivery.
### 1.2 Framework form and publication model

This framework is a full **operating model** for work definition and delivery readiness. It is not optional guidance.

**Canonical deliverable**
The canonical source of truth is this document (`work_delivery_framework_specification.md`). Teams MUST treat it as the authoritative operating model definition.

**Workflow and control model**
The framework MUST define:
1. how a business request enters the system
2. the sequence of stages a project moves through
3. the outputs required at each stage
4. what “good” and “complete” mean for each required output
5. when work is blocked due to missing or unclear information

**Machine-consumable structure (Markdown-first)**
This document MUST include machine-consumable definitions embedded as fenced YAML blocks with stable IDs so AI agents can extract and apply the framework consistently.

At minimum, the machine-consumable model MUST represent:
1. stages (with entry and exit criteria)
2. artifacts (with required contents and completeness criteria)
3. gates (with pass/fail criteria and stop/proceed rules)

The YAML blocks MUST use stable identifiers (example shapes only):

```yaml
kind: stage
id: STAGE-INTAKE
name: Intake
entry_criteria: []
exit_criteria: []
required_artifacts: []
gate: GATE-INTAKE-EXIT
```

```yaml
kind: artifact
id: ARTIFACT-BUSINESS-REQUEST
name: Business Request
purpose: ""
required_contents: []
artifact_specific_completeness_rules: []
common_failure_conditions: []
```

```yaml
kind: gate
id: GATE-INTAKE-EXIT
name: Intake Exit Gate
mandatory_pass_conditions: []
immediate_fail_conditions: []
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts: []
default_decision_owner_role: Delivery Owner
requires_named_decision_owner: true
decision_rights: []
```

**Behavioral implication**
The framework MUST support human teams using AI agents as assistants while keeping the final outputs reviewable and enforceable by humans.

## 2. Behavioral Contract

### 2.1 Primary flows

1. When a new business request is introduced, the system defines a clear entry point for teams to evaluate the request and begin documentation.
2. When a team uses the framework for a project, the system guides them through a defined process for producing the required project artifacts.
3. When the project requires delivery documentation, the system defines what artifacts must exist and what each artifact must make observable from the outside.
4. When the project requires solution definition, the system requires documentation of the proposed solution in enough detail for a delivery team to understand what is being built.
5. When the project requires delivery planning, the system requires documentation of how the work will be delivered, not just what the solution is.
6. When the project requires operational readiness, the system requires documentation of how the delivered solution will be supported and maintained over time.
7. When an external development team will implement the work, the system requires a handoff package that is usable by that external team without relying on undocumented assumptions.
8. When internal teams or AI agents will implement the work, the system requires documentation detailed enough for them to produce build specifications, plans, and the required solution without redefining the underlying business need.
9. When teams complete the framework correctly, the system produces a delivery-ready documentation set that includes sufficient context, rules, acceptance criteria, and observable expectations to enable autonomous downstream execution.
10. When a team evaluates whether documentation is complete, the system defines completeness in terms of whether engineering teams can derive technical specifications and produce the required solution without having to reinterpret or reinvent business requirements.

### 2.2 Error flows

1. When required business inputs are missing, the system identifies the missing information as a blocker and records it explicitly.
2. When required dependencies are unavailable or unclear, the system requires those gaps to be documented and raised to stakeholders.
3. When “good” or “complete” cannot be defined because dependencies or requirements are unclear, the system prevents the work from proceeding.
4. When a team attempts to move forward with unresolved ambiguity, the system treats that state as incomplete rather than allowing silent assumption-making.
5. When project documentation appears complete but does not contain enough detail for autonomous delivery, the system treats that output as insufficient.
6. When teams use the framework inconsistently, the system makes inconsistency visible by defining a standard set of required outputs and evaluation criteria.
7. When a project contains risk that is not adequately specified, the system requires that risk to be surfaced in the documentation rather than left implicit.

### 2.3 Boundary conditions

1. When work is simple, the system must still require enough documentation to make the work buildable, but it must not force documentation that does not contribute to delivery readiness.
2. When work is complex, cross-functional, or multi-team, the system must scale to produce a more complete documentation set without lowering the standard of clarity.
3. When work is intended for long-term support and maintenance, the system must require documentation that addresses supportability and maintainability, not only initial delivery.
4. When multiple teams read the same documentation, the system must make the intended outcome clear enough that different teams do not reasonably arrive at conflicting interpretations.
5. When AI agents are used as delivery teams, the system must provide enough precision that the agents do not need to infer missing business requirements.
6. When a project cannot be described with testable acceptance patterns or equivalent observable outcome definitions, the system must treat that as an unresolved gap.
7. When a project would require undocumented assumptions to proceed, the system must stop progression until those assumptions are replaced with explicit decisions or documented open issues.
8. When teams want to omit framework steps, artifacts, or requirements to reduce overhead, the system must allow omission only where the framework explicitly permits it and only when readiness is not weakened.
9. When a control is part of the framework's non-waivable core, the system must treat that control as mandatory regardless of schedule pressure, team preference, or local judgments about convenience.

### 2.4 Lifecycle stages, progression gates, and exit criteria

The framework lifecycle is defined as a sequence of formal stages with explicit progression gates. A project MAY be blocked at any gate if the required evidence is missing or material ambiguity remains unresolved.

**Important boundary note**
Stages and gates define the control model. The canonical artifact taxonomy is defined in Section 2.5. Proportionate rigor expectations for different initiative shapes are defined in Section 2.7.

**Stages (in order)**
1. Intake
2. Assessment / Qualification
3. Discovery / Initiative Definition
4. Authorization (conditional)
5. Solution Definition
6. Planning / Project Team Mobilization / MVP Plan
7. Delivery / Execution
8. Handoff / Transition
9. Closure

**Gates (in order)**
1. Qualified Request
2. Initiative Defined (for Authorization decision)
3. Authorized (conditional)
4. Specification Complete
5. MVP Identified (MVP scope + MVP success/acceptance criteria approved)
6. All Deliverables Accepted (Acceptance Owner accepts delivered solution against specified acceptance criteria)
7. Transition Complete (supported operating state accepted)
8. Closure Complete

**Stage → gate mapping**
1. Intake has no progression gate; it establishes initial ownership and opens the record.
2. Assessment / Qualification ends at Gate 1 (Qualified Request).
3. Discovery / Initiative Definition ends at Gate 2 (Initiative Defined).
4. Authorization (conditional) ends at Gate 3 (Authorized).
   - If Authorization is not required, the project transitions from Discovery directly to Solution Definition after Gate 2.
   - Authorization applicability is informed by the initiative's business, funding, and governance context (see Section 2.7). The Gate Decision Owner must declare Authorization as “Required” or “Not Required” at Gate 2.
5. Solution Definition ends at Gate 4 (Specification Complete).
6. Planning / Mobilization / MVP Plan ends at Gate 5 (MVP Identified).
7. Delivery / Execution ends at Gate 6 (All Deliverables Accepted).
8. Handoff / Transition ends at Gate 7 (Transition Complete).
9. Closure ends at Gate 8 (Closure Complete).

**Minimum evidence categories by gate (high-level)**
1. Gate 1 (Qualified Request): request intake record is complete enough to support qualification; in-scope determination; threshold determination (if applicable); accountable Delivery Owner assigned; initial stakeholder list; known unknowns captured.
2. Gate 2 (Initiative Defined): bounded scope; desired outcomes and success measures; major constraints and dependencies; initial solution direction; estimated effort/shape at an appropriate level; decision on whether Authorization is required; provisional external engagement mode declared if external participation is expected.
3. Gate 3 (Authorized): explicit business authorization to invest resources; budget/resource commitment (as applicable); funding/priority decision recorded; Gate Decision Owner named.
4. Gate 4 (Specification Complete): solution definition is complete enough for downstream planning and task breakdown without inventing business requirements; acceptance criteria are defined; critical risks/unknowns are either resolved or explicitly managed as open issues; external engagement mode is finalized if applicable; Delivery Charter is complete when required.
5. Gate 5 (MVP Identified): MVP scope is defined; MVP success measures and MVP acceptance criteria are explicit and approved; delivery approach is feasible with the current team and constraints.
6. Gate 6 (All Deliverables Accepted): delivered solution is accepted by the named Acceptance Owner against the specified acceptance criteria; any deviations are explicitly approved and recorded.
7. Gate 7 (Transition Complete): operating ownership is established; support model is ready; transition activities are complete; the solution is in a supported operating state.
8. Gate 8 (Closure Complete): closure record is complete; final acceptance evidence is present; transition is complete; decision log is updated; outcomes are recorded; closure rationale is documented.

**Machine-consumable lifecycle model (YAML)**

```yaml
kind: stage
id: STAGE-INTAKE
name: Intake
entry_criteria: []
exit_criteria:
  - Initial request captured
  - Provisional triage ownership assigned
required_artifacts: []
gate: null
```

```yaml
kind: stage
id: STAGE-ASSESSMENT
name: Assessment / Qualification
entry_criteria:
  - Intake completed
exit_criteria:
  - Request qualified as in-scope (or rejected as out-of-scope)
required_artifacts: []
gate: GATE-QUALIFIED-REQUEST
```

```yaml
kind: stage
id: STAGE-DISCOVERY
name: Discovery / Initiative Definition
entry_criteria:
  - Gate 1 passed
exit_criteria:
  - Initiative definition is sufficient to decide authorization requirement
required_artifacts: []
gate: GATE-INITIATIVE-DEFINED
```

```yaml
kind: stage
id: STAGE-AUTHORIZATION
name: Authorization
conditional: true
entry_criteria:
  - Authorization is required (declared at Gate 2)
exit_criteria:
  - Authorization decision recorded
required_artifacts: []
gate: GATE-AUTHORIZED
```

```yaml
kind: stage
id: STAGE-SOLUTION-DEFINITION
name: Solution Definition
entry_criteria:
  - Gate 2 passed
exit_criteria:
  - Solution definition is complete enough for planning and task breakdown
required_artifacts: []
gate: GATE-SPECIFICATION-COMPLETE
```

```yaml
kind: stage
id: STAGE-PLANNING
name: Planning / Project Team Mobilization / MVP Plan
entry_criteria:
  - Gate 4 passed
exit_criteria:
  - MVP scope and MVP acceptance criteria approved
required_artifacts: []
gate: GATE-MVP-IDENTIFIED
```

```yaml
kind: stage
id: STAGE-DELIVERY
name: Delivery / Execution
entry_criteria:
  - Gate 5 passed
exit_criteria:
  - Delivered solution accepted against acceptance criteria
required_artifacts: []
gate: GATE-DELIVERABLES-ACCEPTED
```

```yaml
kind: stage
id: STAGE-TRANSITION
name: Handoff / Transition
entry_criteria:
  - Gate 6 passed
exit_criteria:
  - Supported operating state accepted
required_artifacts: []
gate: GATE-TRANSITION-COMPLETE
```

```yaml
kind: stage
id: STAGE-CLOSURE
name: Closure
entry_criteria:
  - Gate 7 passed
exit_criteria:
  - Closure requirements satisfied and recorded
required_artifacts: []
gate: GATE-CLOSURE-COMPLETE
```

```yaml
kind: gate
id: GATE-QUALIFIED-REQUEST
name: Qualified Request
mandatory_pass_conditions:
  - Request is in scope for the framework
  - Gate Decision Owner is named
immediate_fail_conditions:
  - Request is out of scope
  - Scope cannot be determined due to missing inputs
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-REQUEST-INTAKE-RECORD
critical_mapping_rule_ref: RULE-GATE-1-CRITICAL-ARTIFACTS
default_decision_owner_role: Delivery Owner
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-INITIATIVE-DEFINED
name: Initiative Defined (for Authorization decision)
mandatory_pass_conditions:
  - Scope is bounded
  - Outcomes and success measures are defined at an appropriate level
  - Authorization requirement is declared (Required or Not Required)
  - If external participation is expected, a provisional external engagement mode is declared
immediate_fail_conditions:
  - Critical ambiguity remains unresolved
  - Authorization requirement cannot be decided due to missing information
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
critical_mapping_rule_ref: RULE-GATE-2-CRITICAL-ARTIFACTS
default_decision_owner_role: Delivery Owner
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-AUTHORIZED
name: Authorized
conditional: true
mandatory_pass_conditions:
  - Business authorization to invest resources is explicit and recorded
immediate_fail_conditions:
  - Authorization is required but not granted
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-CHARTER
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
critical_mapping_rule_ref: RULE-GATE-3-CRITICAL-ARTIFACTS
default_decision_owner_role: Business / Product Owner (Budget Owner)
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-SPECIFICATION-COMPLETE
name: Specification Complete
mandatory_pass_conditions:
  - Solution definition is sufficient for planning and task breakdown
  - Acceptance criteria are defined
  - If external delivery is used, the engagement mode is finalized and Delivery Charter obligations are satisfied
immediate_fail_conditions:
  - Downstream delivery would require inventing business requirements
minimum_qualitative_threshold: strong
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-TDD
  - ARTIFACT-API-CONTRACT-SPEC
  - ARTIFACT-DATA-ASSET-SPEC
  - ARTIFACT-DATA-MIGRATION-PLAN
  - ARTIFACT-ACCESS-MODEL
  - ARTIFACT-SECURITY-PRIVACY-RIA
critical_mapping_rule_ref: RULE-GATE-4-CRITICAL-ARTIFACTS
default_decision_owner_role: Delivery Owner
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-MVP-IDENTIFIED
name: MVP Identified
mandatory_pass_conditions:
  - MVP scope is defined
  - MVP success measures are explicit
  - MVP acceptance criteria are explicit and approved
immediate_fail_conditions:
  - MVP is undefined or acceptance expectations are ambiguous
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-TDD
  - ARTIFACT-API-CONTRACT-SPEC
  - ARTIFACT-DATA-ASSET-SPEC
  - ARTIFACT-DATA-MIGRATION-PLAN
  - ARTIFACT-ACCESS-MODEL
  - ARTIFACT-SECURITY-PRIVACY-RIA
critical_mapping_rule_ref: RULE-GATE-5-CRITICAL-ARTIFACTS
default_decision_owner_role: Delivery Owner
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-DELIVERABLES-ACCEPTED
name: All Deliverables Accepted
mandatory_pass_conditions:
  - Delivered solution is accepted by the Acceptance Owner against the specified acceptance criteria
immediate_fail_conditions:
  - Acceptance criteria are not met and no explicit deviation approval exists
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-DEPLOYMENT-GUIDE
  - ARTIFACT-USER-ADOPTION-PLAN
critical_mapping_rule_ref: RULE-GATE-6-CRITICAL-ARTIFACTS
default_decision_owner_role: Acceptance Owner (Business / Product Owner)
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-TRANSITION-COMPLETE
name: Transition Complete
mandatory_pass_conditions:
  - Support model and operating ownership are accepted
immediate_fail_conditions:
  - The solution cannot be supported as delivered
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-DEPLOYMENT-GUIDE
  - ARTIFACT-USER-ADOPTION-PLAN
critical_mapping_rule_ref: RULE-GATE-7-CRITICAL-ARTIFACTS
default_decision_owner_role: Operations / Support Owner
requires_named_decision_owner: true
decision_rights: []
```

```yaml
kind: gate
id: GATE-CLOSURE-COMPLETE
name: Closure Complete
mandatory_pass_conditions:
  - Closure requirements are satisfied and recorded
immediate_fail_conditions:
  - Closure evidence is incomplete
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - ARTIFACT-CLOSURE-RECORD
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
critical_mapping_rule_ref: RULE-GATE-8-CRITICAL-ARTIFACTS
default_decision_owner_role: PMO / ITS Director
requires_named_decision_owner: true
decision_rights: []
```

### 2.5 Required artifact taxonomy

This section defines the canonical artifact taxonomy for this framework.

#### 2.5.1 Category labels vs artifacts

Some labels in this framework are **category labels** rather than artifacts. Category labels are used to organize thinking and required content, but do not imply a mandatory standalone file.

The following are category labels (not artifacts):
1. Project Governance
2. Solution Design
3. DevOps & Support
4. User Adoption

#### 2.5.2 Primary definition artifact model

The framework uses one canonical primary definition artifact for every in-scope initiative:
1. **Initiative Definition / Project Brief**

Conditional artifacts supplement the primary definition artifact when their trigger conditions are true, but they do not replace it.

#### 2.5.3 Canonical artifacts (names, triggers, and required-by gates)

**Always required**
1. Request Intake Record — required by **Gate 1**
2. Initiative Definition / Project Brief — required by **Gate 2**
3. Decision Log — must exist for every initiative and must exist no later than **Gate 2**
4. Open Items Register — must exist for every initiative and must exist no later than **Gate 2**
5. Closure Record — required by **Gate 8**

**Conditional artifacts (trigger → artifact(s) → required-by gate)**
1. Co-delivery or full external delivery → Delivery Charter → **Gate 4** (or **Gate 3** when early delivery-team commitment is required)
2. Authorization required → Approved Project Charter → **Gate 3**
3. Material ops/support impact → Technical Design Document (TDD) + Deployment Guide → TDD by **Gate 4**, Deployment Guide by **Gate 6**
4. Data migration → Data Asset Specification + Data Migration Plan → **Gate 4**
5. Security/compliance impact → Access Model + Security/Privacy Risk Impact Assessment → **Gate 4**
6. New integration / API change → API/Contract Specification → **Gate 4**
7. Customer-facing change → User Adoption Plan → start between **Gate 4** and **Gate 6** (earlier is better); must be complete no later than **Gate 6**

**Filename guidance**
Artifact names are canonical. Exact filenames are not enforced, but projects are strongly encouraged to use the canonical artifact names as filenames to support consistent discovery and audit.

**External engagement mode rule**
When external participation is expected, the initiative MUST declare one provisional external engagement mode by **Gate 2** and finalize it no later than **Gate 4**. The canonical modes are:
1. **Staff augmentation** — external personnel work inside the internal team's delivery model; this does **not** by itself trigger a Delivery Charter or formal external handoff package.
2. **Co-delivery** — internal and external teams share delivery responsibility; this **does** trigger a Delivery Charter and explicit responsibility/coordination rules.
3. **Full external delivery** — the external team is expected to execute from the approved package with minimal reliance on recurring requirement clarification; this **does** trigger a Delivery Charter and the strongest handoff completeness standard.

Advisory or review-only vendors are not a separate framework mode unless they become materially involved in delivery.

**Framework evolution note**
The artifact set may evolve over time. Changes MUST be applied by updating this specification’s artifact definitions (including the machine-consumable YAML blocks) rather than introducing parallel shadow taxonomies.

#### 2.5.4 Machine-consumable artifact model (YAML)

```yaml
kind: artifact
id: ARTIFACT-REQUEST-INTAKE-RECORD
name: Request Intake Record
packaging_mode: standalone
required_by_gate: GATE-QUALIFIED-REQUEST
purpose: Lightweight intake and assessment record that captures the minimum request information, initial scope qualification evidence, accountable triage ownership, and known unknowns needed to decide whether the request is a qualified framework candidate.
required_contents:
  - Requester name
  - Background / problem / opportunity
  - Desired outcome
  - Success measures (explicitly Unknown/TBD allowed at entry)
  - Affected systems / processes (explicitly Unknown/TBD allowed at entry)
  - Triage owner
  - Initial in-scope / out-of-scope assessment
  - Initial known unknowns, dependencies, or blockers
artifact_specific_completeness_rules:
  - The record is sufficient to determine whether the request can be qualified, rejected, or sent for further clarification.
  - Ownership, initial scope judgment, and known unknowns are visible without requiring meeting-only context.
common_failure_conditions:
  - The request can only be understood from informal conversation rather than from the captured intake record.
  - Scope qualification or accountable ownership is missing or implied rather than explicit.
```

```yaml
kind: artifact
id: ARTIFACT-PROJECT-BRIEF
name: Initiative Definition / Project Brief
packaging_mode: standalone
required_by_gate: GATE-INITIATIVE-DEFINED
purpose: Primary initiative definition artifact that defines the initiative, its scope, business intent, operating context, and the named owners needed for gate decisions.
required_contents:
  - Background / problem / opportunity
  - Desired outcomes and success measures
  - Scope boundaries (in-scope / out-of-scope) and assumptions
  - Stakeholders and owners (including Gate Decision Owner assignments)
  - Constraints and dependencies
  - Known unknowns and open questions (explicitly tracked as such)
  - Functional requirements and use cases
  - User roles
  - Business rules
  - Solution direction (high-level)
  - Delivery approach (high-level)
  - Support and operational considerations (if applicable)
  - User adoption considerations (if applicable)
artifact_specific_completeness_rules:
  - The initiative can be understood, bounded, and discussed without relying on tribal knowledge.
  - Scope, business rules, and known unknowns are explicit enough to support gate decisions and downstream solution definition.
  - Ownership and decision authority are visible from the document itself.
common_failure_conditions:
  - Business outcomes, scope boundaries, or stakeholder accountabilities remain materially ambiguous.
  - The document appears complete but leaves foundational questions unresolved for the next stage.
```

```yaml
kind: artifact
id: ARTIFACT-DECISION-LOG
name: Decision Log
packaging_mode: standalone
required_by_gate: GATE-INITIATIVE-DEFINED
purpose: Durable record of material decisions, options considered, rationale, ownership, and implications so downstream teams do not silently reconstruct prior intent.
required_contents:
  - Decision entries (one per decision)
artifact_specific_completeness_rules:
  - Material stop/proceed, scope, requirement, risk-treatment, and approach decisions are recorded when made.
  - Each entry identifies the decision, owner, status, rationale, and implications clearly enough for later review.
  - Open decisions are distinguishable from settled decisions.
common_failure_conditions:
  - Important decisions are only implied in other artifacts or meeting context.
  - Entries omit enough rationale or status information that downstream teams must reinterpret why the decision exists.
entry_schema_notes:
  - Each decision entry should include: decision statement, date, owner, status, options considered, rationale, and implications.
```

```yaml
kind: artifact
id: ARTIFACT-OPEN-ITEMS-REGISTER
name: Open Items Register
packaging_mode: standalone
required_by_gate: GATE-INITIATIVE-DEFINED
purpose: Canonical initiative-level register for tracking blockers, risks, issues, assumptions, and dependencies in a single standard structure so gate decisions, escalation, and closure are auditable and consistent.
required_contents:
  - Entry ID
  - Entry type (blocker, risk, issue, assumption, dependency)
  - Title
  - Description
  - Owner
  - Status (open, in progress, monitoring, resolved, closed)
  - Affected stage or gate
  - Impact summary
  - Next action
  - Target resolution or decision date
  - Created date
  - Last updated date
  - Resolution note (required when resolved or closed)
  - Origin reference (required for blocker entries that arose from another open item)
artifact_specific_completeness_rules:
  - The register exists for every initiative even if empty or near-empty.
  - Every open item is specific enough to support a gate decision rather than acting as a vague reminder.
  - No open blocker affecting the current gate remains at gate passage.
  - Any open non-blocker item that remains at gate passage is explicitly owned, has a next action and target date where applicable, and does not invalidate the gate's mandatory pass conditions.
common_failure_conditions:
  - Teams track unresolved items in local notes, meetings, or artifact margins instead of the canonical register.
  - Entries omit enough ownership, impact, or next-step information that gate reviewers cannot judge whether progression is valid.
  - A gate-disqualifying item remains classified as a non-blocker instead of being reclassified or recorded as a blocker.
entry_schema_notes:
  - The Open Items Register is a single table or equivalent single register structure with typed entries, not separate RAID tables.
  - Blocker entries SHOULD reference the originating item when they arise from a risk, issue, assumption, or dependency.
```

```yaml
kind: artifact
id: ARTIFACT-CLOSURE-RECORD
name: Closure Record
packaging_mode: standalone
required_by_gate: GATE-CLOSURE-COMPLETE
purpose: Formal closure artifact that records the final closure decision, closure evidence, remaining post-closure obligations if any, and the rationale for closing the initiative.
required_contents:
  - Closure decision and date
  - Closure owner
  - Final acceptance reference
  - Transition completion reference
  - Outcome summary against intended objectives
  - Final decision/open-item disposition summary
  - Closure rationale
  - Post-closure actions or obligations (if any)
artifact_specific_completeness_rules:
  - The closure basis is explicit enough that a later reviewer can understand why the initiative was closed and what remained outstanding, if anything.
  - Closure evidence links back to acceptance, transition, and final control records rather than asserting closure without traceable support.
common_failure_conditions:
  - Closure is declared without visible linkage to acceptance or transition completion.
  - The record omits enough rationale or status information that later audit cannot determine what was actually closed.
```

```yaml
kind: artifact
id: ARTIFACT-PROJECT-CHARTER
name: Project Charter (Approved)
conditional_on:
  - Authorization is required
required_by_gate: GATE-AUTHORIZED
purpose: Formal authorization artifact that records the approved purpose, scope, governance, and resource commitment for initiatives that require explicit authorization.
required_contents:
  - Project purpose and scope summary
  - Sponsor and authorization statement
  - Budget/resource commitment (as applicable)
  - Governance and decision rights (including named Gate Decision Owners)
  - High-level risks and constraints
artifact_specific_completeness_rules:
  - The authorization decision, sponsor intent, and resource commitment are explicit and attributable.
  - Governance and scope are clear enough that the team can act on the authorization without reopening its meaning.
common_failure_conditions:
  - Authorization is implied but not explicitly recorded.
  - Scope or authority remains vague enough that the team cannot tell what was actually approved.
```

```yaml
kind: artifact
id: ARTIFACT-DELIVERY-CHARTER
name: Delivery Charter
conditional_on:
  - External engagement mode is Co-delivery or Full External Delivery
required_by_gate_default: GATE-SPECIFICATION-COMPLETE
may_be_required_by_gate:
  - GATE-AUTHORIZED
purpose: Defines the external delivery engagement model, delivery responsibilities, working agreements, and handoff expectations needed for usable collaboration with or handoff to an external delivery team.
required_contents:
  - External engagement mode (Co-delivery or Full External Delivery)
  - Delivery engagement model and roles/responsibilities
  - Delivery cadence and working agreements
  - Communication and escalation paths
  - Handoff expectations and acceptance workflow (high-level)
  - Access and environment expectations (as applicable)
  - Decision and dependency interfaces between internal and external teams
  - Internal named owners for framework gates and acceptance
artifact_specific_completeness_rules:
  - Engagement roles, interfaces, and responsibilities are explicit enough to prevent delivery-governance gaps.
  - External parties can understand how work, decisions, escalation, and acceptance will operate.
  - For Co-delivery, the shared-delivery model and coordination boundaries are explicit enough to avoid duplicated or unowned work.
  - For Full External Delivery, the approved package is close to standalone: the external team can execute without routine requirement-reconstruction or repeated dependence on undocumented clarification.
common_failure_conditions:
  - The delivery mode is too vague to determine responsibilities or handoff expectations.
  - The document leaves unowned coordination or escalation gaps between internal and external teams.
  - A Full External Delivery engagement still depends on recurring clarification of foundational business intent, scope boundaries, or acceptance expectations.
```

```yaml
kind: artifact
id: ARTIFACT-TDD
name: Technical Design Document (TDD)
conditional_on:
  - Material ops/support impact
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: System-level design artifact that explains the proposed solution structure well enough for downstream engineering planning without dropping into code-level design.
required_contents:
  - Design goals and non-goals
  - System context and boundaries
  - Major components and responsibilities
  - Data flows and key interactions
  - Non-functional requirements (as applicable)
  - Operational considerations relevant to supportability (as applicable)
artifact_specific_completeness_rules:
  - The proposed system shape, boundaries, and major interactions are clear enough to derive downstream technical planning without inventing business requirements.
  - Design goals, non-goals, and operational implications align with the business and delivery artifacts.
common_failure_conditions:
  - Major components, boundaries, or key flows are absent or contradictory.
  - The artifact drifts into code-level design while still failing to explain system-level behavior.
explicitly_out_of_scope:
  - Task breakdown (epics/stories/tasks)
  - Code-level design
  - Per-endpoint acceptance tests
```

```yaml
kind: artifact
id: ARTIFACT-API-CONTRACT-SPEC
name: API/Contract Specification
conditional_on:
  - New integration / API change
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Defines externally visible contracts and integration expectations so downstream teams can implement and validate interfaces without guesswork.
required_contents:
  - Endpoints and/or events
  - Schemas
  - Authentication and authorization
  - Error handling
  - Versioning and backward-compatibility expectations
  - Dependencies
artifact_specific_completeness_rules:
  - Interface behavior, schemas, and failure behavior are explicit enough for independent implementation and review.
  - Contract assumptions align with security, access, and dependency constraints defined elsewhere.
common_failure_conditions:
  - Consumers or implementers would need to infer payload shape, error behavior, or compatibility expectations.
  - The contract conflicts with other framework artifacts or leaves material interface decisions unstated.
explicitly_out_of_scope:
  - Task breakdown (epics/stories/tasks)
  - Code-level design
  - Per-endpoint acceptance tests
```

```yaml
kind: artifact
id: ARTIFACT-DEPLOYMENT-GUIDE
name: Deployment Guide
conditional_on:
  - Material ops/support impact
required_by_gate: GATE-DELIVERABLES-ACCEPTED
purpose: Operational deployment and recovery artifact that enables controlled release, validation, rollback, and support handoff.
required_contents:
  - Deployment steps and prerequisites
  - Environments and configuration expectations
  - Rollback / recovery approach
  - Operational validation steps
  - Monitoring and support handover notes (as applicable)
artifact_specific_completeness_rules:
  - A qualified operator can understand how to deploy, validate, and recover the solution in the intended environments.
  - Release and support steps are explicit enough to establish a supported operating state.
common_failure_conditions:
  - Deployment or rollback depends on undocumented knowledge.
  - Operational validation or handover expectations are too vague to support transition.
```

```yaml
kind: artifact
id: ARTIFACT-USER-ADOPTION-PLAN
name: User Adoption Plan
conditional_on:
  - Customer-facing change
start_by_gate: GATE-SPECIFICATION-COMPLETE
required_by_gate: GATE-DELIVERABLES-ACCEPTED
purpose: Defines how affected users will be informed, enabled, and supported through rollout and adoption of the change.
required_contents:
  - Impacted user groups and change scope
  - Communications plan
  - Training and enablement approach (as applicable)
  - Rollout plan and adoption checkpoints
  - Support and feedback loop plan
artifact_specific_completeness_rules:
  - Impacted users, rollout expectations, and support loops are explicit enough to avoid unmanaged adoption risk.
  - Communications and enablement plans are proportionate to the change and aligned to the delivery plan.
common_failure_conditions:
  - The plan names user impact but provides no credible adoption or support path.
  - Rollout assumptions depend on undocumented communications, training, or ownership.
```

```yaml
kind: artifact
id: ARTIFACT-DATA-ASSET-SPEC
name: Data Asset Specification
conditional_on:
  - Data migration
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Defines the in-scope data assets, structures, constraints, and validation expectations required for safe migration or data-affecting change.
required_contents:
  - Data assets in scope
  - Schemas and mappings (as applicable)
  - Data quality and validation expectations
  - Sensitivity classification and retention considerations (as applicable)
  - Access considerations (as applicable)
artifact_specific_completeness_rules:
  - In-scope data, mappings, and validation expectations are explicit enough to design migration and verification safely.
  - Data sensitivity, access, and retention implications are visible where relevant.
common_failure_conditions:
  - The team cannot tell what data is moving, changing, or being validated.
  - Material quality, sensitivity, or access implications are omitted or contradictory.
```

```yaml
kind: artifact
id: ARTIFACT-DATA-MIGRATION-PLAN
name: Data Migration Plan
conditional_on:
  - Data migration
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Execution-level migration approach artifact that explains sequencing, cutover, validation, and rollback for data movement.
required_contents:
  - Migration approach and sequencing
  - Cutover plan and downtime expectations (as applicable)
  - Validation plan
  - Rollback / backout approach
artifact_specific_completeness_rules:
  - Migration sequencing, validation, and recovery are explicit enough to assess feasibility and delivery risk.
  - The plan aligns with the data asset definition and business continuity expectations.
common_failure_conditions:
  - Validation or rollback is missing, vague, or not credible.
  - Migration sequencing depends on undocumented assumptions about systems, data, or operating windows.
```

```yaml
kind: artifact
id: ARTIFACT-ACCESS-MODEL
name: Access Model
conditional_on:
  - Security/compliance impact
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Defines the intended access-control model, role boundaries, and related lifecycle expectations for secure operation.
required_contents:
  - Roles and permissions model
  - Authentication and authorization expectations
  - Provisioning and deprovisioning (as applicable)
  - Audit/logging expectations (as applicable)
artifact_specific_completeness_rules:
  - Access expectations are explicit enough to understand who can do what and how access is governed.
  - The model aligns with user roles, security expectations, and operational ownership elsewhere in the documentation set.
common_failure_conditions:
  - The access model leaves material role, permission, or lifecycle gaps unresolved.
  - Authentication, authorization, or audit assumptions conflict with other artifacts.
```

```yaml
kind: artifact
id: ARTIFACT-SECURITY-PRIVACY-RIA
name: Security/Privacy Risk Impact Assessment
conditional_on:
  - Security/compliance impact
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Captures the security, privacy, and compliance implications of the initiative so required controls and approvals are explicit before delivery proceeds.
required_contents:
  - Data types and sensitivity (as applicable)
  - Key risks and threat considerations
  - Required controls and mitigations
  - Compliance/privacy considerations and approvals (as applicable)
artifact_specific_completeness_rules:
  - Material security/privacy risks and required mitigations are visible enough to guide scope, design, and approval decisions.
  - Required approvals or control obligations are explicit where applicable.
common_failure_conditions:
  - Material security or privacy exposure is left implicit.
  - Required controls or approvals are missing, unclear, or disconnected from the proposed solution.
```

### 2.6 Completeness and delivery-readiness model

This section defines the completeness and delivery-readiness model used by the framework.

#### 2.6.1 Model type

Completeness is a **hybrid review model**:
1. **Mandatory pass/fail criteria** determine whether an artifact or gate can pass.
2. **Qualitative ratings** (`weak`, `adequate`, `strong`) describe the quality of the artifact or gate once mandatory criteria have been applied.

If any mandatory criterion fails, the artifact or gate fails immediately. The qualitative rating does not override failure.

#### 2.6.2 Scope of evaluation

Completeness MUST be evaluated at both levels:
1. **Artifact level** — each required artifact is judged on its own contents and coherence.
2. **Gate level** — the documentation set for that gate is judged as a coherent whole.

This is both:
1. a **review standard** used by reviewers and Gate Decision Owners, and
2. a **required design property** of this framework, meaning each artifact and gate definition in the specification MUST explicitly declare how completeness is judged.

#### 2.6.3 Shared artifact-level core

Every required artifact MUST be judged against this shared core:
1. **Clarity** — the artifact states what it means clearly enough that the next consumer does not need to guess the intended meaning.
2. **Internal consistency** — the artifact does not materially contradict itself.
3. **Decision and assumption visibility** — decisions, assumptions, unknowns, and open issues are explicit rather than implicit.
4. **Actionability for the next consumer** — the intended next consumer can use the artifact for its stated purpose without redefining the problem.
5. **AI sufficiency** — the artifact satisfies the AI-agent sufficiency standard in Section 2.12 when judged as a delivery-ready input for AI-assisted downstream work.

Each artifact MUST also define:
1. its **purpose**
2. its **required contents**
3. its **artifact-specific completeness rules**
4. its **common failure conditions**

#### 2.6.4 Shared gate-level mandatory checks

Every gate review MUST check that:
1. the documentation set is complete enough for that stage
2. the required artifacts are cross-artifact consistent
3. unresolved blockers do not force downstream teams to invent business requirements
4. the documentation is sufficient for the named downstream consumer to proceed without redefining the problem
5. the documentation set satisfies the AI-agent sufficiency standard in Section 2.12

Each gate definition MUST explicitly include:
1. **mandatory pass conditions**
2. **immediate fail conditions**
3. **minimum qualitative threshold**
4. **critical stage-defining artifacts**

The exact mapping rules for critical stage-defining artifacts are defined in Section 2.14. Reviewers and AI agents MUST apply those mapping rules rather than treating the gate YAML lists as flat unconditional artifact checklists.

#### 2.6.5 Blockers vs controlled open items

The framework MUST distinguish between:
1. **Blockers** — first-class open-item entries that force gate failure when they affect the current gate
2. **Controlled open items** — non-blocker open-item entries (`risk`, `issue`, `assumption`, `dependency`) that may remain open only if they are explicitly managed in the Open Items Register

A controlled open item MAY remain open at gate passage only if all of the following are true:
1. the item is stated explicitly in the Open Items Register
2. a named owner is assigned
3. a next action exists
4. a target resolution or decision date exists where appropriate
5. the item does not invalidate the gate's mandatory pass conditions
6. downstream work can proceed without inventing business requirements

If a non-blocker item becomes gate-disqualifying, it MUST be reclassified or recorded as a `blocker` entry and handled under the blocker rules defined in Section 2.11.

#### 2.6.6 Qualitative rating definitions

Qualitative ratings are standardized globally using an execution-oriented definition:
1. **Weak** — the downstream team would need to guess or reopen fundamentals
2. **Adequate** — the downstream team can proceed safely with limited clarification
3. **Strong** — the downstream team can proceed efficiently without material clarification

The qualitative rating is descriptive. It is not a substitute for mandatory pass criteria and cannot override a blocker or immediate fail condition.

#### 2.6.7 Gate-level rating thresholds

Gate-level thresholds are:
1. **Gates 1–3 and 5–8** — minimum rating is `adequate`
2. **Gate 4 (Specification Complete)** — minimum rating is `strong`

The gate-level qualitative judgment is separate from individual artifact ratings, but it is constrained by them:
1. the gate judgment MUST consider both artifact ratings and cross-artifact coherence
2. the gate rating cannot exceed the weakest materially relevant cross-artifact condition
3. a gate cannot be rated `strong` unless all required artifacts are at least `adequate`, and the critical stage-defining artifacts are `strong`, with no meaningful cross-artifact inconsistencies

#### 2.6.8 Reviewer discipline and evidence

The framework explicitly forbids reviewers from upgrading an artifact or gate based on:
1. confidence in the team
2. prior knowledge not captured in the documentation
3. verbal context, meeting memory, or undocumented side agreements

Document presence is never evidence of completeness. Reviewers MUST judge content sufficiency against the defined criteria, not against template fill, formatting quality, or presentation polish.

If an artifact or gate fails completeness, the review output MUST include a written deficiency list tied to the specific failed criteria.

If the failure includes one or more AI-agent sufficiency failures, the review output MUST state that explicitly as an **AI-sufficiency failure** rather than burying it inside a generic completeness comment.

There is **no conditional progression** for completeness failure. If the artifact or gate fails, work stops until the documented deficiencies are corrected and re-reviewed.

### 2.7 Scaling rules for planned software initiatives

This section defines how the framework scales within its intended scope of planned software initiatives.

#### 2.7.1 Core scaling principle

The framework uses one initiative path for all in-scope work.

Scaling is achieved by:
1. varying the depth and specificity of content inside the canonical artifacts
2. triggering conditional artifacts only when their trigger conditions are true
3. keeping the same gate standards while allowing evidence to remain proportionate to the initiative's scope, risk, and complexity

The framework does not use alternate initiative classes, packet modes, or substitute primary artifacts.

#### 2.7.2 Scaling factors

The Delivery Owner MUST calibrate rigor based on the initiative's actual characteristics, including:
1. **Scope**
   - number of teams, systems, modules, or affected business processes
2. **Business impact**
   - operational, financial, customer, compliance, or strategic significance
3. **Delivery complexity**
   - uncertainty, integration sensitivity, implementation effort, or dependency load
4. **Operational consequence**
   - support burden, transition complexity, or long-term maintainability expectations

External involvement is relevant context and may trigger specific artifacts, but it does not create a separate framework path.

#### 2.7.3 Timing and recording

The Delivery Owner MUST make the scaling judgment no later than Gate 2 (Initiative Defined) and reflect it in the depth, specificity, and conditional artifact selections used for the initiative.

If the initiative's shape changes materially later, the Decision Log MUST record the change and any newly required artifact work or gate evidence adjustments.

#### 2.7.4 Gate expectations under scaling

Scaling does not change the set of gates or allow gate bypass.

For simpler in-scope initiatives, evidence may be more concise when it still satisfies the gate's mandatory pass conditions and completeness rules.

For more complex, risky, or externally dependent initiatives, evidence is expected to be more explicit, more cross-referenced, and more fully decomposed into conditional artifacts.

Every gate must still be formally evaluated and recorded.

#### 2.7.5 Machine-consumable scaling model (YAML)

```yaml
kind: scaling
id: SCALING-MODEL
name: Work Delivery Framework Scaling Model
primary_artifact: ARTIFACT-PROJECT-BRIEF
scaling_factors:
  - scope
  - business_impact
  - delivery_complexity
  - operational_consequence
conditional_artifact_trigger_model: triggered_per_section_2_5_3
gate_model: all_formal_gates_apply_to_all_in_scope_initiatives
evidence_expectation: proportionate_to_scope_risk_complexity_and_operational_impact
scaling_judgment_timing: no_later_than_gate_GATE-INITIATIVE-DEFINED
material_change_recording: record_decision_and_adjust_artifact_expectations_in_decision_log
```

### 2.8 Acceptance criteria and observable validation model

This section defines the acceptance-criteria and validation model: acceptance criteria must be **observable**, **quantifiable** where possible, and expressed in **hybrid Gherkin** (Gherkin-style Given/When/Then mixed with explicit success metrics and testability rules). The model prioritizes validation that downstream teams (human, vendor, or AI) can execute without subjective interpretation.

#### 2.8.1 Core principle (observable/quantifiable)

Every acceptance criterion **MUST** be:
- **Observable**: Can be verified by inspecting outputs, running tests, or querying system state (no "feels good" language)
- **Quantifiable** when feasible (e.g., "response time < 200ms for 95% of requests" vs "fast enough")
- **Testable** with defined success conditions (pass/fail, thresholds, or holdout examples)

If a requirement cannot be made observable, it is treated as an open issue (see Section 2.6.5) and blocks Gate 4 until resolved.

#### 2.8.2 Hybrid Gherkin guidance

Use this hybrid format for all acceptance criteria:

```
Given [preconditions and context]
When [action or event occurs]
Then [observable outcome] 
  - Metric: [quantifiable success threshold]
  - Validation method: [test, query, inspection, or holdout pattern]
  - Holdout example: [concrete input/output pair for verification]
```

**Rules for embedding**:
- Place acceptance criteria in the **Initiative Definition / Project Brief** under a dedicated "Acceptance Criteria" section
- Cross-reference in relevant artifacts (TDD, API/Contract Spec, User Adoption Plan)
- For complex features, group by use case or user story
- Always include at least one concrete holdout example per major criterion

#### 2.8.3 Scaling and gate expectations

- **Lower-complexity initiatives**: a concise set of acceptance criteria focused on the core outcomes may be sufficient for Gate 4 when the criteria remain complete, observable, and testable
- **Higher-complexity initiatives**: a broader set is expected, covering functional, non-functional, data, integration, security, and operational validation where relevant
- **Gate 4 (Specification Complete)**: All acceptance criteria must be present, observable, and rated `strong`. Gate fails if any criterion requires downstream reinterpretation.
- **Gate 6 (All Deliverables Accepted)**: Acceptance Owner verifies delivered solution against the exact criteria (no deviations without explicit recorded approval).

#### 2.8.4 Updated machine-consumable artifacts and gates (YAML additions)

Add/update the following in existing YAML blocks (or as new blocks):

```yaml
kind: artifact
id: ARTIFACT-ACCEPTANCE-CRITERIA
name: Acceptance Criteria
packaging_mode: embedded
required_by_gate: GATE-SPECIFICATION-COMPLETE
purpose: Defines observable, quantifiable success conditions for the delivered solution using hybrid Gherkin.
required_contents:
  - Hybrid Gherkin statements (Given/When/Then + metrics + validation method)
  - Holdout examples for each major criterion
  - Non-functional thresholds (performance, reliability, etc.)
artifact_specific_completeness_rules:
  - Every criterion is observable and testable without subjective judgment.
  - Quantifiable metrics are provided where applicable.
  - Holdout examples exist for core paths.
  - Criteria are cross-referenced from primary artifacts and align with business outcomes.
common_failure_conditions:
  - Uses vague language ("works well", "user friendly").
  - Lacks validation method or holdout examples.
  - Requires downstream team to invent test conditions.
```

Update GATE-SPECIFICATION-COMPLETE and GATE-DELIVERABLES-ACCEPTED YAML:
- Add to `mandatory_pass_conditions`: "- Acceptance criteria are observable, quantifiable, and include validation methods/holdout examples"
- Update `minimum_qualitative_threshold` for Gate 4 to enforce `strong` on acceptance quality.

#### 2.8.5 Examples

**Good (observable hybrid Gherkin)**:
```
Given a registered user with valid credentials
When they POST to /api/v1/orders with a valid payload
Then order is created with status "pending"
  - Metric: HTTP 201, response time < 300ms (p95)
  - Validation: Query orders table + API response schema match
  - Holdout: Input {"item":"widget","qty":2} → Output orderId=123, status=pending
```

**Bad (vague)**: "The order creation should work correctly and be fast."

### 2.9 Minimum supportability and maintainability definition

This section defines supportability and maintainability as explicit minimum requirements embedded in the **Deployment Guide** when that artifact is required, or in the **Initiative Definition / Project Brief** when a separate Deployment Guide is not required, and cross-referenced in the TDD where applicable.

#### 2.9.1 Minimum required content (always)

The following MUST be defined before Gate 6 (Transition Complete):

1. **Ownership**
   - Named Support Owner (role or individual)
   - Escalation path and RACI for incidents

2. **Support model**
   - Tiered support levels (L1/L2/L3)
   - Expected response times (e.g., P1 incident < 15min)
   - On-call rotation (if applicable)

3. **Observability**
   - Key metrics, logs, and alerts required
   - Monitoring thresholds and dashboard references

4. **Maintainability**
   - Versioning and backward compatibility rules
   - Patching/upgrade process
   - Technical debt acceptance criteria
   - Knowledge transfer requirements (runbooks, architecture decision records)

5. **Transition checklist**
   - Handover activities with owners and evidence
   - Post-transition support window

#### 2.9.2 Scaling

- Lower-complexity initiatives may satisfy this section with a concise but explicit supportability summary in the Initiative Definition / Project Brief plus any lightweight operational notes needed for a supported operating state.
- Higher-complexity or higher-impact initiatives are expected to use a fuller Deployment Guide, TDD operational coverage, and dedicated runbooks where needed.

Gate 7 fails if support model leaves material gaps or cannot establish "supported operating state".

#### 2.9.3 Updated YAML for artifacts/gates

Add to ARTIFACT-DEPLOYMENT-GUIDE and ARTIFACT-TDD `required_contents`:
- Support ownership, observability plan, maintainability commitments, transition checklist.

Update GATE-TRANSITION-COMPLETE:
```yaml
kind: gate
id: GATE-TRANSITION-COMPLETE
...
mandatory_pass_conditions:
  - Support model, ownership, observability, and maintainability are explicitly defined and accepted
  - Transition checklist is complete with evidence
immediate_fail_conditions:
  - No named Support Owner or unaddressed operational gaps
minimum_qualitative_threshold: adequate
```

**Example snippet for Deployment Guide**:
```yaml
support_owner: "Platform Ops Team (J. Smith)"
incident_response:
  p1: "< 15 minutes"
  p2: "< 1 hour"
observability:
  metrics: ["error_rate", "latency_p95", "throughput"]
  alerting: "PagerDuty + Grafana"
maintainability:
  mttr_target: "< 4 hours"
  upgrade_process: "Blue-green with automated rollback"
```

These sections provide enforceable, observable standards for validation and long-term operations.

### 2.10 Review, assurance, and audit mechanism

This section defines the review, assurance, and audit mechanism for the framework.

#### 2.10.1 Default review ownership model

The default review model is **Delivery Owner-led review with PMO assurance oversight**.

The Delivery Owner-led model means:
1. the Delivery Owner is responsible for preparing the evidence package, convening the review, and ensuring the required artifact owners are present
2. the named **Gate Decision Owner** remains accountable for the final stop/proceed decision at the gate
3. the Gate Decision Owner and Delivery Owner MAY be the same person for a given gate

The PMO is the framework assurance function. PMO responsibilities are:
1. define and maintain the review standard for this framework
2. assign the named Gate Decision Owner
3. check evidence completeness for gate reviews
4. attend every substantive gate review meeting
5. audit a sample of completed gate reviews for compliance and quality
6. intervene when escalation, non-compliance, or dispute occurs

#### 2.10.2 Review modes by gate profile

The review mechanism MUST align to the gate profiles already defined in Section 2.7.

1. **Small-work** uses:
   - **substantive review** at Gate 2, Gate 4, and Gate 6
   - **quick-pass review** at Gate 1, Gate 3, Gate 5, Gate 7, and Gate 8
2. **Large-work** uses **substantive review** at every gate

Review-mode definitions:
1. **Substantive review** requires a live gate review meeting
2. **Quick-pass review** does not require a live gate review meeting and requires only the minimum record defined in Section 2.10.5

Quick-pass does not remove the gate. It only changes the review depth and evidence-retention model.

#### 2.10.3 Substantive review meeting model

Every substantive gate review MUST include the following attendees by default:
1. the named Gate Decision Owner
2. the Delivery Owner
3. the relevant artifact owner(s)
4. PMO
5. any triggered independent reviewer

Unless a required domain signoff is triggered (see Section 2.10.4), the Gate Decision Owner makes the final pass/fail decision after hearing the reviewers.

Formal pre-gate artifact review is not required by this framework. Teams MAY perform informal pre-reviews, but the formal decision point remains the gate review itself.

#### 2.10.4 Trigger-based independent review

Independent review is **not** required at every substantive gate. It becomes mandatory only when one or more trigger conditions are present.

The mandatory trigger conditions are:
1. architecture impact
2. security or privacy impact
3. external delivery or vendor handoff
4. material business risk or regulatory exposure

When triggered:
1. the relevant independent reviewer MUST participate for that domain
2. explicit **domain signoff** is required before the gate can pass
3. this required signoff is a domain-assurance precondition, not a transfer of overall gate ownership; the Gate Decision Owner still makes the overall gate decision once required domain signoffs are present

If a normally quick-pass gate hits one of the trigger conditions above, PMO decides case by case whether that gate remains quick-pass with targeted domain review or is converted into a substantive gate review.

#### 2.10.5 Review records and evidence retention

Review evidence retention is standardized by review mode.

For **quick-pass** gates:
1. a **Decision Log** entry is sufficient

For **substantive** gates:
1. a written **committee-action style** review record is required
2. the record MUST include:
   - gate reviewed
   - review date
   - attendees
   - decision
   - deficiencies or conditions (if any)
   - action items

The framework does not require transcripts, full meeting notes, or full informal comment capture unless a local policy outside this framework requires them.

#### 2.10.6 PMO evidence completeness, intervention, and audit reopening

PMO MUST perform an evidence-completeness check for every substantive gate review.

If PMO determines that the evidence package is incomplete:
1. the Gate Decision Owner MAY still proceed with the review and decision
2. the rationale for proceeding despite PMO's completeness concern MUST be documented in the committee-action style review record and/or Decision Log

PMO intervention is required when:
1. a formal escalation is raised
2. non-compliance with the framework is identified
3. a material dispute about gate passage cannot be resolved within the normal gate review

PMO audit findings MAY reopen or invalidate a previously passed gate only when a **material completeness failure** or **material control failure** is discovered after passage.

#### 2.10.7 Machine-consumable review model (YAML)

```yaml
kind: review_model
id: REVIEW-MODEL-GATE-ASSURANCE
name: Gate Review, Assurance, and Audit Model
default_model: delivery_owner_led_with_pmo_assurance
pmo_responsibilities:
  - Define review standard
  - Assign Gate Decision Owner
  - Check evidence completeness
  - Attend every substantive gate review
  - Audit sample reviews
  - Intervene on escalation, non-compliance, or dispute
review_modes:
  quick_pass:
    live_meeting_required: false
    minimum_record:
      - Decision Log entry
  substantive:
    live_meeting_required: true
    required_attendees:
      - Gate Decision Owner
      - Delivery Owner
      - Relevant artifact owner(s)
      - PMO
      - Triggered independent reviewer(s)
    final_decision_rule: >
      Gate Decision Owner decides after hearing reviewers unless a required
      domain signoff is still missing.
    minimum_record:
      - Gate reviewed
      - Review date
      - Attendees
      - Decision
      - Deficiencies or conditions
      - Action items
independent_review_triggers:
  - Architecture impact
  - Security or privacy impact
  - External delivery or vendor handoff
  - Material business risk or regulatory exposure
triggered_independent_review_rule: >
  Independent review is mandatory only when triggered. Required domain signoff
  must be present before the gate can pass.
quick_pass_trigger_override: >
  If a quick-pass gate hits an independent-review trigger, PMO decides whether
  the gate stays quick-pass with targeted review or becomes substantive.
evidence_completeness_override: >
  If PMO identifies incomplete evidence for a substantive gate, the Gate
  Decision Owner may still proceed if the rationale is documented.
audit_reopen_rule: >
  PMO audit findings may reopen a passed gate only when a material completeness
  failure or material control failure is discovered.
```

### 2.11 Blocker, risk, and open-issue handling model

This section defines the blocker, risk, and open-issue handling model for the framework.

#### 2.11.1 Canonical tracking model

The framework MUST use one canonical **Open Items Register** for every initiative.

The Open Items Register:
1. MUST exist for every initiative no later than Gate 2, even if empty or near-empty
2. MUST be the authoritative place for tracking unresolved blockers, risks, issues, assumptions, and dependencies
3. MUST use a single table or equivalent single register structure with typed entries
4. MUST NOT be replaced by separate RAID tables, ad hoc action logs, meeting notes, or artifact margin comments

The allowed entry types are:
1. `blocker`
2. `risk`
3. `issue`
4. `assumption`
5. `dependency`

All item types are valid across the lifecycle, but gate reviewers and Gate Decision Owners MUST interpret them according to stage-specific expectations and gate meaning.

#### 2.11.2 Status model

The standard lifecycle statuses for Open Items Register entries are:
1. `open` — identified, recorded, and assigned, but active response has not yet materially started
2. `in progress` — active work is underway to resolve, reduce, clarify, or decide the item
3. `monitoring` — the item remains unresolved, but observation is the chosen control strategy for now
4. `resolved` — the underlying condition has been dealt with in substance, but formal confirmation or closure is still pending where required
5. `closed` — the item has completed its lifecycle in the register and requires no further action, monitoring, or decision

`Monitoring` is not the default state for all unresolved items. It indicates a conscious decision that watchful observation is the correct current treatment.

#### 2.11.3 Ownership and closure authority

Every open-item entry MUST have one named item owner.

The item owner is responsible for:
1. maintaining the entry
2. driving or coordinating next actions
3. monitoring watch conditions where the status is `monitoring`
4. escalating the item when escalation rules are triggered

Closure authority is separated from day-to-day ownership:
1. the item owner MAY propose resolution or closure
2. closure of a non-blocking item that materially affects progression MUST be confirmed by the relevant accountable owner (typically the Delivery Owner or relevant functional owner)
3. closure of a blocker affecting a gate MUST be confirmed by the named Gate Decision Owner for that gate

#### 2.11.4 Blocker rules and gate effects

`Blocker` is a first-class item type.

At gate passage:
1. any open `blocker` affecting the current gate forces gate failure
2. open non-blocker items (`risk`, `issue`, `assumption`, `dependency`) MAY remain only if they satisfy the controlled-open-item rule already defined in Section 2.6.5
3. if a non-blocker item becomes gate-disqualifying, it MUST be reclassified or recorded as a `blocker` entry before the gate decision is finalized

When a blocker arises from another item type, the blocker entry MUST reference the originating item so the escalation path remains traceable.

#### 2.11.5 Minimum entry fields

Every Open Items Register entry MUST include at least:
1. `id`
2. `type`
3. `title`
4. `description`
5. `owner`
6. `status`
7. `affected_stage_or_gate`
8. `impact_summary`
9. `next_action`
10. `target_resolution_or_decision_date`
11. `created_date`
12. `last_updated_date`

The following are conditionally required:
1. `resolution_note` when the status is `resolved` or `closed`
2. `origin_reference` when a blocker arose from another open item

Projects MAY add local fields, but they MUST NOT remove or rename the canonical minimum fields.

#### 2.11.6 Escalation rules

Escalation is mandatory, not optional, when any of the following is true:
1. an item is classified as a `blocker`
2. an item is overdue against its target resolution or decision date
3. an item has no valid owner
4. an item has no valid next action
5. an item credibly threatens an upcoming gate's mandatory pass conditions

Escalation handling rules:
1. any `blocker` MUST be escalated immediately to the relevant Gate Decision Owner
2. a non-blocker item that meets an escalation trigger MUST be escalated to the Delivery Owner and, where progression is affected, to the relevant Gate Decision Owner
3. escalation outcomes that contain a material decision or stop/proceed determination MUST be recorded in the Decision Log
4. PMO intervention follows the escalation and dispute rules already defined in Section 2.10

#### 2.11.7 Boundary with the Decision Log

The Open Items Register and Decision Log have distinct purposes.

The Open Items Register answers:
1. what unresolved items exist
2. what type each item is
3. who owns it
4. what its current status and next action are

The Decision Log answers:
1. what formal decision was made
2. who made it
3. why it was made
4. what implications it carries

The framework therefore requires strict separation:
1. the Open Items Register tracks the lifecycle of unresolved items
2. the Decision Log records formal decisions such as blocker reclassification, escalation outcomes, explicit proceed decisions with bounded open items, scope/risk treatment decisions, and accepted deviations
3. teams MUST NOT treat register updates as a substitute for recording a formal decision when one has been made

#### 2.11.8 Machine-consumable open-items model (YAML)

```yaml
kind: control_model
id: CONTROL-MODEL-OPEN-ITEMS
name: Open Items Register and Blocker Handling Model
canonical_artifact: ARTIFACT-OPEN-ITEMS-REGISTER
entry_types:
  - blocker
  - risk
  - issue
  - assumption
  - dependency
statuses:
  - open
  - in progress
  - monitoring
  - resolved
  - closed
gate_rules:
  blocker_rule: >
    Any open blocker affecting the current gate forces gate failure.
  controlled_open_item_rule: >
    Open non-blocker items may remain only if they are explicitly managed,
    owned, actionable, and do not invalidate the gate's mandatory pass
    conditions.
  reclassification_rule: >
    A gate-disqualifying non-blocker item must be reclassified or recorded as
    a blocker before the gate decision is finalized.
escalation_triggers:
  - blocker
  - overdue_target_date
  - missing_owner
  - missing_next_action
  - upcoming_gate_threat
decision_log_boundary:
  register_tracks: unresolved_item_lifecycle
  decision_log_tracks: formal_decisions_and_rationale
```

### 2.12 AI-agent sufficiency standard

This section defines the AI-agent sufficiency standard used by the framework.

#### 2.12.1 Standard type and control model

The framework adopts a **human-plus** AI-agent sufficiency standard.

This means:
1. required artifacts and gates MUST remain reviewable and enforceable by humans
2. required artifacts and gates MUST also satisfy additional precision, structure, and explicitness rules needed for reliable AI-assisted downstream use
3. AI sufficiency is not a parallel advisory check; it is a required sub-dimension of completeness

If a required artifact or gate is human-usable but fails a mandatory AI-sufficiency check, it fails completeness.

#### 2.12.2 Scope of application

The AI-agent sufficiency standard applies to:
1. all required artifacts
2. all gate decisions and gate review records
3. all normative framework content used to define how the framework operates

This includes all in-scope planned software initiatives.

#### 2.12.3 Canonical AI-sufficiency checklist

Every required artifact and gate MUST satisfy the following baseline checklist:

1. **Explicit meaning** — material requirements, responsibilities, and constraints are stated directly rather than implied through tribal knowledge or unstated context.
2. **Terminological stability** — the same concept uses the same term throughout, or any alias is explicitly mapped.
3. **Reference clarity** — pronouns, shorthand, and cross-references are specific enough that a reader or agent can determine exactly what is being referenced.
4. **Scope boundedness** — in-scope, out-of-scope, exclusions, assumptions, and constraints are explicit where relevant.
5. **Decision visibility** — settled decisions, open decisions, constraints, and unresolved items are explicitly marked rather than buried in prose.
6. **Traceability** — materially traceable items such as requirements, acceptance criteria, decisions, and open items can be linked to stable identifiers, numbered sections, or equivalent explicit references.
7. **Structural parseability** — the artifact uses consistent headings, lists, tables, and machine-readable blocks where the framework expects structured extraction.
8. **Cross-artifact consistency** — the artifact does not materially conflict with other required artifacts in a way that would force interpretation by the reader or agent.
9. **Actionability for the next consumer** — the intended downstream consumer can act without inventing missing business meaning.
10. **Target-state explicitness** — the artifact makes explicit what acceptable or good output looks like for the next consumer, using observable outcome descriptions, acceptance patterns, or equivalent target-state language.
11. **Controlled unknowns only** — remaining unknowns are explicitly bounded and linked to the Open Items Register rather than left as stray placeholders.
12. **Explicit actor/action/object language** — normative statements identify who does what to what wherever that distinction materially affects execution or accountability.
13. **External-reference discipline** — any material external source, policy, system, standard, or document is explicitly identified in a retrievable way and its relevance is stated.

#### 2.12.4 Traceability and numbering rules

To support human and AI referenceability:
1. normative and reference-bearing documents SHOULD use numbered headings, sections, and subsections by default
2. materially traceable items inside artifacts MUST use stable local identifiers or equivalent explicit references
3. numbered lists SHOULD be used for normative rules, criteria, and ordered sequences where exact reference matters

Framework implementations and downstream templates MUST preserve these traceability properties even if formatting differs.

#### 2.12.5 Immediate AI-sufficiency fail patterns

The following are immediate AI-sufficiency failure conditions when material to meaning:
1. unresolved `TBD`, `TBC`, or equivalent placeholder text that is not explicitly controlled through the Open Items Register
2. contradictory statements across required artifacts
3. undefined terms, acronyms, or role labels that materially affect interpretation
4. references to external context, prior discussions, or informal knowledge that are not explicitly identified and referenceable
5. acceptance criteria, target-state descriptions, or normative expectations that are too vague to observe or apply
6. materially traceable content that cannot be referenced precisely because identifiers, numbering, or equivalent structure are missing

#### 2.12.6 Controlled unknowns rule

Unknowns are allowed only when controlled.

This means:
1. a remaining unknown MUST be explicit
2. it MUST be bounded enough that the reader can understand what is not yet known
3. it MUST be linked to the Open Items Register with ownership and next action
4. it MUST NOT invalidate the current gate's mandatory pass conditions

Stray placeholders or vague future-tense statements are not acceptable substitutes for controlled unknowns.

#### 2.12.7 Review and reporting rule

AI sufficiency is reviewed through the existing completeness model, not through a separate control track.

Review outputs therefore MUST:
1. identify the specific failed AI-sufficiency checklist item(s) when applicable
2. explicitly label the outcome as an **AI-sufficiency failure** when one or more mandatory AI-sufficiency checks fail
3. avoid passing an artifact or gate on the basis that a human reviewer could probably infer the missing meaning

#### 2.12.8 Machine-consumable AI-sufficiency model (YAML)

```yaml
kind: quality_model
id: QUALITY-MODEL-AI-SUFFICIENCY
name: AI-Agent Sufficiency Standard
standard_type: human_plus
integrated_with_completeness: true
applies_to:
  - all_required_artifacts
  - all_gate_decisions
  - normative_framework_content
mandatory_checks:
  - explicit_meaning
  - terminological_stability
  - reference_clarity
  - scope_boundedness
  - decision_visibility
  - traceability
  - structural_parseability
  - cross_artifact_consistency
  - actionability_for_next_consumer
  - target_state_explicitness
  - controlled_unknowns_only
  - explicit_actor_action_object_language
  - external_reference_discipline
immediate_fail_patterns:
  - uncontrolled_placeholder
  - cross_artifact_contradiction
  - undefined_material_term
  - unreferenceable_external_context
  - vague_acceptance_or_target_state
  - missing_material_traceability
reporting_rule: >
  When one or more mandatory AI-sufficiency checks fail, the review output
  must explicitly label the result as an AI-sufficiency failure.
```

### 2.13 Anti-bureaucracy guardrails

This section converts the framework's anti-bureaucracy intent into enforceable rules.

#### 2.13.1 Core principle

The framework MUST minimize overhead by design, but it MUST NOT allow teams to bypass controls that preserve delivery readiness, traceability, ownership clarity, or downstream executability/supportability.

Anti-bureaucracy is achieved by:
1. using the scaling model to keep evidence proportionate to the initiative
2. defining optional and conditional artifacts explicitly
3. allowing only controlled omission of non-core items

Anti-bureaucracy is **not** achieved by ad hoc skipping of required controls.

#### 2.13.2 Non-waivable core controls

The following controls are non-waivable:
1. All formal gates defined by the framework
2. A named Gate Decision Owner for every gate
3. The required primary artifact for the initiative path
4. The `Decision Log`
5. The `Open Items Register`
6. Any conditional artifact whose trigger condition is true

No project, reviewer, or Delivery Owner may waive these controls under the banner of speed or practicality.

#### 2.13.3 What may be omitted

Only non-core items may be omitted, and only when the framework explicitly makes them optional, conditional, discretionary, or packaging-flexible.

Examples of potentially omittable non-core items include:
1. conditional artifacts whose trigger conditions are not true
2. duplicated sections or repeated content that can be consolidated without loss of meaning
3. artifact-local presentation choices that do not change the required content, ownership visibility, or gate evidence

If the framework does not explicitly allow an item to be optional, conditional, discretionary, or packaging-flexible, teams MUST treat it as required.

#### 2.13.4 Omission / waiver test

A non-core item may be omitted only when the omission does **not** reduce any of the following:
1. completeness against the framework's readiness model
2. decision traceability
3. ownership clarity
4. downstream executability
5. downstream supportability

If omission weakens any of those outcomes, the omission is not permitted.

#### 2.13.5 Approval model

The framework uses a structured approval model for non-core omissions:
1. The Delivery Owner may approve omission of explicitly waivable non-core items when the required rationale is documented.
2. PMO review is required before omission is approved when the omission affects:
   - gate evidence
   - cross-team coordination
   - external delivery controls
   - security, privacy, or compliance assurance

PMO review for these cases is a control requirement, not an optional escalation path.

#### 2.13.6 Recording rule

Every approved omission or waiver decision MUST be recorded canonically in the `Decision Log`.

When the omission affects a specific artifact or gate review, the affected artifact or review record SHOULD reference the corresponding `Decision Log` entry so auditors and downstream teams can trace the rationale from either direction.

Unrecorded omissions are invalid for framework purposes, even if they were discussed informally.

#### 2.13.7 Machine-consumable anti-bureaucracy model (YAML)

```yaml
kind: policy
id: POLICY-ANTI-BUREAUCRACY
name: Anti-Bureaucracy Guardrail
non_waivable_core_controls:
  - all_formal_gates
  - named_gate_decision_owner
  - required_primary_artifact
  - decision_log
  - open_items_register
  - triggered_conditional_artifacts
omission_allowed_only_when:
  - item_is_explicitly_optional_or_conditional_or_discretionary_or_packaging_flexible
  - omission_does_not_reduce_completeness
  - omission_does_not_reduce_traceability
  - omission_does_not_reduce_ownership_clarity
  - omission_does_not_reduce_downstream_executability
  - omission_does_not_reduce_downstream_supportability
delivery_owner_may_approve:
  - explicitly_waivable_non_core_items
pmo_review_required_when_affecting:
  - gate_evidence
  - cross_team_coordination
  - external_delivery_controls
  - security_privacy_compliance_assurance
recording_system:
  canonical_record: ARTIFACT-DECISION-LOG
  local_reference_when_relevant: true
```

### 2.14 Critical stage-defining artifact mapping

This section defines the canonical gate-to-critical-artifact mapping rules for the framework.

#### 2.14.1 Mapping philosophy

The framework uses a rule-based mapping model:
1. each gate has a canonical base critical set
2. triggered conditional artifacts become gate-critical only when their absence would invalidate that gate's mandatory pass conditions
3. some control artifacts remain persistently gate-critical from Gate 2 onward
4. where a gate has no dedicated standalone artifact for part of its evidence, the required evidence may be embedded in the persistent artifacts, triggered artifacts, or the formal gate review/decision record

Critical mapping is therefore not a flat list. It is a combination of:
1. persistent control artifacts
2. gate-specific artifacts
3. triggered conditional artifacts
4. explicitly elevated project-specific deliverables when the primary definition artifact ties them to a gate
5. embedded gate evidence where no standalone artifact exists

#### 2.14.2 Persistent critical artifacts

From Gate 2 onward, the following artifacts are persistently gate-critical:
1. `ARTIFACT-PROJECT-BRIEF`
2. `ARTIFACT-DECISION-LOG`
3. `ARTIFACT-OPEN-ITEMS-REGISTER`

These artifacts remain critical through Closure because later gates must still be judged against the bounded scope, intended outcomes, decision history, and open-item status established earlier.

#### 2.14.3 Project-specific deliverable elevation rule

1. The `Initiative Definition / Project Brief` is the base primary artifact at all applicable gates.
2. A project-specific deliverable becomes gate-critical only when the `Initiative Definition / Project Brief` explicitly ties that deliverable to a named gate.
3. A project-specific deliverable mentioned in the `Initiative Definition / Project Brief` does not become gate-critical merely because it is listed as a deliverable; the gate tie MUST be explicit.

#### 2.14.4 Conditional-artifact criticality rule

A triggered conditional artifact becomes gate-critical at the gate where its absence would invalidate that gate's mandatory pass conditions.

This means:
1. a conditional artifact may be required by one gate and still remain critical at a later gate if its contents remain necessary for the later stop/proceed decision
2. a conditional artifact does not become gate-critical merely because it exists; it becomes gate-critical when the current gate depends on it materially

#### 2.14.5 Gate-by-gate canonical mapping

1. **Gate 1 (`Qualified Request`)**
   - Base critical artifact: `ARTIFACT-REQUEST-INTAKE-RECORD`
   - No `Project Brief` is required yet.

2. **Gate 2 (`Initiative Defined`)**
   - Base critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`

3. **Gate 3 (`Authorized`)**
   - Gate-specific critical artifact:
     - `ARTIFACT-PROJECT-CHARTER`
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - `Project Charter` is the only gate-specific critical artifact at Gate 3; persistent controls still apply.

4. **Gate 4 (`Specification Complete`)**
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - Gate-critical conditional artifacts when triggered and materially required:
     - `ARTIFACT-DELIVERY-CHARTER`
     - `ARTIFACT-TDD`
     - `ARTIFACT-API-CONTRACT-SPEC`
     - `ARTIFACT-DATA-ASSET-SPEC`
     - `ARTIFACT-DATA-MIGRATION-PLAN`
     - `ARTIFACT-ACCESS-MODEL`
     - `ARTIFACT-SECURITY-PRIVACY-RIA`
   - Required explicit evidence may be embedded in the primary artifact set where no separate standalone artifact exists.

5. **Gate 5 (`MVP Identified`)**
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - Gate-critical conditional artifacts when triggered and materially required for MVP feasibility:
     - any Gate 4 conditional artifact whose absence would invalidate MVP definition or feasibility
   - Explicit MVP evidence (scope, success measures, acceptance criteria) MUST exist in the primary artifact set and/or formal gate review record.
   - The `Initiative Definition / Project Brief` may elevate named project deliverables to Gate 5 criticality only through an explicit gate tie.

6. **Gate 6 (`All Deliverables Accepted`)**
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - Gate-critical conditional artifacts when triggered and materially required for acceptance:
     - `ARTIFACT-DEPLOYMENT-GUIDE`
     - `ARTIFACT-USER-ADOPTION-PLAN`
     - `ARTIFACT-DELIVERY-CHARTER` where external-delivery obligations materially affect acceptance
      - any project-specific deliverable explicitly tied to Gate 6 in the `Initiative Definition / Project Brief`
   - Explicit acceptance evidence against the defined acceptance criteria MUST exist in the formal gate review/decision record and reference the relevant artifacts or deliverables.

7. **Gate 7 (`Transition Complete`)**
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - Gate-critical conditional artifacts when triggered and materially required for supported operation:
     - `ARTIFACT-DEPLOYMENT-GUIDE`
     - `ARTIFACT-USER-ADOPTION-PLAN`
     - `ARTIFACT-DELIVERY-CHARTER` where external transition responsibilities materially affect operating-state acceptance
      - any project-specific deliverable explicitly tied to Gate 7 in the `Initiative Definition / Project Brief`
   - Explicit supportability and transition evidence MUST exist in the formal gate review/decision record and/or the triggered operational artifacts.

8. **Gate 8 (`Closure Complete`)**
   - Gate-specific critical artifact:
     - `ARTIFACT-CLOSURE-RECORD`
   - Persistent critical artifacts:
      - `ARTIFACT-PROJECT-BRIEF`
     - `ARTIFACT-DECISION-LOG`
     - `ARTIFACT-OPEN-ITEMS-REGISTER`
   - `Closure Record` is the universal closure artifact for the framework and is always required by Gate 8.

#### 2.14.6 Machine-consumable gate-mapping rules (YAML)

```yaml
kind: gate_mapping
id: RULE-GATE-1-CRITICAL-ARTIFACTS
gate_id: GATE-QUALIFIED-REQUEST
base_critical_artifacts:
  - ARTIFACT-REQUEST-INTAKE-RECORD
```

```yaml
kind: gate_mapping
id: RULE-GATE-2-CRITICAL-ARTIFACTS
gate_id: GATE-INITIATIVE-DEFINED
base_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
```

```yaml
kind: gate_mapping
id: RULE-GATE-3-CRITICAL-ARTIFACTS
gate_id: GATE-AUTHORIZED
gate_specific_artifacts:
  - ARTIFACT-PROJECT-CHARTER
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
```

```yaml
kind: gate_mapping
id: RULE-GATE-4-CRITICAL-ARTIFACTS
gate_id: GATE-SPECIFICATION-COMPLETE
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
conditional_artifacts_become_critical_when_gate_invalidated:
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-TDD
  - ARTIFACT-API-CONTRACT-SPEC
  - ARTIFACT-DATA-ASSET-SPEC
  - ARTIFACT-DATA-MIGRATION-PLAN
  - ARTIFACT-ACCESS-MODEL
  - ARTIFACT-SECURITY-PRIVACY-RIA
embedded_evidence_required: true
```

```yaml
kind: gate_mapping
id: RULE-GATE-5-CRITICAL-ARTIFACTS
gate_id: GATE-MVP-IDENTIFIED
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
conditional_artifacts_become_critical_when_gate_invalidated:
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-TDD
  - ARTIFACT-API-CONTRACT-SPEC
  - ARTIFACT-DATA-ASSET-SPEC
  - ARTIFACT-DATA-MIGRATION-PLAN
  - ARTIFACT-ACCESS-MODEL
  - ARTIFACT-SECURITY-PRIVACY-RIA
project_brief_may_elevate_gate_specific_deliverables: true
embedded_evidence_required: true
```

```yaml
kind: gate_mapping
id: RULE-GATE-6-CRITICAL-ARTIFACTS
gate_id: GATE-DELIVERABLES-ACCEPTED
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
conditional_artifacts_become_critical_when_gate_invalidated:
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-DEPLOYMENT-GUIDE
  - ARTIFACT-USER-ADOPTION-PLAN
project_brief_may_elevate_gate_specific_deliverables: true
embedded_evidence_required: true
```

```yaml
kind: gate_mapping
id: RULE-GATE-7-CRITICAL-ARTIFACTS
gate_id: GATE-TRANSITION-COMPLETE
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
conditional_artifacts_become_critical_when_gate_invalidated:
  - ARTIFACT-DELIVERY-CHARTER
  - ARTIFACT-DEPLOYMENT-GUIDE
  - ARTIFACT-USER-ADOPTION-PLAN
project_brief_may_elevate_gate_specific_deliverables: true
embedded_evidence_required: true
```

```yaml
kind: gate_mapping
id: RULE-GATE-8-CRITICAL-ARTIFACTS
gate_id: GATE-CLOSURE-COMPLETE
gate_specific_artifacts:
  - ARTIFACT-CLOSURE-RECORD
persistent_critical_artifacts:
  - ARTIFACT-PROJECT-BRIEF
  - ARTIFACT-DECISION-LOG
  - ARTIFACT-OPEN-ITEMS-REGISTER
```

## 3. Explicit Non-Behaviors

1. The system must not add bureaucracy for its own sake because extra process that does not improve delivery quality weakens adoption and slows execution.
2. The system must not require unnecessary work that is unrelated to delivering the project because the purpose of the framework is delivery readiness, not procedural compliance.
3. The system must not produce code because its role is to define work and delivery expectations, not to implement the solution.
4. The system must not allow work to proceed on incomplete or unclear inputs because downstream teams would be forced to guess or redefine requirements.
5. The system must not treat document presence as proof of completeness because a filled template can still hide critical gaps.
6. The system must not allow teams to substitute local interpretation for explicit specification because the framework is intended to reduce inconsistent delivery behavior.
7. The system must not assume that technically correct delivery is sufficient if supportability, maintainability, or operational readiness are undefined because the outcome would be incomplete in practice.
8. The system must not optimize only for human readers if AI agents are expected consumers because ambiguity tolerated by people can cause agent failure or hallucinated requirements.

## 4. Integration Boundaries

### 4.1 External systems currently in scope

No external software systems, APIs, databases, auth systems, or third-party services are currently defined as part of this framework.

### 4.2 Current operating boundary

The framework currently operates as a standalone knowledge and delivery-definition system. Its primary inputs and outputs are human-authored project information and framework-defined delivery artifacts rather than machine-to-machine integrations.

### 4.3 Data flowing in

1. New business requests
2. Project context
3. Business rules
4. Requirements
5. Constraints
6. Dependencies
7. Acceptance criteria
8. Delivery expectations
9. Support and maintenance expectations
10. Vendor engagement context where applicable, including expected external engagement mode when known

**Minimum request entry payload (Intake entry readiness)**
A request may enter Intake even if it is not yet confirmed in-scope. The purpose of Intake entry is to create a tracked item with an accountable triage owner and to schedule an initial clarification session.

**Required at entry**
1. Requester name
2. Short description that includes:
   - Background / problem / opportunity
   - Desired outcome
   - Success measures (allowed to be explicitly "Unknown/TBD" at entry)
   - Affected systems / processes (allowed to be explicitly "Unknown/TBD" at entry)

**Required operational actions at entry**
1. Assign a triage owner immediately (provisional ownership is allowed).
2. Perform an initial clarification session as part of the initial assessment.

**Entry rejection conditions**
1. Requester name is missing.
2. Short description is missing background / problem / opportunity, or missing desired outcome.
### 4.4 Data flowing out

1. Project documentation
2. Solution definition artifacts
3. Delivery approach documentation
4. Support and maintenance documentation
5. External team handoff documentation where applicable
6. Documentation sufficient for internal teams or AI agents to derive build specifications and delivery plans

### 4.5 Expected contract

Because no external system contract has been defined, the current contract is behavioral rather than technical:

1. Inputs must be clear enough to define what “good” and “complete” mean for the project.
2. Outputs must be specific enough that downstream delivery teams can proceed without redefining business intent.
3. Blockers, missing dependencies, and unresolved questions must be explicitly documented.
4. Work must not be marked ready when hidden assumptions remain.

### 4.6 When external systems are unavailable or return unexpected data

Not applicable as currently specified. No system integrations have been declared.

### 4.7 Real service vs simulated twin during development

Not applicable as currently specified. No external service dependencies have been declared.

## 5. Behavioral Scenarios

These scenarios are intended for external evaluation of the framework’s outcomes. They should be used by reviewers to assess whether the framework works in practice, not by an implementation agent as internal development guidance.

### 5.1 Happy-path scenario 1: Greenfield project reaches delivery-ready definition

**Setup conditions**
1. A new internal software project request is received.
2. Required stakeholders are available.
3. Business objectives and constraints are known.

**Actions**
1. A delivery manager and internal team enter the framework.
2. They follow the framework from request intake through documentation production.
3. They produce the required solution, delivery, and support artifacts.

**Expected observable outcomes**
1. A reviewer can identify the proposed solution, delivery approach, support expectations, and acceptance criteria from the resulting documentation.
2. An engineering team can explain what needs to be built without redefining the business problem.
3. The documentation contains enough detail for technical specifications and delivery planning to proceed without requesting foundational clarification.

### 5.2 Happy-path scenario 2: External development team receives a usable handoff

**Setup conditions**
1. A project will be delivered by an external development team.
2. Stakeholders have provided the needed business context and objectives.

**Actions**
1. The internal team uses the framework to prepare the project documentation and external handoff pack.
2. The handoff is given to an independent delivery reviewer acting as the external team.

**Expected observable outcomes**
1. The reviewer can state what the external team is expected to build, how success will be judged, and what support expectations exist after delivery.
2. The reviewer does not need undocumented tribal knowledge to understand the assignment.
3. The reviewer can identify what is in scope and what is not in scope from the artifacts alone.

### 5.3 Happy-path scenario 3: AI-assisted delivery can proceed without requirement redefinition

**Setup conditions**
1. A project is intended to be delivered with material AI-agent participation.
2. The business request includes rules and intended outcomes.

**Actions**
1. The framework is used to define the project and produce its documentation.
2. A separate evaluator reviews the documentation from the perspective of an AI-enabled engineering team.

**Expected observable outcomes**
1. The evaluator can derive build specifications or implementation plans from the documentation without inventing missing business rules.
2. Acceptance criteria are expressed in a way that allows observable validation rather than subjective interpretation.
3. The evaluator finds no critical area where the only path forward is to guess what the business intended.

### 5.4 Error scenario 1: Missing dependency blocks progression

**Setup conditions**
1. A business request exists, but a required dependency or decision is unavailable or unclear.

**Actions**
1. The team begins using the framework.
2. During definition, they discover the missing dependency.

**Expected observable outcomes**
1. The missing dependency is explicitly documented.
2. The issue is visible as a blocker requiring stakeholder resolution.
3. The work is not marked ready to proceed.
4. No artifact falsely presents the project as complete.

### 5.5 Error scenario 2: Documentation looks finished but hides critical gaps

**Setup conditions**
1. A team has completed the framework artifacts.
2. The artifacts are formatted well and appear complete on first review.

**Actions**
1. An independent engineering reviewer attempts to derive technical specifications from the documentation.
2. The reviewer checks whether assumptions are required to continue.

**Expected observable outcomes**
1. If critical business logic, constraints, support expectations, or acceptance conditions are missing, the framework evaluation fails the documentation.
2. The output is judged incomplete even though documents exist.
3. The gaps are surfaced explicitly rather than being absorbed into downstream interpretation.

### 5.6 Edge-case scenario 1: Small request with pressure to over-document

**Setup conditions**
1. A relatively small change request is raised.
2. Team members are concerned the framework may force unnecessary work.

**Actions**
1. The team applies the framework to the request.
2. A reviewer compares the produced outputs with the actual delivery need.

**Expected observable outcomes**
1. The documentation is sufficient to make the work buildable and supportable.
2. The framework does not require obviously irrelevant or non-value-adding outputs merely to satisfy process formality.
3. Any omitted non-core item is explicitly justified and recorded rather than skipped informally.
4. Reviewers conclude that the framework supported delivery readiness without adding avoidable bureaucracy or waiving core controls.

### 5.7 Edge-case scenario 2: Large multi-team initiative with long-term support needs

**Setup conditions**
1. A complex enterprise initiative spans multiple internal teams and has long-term operational impact.

**Actions**
1. The framework is applied across the initiative.
2. Multiple teams review the resulting documentation independently.

**Expected observable outcomes**
1. Teams can align on the intended solution and delivery shape from the same documentation set.
2. Supportability and maintainability expectations are visible, not implied.
3. Reviewers judge the artifacts sufficient for coordinated downstream planning across teams without conflicting interpretations of core requirements.

## 6. Implementation Constraints

1. The implementation must remain minimal and avoid adding process overhead that does not improve delivery readiness, using the anti-bureaucracy control model in Section 2.13.
2. The implementation must be suitable for human teams and AI-agent consumers.
3. The implementation must support complex enterprise and large multi-team initiatives.
4. No software integrations are currently required.
5. No code generation or solution implementation is in scope.
