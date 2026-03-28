# Solution Design Process

## 1. Purpose

This Solution Design Process operates across two levels of the [Work Delivery Framework](work_delivery_framework.md):

- **Stage 2 – Work Definition:** confirm the problem and outcomes, select active deliverable domains, define the authorization-level scope baseline (Functional Capabilities), record authorization-level acceptance focus, and surface summary-level cross-domain impacts – all within the "no more, no less" authorization boundary.
- **Stage 4 – Work Definition Details:** elaborate the authorized scope into delivery-ready behavioral and technical detail – actor model, modules, use cases, domain-specific artifacts, and evidence plans – without expanding approved scope.

It is a **governance process**, not a brainstorming session. Every step ensures the solution remains traceable to its authorized scope, is supportable and secure, and is described in a way that non-technical stakeholders can understand.

Use it together with:
- The [Work Delivery Framework](work_delivery_framework.md), which defines the seven stages of work from intake to closure.
- The [Standard Deliverables Guide](standard_deliverables_guide.md) and [Deliverable Specifications Index](deliverable_specifications_index.md), which list deliverable domains and when each deliverable is needed.
- The deliverable specifications in `work_delivery`, especially **Functional Capabilities**, **Solution Modules**, **Use Case Narratives**, **Solution Module Definition**, **User Roles, Personas & Access Model**, **Operations & Support Model**, **Technical Design Document**, **DevOps Guide**, **Acceptance Record**, and others.
- The [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md), which defines how AI tools may assist with drafting, summarizing, and traceability without becoming decision-makers.

## 2. Where This Process Fits

| Stage | Stage Name | Solution design activities at this stage |
|---|---|---|
| **2** | Work Definition | Confirm problem and outcomes; select active deliverable domains; define Functional Capabilities (authorization-level scope baseline); record authorization-level acceptance focus; capture summary-level cross-domain impacts |
| **3** | Work Authorization | Present the authorization package; no new design work at this stage |
| **4** | Work Definition Details | Define actor and control model; structure solution into modules and use cases; shape domain-specific readiness artifacts; plan evidence and acceptance approach |
| **5** | Delivery Mobilization | Confirm delivery readiness; finalize domain artifacts and acceptance package; no scope expansion |
| **6** | Work Delivery | Build, validate, and evidence the solution incrementally |
| **7** | Acceptance, Transition & Closure | Confirm cross-domain readiness; obtain formal acceptance; transfer operational ownership; close the work; capture early-life learning |

Stages 1, 3, and 5 are not design stages. Bring only what those stages need: Stage 1 receives assessment output, Stage 3 receives the authorization package, Stage 5 confirms readiness.

## 3. Why This Process Matters

1. **Scope control** – All design artifacts must trace back to the approved Stage 2 baseline. Do not quietly add features or change outcomes.
2. **Traceability** – Each behavior, module, and test must map back to a **Functional Capability (FC‑###)**. Each delivered component must be evidenced and accepted.
3. **Clarity** – Design documents are written for business owners, testers, operations, and auditors – not just developers.
4. **Supportability** – Operations, data, security, and user adoption concerns must shape the design, not react to it.
5. **Evidence** – Acceptance criteria and evidence requirements are defined early so delivery can be verified later.
6. **Responsible AI** – AI may draft documents, transform, and summarize content, but it cannot invent scope, invent evidence, or approve acceptance. Humans remain accountable.

## 4. Quick Start

Use this as an orientation guide. For detail on each activity, see [Section 6 (Stage 2)](#6.%20Stage%202%20%E2%80%93%20Solution%20Definition%20Minimum) and [Section 7 (Stage 4)](#7.%20Stage%204%20%E2%80%93%20Delivery-Ready%20Elaboration).

### Stage 2 – Solution Definition Minimum at a Glance

| Activity | What to produce | Where it lives |
|---|---|---|
| Confirm problem, outcomes, assumptions, exclusions | Problem statement, current state, future state, success measures, key assumptions, and explicit exclusions | Inside the Initiative Definition Document or Work Brief |
| Select active deliverable domains and minimum viable depth | Domain activation list with rationale, minimum viable depth, and named Acceptance Authorities | Inside the Initiative Definition Document |
| Define authorization-level scope | Functional Capabilities (FC‑###) | Functional Capabilities artifact |
| Record authorization-level acceptance focus | Summary of what "done" broadly means and who accepts it, per active domain | Inside the Initiative Definition Document |
| Record summary-level cross-domain impacts | Brief impact notes for operational, data, security/privacy, and user adoption domains as applicable | Inside the Initiative Definition Document |

**Stage 2 does not include:** User Roles, Personas & Access Model; Solution Modules; Use Case Narratives; detailed design; or detailed test plans. Those belong in Stage 4.

### Stage 4 – Delivery-Ready Elaboration at a Glance

| Activity | What to produce | Where it lives |
|---|---|---|
| Define actor and control model | User Roles, Personas & Access Model | Dedicated artifact |
| Structure solution into modules and use cases | Solution Modules Register, Solution Module Definitions, Use Case Narratives | Dedicated artifacts |
| Shape domain-specific readiness in parallel | Technical Design Document, DevOps Guide, Operations & Support Model, data and security artifacts, adoption plans | Domain-specific artifacts |
| Plan evidence and acceptance approach | Acceptance criteria, test approach, evidence plan (at module and use case level) | Inside module definitions or as a dedicated test plan |

**Stage 4 must not:** introduce new Functional Capabilities, alter the authorized scope, change the acceptance structure, or expand domain activation beyond what Stage 2 established.

### Tailoring and Iteration

- **Scale depth to size and risk.** For low-risk or small enhancements, Steps 0 and 1 may be combined into a quick discussion recorded in the Work Brief. Modules may be simple features; use cases may be short bullet points.
- **Iterate within Stage 4.** Steps 3–6 repeat in loops: draft roles and modules, review, build a module slice, collect evidence, refine design, then proceed to the next module.
- **Keep artifacts human-readable.** Write design documents in plain language, referencing FC‑IDs, SM‑IDs, and UC‑IDs. Summaries and tables should help non-technical stakeholders understand the solution.
- **Use AI responsibly.** AI tools can draft, transform, translate, and summarize; they can propose modules, use cases, and test cases; they can check traceability. They must not define scope, assign Acceptance Authorities, decide acceptance, or invent evidence.

## 5. Step Summary

Steps 0–2 belong to **Stage 2**. Steps 3–6 belong to **Stage 4**. Step 7 belongs to **Stage 6**. Steps 8–9 belong to **Stage 7**.

| Step | Stage | Goal | Main outputs | Key control question |
|---|---|---|---|---|
| **0. Confirm problem, outcomes & assumptions** | 2 | Ensure the team is solving the right problem and that the desired outcomes, assumptions, exclusions, and success measures are explicit before any scope is drafted | Problem and outcome alignment captured in the Initiative Definition Document or Work Brief | Are we solving the right problem? |
| **1. Select active domains, depth & Acceptance Authorities** | 2 | Decide which deliverable domains need active deliverables and at what depth; name the Acceptance Authority for each; record authorization-level acceptance focus and summary cross-domain impacts | Domain activation list with named Acceptance Authorities; acceptance focus and impact summaries inside the Initiative Definition Document | Have we activated all critical areas and named who will accept each domain's deliverables? |
| **2. Define authorized scope via Functional Capabilities** | 2 | Produce the authorization-level scope baseline as atomic Functional Capabilities (FC‑###) | Functional Capabilities with assumptions and exclusions | Is the approved scope clear and free of design detail? |
| **3. Define actor & control model** | 4 | Identify user roles, personas, and access model based on responsibility and least-privilege principles | User Roles, Personas & Access Model | Are roles, access boundaries, and control-sensitive actions explicit? |
| **4. Structure solution into modules & use cases** | 4 | Group behaviors into meaningful Solution Modules (SM‑###) that can be delivered, reviewed, and accepted as units; define supporting Use Case Narratives (UC‑###) | Solution Modules Register, Solution Module Definition files, Use Case Narratives | Can each module be explained, reviewed, built, and accepted as a meaningful unit? |
| **5. Shape readiness in parallel** | 4 | Draft technical and operational domain artifacts alongside module and use case design, so operations, data, security, and adoption considerations influence the design | Draft Technical Design Document, DevOps Guide, Operations & Support Model, Backup, Restore & Recovery Plan, data models, security/privacy notes, adoption plans | What support, security, data, or adoption implications must influence design now? |
| **6. Plan evidence & acceptance** | 4 | For each module and use case, define acceptance criteria, test approach, evidence plan, and defect thresholds | Acceptance criteria, test approach, evidence plan | How will we know that the delivered solution meets the intent and satisfies stakeholders? |
| **7. Build, validate & evidence incrementally** | 6 | Deliver the solution in module-sized increments, validate against use cases and acceptance criteria, and collect evidence | Delivered solution components, evidence records, defect/condition records, Deployed Solution record | Is every delivered behavior evidenced and traceable to the authorized scope? |
| **8. Confirm cross-domain readiness** | 7 | Before formal acceptance, ensure each active domain has addressed its responsibilities and evidence is complete | Readiness package across active domains | Is the work actually ready for acceptance and operational handover? |
| **9. Accept, transition & capture early-life learning** | 7 | Obtain formal acceptance, transfer operational ownership, close the initiative, and capture early-life observations | Formal Acceptance & Closure Record, operational handover confirmation, early-life review note | Does the Acceptance Authority know exactly what is being accepted, and what improvements or lessons should be recorded? |

## 6. Stage 2 – Solution Definition Minimum

Stage 2 defines the initiative clearly enough for an authorization decision – no more, no less. The activities in this section establish the scope baseline, activate the right deliverable domains, and surface key cross-domain implications needed for a sound decision.

Start from the completed Work Assessment handoff. Confirm the baseline problem and outcomes before producing any scope artifacts.

**Do not** use Stage 2 to produce User Roles, Solution Modules, Use Case Narratives, or detailed design. Those belong in Stage 4.

### Step 0: Confirm problem, outcomes & assumptions

Before drafting any Functional Capabilities, ensure the team is solving the right problem. The **Initiative Definition Document** or **Work Brief** must make visible:
- The problem statement: what is wrong, missing, or changing, and why it matters.
- The current state: how things work now and where the gaps are.
- The intended future state: what the situation will look like when the work is done.
- Outcome statement and success measures: how the organization will know the initiative succeeded.
- Key assumptions and constraints.
- Any explicit exclusions – what the solution will not do.
- Affected stakeholders and parties.

If any of these are unclear, return to Stage 2 for clarification. Without this alignment, scope control becomes meaningless.

### Step 1: Select active domains, depth & Acceptance Authorities

Review the [Standard Deliverables Guide](standard_deliverables_guide.md) and ask the domain trigger questions for each domain:
- Does this initiative create, change, or govern data?
- Does it introduce or modify sensitive access, approvals, or compliance exposure?
- Does it create new operational ownership or recovery obligations?
- Does it materially change user behavior, training, or adoption needs?

Activate the domains that matter and decide the minimum viable depth for each. For each active domain:
- Name the **Acceptance Authority** (by name or role) who will formally accept the domain deliverables.
- Record at summary level what **"done"** broadly means for that domain (outcome-focused intent, not detailed test language).
- Note what **kind of evidence** will later be needed (for example: test results, sign-off, audit log).

Also capture a brief cross-domain impact summary for each active non-Solution domain inside the Initiative Definition Document:

| Domain | What to capture |
|---|---|
| Operational Readiness | Support ownership, operational change, and any recovery or continuity obligation |
| Data Governance & Records | Data created, changed, or migrated; classification implications; stewardship expectations |
| Security, Privacy & Compliance | Sensitive access, privacy obligations, and regulatory exposure |
| User Adoption & Change Enablement | Users affected, expected behavior change, and high-level enablement needs |

Keep these summaries concise. They exist to support the authorization decision, not to replace domain elaboration. Domain deliverables will be elaborated in Stage 4 (Step 5).

Record all domain activation decisions with rationale. This ensures that operational, data, security, and adoption implications are visible and owned before design begins.

### Step 2: Define authorized scope via Functional Capabilities

Functional Capabilities (FC‑###) are short, unambiguous statements of what the system must enable, written in business language without design detail. Each FC should:
- Be traceable to a problem or outcome from Step 0.
- Be atomic (a single ability).
- Have any assumptions or exclusions stated.
- Not include workflows, screens, technical solution, or actors.

Once approved, FC‑IDs become the baseline that all downstream design artifacts must trace back to. They should not change unless the Stage 2 baseline changes.

**Done when:**
- Each FC can be traced to a problem or outcome.
- The FC set covers all intended business abilities without overlapping or including design detail.
- Assumptions and exclusions are stated.
- Acceptance Authorities are named for the Functional Capabilities.

## 7. Stage 4 – Delivery-Ready Elaboration

Stage 4 translates the authorized Stage 2 baseline into delivery-ready behavioral and technical detail. It elaborates only what was authorized and must not introduce new scope or change approved outcomes.

**Do not** use Stage 4 to create new Functional Capabilities, alter the acceptance structure, or expand domain activation beyond what Stage 2 established. Any material scope change requires a change decision and may require return to Stage 2.

### Step 3: Define actor & control model

Determine who interacts with the solution and why. The **User Roles, Personas & Access Model** document should:
- Identify user roles based on responsibilities, not job titles.
- Define personas if user context affects behavior (for example, novice vs. expert).
- Specify default-deny access rules and least-privilege principles.
- Highlight control-sensitive actions, separation-of-duties needs, and auditability requirements.

If the access model reveals new privileged actions or sensitive data handling not anticipated in Stage 2, activate the Security, Privacy & Compliance domain deliverables if not already active, and record this in the domain activation log.

### Step 4: Structure the solution into modules & use cases

Organize the solution around **Solution Modules (SM‑###)**. A module is a logical grouping of related behaviors that can be delivered, reviewed, and accepted together. For each module, produce:
- A row in the **Solution Modules Register** summarizing its purpose and supporting FC‑IDs.
- A **Solution Module Definition** file (SM‑###) describing the module boundary, included use cases, dependencies, high-level flow, key decisions, risks, and assumptions.
- A set of **Use Case Narratives (UC‑###)** describing each user goal in business language. Use cases should define:
  - Actor goal and trigger.
  - Preconditions and postconditions.
  - Success outcome and alternative paths.
  - Access expectations and auditability.
  - Observable acceptance criteria.

Modules and use cases must not introduce new scope. They are elaborations of the approved FC‑IDs. They enable traceable development and acceptance.

### Step 5: Shape readiness in parallel

As modules and use cases are defined, begin drafting domain-specific deliverables. Examples include:
- **Technical Design Document** – architecture, component design, technology choices, patterns, high-level data flows.
- **DevOps Guide** – CI/CD pipelines, environment setup, configuration and secret management, monitoring and alerting.
- **Operations & Support Model** – support roles, monitoring procedures, escalation paths, contact points.
- **Backup, Restore & Recovery Plan** – data protection strategy, RPO/RTO targets, test procedures.
- **Data Models and Governance Artifacts** – data flows, classifications, stewardship, retention.
- **Security & Privacy Artifacts** – threat models, control designs, compliance mapping.
- **User Adoption & Change Enablement Plans** – training, communications, enablement materials.

Drafting these in parallel ensures that technical, operational, data, security, and adoption requirements shape module design rather than being bolted on later.

### Step 6: Plan evidence & acceptance

For each module and use case, plan how acceptance will be demonstrated. Determine:
- **Acceptance criteria** – observable statements tied to use case outcomes and control requirements.
- **Test approach** – unit tests, integration tests, end-to-end tests, security tests, performance tests.
- **Evidence plan** – what evidence will be collected (test results, screen captures, system logs, audit trails), where it will be stored, and how it will be linked to FC‑IDs, SM‑IDs, and UC‑IDs.
- **Defect/condition thresholds** – what constitutes a blocker or condition for acceptance.

Document these plans to guide the delivery team and to avoid last-minute guessing about what constitutes "done".

## 8. Delivery, Acceptance & Closure

### Step 7: Build, validate & evidence incrementally

Execute development in module-sized increments:
- Build the module according to the design.
- Validate it against the related use cases and acceptance criteria.
- Collect evidence as the work progresses.
- Record any defects or conditions and address them.
- Update the **Deployed Solution** record with version, configuration, and environment details.

This iterative approach makes progress visible and prevents large unreviewed drops. Modules may be delivered concurrently or sequentially depending on dependencies.

### Step 8: Confirm cross-domain readiness

Before seeking formal acceptance, run a cross-domain readiness checkpoint. For each active domain:
- **Solution** – are all delivered behaviors traceable to FC‑IDs and evidenced? Are defects closed or accepted?
- **Operational Readiness** – are support roles identified? Are monitoring and runbooks in place? Are backup and recovery procedures tested?
- **Data Governance & Records** – are data models approved? Are data migration and retention plans executed?
- **Security, Privacy & Compliance** – have controls been implemented and tested? Are audit and access logs enabled?
- **User Adoption & Change Enablement** – are users trained? Are enablement materials delivered?

If any domain is not ready, return to Step 5 and close gaps. Only proceed when the readiness package is complete.

### Step 9: Accept, transition & capture early-life learning

Formal acceptance must be given by the named **Acceptance Authority**. The **Formal Acceptance & Closure Record** should link each deliverable (FC‑IDs, SM‑IDs, UC‑IDs) to evidence demonstrating compliance with acceptance criteria. After acceptance:
- Transfer operational ownership and confirm the handover with an **operational handover confirmation** documented in the relevant Operational Readiness artifacts (for example, the Operations & Support Model or runbooks).
- Close the work with the **Formal Acceptance & Closure Record** summarizing outcomes, residual actions, and lessons.
- For initiatives with material operational or behavioral change, conduct an early-life review after a defined period (for example, 30–60 days). Capture observations, support tickets, user feedback, and improvement opportunities. Record them to inform future iterations or enhancements.

## 9. What Not To Do

| Do not | Why |
|---|---|
| Turn Stage 2 into delivery-ready behavior design | Stage 2 must remain decision-ready, not design-heavy. Detailed behavior belongs in Stage 4 |
| Produce User Roles, Modules, or Use Cases in Stage 2 | These are Stage 4 elaboration artifacts. Producing them early bypasses authorization controls and creates untraceable scope |
| Use modules or use cases to introduce hidden scope | Modules and use cases must elaborate only the approved FC‑IDs. New scope requires a change to the Stage 2 baseline |
| Elaborate non-required domain deliverables before authorization | Only produce what is needed for a sound authorization decision. Premature elaboration wastes effort and can obscure actual scope |
| Replace the Initiative Definition Document with downstream design artifacts | The Initiative Definition Document is the authorization baseline. Downstream artifacts trace to it, not the other way around |
| Let AI invent scope, assign Acceptance Authorities, or mark work complete | AI may assist with drafting, summarizing, and traceability checks. Humans remain accountable for every decision. If control inputs are missing, label the output as a working draft |

## 10. Traceability and Numbering

The traceability path for solution work is:

`Work Assessment → Initiative Definition / Work Brief → domain selection and deliverable map → Functional Capabilities (FC‑###) → Stage 4 actor / module / use case elaboration → technical and operational artifacts → delivery evidence → Deployed Solution → Formal Acceptance & Closure Record`

Assign stable identifiers:
- **FC‑###** for Functional Capabilities.
- **SM‑###** for Solution Modules.
- **UC‑###** for Use Case Narratives.

Optionally, teams may define local identifiers (not part of the core Work Delivery numbering scheme), for example:
- **TS‑###** for test scripts or test suites (if used).
- **EV‑###** for evidence records (if used).

Each artifact should reference the IDs it supports. Modules and use cases must link back to FC‑IDs. Evidence must link back to FC‑IDs, SM‑IDs, and UC‑IDs. This ensures traceability from approval through design to acceptance.

## 11. AI-Assisted Authoring Guidance

Use AI to:
- Draft Functional Capabilities, modules, and use cases from structured inputs.
- Transform, translate, and summarize existing specifications.
- Generate bullet lists of risks, assumptions, dependencies, and test cases.
- Check whether scope is being expanded inadvertently.
- Produce tables linking FC‑IDs to modules, use cases, and tests.
- Highlight ambiguous or conflicting statements in drafts.

**Do not** use AI to:
- Invent new scope, requirements, user roles, or acceptance criteria.
- Decide which deliverables or domains are needed.
- Assign or change Acceptance Authorities without instruction.
- Provide final acceptance or evidence.
- Hide or overwrite source material.
- Present output as approved when control inputs are missing; label it as a working draft instead.

Follow the [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md) at all times.

## 12. Change Control

If the authorized scope (Functional Capabilities) or high-level outcomes must change, return to the appropriate work stage:
- Minor changes may be handled in Stage 4 if they do not alter outcomes, acceptance criteria, budgets, or schedules. Document the change with decision records.
- Material changes require a major change decision, documented in a decision record, and may send the initiative back to Stage 2 for redefinition and authorization.
- All changes must be recorded with decision authority, rationale, and effect on scope, cost, time, and risk.

---

This process ensures that solution design is **outcome-aligned, risk-based, traceable, supportable, and human-comprehensible**. Use it flexibly; scale the depth of each step to the size and risk of the work; always maintain the core principles of scope control and formal acceptance.
