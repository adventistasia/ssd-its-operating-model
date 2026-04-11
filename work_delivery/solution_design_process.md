# Solution Design Process

Status: working draft

## Purpose

This document shows how solution design work should be done inside the Work Delivery Framework, without drifting into design too early or skipping required controls.

It helps Delivery Owners and solution leads keep design work stage-appropriate (Stage 2 is decision-ready; Stage 4 is delivery-ready).

## Start Here

Use this document for:

- routing solution design work to the correct stage (Stage 2 vs Stage 4)
- choosing what to define now vs what to defer
- linking solution deliverables to acceptance and evidence early
- routing overall day-to-day delivery control back to the [Delivery Owner Runbook](delivery_owner_runbook.md)

Do not use this document for:

- using Stage 2 to create detailed design, module decomposition, or build plans
- treating Stage 5 as extra design time (Stage 5 is readiness and operating rhythm)

### Quick Navigation

| If you need to... | Start here |
| --- | --- |
| Know what design work is allowed in Stage 2 | [Where This Process Fits](#2.%20Where%20This%20Process%20Fits) and [Stage 2 - Guidance](#4.%20Stage%202%20-%20Guidance) |
| Know what design work happens in Stage 4 | [Steps at a Glance](#3.%20Steps%20at%20a%20Glance) and Step 3-6 in the table |
| Prevent scope creep during elaboration | [Boundary Rule Between Stage 4 and Stage 5](#3.1.%20Boundary%20Rule%20Between%20Stage%204%20and%20Stage%205) |

## Use This When

- the work is in Stage 2 (Work Definition) or Stage 4 (Work Definition Details)
- the initiative needs solution deliverables (capabilities, roles, modules, use cases, NFRs, integrations)
- you need acceptance and evidence to be defined early enough to avoid late-stage disputes

## What You Need First

Before using this process, confirm:

- the current stage is Stage 2 or Stage 4 (if not, return to the Work Delivery Framework)
- a named Delivery Owner and Solution Lead / owner for solution deliverables
- a working scope boundary (Stage 2) or authorized baseline (post-Stage 3)
- the active deliverable domains and named Acceptance Authorities per domain

## What To Do

1. Stage 2: confirm the problem and outcomes, select active domains, define Functional Capabilities, and keep it decision-ready.
2. Stage 4: elaborate roles/access, modules, use cases, and cross-domain artifacts only within authorized scope.
3. Define acceptance focus and evidence expectations early and keep them linked as delivery progresses.

## Minimum Required Content

Keep these visible at the appropriate level:

- problem and intended outcomes
- Functional Capabilities (traceable to outcomes)
- active deliverable domains with Acceptance Authorities
- acceptance focus and evidence expectations per domain

## Who Is Involved

| Role | What they do |
| ---- | ------------ |
| Delivery Owner | Ensures stage discipline and keeps definition decision-ready / elaboration scope-controlled |
| Solution Lead / solution deliverable owners | Produce and maintain solution deliverables and cross-domain alignment |
| Acceptance Authorities | Define what acceptance means and provide explicit sign-off by domain |
| Outcome Owner / Sponsor | Confirm the solution is solving the right problem |

## Required Checks

Confirm:

- Stage 2 stays decision-ready and does not become detailed design
- Stage 4 elaborates only what was authorized (no silent scope expansion)
- acceptance and evidence are defined early enough to guide design and testing

## Related Documents

- [Work Delivery Framework](work_delivery_framework.md)
- [Standard Deliverables Guide](standard_deliverables_guide.md)
- [Deliverable Specifications Index](deliverable_specifications_index.md)
- [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md)

## More Detail

## 1. Purpose

This process governs solution design across the [Work Delivery Framework](work_delivery_framework.md). It runs at two levels:

- **Stage 2 - Work Definition:** confirm the problem, select the active deliverable domains, define what the solution must do (Functional Capabilities), note what "done" means per domain, and flag cross-domain impacts. Keep this decision-ready, not design-heavy.
- **Stage 4 - Work Definition Details:** define who uses the solution and how, structure it into modules and use cases, start domain-specific design work, and plan testing and acceptance. Elaborate only what was authorized.

Use it together with:
- [Work Delivery Framework](work_delivery_framework.md)
- [Standard Deliverables Guide](standard_deliverables_guide.md) - which domains apply and what deliverables each needs
- [Deliverable Specifications Index](deliverable_specifications_index.md) - individual deliverable specs
- [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md)

For larger engineering initiatives, this process also supports the simpler four-phase operating view used in the Work Delivery Framework:

- **Assess** = Stage 1
- **Define and Authorize** = Stages 2-3
- **Elaborate and Mobilize** = Stages 4-5
- **Deliver, Accept and Close** = Stages 6-7

## 2. Where This Process Fits

| Stage | Stage name | Solution design work at this stage |
|---|---|---|
| **2** | Work Definition | Confirm problem and outcomes; select active domains; define Functional Capabilities; note acceptance focus and cross-domain impacts per domain |
| **3** | Work Authorization | Present the authorization package; no design work |
| **4** | Work Definition Details | Define roles and access; structure modules and use cases; start domain-specific artifacts; plan testing and acceptance |
| **5** | Delivery Mobilization | Confirm readiness to execute; finalize artifact set; no scope changes |
| **6** | Work Delivery | Build, test, and collect evidence module by module |
| **7** | Acceptance, Transition & Closure | Check each domain is ready; obtain formal acceptance; hand over ownership; close and capture lessons |

### 2.1. Default Engineering Path for Larger Initiatives

For larger engineering initiatives, use this process through the four-phase operating view:

| Four-phase view | What solution teams should focus on |
| --- | --- |
| **Assess** | Confirm the work is worth defining. No solution design yet beyond what assessment needs. |
| **Define and Authorize** | Confirm problem and outcomes, select active deliverable domains, define Functional Capabilities, and support the authorization decision without drifting into detailed design. |
| **Elaborate and Mobilize** | Produce delivery-ready design, modules, use cases, domain artifacts, testing and evidence approach, then activate the execution controls and initial task breakdown needed to start controlled delivery. |
| **Deliver, Accept and Close** | Deliver module by module, collect evidence, confirm readiness across active domains, obtain acceptance, hand over, and close. |

This simpler view is for navigation and operating clarity.

The stage numbers remain authoritative for control and artifact discipline.

## 3. Steps at a Glance

Steps 0 - 2 = **Stage 2**. Steps 3 - 6 = **Stage 4**. Step 7 = **Stage 6**. Steps 8 - 9 = **Stage 7**.

| Step | Stage | What to do | What to produce |
|---|---|---|---|
| **0. Confirm problem & outcomes** | 2 | Confirm the team is solving the right problem before writing any scope | Problem statement, current and future state, success measures, assumptions, exclusions - inside the Initiative Definition Document or Work Brief |
| **1. Select domains & name Acceptance Authorities** | 2 | Decide which domains are active and how deep each needs to go; name who accepts each domain's output; note what "done" means and what evidence will be needed | Domain list with Acceptance Authorities and brief acceptance notes - inside the Initiative Definition Document |
| **2. Define scope (Functional Capabilities)** | 2 | Write atomic business ability statements (FC-###) traceable to outcomes from Step 0 | Functional Capabilities with assumptions and exclusions |
| **3. Define roles & access** | 4 | Identify who uses the solution; define access boundaries and control rules | User Roles, Personas & Access Model |
| **4. Structure modules & use cases** | 4 | Group behaviors into modules (SM-###) and describe each user goal as a use case (UC-###) | Solution Modules Register, Solution Module Definitions, Use Case Narratives |
| **5. Start domain work alongside design** | 4 | Draft technical, operational, data, security, and adoption artifacts as modules are defined - not after | Technical Design Document, DevOps Guide, Operations & Support Model, Backup, Restore & Recovery Plan, data and security artifacts, adoption plans |
| **6. Plan testing & acceptance** | 4 | For each module and use case, define what success looks like and how it will be evidenced | Acceptance criteria, test approach, evidence plan |
| **7. Build, test & collect evidence** | 6 | Deliver in module-sized increments; validate against use cases; collect evidence; record defects | Delivered components, evidence records, Deployed Solution record |
| **8. Check readiness across all domains** | 7 | Confirm every active domain has met its obligations before seeking formal acceptance | Readiness confirmation across active domains |
| **9. Accept, hand over & close** | 7 | Obtain formal acceptance; confirm operational handover; close the initiative; capture early-life observations | Formal Acceptance & Closure Record, operational handover confirmation, early-life review note |

### 3.1. Boundary Rule Between Stage 4 and Stage 5

Stage 4 and Stage 5 sit in the same simplified operating phase, but they do different work:

- Stage 4 creates delivery-ready design and acceptance-ready elaboration.
- Stage 5 confirms execution readiness, team cadence, trackers, escalation path, and the initial execution plan.
- Stage 5 must not be used to continue unresolved design work except for minor completion items that do not change scope.

## 4. Stage 2 - Guidance

Start from the completed Work Assessment. Do not start design until the problem is clear.

**Do not** use Stage 2 to produce User Roles, Solution Modules, Use Case Narratives, or detailed design. Those belong in Stage 4.

### Step 0: Confirm problem & outcomes

**Do:** Confirm the team is solving the right problem before drafting any scope.

**Produce** (inside the Initiative Definition Document or Work Brief):
- Problem statement - what is wrong, missing, or changing, and why it matters
- Current state and intended future state
- Outcome statement and measurable success criteria
- Key assumptions, constraints, and explicit exclusions
- Affected stakeholders

**Do not:** Start drafting Functional Capabilities until outcomes and exclusions are agreed.

**Done when:** The problem, intended outcomes, key assumptions, and exclusions are visible and agreed.

---

### Step 1: Select domains & name Acceptance Authorities

**Do:** Review the [Standard Deliverables Guide](standard_deliverables_guide.md). For each domain, ask:
- Does this initiative create, change, or govern data?
- Does it introduce or modify sensitive access, approvals, or compliance obligations?
- Does it create new operational ownership or recovery obligations?
- Does it change how people work or what training they need?

For each active domain:
- Name the **Acceptance Authority** (by name or role).
- Note what **"done"** broadly means for that domain.
- Note what **kind of evidence** will later be needed.

Also capture a brief impact note per active non-Solution domain:

| Domain | What to capture |
|---|---|
| Operational Readiness | Support ownership, operational change, recovery obligations |
| Data Governance & Records | Data created, changed, or migrated; classification; stewardship |
| Security, Privacy & Compliance | Sensitive access, privacy obligations, regulatory exposure |
| User Adoption & Change Enablement | Users affected, expected behavior change, enablement needs |

**Do not:** Over-elaborate. These notes support the authorization decision; they are not domain deliverables.

**Done when:** Active domains are identified, Acceptance Authorities are named, and brief acceptance notes and impact notes are recorded.

---

### Step 2: Define scope (Functional Capabilities)

**Do:** Write atomic business ability statements in plain language. Each FC-### should:
- Trace to a problem or outcome from Step 0
- State a single ability the solution must provide
- List any assumptions or exclusions
- Stay free of workflows, screens, technical design, and actor detail

**Do not:** Include design detail, user behavior, or system behavior in Functional Capabilities.

**Done when:**
- Each FC traces to a problem or outcome
- The FC set covers all intended scope without overlapping or including design
- Assumptions and exclusions are stated
- Acceptance Authorities are named

---

## 5. Stage 4 - Guidance

Stage 4 turns the approved scope into design and build artifacts. Elaborate only what was authorized.

**Do not** introduce new Functional Capabilities, change approved outcomes, or expand domain activation without a change decision.

### Step 3: Define roles & access

**Do:** Produce the **User Roles, Personas & Access Model**:
- Identify roles based on responsibilities, not job titles
- Define personas where user context affects behavior
- Apply default-deny and least-privilege access rules
- Flag control-sensitive actions and separation-of-duties requirements

**Do not:** Let access boundaries drift into new scope. If Step 3 reveals sensitive data handling or access not anticipated in Stage 2, record it in the domain activation log.

**Done when:** Roles, personas, and access boundaries are defined and traceable to approved scope.

---

### Step 4: Structure modules & use cases

**Do:** Organize the solution into **Solution Modules (SM-###)**. For each module, produce:
- A row in the **Solution Modules Register** (purpose and FC-IDs supported)
- A **Solution Module Definition** (SM-###) covering module boundary, included use cases, dependencies, flow, decisions, risks, and assumptions
- **Use Case Narratives (UC-###)** for each user goal, covering: actor, trigger, preconditions, success outcome, alternative paths, access expectations, and acceptance criteria

**Do not:** Use modules or use cases to add scope. They elaborate approved FC-IDs only.

**Done when:** Every module traces to approved FC-IDs; every use case traces to a module; use cases have observable acceptance criteria.

---

### Step 5: Start domain work alongside design

**Do:** Begin domain-specific artifacts as modules are defined - not after. Examples:
- **Technical Design Document** - architecture, components, technology choices, data flows
- **DevOps Guide** - CI/CD, environment setup, config and secret management, monitoring
- **Operations & Support Model** - support roles, monitoring, escalation, contact points
- **Backup, Restore & Recovery Plan** - data protection strategy, RPO/RTO, test approach
- **Data and governance artifacts** - data flows, classifications, stewardship, retention
- **Security and privacy artifacts** - threat models, controls, compliance mapping
- **User adoption and change enablement plans** - training, communications, enablement

**Do not:** Leave domain work until after modules are complete. Doing so forces late rework.

**Done when:** Active domain artifacts are drafted and are shaping module design.

---

### Step 6: Plan testing & acceptance

**Do:** For each module and use case, define:
- **Acceptance criteria** - observable statements tied to use case outcomes
- **Test approach** - unit, integration, end-to-end, security, performance tests as needed
- **Evidence plan** - what evidence will be collected, where it will be stored, and how it links to FC-IDs, SM-IDs, and UC-IDs
- **Defect thresholds** - what blocks or conditions acceptance

**Do not:** Leave acceptance planning until late in delivery.

**Done when:** Every module and use case has acceptance criteria and an evidence plan.

---

## 6. Delivery, Acceptance & Closure - Guidance

### Step 7: Build, test & collect evidence

**Do:** Deliver module by module:
- Build to the design
- Validate against use cases and acceptance criteria
- Collect and store evidence as work progresses
- Record and address defects
- Update the **Deployed Solution** record with version, configuration, and environment details

**Done when:** Each module is built, validated, evidenced, and defects are closed or accepted.

---

### Step 8: Check readiness across all domains

**Do:** Before seeking formal acceptance, confirm each active domain is ready:
- **Solution** - all behaviors evidenced and traced to FC-IDs; defects closed or accepted
- **Operational Readiness** - support roles in place; monitoring and runbooks ready; backup and recovery tested
- **Data Governance & Records** - data models approved; migration and retention complete
- **Security, Privacy & Compliance** - controls implemented and tested; audit logs enabled
- **User Adoption & Change Enablement** - users trained; enablement materials delivered

**Do not:** Proceed to acceptance if any active domain has open gaps.

**Done when:** All active domains are ready and the readiness package is complete.

---

### Step 9: Accept, hand over & close

**Do:**
- Obtain formal acceptance from the named **Acceptance Authority**
- Record acceptance in the **Formal Acceptance & Closure Record**, linking each deliverable to evidence
- Confirm operational handover in the relevant Operational Readiness artifacts (for example, the Operations & Support Model or runbooks)
- Close the work in the **Formal Acceptance & Closure Record** with outcomes, residual actions, and lessons
- For initiatives with significant operational or behavior change, conduct an early-life review after 30 - 60 days and record observations

**Done when:** Acceptance is formally given, handover is confirmed, and the work is closed.

---

## 7. What Not To Do

| Do not | Why |
|---|---|
| Turn Stage 2 into detailed design | Stage 2 must be decision-ready. Detailed behavior design belongs in Stage 4 |
| Produce roles, modules, or use cases in Stage 2 | These are Stage 4 artifacts. Producing them in Stage 2 bypasses authorization and creates uncontrolled scope |
| Use modules or use cases to add new scope | They must elaborate approved FC-IDs only. New scope requires a change to the Stage 2 baseline |
| Produce domain deliverables not needed for authorization | Only produce what the decision needs. Over-elaboration wastes effort and obscures scope |
| Replace the Initiative Definition Document with design artifacts | The Initiative Definition Document is the authorization baseline. Design artifacts trace to it |
| Let AI define scope, assign Acceptance Authorities, or mark work complete | AI assists with drafting, summarizing, and traceability. If control inputs are missing, label the output as a working draft |

## 8. Traceability

`Work Assessment -> Initiative Definition / Work Brief -> domain selection -> Functional Capabilities (FC-###) -> roles / modules (SM-###) / use cases (UC-###) -> domain artifacts -> evidence -> Deployed Solution -> Formal Acceptance & Closure Record`

Use stable IDs:
- **FC-###** - Functional Capabilities
- **SM-###** - Solution Modules
- **UC-###** - Use Case Narratives

Each artifact references the IDs it supports. Modules and use cases link back to FC-IDs. Evidence links to FC-IDs, SM-IDs, and UC-IDs.

Teams may optionally define local IDs (not part of the core scheme), for example **TS-###** for test scripts or **EV-###** for evidence records.

## 9. AI-Assisted Authoring

**Use AI to:**
- Draft Functional Capabilities, modules, and use cases from structured inputs
- Summarize and transform existing specifications
- Generate lists of risks, assumptions, dependencies, and test cases
- Check whether scope is drifting from the approved baseline
- Produce traceability tables linking FC-IDs to modules, use cases, and tests

**Do not use AI to:**
- Invent scope, requirements, or acceptance criteria
- Decide which domains or deliverables are needed
- Assign or change Acceptance Authorities
- Mark work as accepted or evidence as complete
- Present a draft as approved - label it as a working draft if control inputs are missing

See the [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md) for full guidance.

## 10. Change Control

- **Minor changes** that do not alter outcomes, acceptance criteria, budgets, or schedules may be handled in Stage 4 with a decision record.
- **Material changes** require a major change decision, documented in a decision record, and may send the initiative back to Stage 2 for redefinition and authorization.
- All changes must be recorded with decision authority, rationale, and effect on scope, cost, time, and risk.




