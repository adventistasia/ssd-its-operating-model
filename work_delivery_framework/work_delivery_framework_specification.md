# Work Delivery Framework Specification

## 1. System Overview

This framework defines how internal teams, the PMO, delivery managers, and internal engineers turn a new business request into delivery-ready project documentation. Its purpose is to produce complete, unambiguous, buildable, supportable specifications that are sufficient for internal human teams, external development teams, or AI agents to deliver work without redefining the problem during execution.

The framework exists to make “good” and “complete” explicit while avoiding unnecessary process overhead for its own sake.

### 1.1 Scope of applicability

The framework is optimized for software initiatives.

**In scope**
1. Greenfield software projects
2. Brownfield software projects

**Out of scope**
1. Minor low-risk changes
2. Research spikes
3. Support work
4. Small internal process changes

**Conditionally in scope**
1. Complex operational changes affecting multiple organizations
2. Complex internal process changes affecting the whole organization
3. Non-software initiatives that can use the framework with minimum changes

Conditional use does not make this a general enterprise change framework by default. The default design target remains software project delivery.
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

### 2.4 Lifecycle stages, progression gates, and exit criteria (resolved)

The framework lifecycle is defined as a sequence of formal stages with explicit progression gates. A project MAY be blocked at any gate if the required evidence is missing or ambiguity remains unresolved.

**Important boundary note**
Stages and gates define the control model. The canonical artifact taxonomy is now defined (see Section 2.5). Scaling thresholds for “small vs large work” are now resolved (see Section 2.7, Ambiguity A09).

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
   - Authorization applicability is now informed by the scaling model (see Section 2.7). For small-work, Authorization is typically “Not Required” since requiring an approved budget would already trigger large-work classification. For large-work, the Gate Decision Owner must declare Authorization as “Required” or “Not Required” at Gate 2.
5. Solution Definition ends at Gate 4 (Specification Complete).
6. Planning / Mobilization / MVP Plan ends at Gate 5 (MVP Identified).
7. Delivery / Execution ends at Gate 6 (All Deliverables Accepted).
8. Handoff / Transition ends at Gate 7 (Transition Complete).
9. Closure ends at Gate 8 (Closure Complete).

**Minimum evidence categories by gate (high-level)**
1. Gate 1 (Qualified Request): in-scope determination; threshold determination (if applicable); accountable Delivery Owner assigned; initial stakeholder list; known unknowns captured.
2. Gate 2 (Initiative Defined): bounded scope; desired outcomes and success measures; major constraints and dependencies; initial solution direction; estimated effort/shape at an appropriate level; decision on whether Authorization is required.
3. Gate 3 (Authorized): explicit business authorization to invest resources; budget/resource commitment (as applicable); funding/priority decision recorded; Gate Decision Owner named.
4. Gate 4 (Specification Complete): solution definition is complete enough for downstream planning and task breakdown without inventing business requirements; acceptance criteria are defined; critical risks/unknowns are either resolved or explicitly managed as open issues.
5. Gate 5 (MVP Identified): MVP scope is defined; MVP success measures and MVP acceptance criteria are explicit and approved; delivery approach is feasible with the current team and constraints.
6. Gate 6 (All Deliverables Accepted): delivered solution is accepted by the named Acceptance Owner against the specified acceptance criteria; any deviations are explicitly approved and recorded.
7. Gate 7 (Transition Complete): operating ownership is established; support model is ready; transition activities are complete; the solution is in a supported operating state.
8. Gate 8 (Closure Complete): closure requirements are satisfied (final acceptance evidence present, transition complete, decision log updated, outcomes recorded, and closure rationale documented).

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
  - TBD-DEFERRED-TO-A17
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
immediate_fail_conditions:
  - Critical ambiguity remains unresolved
  - Authorization requirement cannot be decided due to missing information
minimum_qualitative_threshold: adequate
critical_stage_defining_artifacts:
  - TBD-DEFERRED-TO-A17
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
  - TBD-DEFERRED-TO-A17
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
immediate_fail_conditions:
  - Downstream delivery would require inventing business requirements
minimum_qualitative_threshold: strong
critical_stage_defining_artifacts:
  - TBD-DEFERRED-TO-A17
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
  - TBD-DEFERRED-TO-A17
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
  - TBD-DEFERRED-TO-A17
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
  - TBD-DEFERRED-TO-A17
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
  - TBD-DEFERRED-TO-A17
default_decision_owner_role: PMO / ITS Director
requires_named_decision_owner: true
decision_rights: []
```

### 2.5 Required artifact taxonomy (resolved)

This section defines the canonical artifact taxonomy for this framework (Ambiguity A06).

#### 2.5.1 Category labels vs artifacts

Some labels in this framework are **category labels** rather than artifacts. Category labels are used to organize thinking and required content, but do not imply a mandatory standalone file.

The following are category labels (not artifacts):
1. Project Governance
2. Solution Design
3. DevOps & Support
4. User Adoption

#### 2.5.2 Packaging model: small-work packet vs large-work artifact set

The framework supports two packaging modes:
1. **Small work:** one packet artifact called **Work Brief**.
2. **Large work:** separate canonical artifacts (files) as defined in this section.

**Important note (scaling resolved):**
The thresholds for “small vs large work” and formal tiering are now defined (see Section 2.7, Ambiguity A09). The Delivery Owner MUST classify the project as small-work or large-work no later than Gate 2.

Both names MUST exist:
- **Work Brief** is the small-work form.
- **Initiative Definition / Project Brief** is the large-work form.

#### 2.5.3 Canonical artifacts (names, triggers, and required-by gates)

**Always required**
1. Initiative Definition / Project Brief (large-work mode) **OR** Work Brief (small-work mode) — required by **Gate 2**
2. Decision Log — must exist for every initiative and must exist no later than **Gate 2**
3. Open Items Register — must exist for every initiative and must exist no later than **Gate 2**

**Conditional artifacts (trigger → artifact(s) → required-by gate)**
1. External vendor involved → Delivery Charter → **Gate 4** (or **Gate 3** when early delivery-team commitment is required)
2. Authorization required → Approved Project Charter → **Gate 3**
3. Material ops/support impact → Technical Design Document (TDD) + Deployment Guide → TDD by **Gate 4**, Deployment Guide by **Gate 6**
4. Data migration → Data Asset Specification + Data Migration Plan → **Gate 4**
5. Security/compliance impact → Access Model + Security/Privacy Risk Impact Assessment → **Gate 4**
6. New integration / API change → API/Contract Specification → **Gate 4**
7. Customer-facing change → User Adoption Plan → start between **Gate 4** and **Gate 6** (earlier is better); must be complete no later than **Gate 6**

**Filename guidance**
Artifact names are canonical. Exact filenames are not enforced, but projects are strongly encouraged to use the canonical artifact names as filenames to support consistent discovery and audit.

**Framework evolution note**
The artifact set is expected to evolve as the framework is made clearer. Changes MUST be applied by updating this specification’s artifact definitions (including the machine-consumable YAML blocks) rather than introducing parallel shadow taxonomies.

#### 2.5.4 Machine-consumable artifact model (YAML)

```yaml
kind: artifact
id: ARTIFACT-WORK-BRIEF
name: Work Brief
packaging_mode: packet
required_by_gate: GATE-INITIATIVE-DEFINED
purpose: Consolidated packet for small-work initiatives that captures the minimum business, delivery, and operational definition needed to decide whether the initiative is sufficiently defined to proceed.
required_contents:
  - Background / problem / opportunity
  - Desired outcome
  - Success measures (allowed: explicitly Unknown/TBD at entry)
  - Affected systems / processes (allowed: explicitly Unknown/TBD at entry)
  - In-scope statement and scope boundaries
  - Stakeholders and owners (including Gate Decision Owner assignments)
  - Constraints, dependencies, and known unknowns (explicit TBD allowed where appropriate)
  - Functional requirements and use cases (as applicable)
  - User roles (as applicable)
  - Business rules (as applicable)
  - Delivery approach (high-level)
  - Support and operational considerations (if applicable)
  - User adoption considerations (if applicable)
artifact_specific_completeness_rules:
  - Scope boundaries, desired outcome, and key constraints are explicit enough to determine whether the work is bounded.
  - The packet is internally coherent across business need, scope, delivery approach, and operating implications.
  - Unknowns are explicitly marked rather than implied or omitted.
common_failure_conditions:
  - The packet mixes multiple plausible interpretations of the work without resolving or exposing them.
  - A downstream team would need to infer core business intent, scope boundaries, or ownership.
```

```yaml
kind: artifact
id: ARTIFACT-PROJECT-BRIEF
name: Initiative Definition / Project Brief
packaging_mode: standalone
required_by_gate: GATE-INITIATIVE-DEFINED
purpose: Primary large-work artifact that defines the initiative, its scope, business intent, operating context, and the named owners needed for gate decisions.
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
  - External vendor involved
required_by_gate_default: GATE-SPECIFICATION-COMPLETE
may_be_required_by_gate:
  - GATE-AUTHORIZED
purpose: Defines the external delivery engagement model, delivery responsibilities, and working agreements needed for a usable vendor or partner handoff.
required_contents:
  - Delivery engagement model and roles/responsibilities
  - Delivery cadence and working agreements
  - Communication and escalation paths
  - Handoff expectations and acceptance workflow (high-level)
  - Access and environment expectations (as applicable)
artifact_specific_completeness_rules:
  - Engagement roles, interfaces, and responsibilities are explicit enough to prevent delivery-governance gaps.
  - External parties can understand how work, decisions, escalation, and acceptance will operate.
common_failure_conditions:
  - The delivery mode is too vague to determine responsibilities or handoff expectations.
  - The document leaves unowned coordination or escalation gaps between internal and external teams.
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

### 2.6 Completeness and delivery-readiness model (resolved)

This section resolves Ambiguity A08.

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

Each gate definition MUST explicitly include:
1. **mandatory pass conditions**
2. **immediate fail conditions**
3. **minimum qualitative threshold**
4. **critical stage-defining artifacts**

The exact mapping of critical stage-defining artifacts is deferred to a later ambiguity (see Section 6.13 / Ambiguity A17). Until that mapping is resolved, gate definitions MUST retain an explicit placeholder rather than silently assuming which artifacts are critical.

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

There is **no conditional progression** for completeness failure. If the artifact or gate fails, work stops until the documented deficiencies are corrected and re-reviewed.

### 2.7 Scaling rules for small-work vs large-work (resolved)

This section resolves Ambiguity A09.

#### 2.7.1 Tiers

The framework defines two tiers:
1. **Small-work** — uses the Work Brief packet (see Section 2.5.2)
2. **Large-work** — uses the separate artifact set (see Section 2.5.3)

There is no intermediate tier.

#### 2.7.2 Classification factors

A project is classified as **large-work** if **any one** of the following primary factors is true (single-factor trigger, OR logic):

1. **Scope** — any of the following:
   - Multi-team
   - Multi-system
   - Multi-component
   - Greenfield (all greenfield projects are large-work regardless of team size or system count)

2. **Business impact** — any of the following:
   - Affects multiple departments, employees, or organizations (cross-department)
   - Material impact on operations, revenue, or strategic objectives
   - Requires an approved budget

3. **Effort/complexity** — Delivery Owner judgment; when uncertain, **default to large-work**

External involvement is relevant context but is not a primary forcing factor.

#### 2.7.3 Classification timing and declaration

The Delivery Owner MUST declare the classification (small-work or large-work) no later than Gate 2 (Initiative Defined). The classification determines the packaging mode (Work Brief or separate artifact set).

Classification documentation is not required beyond the declaration in the Initiative Definition / Project Brief or Work Brief.

#### 2.7.4 Reclassification

If a project initially classified as small-work grows beyond the small-work thresholds (e.g., scope expands to multi-team, a budget requirement is discovered, or effort/complexity increases materially), the project MUST be reclassified to large-work. Reclassification requires switching to the separate artifact set and completing any missing artifacts to satisfy the gate requirements of the new tier.

Reclassification events MUST be recorded in the Decision Log.

#### 2.7.5 Small-work gate passage profile

All gates apply to small-work. However, the following gates allow **quick passage** for small-work (brief confirmation, lighter evidence, Delivery Owner can mark as passed with documented rationale):

1. **Gate 1 (Qualified Request)** — in-scope confirmation and owner assignment is straightforward for small-work
2. **Gate 3 (Authorized)** — typically "Not Required" for small-work since requiring an approved budget would already trigger large-work classification
3. **Gate 5 (MVP Identified)** — for small-work, MVP scope often equals the full scope; brief confirmation suffices
4. **Gate 7 (Transition Complete)** — transition is typically simpler for small-work
5. **Gate 8 (Closure Complete)** — closure is typically simpler for small-work

The following gates still require **substantive review** for small-work (the Work Brief packet serves as evidence, but the gate standard still applies):

1. **Gate 2 (Initiative Defined)** — scope, outcomes, and ownership must still be clear
2. **Gate 4 (Specification Complete)** — this is the core quality gate; minimum `strong` rating still required
3. **Gate 6 (All Deliverables Accepted)** — acceptance must still be verified

Quick passage does not mean gate bypass. Every gate must still be formally evaluated and recorded.

#### 2.7.6 Small-work conditional artifacts

For small-work, only the Work Brief is required. Conditional artifacts (e.g., Delivery Charter, Access Model, Security/Privacy RIA) are at Delivery Owner and team discretion. There is no automatic upgrade to large-work triggered by a conditional artifact.

If the Delivery Owner determines that a conditional artifact is needed for small-work, it is produced and included as a companion to the Work Brief, and its completeness is still judged against the standard completeness model (see Section 2.6).

#### 2.7.7 Machine-consumable scaling model (YAML)

```yaml
kind: scaling
id: SCALING-MODEL
name: Work Delivery Framework Scaling Model
tiers:
  - id: TIER-SMALL-WORK
    name: Small-Work
    packaging_mode: packet
    primary_artifact: ARTIFACT-WORK-BRIEF
    classification_rule: >
      None of the primary forcing factors are true.
      Scope is single-team, single-system, and non-greenfield.
      Business impact does not cross departments, is not material, and does not require approved budget.
      Effort/complexity is judged manageable as small-work.
    gate_passage_profile: quick_pass
    quick_pass_gates:
      - GATE-QUALIFIED-REQUEST
      - GATE-AUTHORIZED
      - GATE-MVP-IDENTIFIED
      - GATE-TRANSITION-COMPLETE
      - GATE-CLOSURE-COMPLETE
    substantive_review_gates:
      - GATE-INITIATIVE-DEFINED
      - GATE-SPECIFICATION-COMPLETE
      - GATE-DELIVERABLES-ACCEPTED
    conditional_artifacts: delivery_owner_discretion
    reclassification_required: true
  - id: TIER-LARGE-WORK
    name: Large-Work
    packaging_mode: separate_artifacts
    primary_artifact: ARTIFACT-PROJECT-BRIEF
    classification_rule: >
      Any one primary forcing factor is true:
      scope is multi-team OR multi-system OR multi-component OR greenfield;
      business impact is cross-department OR material OR requires approved budget;
      effort/complexity is judged beyond small-work.
      Default to large-work when uncertain.
    gate_passage_profile: full_review
    quick_pass_gates: []
    substantive_review_gates:
      - GATE-QUALIFIED-REQUEST
      - GATE-INITIATIVE-DEFINED
      - GATE-AUTHORIZED
      - GATE-SPECIFICATION-COMPLETE
      - GATE-MVP-IDENTIFIED
      - GATE-DELIVERABLES-ACCEPTED
      - GATE-TRANSITION-COMPLETE
      - GATE-CLOSURE-COMPLETE
    conditional_artifacts: triggered_per_section_2_5_3
    reclassification_required: not_applicable
classification_timing: no_later_than_gate_GATE-INITIATIVE-DEFINED
classification_declaration: Initiative_Definition_or_Work_Brief
reclassification_rule: >
  If a small-work project exceeds any primary forcing factor threshold,
  it MUST be reclassified to large-work. Reclassification events MUST be
  recorded in the Decision Log. The project MUST then complete any
  missing artifacts to satisfy the gate requirements of the large-work tier.
```

### 2.8 Acceptance criteria and observable validation model (resolved: A10)

This section resolves Ambiguity A10 using clarified user intent: acceptance criteria must be **observable**, **quantifiable** where possible, and expressed in **hybrid Gherkin** (Gherkin-style Given/When/Then mixed with explicit success metrics and testability rules). The model prioritizes validation that downstream teams (human, vendor, or AI) can execute without subjective interpretation.

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
- Place acceptance criteria in the **Initiative Definition / Project Brief** (or Work Brief) under a dedicated "Acceptance Criteria" section
- Cross-reference in relevant artifacts (TDD, API/Contract Spec, User Adoption Plan)
- For complex features, group by use case or user story
- Always include at least one concrete holdout example per major criterion

#### 2.8.3 Scaling and gate expectations

- **Small-work**: 5-8 acceptance criteria focused on core outcomes sufficient for Gate 4 (`strong` rating required)
- **Large-work**: Comprehensive set covering functional, non-functional, data, integration, security, and operational validation
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

### 2.9 Minimum supportability and maintainability definition (resolved: A11)

This section resolves Ambiguity A11. Supportability and maintainability are now explicit minimum requirements embedded in the **Deployment Guide** (for large-work) or **Work Brief** (small-work) and cross-referenced in TDD.

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

- **Small-work**: Summary in Work Brief + basic runbook (1-2 pages)
- **Large-work**: Full Deployment Guide + TDD operational section + dedicated runbooks

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

This completes resolution of A10 and A11. The framework now provides enforceable, observable standards for validation and long-term operations.

### 2.10 Review, assurance, and audit mechanism (resolved: A13)

This section resolves Ambiguity A13.

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

### 2.11 Blocker, risk, and open-issue handling model (resolved: A14)

This section resolves Ambiguity A14.

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
10. Vendor engagement context where applicable

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
3. Reviewers conclude that the framework supported delivery readiness without adding avoidable bureaucracy.

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

## 6. Ambiguity Warnings

### 6.1 Framework format is resolved

**Resolved decision**
This framework is a full operating model for work definition and delivery readiness, expressed as a Markdown-first canonical specification with enforceable workflow stages, stage gates, and artifact definitions.

**Publication model**
The canonical source of truth is this specification file. It MUST embed machine-consumable YAML blocks (with stable IDs) for stages, artifacts, and gates so AI agents can apply it consistently.

**Implication for implementation**
Subsequent framework refinements MUST extend the structured YAML model in this document rather than creating parallel “shadow” definitions elsewhere.
### 6.2 Required artifact set is resolved

**Resolved decision**
The canonical artifact taxonomy is now defined in Section 2.5, including:
1. The small-work packet model (Work Brief)
2. The large-work separate-artifact model
3. The always-required artifacts (including a Decision Log)
4. The conditional artifacts and their triggers
5. Gate timing expectations for when each artifact must exist

**Implication for implementation**
Implementations and downstream templates MUST align to the canonical artifact names and the machine-consumable artifact YAML blocks in Section 2.5, rather than inventing alternative local artifact taxonomies.

### 6.3 Entry and exit criteria are not explicit

**What is ambiguous**
The framework’s starting trigger is broadly “a new business request,” but the exact readiness gates for entering, progressing, and completing the framework are not fully defined.

**Likely agent assumption**
An agent would likely invent stage gates such as intake, discovery, definition, handoff, and approval.

**Question to resolve**
What are the formal stages, and what evidence is required to move from one stage to the next?

### 6.4 Scope differentiation by work type is resolved

**Resolved decision**
The framework is optimized for software initiatives. It is in scope for greenfield and brownfield software projects. It is out of scope for minor low-risk changes, research spikes, support work, and small internal process changes. It may be used conditionally for complex operational changes affecting multiple organizations, complex internal process changes affecting the whole organization, and non-software initiatives that can use the framework with minimum changes.

**Implication for implementation**
The default framework shape should be designed for software project delivery first. Conditional reuse is allowed where the same control logic fits, but this decision does not broaden the framework into a universal model for all organizational work.

### 6.5 Completeness and delivery-readiness criteria are resolved

**Resolved decision**
Completeness is now defined as a hybrid model with:
1. mandatory pass/fail criteria that fail immediately when unmet
2. qualitative ratings (`weak`, `adequate`, `strong`) that describe quality after mandatory checks

The model applies at both the artifact level and the gate level. Every artifact definition must include purpose, required contents, artifact-specific completeness rules, and common failure conditions. Every gate definition must include mandatory pass conditions, immediate fail conditions, a minimum qualitative threshold, and a critical-artifact field.

The shared artifact core is:
1. clarity
2. internal consistency
3. decision/assumption visibility
4. actionability for the next consumer

The shared gate-level mandatory checks are:
1. stage-appropriate completeness
2. cross-artifact consistency
3. no unresolved blockers that force assumption-making
4. sufficiency for the named downstream consumer to proceed without redefining the problem

Qualitative thresholds are:
1. Gates 1-3 and 5-8 require at least `adequate`
2. Gate 4 (`Specification Complete`) requires `strong`

Open issues may remain only when they are explicit, owned, have a resolution path, and do not force downstream invention of business requirements. There is no conditional progression for completeness failure, and reviewers may not upgrade ratings based on team confidence or undocumented context.

**Implication for implementation**
Framework reviews and any AI-assisted validation logic MUST apply the explicit completeness model in Section 2.6 rather than inventing local quality heuristics.

### 6.6 Scaling rules for simple vs complex work are resolved

**Resolved decision**
The framework defines two tiers: small-work (Work Brief packet) and large-work (separate artifact set). Classification is a single-factor trigger: if any one of scope (multi-team, multi-system, multi-component, or greenfield), business impact (cross-department, material impact, or requires approved budget), or effort/complexity (Delivery Owner judgment; default to large-work when uncertain) hits the large-work threshold, the project is large-work. External involvement is relevant context but not a primary forcing factor.

Small-work uses a quick-pass gate profile for Gates 1, 3, 5, 7, and 8; substantive review is still required at Gates 2, 4, and 6. Small-work requires only the Work Brief; conditional artifacts are at Delivery Owner discretion. Large-work follows the full gate and artifact model.

Classification is declared no later than Gate 2. Reclassification from small-work to large-work is required if thresholds are exceeded mid-stream, and must be recorded in the Decision Log.

**Implication for implementation**
The scaling model MUST be applied as defined in Section 2.7. No intermediate tiers are introduced. The Delivery Owner MUST declare the tier no later than Gate 2 and MUST reclassify if thresholds are exceeded.

### 6.7 Governance and ownership are resolved

**Resolved decision**
1. The framework owner is the PMO. The PMO is accountable for maintaining, evolving, and publishing this framework.
2. Every gate in the framework MUST have a single accountable Gate Decision Owner (a named person) for the stop/proceed decision.
3. The Gate Decision Owner for each gate is assigned at Intake by the PMO or the project Delivery Owner and recorded in the Initiative Definition / Project Brief. For large projects with a formal project charter, this information MUST also be recorded in the Project Charter.
4. There are no role-based veto rights in this framework. The Gate Decision Owner is accountable for decisions made.
5. If there is substantive disagreement at a gate, the Gate Decision Owner MUST identify an alternative path forward (scope, sequencing, approach, or risk treatment) and record a plan of action forward in the project Decision Log.

**Default Gate Decision Owner roles (unless explicitly overridden by name in the Initiative Definition / Project Brief)**
1. Qualified Request: Delivery Owner
2. Initiative Defined (for Authorization decision): Delivery Owner
3. Authorized (when Authorization is required): Business / Product Owner (Budget Owner)
4. Specification Complete: Delivery Owner
5. MVP Identified: Delivery Owner
6. All Deliverables Accepted: Acceptance Owner (Business / Product Owner)
7. Transition Complete: Operations / Support Owner
8. Closure Complete: PMO / ITS Director
9. External handoff readiness (if an external team will build): Delivery Owner

**Consent model (for being named as Gate Decision Owner)**
Consent is implied when there is no objection upon acceptance of the document where the person is listed. It is expected that the named Gate Decision Owner will be informed of their responsibilities.

**Implication for implementation**
Gate definitions in the machine-consumable YAML model MUST specify a default_decision_owner_role and MUST require a named decision owner per project (recorded in the Initiative Definition / Project Brief).

### 6.8 Relationship to technical specification work is resolved

**Resolved decision**
The framework MUST produce business and system-level documentation that is strong enough for engineering teams to derive downstream technical specifications **without needing foundational clarification**.

The framework does **not** require downstream engineering planning outputs (task breakdown) or code-level technical specification artifacts.

**In-framework (this framework produces / requires)**
1. Business and functional definition sufficient to avoid redefinition of intent (including functional requirements, use cases, user roles, and business rules).
2. System-level technical documentation sufficient to derive downstream specs when needed, including:
   - architecture and major system components
   - data flows and/or system process diagrams
3. In-framework design artifacts (as applicable), such as the Technical Design Document (TDD) and API/Contract Specification.
4. Acceptance criteria and behavior-level tests derived from in-framework use cases (not detailed engineering test cases).

**Out-of-scope / downstream (engineering planning and code-level technical specification work)**
1. Work breakdown structures (epics/stories/tasks), sprint planning, and detailed implementation sequencing.
2. Code-level design (module/class/function-level details) and per-endpoint acceptance test suites.
3. Detailed engineering test plans and test cases (except where acceptance criteria require observable validation statements).

**Notes**
1. This boundary does not shift based on delivery mode (internal vs vendor), but completeness standards MAY need to be higher for AI-agent consumption (see Ambiguity A15).
2. Long-term maintainability is supported by requiring durable business + system-level documentation, and by requiring operational artifacts (e.g., Deployment Guide) where applicable; it is not achieved by forcing in-framework task breakdowns or code-level specs.

### 6.9 Acceptance and holdout pattern expectations are underdefined

**What is ambiguous**
You mentioned acceptance criteria and holdout patterns as examples of the context engineering teams need, but their required form and level of rigor are not specified.

**Likely agent assumption**
An agent would likely introduce its own testing or acceptance-writing model.

**Question to resolve**
What form should acceptance criteria take, and what do you mean by “testable using holdout patterns” in this framework?

### 6.10 External team engagement modes are underspecified

**What is ambiguous**
You mentioned external development teams, but not whether this includes full outsourced delivery, co-delivery, staff augmentation, or advisory vendors.

**Likely agent assumption**
An agent would likely design for one generic vendor handoff model.

**Question to resolve**
What external engagement models must the framework support, and how should handoff requirements differ across them?

### 6.11 Supportability and maintainability expectations are not yet decomposed

**What is ambiguous**
You require long-term supportability and maintainability, but the exact observable requirements are not stated.

**Likely agent assumption**
An agent would likely invent generic operational-readiness sections.

**Question to resolve**
What minimum support and maintenance information must always be defined before work is considered ready?

### 6.12 Review and audit mechanism is resolved

**Resolved decision**
1. The default model is Delivery Owner-led review with PMO assurance oversight.
2. PMO defines the review standard, assigns the Gate Decision Owner, checks evidence completeness, attends every substantive gate review, audits samples, and intervenes on escalation, non-compliance, or dispute.
3. Review mode follows the existing gate profile: small-work uses substantive review at Gates 2, 4, and 6 and quick-pass for the remaining gates; large-work uses substantive review at every gate.
4. Substantive gate reviews require a live meeting. Quick-pass gates require only a Decision Log entry.
5. Independent review is trigger-based only: architecture impact, security/privacy impact, external delivery/vendor handoff, or material business risk/regulatory exposure.
6. When triggered, explicit domain signoff is required before the gate can pass, but overall gate ownership remains with the Gate Decision Owner.
7. PMO audit findings may reopen a passed gate only when a material completeness failure or material control failure is later discovered.

**Implication for implementation**
The framework MUST apply the review mechanism in Section 2.10 rather than inventing local review boards, ad hoc signoff chains, or informal audit rules.

### 6.13 Critical stage-defining artifact mapping is deferred

**What is ambiguous**
The completeness model now requires each gate to identify its critical stage-defining artifacts, but the exact artifact-to-gate mapping has not yet been defined.

**Likely agent assumption**
An agent would likely infer the critical artifacts for each gate from context and apply that inference as if it were canonical.

**Question to resolve**
Which artifacts are the critical stage-defining artifacts for each gate, and what mapping rules apply when packaging modes or conditional artifacts vary?

## 7. Implementation Constraints

1. The implementation must remain minimal and avoid adding process overhead that does not improve delivery readiness.
2. The implementation must be suitable for human teams and AI-agent consumers.
3. The implementation must support complex enterprise and large multi-team initiatives.
4. No software integrations are currently required.
5. No code generation or solution implementation is in scope.

## 8. Remaining Contradictions

No direct contradictions were stated, but there is one tension that should be resolved explicitly: the framework must be rigorous enough for autonomous delivery while also avoiding bureaucracy. That tension is manageable, but only if you define how rigor scales by project type, risk, and complexity.
