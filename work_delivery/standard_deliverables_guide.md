# Standard Deliverables Guide

## 1. Purpose

Provide a practical reference list of common deliverables used in initiatives governed by the Work Delivery Framework.

This document helps teams think through what artifacts may be needed across different areas of an initiative (such as solution design, data, operations, security, governance, and user adoption).

It is not the starting point for deciding whether work should proceed. Start with Stage 1 Work Assessment or, for small governed work, the Work Brief path. Use this guide once the work is being defined and the team needs to decide which deliverables must exist for the work to stay clear, visible, accountable, traceable, and supportable.

## Related Documents

- [Work Assessment Process](work_assessment/work_assessment_process.md)
- [Work Delivery Framework](work_delivery_framework.md)
- [Deliverable Specifications Index](deliverable_specifications_index.md)
- [Solution Design Process](solution_design_process.md)

## 2. Deliverable Domains

A deliverable domain is a practical grouping of related deliverables.

Each domain covers one important area of delivery, such as solution design, governance, operations, data, security, or user adoption.

Using domains helps teams answer a simple question early: **"Have we covered all critical areas, not only build work?"**

During Work Definition, the team uses domains to organize the deliverables view. Domains do not replace visibility of the actual deliverables expected for the initiative.

Not every initiative needs every domain.

## 3. How to Use Standard Deliverables

Use this document as a **selection and control guide**, not as a requirement to produce every document listed.

1. Confirm which deliverables are required for the initiative, using deliverable domains as an organizing structure where useful.
2. For each relevant domain, select the standard deliverables that fit the initiative size, risk, and complexity.
3. Assign a clear owner and Acceptance Authority for each selected deliverable.
4. Use the deliverable Acceptance Criteria section to define what "done" means.
5. Collect acceptance evidence as delivery progresses, then record formal acceptance.

Deliverables not needed for authorization may still be listed at summary level during Work Definition so the likely delivery footprint remains visible, even if they will only be elaborated later.

For small governed work using a [Work Brief](work_brief/work_brief_specification.md), use this guide in the same way. Select only the deliverables the work actually needs, then make the owner, Acceptance Authority, and evidence basis visible in the Work Brief or linked supporting artifacts.

## 4. Operational Use Model

Use this reference differently at each stage:

- **Stage 1 - Work Assessment:** use the [Work Assessment Process](work_assessment/work_assessment_process.md) and its three assessment artifacts to decide whether the work should proceed into definition. This guide mainly becomes active after that decision, except for the Work Assessment Deliverables domain, which can be used after Initial Review and Validation Assessment are complete and the decision is to continue with fuller work assessment.
- **Stage 2 - Work Definition:** identify the required deliverables for the initiative, use domains to organize them where helpful, identify Acceptance Authorities, and define the minimum authorization-level output needed for a sound decision.
- **Stage 3 - Work Authorization:** confirm that selected deliverables, owners, acceptance approach, and major cost/risk implications are decision-ready.
- **Stage 4 - Work Definition Details:** elaborate the required deliverables and any additional definition deliverables needed to build, test, transition, and accept the work.
- **Stage 5 - Delivery Mobilization:** activate the delivery governance and execution controls needed to run the authorized work in a controlled and visible way.
- **Stage 6 - Work Delivery:** produce the selected deliverables and collect evidence against the agreed acceptance criteria.
- **Stage 7 - Acceptance, Transition & Closure:** confirm that each in-scope domain has evidence and explicit acceptance.

For smaller initiatives, use the minimum viable deliverable depth. The framework does not require every listed deliverable; it requires deliberate choices, explicit ownership, and acceptance-ready outputs.

The practical operating sequence is:

`Assess the work -> define the approved scope -> select the needed deliverables -> authorize the work -> elaborate only what is needed -> deliver with evidence -> accept, hand over, and close`

## 5. Minimum Viable Deliverable Depth

Apply the lightest depth that still makes the work understandable, controllable, and supportable.

| Initiative profile | Expected depth |
| --- | --- |
| Low complexity / low risk | Concise artifact, possibly combined into one controlled document or appendix |
| Medium complexity / cross-team impact | Separate artifacts for the core in-scope domains, with explicit owners and acceptance evidence |
| High complexity / high risk / regulated / operationally critical | Full domain-specific artifacts, stronger traceability, and more formal review and evidence |

## 6. AI Drafting Guidance

AI is most useful when the team provides:

- the relevant stage and artifact type
- in-scope and out-of-scope boundaries
- named owner and reviewer
- source notes or reference materials
- the required structure or specification
- any required IDs or traceability references

AI should help accelerate drafting, summarization, and traceability checks. It should not decide whether a domain is in scope, assign Acceptance Authorities, or claim that a deliverable is complete without human confirmation.

Use the [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md) as the default prompt and review protocol when drafting these deliverables.

Where a selected deliverable is written as a structured document with multiple sections or sub-sections, visible section numbering is recommended so the content is easier to review, reference, approve, and update.

Use numbering consistently in headings where practical, for example:

- `## 1. Purpose and Intended Outcome`
- `## 7. Required Content or Minimum Structure`
- `### 7.1. Record identity`
- `### 12.3. Validation prompts`

## 7. Solution Deliverables

### 7.1. Purpose

Use the Solution Deliverables domain to turn approved scope into a delivered and accepted solution in a controlled, easy-to-follow way.

This domain answers five practical questions:

- what is the approved solution scope
- who uses the solution and under what boundaries
- how is the approved scope grouped for delivery
- how should the solution behave
- what evidence supports formal acceptance

### 7.2. Simple Working Order

If a team is new to solution design, use the deliverables in this order:

| Stage | Deliverable | Why it exists | Specification |
| --- | --- | --- | --- |
| Stage 2 | Functional Capabilities | Defines the approved solution scope baseline | [functional_capabilities_specification](solution_deliverables/functional_capabilities_specification.md) |
| Stage 4 | User Roles, Personas & Access Model | Clarifies actors, boundaries, and control-sensitive roles | [user_roles_personas_and_access_model_specification](solution_deliverables/user_roles_personas_and_access_model_specification.md) |
| Stage 4 | Solution Modules Register | Lists all modules and their traceability at overview level | [solution_modules_specification](solution_deliverables/solution_modules_specification.md) |
| Stage 4 | Solution Module Definition | Describes one module in detail, including use cases and module acceptance criteria | [solution_module_definition_specification](solution_deliverables/solution_module_definition_specification.md) |
| Stage 4 | Use Case Narratives | Describes expected behavior in plain business language, either as a combined set or inside module definitions | [use_case_narratives_specification](solution_deliverables/use_case_narratives_specification.md) |
| Stage 6 | Deployed Solution | Records what approved scope is actually live | [deployed_solution_specification](solution_deliverables/deployed_solution_specification.md) |
| Stage 7 | Acceptance Record | Summarizes what was reviewed, what evidence was used, and what decision was made | [acceptance_record_specification](solution_deliverables/acceptance_record_specification.md) |

Use the [Solution Design Process](solution_design_process.md) as the operating guide that tells teams when to use each of these artifacts and how they fit together.

Solution deliverables should make the solution understandable for both future enhancement work and operational support after delivery.

For mobilization and coordination, pair the solution deliverables with:

- [delivery_roadmap_specification](governance_and_control_deliverables/delivery_roadmap_specification.md)
- [delivery_charter_specification](governance_and_control_deliverables/delivery_charter_specification.md)

These governance artifacts support timing, coordination, and operating rhythm. They do not replace solution scope, behavior, or acceptance controls.

### 7.3. Standard Deliverables (as applicable)

- **[Functional Capabilities](#7.4.%20Functional%20Capabilities)**
- **[Solution Modules Register](#7.5.%20Solution%20Modules%20Register)**
- **[Solution Module Definition](#7.6.%20Solution%20Module%20Definition)**
- **[Use Case Narratives](#7.7.%20Use%20Case%20Narratives)**
- **[User Roles, Personas & Access Model](#7.8.%20User%20Roles,%20Personas%20&%20Access%20Model)**
- **[Deployed Solution](#7.9.%20Deployed%20Solution)**
- **[Acceptance Record](#7.10.%20Acceptance%20Record)**

### 7.4. Functional Capabilities

The approval-level list of business abilities the solution must provide.

This deliverable establishes the solution scope baseline before detailed design begins.

#### Acceptance Criteria

- Each capability is clear enough to be understood and traced later.
- Capability statements stay at business ability level.
- Exclusions, assumptions, or dependencies that affect scope understanding are visible.

### 7.5. Solution Modules Register

The overview document that lists all approved modules and shows how they relate to roles, use cases, and approved scope.

This deliverable helps teams organize scope around user behaviors and use cases for build, validation, and acceptance without changing the approved baseline.

#### Acceptance Criteria

- Modules are listed clearly at overview level.
- Module boundaries do not introduce new scope.
- Each module can be traced to the relevant Functional Capabilities and module detail.

### 7.6. Solution Module Definition

The detailed document for one module, including what it will deliver, the related use cases, and the module-level acceptance criteria.

This deliverable gives reviewers and delivery teams a one-module-at-a-time view of behavior and acceptance.

#### Acceptance Criteria

- The module purpose and boundary are clear.
- Included use cases and supporting capabilities are visible.
- Module-level acceptance criteria are reviewable and testable.

### 7.7. Use Case Narratives

The business-behavior view of how users achieve outcomes using the solution.

This deliverable gives developers, testers, reviewers, and Acceptance Authorities a shared view of correct behavior.

#### Acceptance Criteria

- Each use case identifies the actor, trigger, outcome, and major behavior clearly.
- Rules, exceptions, and acceptance criteria are visible where they matter.
- Each use case traces back to a Solution Module and approved Functional Capabilities.

### 7.8. User Roles, Personas & Access Model

The actor model for the solution, including role purpose, access boundaries, and control-sensitive responsibilities.

This deliverable keeps role assumptions consistent across modules, use cases, security review, training, and acceptance.

#### Acceptance Criteria

- Important roles and access boundaries are documented.
- Approval, stewardship, or sensitive-role responsibilities are visible where relevant.
- Persona content, if used, adds context without expanding scope.

### 7.9. Deployed Solution

The record of what approved scope is actually live, where it is live, and under what operational conditions.

This deliverable makes the live state visible and traceable to approved scope and evidence.

#### Acceptance Criteria

- The live boundary is clear.
- Delivered behavior matches approved scope or accepted changes.
- Operational ownership and open live conditions are visible.

### 7.10. Acceptance Record

The formal summary of what was reviewed, what evidence supports acceptance, what conditions remain, and what decision was made.

This deliverable keeps sign-off explicit and attributable.

#### Acceptance Criteria

- The record links reviewed items to approved scope and evidence.
- Acceptance status and decision authority are explicit.
- Conditions, exclusions, or deferred items are visible.

### 7.11. Recommended Acceptance Evidence

- Completed Acceptance Record
- linked validation and deployment evidence
- visible traceability from approved scope to delivered behavior

### 7.12. Recommended Acceptance Authority

- Business Owner / Process Owner

## 8. Governance & Control Deliverables

### 8.1. Purpose

Ensure that intent, scope, authority, funding, risk acceptance, and closure decisions are explicit, attributable, and auditable across the lifecycle of the initiative.

### 8.2. Standard Deliverables (as applicable)

- **[Initiative Definition Document](#8.3.%20Initiative%20Definition%20Document)**
- **[Project Charter](#8.4.%20Project%20Charter)**
- **[Delivery Charter](#8.5.%20Delivery%20Charter)**
- **[Delivery Roadmap](#8.6.%20Delivery%20Roadmap)**
- **[Decision Record Log](#8.7.%20Decision%20Record%20Log)**
- **[Formal Acceptance & Closure Record](#8.8.%20Formal%20Acceptance%20&%20Closure%20Record)**

### 8.3. Initiative Definition Document

Defines the problem, future state, outcomes, scope boundaries, and high-level approach that justify investment and guide all downstream artifacts.

It establishes the baseline intent against which scope, design, and acceptance are validated. No downstream artifact may contradict this document without formal revision.

#### Acceptance Criteria

- The problem statement, intended outcomes, and scope boundaries are documented clearly.
- Key assumptions, constraints, and exclusions are recorded.
- The document is usable as the authoritative baseline for downstream deliverables.

### 8.4. Project Charter

Formally records sponsorship, authority, priority, and commitment to deliver the defined outcomes.

This document confirms that people, time, and funding are intentionally committed.

#### Acceptance Criteria

- Sponsor or decision authority is explicitly named.
- The charter records the authority basis for proceeding with the work.
- Funding or resource commitment is stated at the level required for the initiative.

### 8.5. Delivery Charter

Specification: [delivery_charter_specification](governance_and_control_deliverables/delivery_charter_specification.md)

Defines how the authorized initiative team is chartered and mobilized for controlled execution.

This should make visible:

- what is expected of the delivery team
- team roles and operating responsibilities
- communication methods and operating rhythm
- change, escalation, and decision paths
- control expectations for execution
- acceptance-readiness management expectations

This artifact may also be used as the practical agenda and record for a delivery team kickoff meeting.

This artifact supports controlled execution after authorization. It does not replace the Project Charter, detailed delivery plans, or active trackers.

This deliverable is primarily used in **Stage 5 - Delivery Mobilization**, though it may be prepared in draft form earlier if helpful.

#### Acceptance Criteria

- Core team roles, responsibilities, and operating expectations are documented.
- Communication, escalation, and decision paths are defined.
- Execution controls and acceptance-readiness expectations are stated clearly enough for mobilization.

### 8.6. Delivery Roadmap

Specification: [delivery_roadmap_specification](governance_and_control_deliverables/delivery_roadmap_specification.md)

Shows the planned delivery path from mobilization through acceptance, including high-level phases, major milestones, dependencies, and review checkpoints.

Use this deliverable progressively across stages:

- Stage 2: draft a high-level roadmap for authorization-level visibility
- Stage 4: elaborate the roadmap with releases, dependencies, and control checkpoints
- Stage 5: confirm and baseline the roadmap with the mobilized delivery team

The roadmap should remain aligned to approved scope and should be revised through change control when material changes occur.

#### Acceptance Criteria

- The roadmap includes the major phases or milestones needed to govern delivery.
- Significant dependencies, reviews, or control points are identified.
- Material changes to the roadmap are expected to be managed through change control.

### 8.7. Decision Record Log

Maintains a clear record of material decisions affecting scope, funding, risk, sequencing, or acceptance.

This ensures that governance decisions are attributable and reviewable.

#### Acceptance Criteria

- Material decisions are logged with decision statement, date, and decision authority.
- The log distinguishes decisions from unresolved issues or discussion notes.
- Decision entries are maintained as the initiative progresses.

### 8.8. Formal Acceptance & Closure Record

Provides documented confirmation that:

- Deliverables met defined acceptance expectations
- The appropriate Acceptance Authorities have signed off
- The initiative is formally closed

This prevents informal completion without accountability.

#### Acceptance Criteria

- The record identifies the closure decision, date, and responsible authority.
- Acceptance status for the initiative or relevant deliverables is explicitly recorded.
- Any open items, conditions, or post-closure responsibilities are documented.

### 8.9. Recommended Acceptance Evidence

- Approved Initiative Definition Document
- Approved Project Charter
- Approved Delivery Charter where controlled mobilization is required
- Delivery Roadmap (drafted in Stage 2, elaborated in Stage 4, and confirmed in Stage 5)
- Maintained Decision Record Log
- Completed Formal Acceptance & Closure Record

### 8.10. Recommended Acceptance Authority

- Sponsor or Delegated Decision Authority

## 9. Operational Readiness Deliverables

### 9.1. Purpose

Ensure the solution can be deployed, administered, operated, supported, restored, and sustained under clear operational ownership beyond the original delivery team.

For solutions with operational impact, these deliverables should start being shaped during solution design, not only near go-live. They should be driven by the solution behaviors, module definitions, and technical choices that operations teams will need to support later.

### 9.2. Standard Deliverables (as applicable)

- **[Technical Design Document](#9.3.%20Technical%20Design%20Document)**
- **[DevOps Guide](#9.4.%20DevOps%20Guide)**
- **[Operations & Support Model](#9.5.%20Operations%20&%20Support%20Model)**
- **[Backup, Restore & Recovery Plan](#9.6.%20Backup,%20Restore%20&%20Recovery%20Plan)**
- **[Operational Readiness Confirmation Record](#9.7.%20Operational%20Readiness%20Confirmation%20Record)**

### 9.3. Technical Design Document

Documents the technical design of the solution so that delivery, operations, and support teams can understand how it is structured, what it depends on, and what technical assumptions affect operation and change.

This should define the design-level view of the solution, including:

- System architecture, solution structure, and major components
- Environment and hosting design
- Key integrations and dependencies
- Important configuration, data, and interface design considerations
- Security, reliability, capacity, and performance design considerations
- Key technical assumptions and constraints that affect support, restore, or future change
- Significant design decisions that operations or future maintainers must understand

This artifact explains how the solution is built. It does not replace operating procedures, support processes, or step-by-step administration instructions.

#### Acceptance Criteria

- Major components, environments, dependencies, and design considerations are documented.
- Important assumptions, constraints, and operationally significant design decisions are recorded.
- The document is sufficient to inform support and future technical change.

### 9.4. DevOps Guide

Provides the practical instructions and reference information needed to deploy, configure, maintain, troubleshoot, and support the solution in day-to-day operations.

This should define the execution-level guidance needed to operate the solution in practice, including:

- Environment setup and configuration steps
- Deployment and update procedures
- Release, cutover, and rollback steps
- Routine administration and maintenance tasks
- Operational checks, monitoring checks, and troubleshooting guidance
- Known failure scenarios, common support actions, and escalation notes

This artifact explains how the solution is administered and supported in practice. It complements the Technical Design Document by converting design knowledge into repeatable operational guidance.

#### Acceptance Criteria

- Deployment, configuration, and maintenance guidance is documented for the relevant environment.
- Troubleshooting, support actions, and escalation notes are included for expected operational use.
- The guide is usable without relying on undocumented knowledge held by one individual.

### 9.5. Operations & Support Model

Defines:

- Named Service Owner
- Named Support Owner
- Support boundaries and escalation paths
- Support model and responsibility split (for example, internal team, vendor, or shared support)
- Monitoring and incident response expectations
- Hypercare, transition, or steady-state support assumptions
- Known operational risks, constraints, and dependency assumptions

This artifact ensures the solution has clear long-term accountability.

#### Acceptance Criteria

- Service ownership and support ownership are explicitly assigned.
- Support boundaries, escalation path, and support model are documented.
- Monitoring, incident response, or hypercare expectations are defined where relevant.

### 9.6. Backup, Restore & Recovery Plan

Defines how the solution can be backed up, restored, recovered, or rolled back in the event of failure or deployment issue, including:

- Backup scope and assumptions
- Restore, recovery, or rollback approach
- Recovery responsibilities and required access
- Critical dependencies
- Recovery prerequisites and operational impact considerations
- Validation expectations showing that recovery is realistic and understood

This artifact ensures the solution can survive incidents and disruption without relying on undocumented knowledge.

#### Acceptance Criteria

- Backup or recovery scope and method are documented for the relevant solution components.
- Recovery responsibilities, dependencies, and required access are identified.
- Validation expectations or evidence for restore, recovery, or rollback are recorded.

### 9.7. Operational Readiness Confirmation Record

Provides formal confirmation that:

- Service ownership is assigned
- Support ownership is assigned
- Required design and administration documentation is available
- Support, monitoring, and recovery expectations are understood
- Material readiness gaps, conditions, or follow-up actions are recorded
- The solution is formally accepted into operational responsibility

This artifact prevents informal or unsupported handover.

#### Acceptance Criteria

- Named Service Owner and Support Owner are recorded.
- The record confirms availability of the required design, administration, and recovery documentation.
- Acceptance decision, conditions, and outstanding readiness actions are explicitly documented.

### 9.8. Recommended Acceptance Evidence

- Approved Technical Design Document
- Approved DevOps Guide
- Approved Operations & Support Model
- Approved Backup, Restore & Recovery Plan
- Completed Operational Readiness Confirmation Record

### 9.9. Recommended Acceptance Authority

- IT Operations / Service Owner

## 10. Data Governance & Records Deliverables

### 10.1. Purpose

Ensure data produced, stored, or processed by the initiative is explicitly defined, governed, owned, and auditable, with clear operational and lifecycle accountability.

### 10.2. Standard Deliverables (as applicable)

- **[Data Governance & Impact Assessment](#10.3.%20Data%20Governance%20&%20Impact%20Assessment)**
- **[Data Asset Specification](#10.4.%20Data%20Asset%20Specification)**
- **[Data Migration Record](#10.5.%20Data%20Migration%20Record)** (if applicable)

### 10.3. Data Governance & Impact Assessment

Defines the governance and organizational impact of data handled by the initiative, including:

- Categories of data produced, stored, or processed
- Data sensitivity and classification
- Compliance and policy implications
- Operational and governance impact considerations
- Identified Data Steward

#### Acceptance Criteria

- Relevant data categories and sensitivity classifications are documented.
- Material compliance, policy, or governance implications are identified.
- A Data Steward or equivalent accountable role is named.

### 10.4. Data Asset Specification

Provides authoritative documentation of the known data handled by the initiative, including:

- Logical data structure (key entities and relationships)
- Data dictionary (field definitions and key attributes)
- System of record declaration
- Storage location(s)
- Responsible owner(s) and stewardship
- Retention and lifecycle rules
- Backup inclusion status (as applicable)

#### Acceptance Criteria

- Key entities, attributes, or equivalent data definitions are documented.
- System of record, storage location, and responsible owner or steward are identified.
- Retention, lifecycle, and backup inclusion status are stated where relevant.

### 10.5. Data Migration Record

Used when data is materially migrated, transformed, or restructured.

Documents both the **planned migration approach** and the **evidence confirming the migration was successful**.

May include:

**Migration Plan**

- Source and target systems
- Data mapping or transformation logic
- Migration sequencing or cutover approach
- Rollback or recovery considerations

**Validation Evidence**

- Validation and reconciliation approach
- Results confirming source and target data consistency
- Exceptions identified and their disposition
- Steward or Acceptance Authority sign-off

#### Acceptance Criteria

- Source and target scope, migration approach, and validation method are documented.
- Reconciliation or validation results are recorded, including exceptions and disposition.
- Steward or Acceptance Authority sign-off is recorded when migration is performed.

### 10.6. Recommended Acceptance Evidence

- Approved Data Governance & Impact Assessment
- Approved Data Asset Specification
- Approved Data Migration Record (if applicable)
- Steward or Data Governance sign-off

### 10.7. Recommended Acceptance Authority

- Data Steward (dataset correctness and stewardship accountability)
- Data Governance Officer (governance compliance)

## 11. Security, Privacy & Compliance Deliverables

### 11.1. Purpose

Ensure that security, privacy, and regulatory risks introduced by the initiative are explicitly identified, evaluated, controlled, and formally accepted where necessary.

### 11.2. Standard Deliverables (as applicable)

- **[Security & Privacy Risk Assessment](#11.3.%20Security%20&%20Privacy%20Risk%20Assessment)**
- **[Access Control & Authorization Model](#11.4.%20Access%20Control%20&%20Authorization%20Model)**
- **[Audit & Monitoring Design Summary](#11.5.%20Audit%20&%20Monitoring%20Design%20Summary)**
- **[Compliance & Regulatory Alignment Statement](#11.6.%20Compliance%20&%20Regulatory%20Alignment%20Statement)**
- **[Residual Risk Acceptance Record](#11.7.%20Residual%20Risk%20Acceptance%20Record%20(if%20applicable))** (if applicable)

### 11.3. Security & Privacy Risk Assessment

Identifies and evaluates security and privacy risks associated with the solution, including:

- Types of sensitive data handled
- Threat exposure and misuse scenarios
- Potential impact to the organization
- Required control measures

This artifact clarifies what could go wrong and how risk is reduced.

#### Acceptance Criteria

- Material security and privacy risks are identified and assessed.
- Required controls or treatment actions are documented for the identified risks.
- Residual exposure requiring escalation or acceptance is made visible.

### 11.4. Access Control & Authorization Model

Defines how access to the solution is controlled, including:

- Role-based or responsibility-based access boundaries
- Separation-of-duties assumptions
- Privileged access considerations
- Governance expectations for account management

This ensures access decisions are intentional and reviewable.

#### Acceptance Criteria

- Relevant roles or access groupings are defined with their intended permissions.
- Privileged or sensitive access considerations are explicitly documented.
- Separation-of-duties or account-governance expectations are stated where relevant.

### 11.5. Audit & Monitoring Design Summary

Describes how key actions within the solution are logged and monitored, including:

- Events that must be traceable
- Monitoring expectations for sensitive or high-risk activity
- Escalation or review triggers

This ensures accountability and forensic reconstructability.

#### Acceptance Criteria

- Key events requiring traceability are identified.
- Monitoring or alert expectations are documented for material risk scenarios.
- Review, escalation, or follow-up triggers are defined where needed.

### 11.6. Compliance & Regulatory Alignment Statement

Documents how the initiative aligns with applicable internal policies, regulatory obligations, and data protection requirements.

This ensures that compliance exposure is evaluated before and after implementation.

#### Acceptance Criteria

- Applicable policies or obligations are identified.
- The document states how the initiative aligns with, satisfies, or is conditioned by those obligations.
- Material compliance issues needing action or approval are explicitly recorded.

### 11.7. Residual Risk Acceptance Record (if applicable)

Records formal acknowledgment and acceptance of any material risks that remain after mitigation controls are applied.

This prevents silent or assumed risk acceptance.

#### Acceptance Criteria

- Residual risks being accepted are described clearly.
- Compensating controls, conditions, or limitations are recorded where relevant.
- Acceptance authority and acceptance decision are explicitly documented.

### 11.8. Recommended Acceptance Evidence

- Approved Security & Privacy Risk Assessment
- Approved Access Control & Authorization Model
- Approved Audit & Monitoring Design Summary
- Approved Compliance & Regulatory Alignment Statement
- Residual Risk Acceptance Record (if applicable)

### 11.9. Recommended Acceptance Authority

- Security / Data Protection Officer

## 12. User Adoption & Change Enablement Deliverables

### 12.1. Purpose

Ensure that impacted users understand the change, are prepared to use the solution correctly, and can adopt it without introducing avoidable operational risk or resistance.

### 12.2. Standard Deliverables (as applicable)

- **[User Impact Assessment](#12.3.%20User%20Impact%20Assessment)**
- **[Change & Communication Plan](#12.4.%20Change%20&%20Communication%20Plan)**
- **[Training & Enablement Materials](#12.5.%20Training%20&%20Enablement%20Materials)**
- **[Adoption Support Model](#12.6.%20Adoption%20Support%20Model)**
- **[Adoption Confirmation Record](#12.7.%20Adoption%20Confirmation%20Record)**

### 12.3. User Impact Assessment

Identifies:

- Impacted user groups and roles
- Nature and scale of behavioral change
- Process changes required
- Adoption risks and resistance factors

This artifact clarifies who is affected and what will change for them.

#### Acceptance Criteria

- Impacted user groups or roles are identified.
- The expected behavioral or process change is described for the relevant groups.
- Material adoption risks or resistance factors are documented.

### 12.4. Change & Communication Plan

Defines how the change will be communicated and managed, including:

- Key messages and timing
- Stakeholder communication approach
- Leadership alignment expectations
- Feedback and escalation channels
- Development of promotional or informational websites, campaign pages, or launch materials intended to build awareness and support adoption

This ensures that change is intentional rather than assumed.

Clarification:
Promotional or informational websites created solely to support awareness, communication, or adoption of the initiative fall within this domain. If a website or portal delivers core business capabilities (e.g., application submission, transactions, self-service functionality), it is part of the Solution Deliverables domain and must be governed under authorized scope, behavioral definition, and acceptance controls.

#### Acceptance Criteria

- Key messages, audiences, and timing are documented.
- Communication channels or activities are defined for the affected stakeholder groups.
- Feedback or escalation routes are identified for questions, issues, or resistance.

### 12.5. Training & Enablement Materials

Provide structured support for users to perform required behaviors, including:

- User guides or reference materials
- Training sessions or walkthroughs (if appropriate)
- Context-specific instructions aligned with real user roles

This ensures users can perform expected tasks correctly and consistently.

#### Acceptance Criteria

- Training or enablement materials exist for the relevant user groups.
- Content is aligned to the roles, tasks, or scenarios users must perform.
- The materials are usable in the form needed for the initiative, whether reference, walkthrough, or formal training.

### 12.6. Adoption Support Model

Defines how users receive help after go-live, including:

- Initial hypercare or transition support (if applicable)
- Support channels and escalation expectations
- Known adoption risks and mitigation approach

This ensures adoption issues do not silently degrade outcomes.

#### Acceptance Criteria

- Adoption support channels or responsibilities are defined.
- Hypercare, transition support, or early-life support expectations are documented where relevant.
- Known adoption risks and mitigation actions are recorded.

### 12.7. Adoption Confirmation Record

Provides confirmation that:

- Impacted user groups were informed
- Required training or enablement activities occurred
- Adoption risks were reviewed
- The Business Owner acknowledges user readiness

This prevents informal or assumed adoption.

#### Acceptance Criteria

- The record confirms completion or status of the required communication and enablement activities.
- User readiness risks, conditions, or outstanding follow-up actions are documented.
- Business Owner or delegated authority acknowledgment is explicitly recorded.

### 12.8. Recommended Acceptance Evidence

- Approved User Impact Assessment
- Approved Change & Communication Plan
- Published Training & Enablement Materials
- Defined Adoption Support Model
- Completed Adoption Confirmation Record

### 12.9. Recommended Acceptance Authority

- Business Owner
- Change or Communications Lead

## 13. Work Assessment Deliverables

### 13.1. Purpose

Use this domain when Initial Review and Validation Assessment are complete, the decision is to continue with fuller work assessment, and the team needs controlled assessment outputs that later definition can reuse directly.

This domain is especially useful when operators need to make explicit:

- the background, challenges, unmet needs, and current-state findings that shape the work
- the workflow, handoff, ownership, or control realities that materially affect the recommendation
- the business opportunity being explored, including opportunities that may be worth preserving even if the work is later deferred
- the recommendation on whether definition effort should now be invested

This domain is for focused assessment work after the earlier screening steps. Do not use it for Initial Review or Validation Assessment themselves.

### 13.2. Standard Deliverables (as applicable)

- **[Challenges and Needs](#13.3.%20Challenges%20and%20Needs)**
- **[Current State Analysis Report](#13.4.%20Current%20State%20Analysis%20Report)**
- **[Business Process Stage Analysis](#13.5.%20Business%20Process%20Stage%20Analysis)**
- **[Work Assessment Report](#13.6.%20Work%20Assessment%20Report)**

### 13.3. Challenges and Needs

Keeps the validated problem basis, unmet needs, and business opportunity context visible while fuller work assessment is underway.

In many cases this will refine and carry forward the existing [Challenges and Needs](work_assessment/challenges_and_needs_specification.md) artifact rather than recreate it.

#### Acceptance Criteria

- The primary challenge, unmet need, or business opportunity is explicit.
- Affected parties, visible impacts, and consequence of inaction or missed opportunity are clear.
- Any visible solution assumptions are still treated as assumptions rather than settled decisions.

### 13.4. Current State Analysis Report

Documents the current operating reality that later definition should be able to reference directly instead of rediscovering it.

Use it when systems, workflows, records, ownership, or operational constraints are material enough that a short summary in the gate artifacts would be too thin.

#### Acceptance Criteria

- The current-state boundary and evidence basis are clear.
- The relevant systems, workflows, handoffs, workarounds, constraints, and ownership signals are visible.
- The report is usable as carry-forward context for later definition.

### 13.5. Business Process Stage Analysis

Makes the current business flow visible stage by stage where delays, handoffs, roles, controls, or exceptions materially shape the work.

Use it when later definition would otherwise need to reconstruct the current process from scratch.

#### Acceptance Criteria

- The important stages, actors, inputs, outputs, handoffs, and controls are explicit.
- Material bottlenecks, ownership gaps, dependencies, or exception paths are visible.
- The analysis stays focused on the current process rather than future-state redesign.

### 13.6. Work Assessment Report

Provides the final recommendation on whether the work should enter definition and what definition should start from if it does.

This is the main decision-ready deliverable in the domain.

#### Acceptance Criteria

- The report makes an explicit stop, defer, or proceed recommendation.
- The recommendation is supported by the relevant assessment findings and supporting artifacts.
- The handoff basis into the next definition artifact is clear and reusable.

### 13.7. Recommended Acceptance Evidence

- Completed Work Assessment Report
- Current State Analysis Report where used
- Business Process Stage Analysis where used
- Challenges and Needs where used or carried forward
- visible references to the assessment decision basis and next-step recommendation

### 13.8. Recommended Acceptance Authority

- ITS leadership / intake governance
- delegated work assessment decision authority where applicable

## 14. Summary Table

| Deliverable Domain                | Primary Intent                                                                 |
| --------------------------------- | ------------------------------------------------------------------------------ |
| Solution Deliverables             | Deliver the approved solution outcomes within authorized scope                 |
| Governance & Control              | Make intent, authority, decisions, funding, acceptance, and closure auditable  |
| Operational Readiness             | Ensure the solution is deployable, operable, supportable, and recoverable      |
| Data Governance & Records         | Make data and records explicit, governed, owned, and auditable                 |
| Security, Privacy & Compliance    | Identify, reduce, and explicitly accept security, privacy, and compliance risk |
| User Adoption & Change Enablement | Prepare users for change, reduce adoption risk, and support sustained usage    |
| Work Assessment Deliverables      | Keep focused assessment findings, opportunities, and the definition handoff usable and traceable |

## 15. Appendix B - Domain Selection Matrix

Use this matrix during Work Definition to decide which domains should be in scope.

| Domain | Common trigger conditions | Minimum viable output | Expand depth when | Do not use this domain for |
| --- | --- | --- | --- | --- |
| Solution Deliverables | New or changed user-facing or system behavior | Functional Capabilities plus concise acceptance approach | Behavior is complex, multi-step, role-sensitive, or needs structured validation through roles, modules, and use cases | General communications, training-only content, or governance-only decisions |
| Governance & Control | Formal sponsorship, funding, prioritization, controlled delivery governance, or closure is needed | Initiative Definition, Project Charter, Decision Record Log, Delivery Charter, and Delivery Roadmap where controlled mobilization is needed | Funding, risk, delivery governance, or closure requires stronger traceability | Technical design or operational procedures |
| Operational Readiness | Service, system, or support impact exists | Named support ownership plus minimum run / recovery view | The solution affects production support, recovery, or long-term maintainability | Business-only justification or user comms |
| Data Governance & Records | Data is created, changed, migrated, classified, or governed | Data impact summary with steward and system-of-record view | Data structures, migration, retention, or stewardship are material | General functional behavior that does not materially affect governed data |
| Security, Privacy & Compliance | Sensitive data, access control, logging, or regulatory exposure exists | Risk summary plus minimum control intent | Privacy, audit, or compliance obligations are material | General project management or user enablement |
| User Adoption & Change Enablement | User behavior, communications, or training are materially affected | Impact summary plus basic communication / enablement approach | Rollout is broad, high-impact, or behavior change is significant | Core solution functionality or system design |
| Work Assessment Deliverables | Initial Review and Validation Assessment are complete, the decision is to continue with fuller work assessment, and the assessment findings need to be preserved as reusable research or opportunity context | Work Assessment Report plus only the supporting assessment artifacts needed to make the recommendation credible and reusable | Current state, workflow, stakeholder need, or business opportunity analysis materially shapes the recommendation or later definition | Initial triage, Validation Assessment itself, or solution design |

## 16. Appendix C - Minimum Viable Outputs by Domain

| Domain | Smallest acceptable content set |
| --- | --- |
| Solution Deliverables | Approved scope baseline, clear actor model where needed, defined behavior, and evidence for acceptance |
| Governance & Control | Named owners, authorization basis, key decisions, and delivery governance / closure confirmation as applicable |
| Operational Readiness | Named run/support owners, basic support approach, and recovery intent |
| Data Governance & Records | Data impact summary, steward, system of record, and major data obligations |
| Security, Privacy & Compliance | Risk summary, key controls, and required authority review |
| User Adoption & Change Enablement | Impacted users, communication approach, enablement actions, and adoption owner |
| Work Assessment Deliverables | Clear recommendation, reusable assessment basis, and only the focused analysis needed to carry the background, needs, current state, process realities, or opportunity context forward |

## 17. Appendix A — Role Glossary

### 17.1. Sponsor

Authorizes the initiative, commits funding and priority, and accepts organizational risk.

### 17.2. Decision Authority

Accountable for the go / no-go decision to commit organizational capacity, time, funding, and risk to delivery.

### 17.3. Acceptance Authority

Accountable for formally accepting deliverables within an in-scope deliverable domain based on defined acceptance criteria and evidence.

### 17.4. Outcome Owner

Accountable for achieving the intended business outcomes and confirming that delivered value meets the agreed success measures.

### 17.5. Business Owner / Process Owner

Accountable for the business process outcomes supported by the solution and commonly serves as the Acceptance Authority for Solution Deliverables.

### 17.6. Data Steward

Accountable for dataset correctness, quality, and governance obligations.

### 17.7. Data Governance Officer (DGO)

Oversees data governance standards and compliance.

### 17.8. Delivery Owner

Accountable for delivery execution, stage discipline, and ensuring required deliverables and evidence are produced.

### 17.9. IT Operations / Service Owner

Accountable for ongoing operation and support of the system.

### 17.10. Security / Data Protection Officer

Accountable for privacy, security, and regulatory compliance.

### 17.11. Change or Communications Lead

Accountable for user readiness, communications, and adoption enablement activities.

## 18. How to Use This Document

This document serves as the authoritative catalog of standard deliverables and acceptance expectations across deliverable domains.

It does not make every deliverable mandatory for every initiative. During Work Definition, teams determine which domains are relevant and which standard deliverables are appropriate for the initiative's nature, scale, and risk.

Deliverable domains mainly organize the deliverables view. The team should still make the actual required deliverables visible.

### 18.1. During Work Definition (Stage 2)

- Confirm which deliverables are required for the initiative, using deliverable domains as an organizing structure where useful.
- If Work Assessment Deliverables were used, make the carry-forward assessment references explicit so definition does not rediscover the same background, challenges, needs, current-state facts, or opportunity context.
- Identify the Acceptance Authority for every required deliverable or clearly defined deliverable grouping.
- Agree which standard deliverables are expected for each relevant domain, at authorization-level depth.
- Additional expected deliverables not needed for authorization may be listed at summary level so likely effort remains visible.
- Use the deliverable Acceptance Criteria section as the basis for defining what "done" will mean later at acceptance.

### 18.2. During Work Authorization (Stage 3)

- Confirm that scope, ownership, funding commitments, and risk implications are decision-ready.
- Confirm Acceptance Authorities remain valid for each required deliverable or deliverable grouping.
- Record the authorization decision and associated commitments.

### 18.3. During Work Definition Details (Stage 4)

- Elaborate the required deliverables identified in Stage 2 and produce any additional definition deliverables needed to build, test, transition, and accept the solution.
- Ensure elaboration remains consistent with the authorized scope and intent.

### 18.4. During Delivery Mobilization (Stage 5)

- Activate the Delivery Charter and related execution controls needed for controlled delivery.
- Confirm the Delivery Roadmap with the mobilized delivery team and key stakeholders.
- Confirm reporting rhythm, escalation path, change path, and acceptance-readiness tracking are in place.

### 18.5. During Work Delivery (Stage 6)

- Produce the required deliverables for each relevant domain and collect acceptance evidence.
- Use the deliverable Acceptance Criteria section to drive validation and evidence collection.
- Track progress by accepted deliverables and evidence, not activity.

### 18.6. During Acceptance, Transition & Closure (Stage 7)

- Validate that the Acceptance Criteria expectations are addressed for every required deliverable.
- Ensure required evidence is complete, reviewable, and attributable.
- Record formal acceptance by the named Acceptance Authorities and formally close the initiative.

Completion requires acceptance across all applicable deliverable domains.
