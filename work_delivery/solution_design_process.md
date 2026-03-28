# Solution Design Process

## 1. Purpose

This Solution Design Process is the Stage 4 path of the **Work Delivery Framework**. It translates an approved intent (Stage 2 scope baseline and Stage 3 authorization) into a delivery-ready design without expanding scope. It is a **governance process**, not a brainstorming session. Each step ensures the solution remains traceable to its authorized scope, is supportable and secure, and is described in a way that non‑technical stakeholders can understand.

Use it together with:
- The [Work Delivery Framework](work_delivery_framework.md), which defines the seven stages of work from intake to closure.
- The [Standard Deliverables Guide](standard_deliverables_guide.md) and [Deliverable Specifications Index](deliverable_specifications_index.md), which explain the deliverable domains (Solution, Operational Readiness, Data Governance, Security/Privacy/Compliance, User Adoption) and when each deliverable is needed.
- The deliverable specifications files in `work_delivery`, especially **Functional Capabilities**, **Solution Modules**, **Use Case Narratives**, **Solution Module Definition**, **User Roles, Personas & Access Model**, **Operations & Support Model**, **Technical Design Document**, **DevOps Guide**, **Acceptance Record**, and others.
- The [AI Assisted Authoring Standard](ai_assisted_authoring_standard.md), which defines how AI tools may assist with drafting, summarizing and traceability without becoming decision‑makers.

## 2. Why this process matters

1. **Scope control** – All design artifacts must trace back to the approved Stage 2 baseline. You must not quietly add features or change outcomes.  
2. **Traceability** – Each behavior, module and test must map back to a **Functional Capability (FC‑###)**. Each delivered component must be evidenced and accepted.  
3. **Clarity** – Design documents are written for business owners, testers, operations, and auditors – not just developers.  
4. **Supportability** – Operations, data, security, and user adoption concerns must shape the design, not react to it.  
5. **Evidence** – Acceptance criteria and evidence requirements are defined early so that delivery can be verified later.  
6. **Responsible AI** – AI may draft documents, transform and summarise content, but it cannot invent scope, invent evidence or approve acceptance. Humans remain accountable.

## 3. Overview of the process

The process is organised into iterative, risk‑based steps. Not every step or deliverable is needed for every initiative. Use the **Standard Deliverables Guide** to decide which domains and artifacts are required based on size, risk and complexity.

### Step summary

| Step | Goal | Main outputs | Key control question |
|---|---|---|---|
| **0. Confirm problem, outcomes & assumptions** | Ensure the team is solving the right problem and that the desired outcomes, assumptions, exclusions and success measures are explicit before any scope is drafted | Outcome alignment note inside the Initiative Definition or Work Brief | Are we solving the right problem? |
| **1. Select domains & depth** | Decide which delivery domains (Solution, Operational Readiness, Data Governance, Security/Privacy/Compliance, User Adoption) need active deliverables and at what depth | A visible list of active domains with minimum viable depth | Have we activated all critical areas, not just build work? |
| **2. Define the authorized scope** | Translate the Stage 2 baseline into atomic **Functional Capabilities (FC‑###)** that state what the solution must enable without including behavior detail | Functional Capabilities with assumptions and exclusions | Is approved scope clear and free of design detail? |
| **3. Define actor & control model** | Identify the user roles, personas, and access model based on responsibility and least‑privilege principles | User Roles, Personas & Access Model | Are roles, access boundaries, and control‑sensitive actions explicit? |
| **4. Structure solution into modules** | Group behaviors into meaningful **Solution Modules (SM‑###)** that can be delivered, reviewed and accepted as units; define boundaries and supporting **Use Case Narratives (UC‑###)** | Solution Modules Register, Solution Module Definition files, Use Case Narratives | Can each module be explained, reviewed, built and accepted as a meaningful unit? |
| **5. Shape readiness in parallel** | Draft technical and operational domain artifacts in parallel with module and use case design, so that operations, data, security and adoption considerations influence the design rather than react to it | Draft Technical Design Document, DevOps Guide, Operations & Support Model, Backup/Restore/Recovery plan, Data models, Security/privacy notes, Adoption plans | What support, security, data or adoption implications must influence design now? |
| **6. Plan evidence & acceptance** | Determine for each module and use case how acceptance will be demonstrated and what evidence will be collected, and design the testing approach accordingly | Acceptance criteria, test approach, evidence plan | How will we know that the delivered solution meets the intent and satisfies stakeholders? |
| **7. Build, validate & evidence incrementally** | Deliver the solution in module‑sized increments, validate behavior against use cases and acceptance criteria, collect evidence and update the **Deployed Solution** record | Delivered solution components, evidence logs, defect/condition records | Is every delivered behavior evidenced and traceable to the authorized scope? |
| **8. Confirm cross‑domain readiness** | Before formal acceptance, ensure that each active domain (Solution, Operational Readiness, Data, Security/Privacy/Compliance, User Adoption) has addressed its responsibilities and that evidence is complete | Readiness package across active domains | Is the work actually ready for acceptance and operational handover? |
| **9. Accept, transition & capture early‑life learning** | Obtain formal acceptance from the named Acceptance Authority, transfer operational ownership, close the initiative, and capture early life observations for future improvement | Acceptance Record, Transition/handover confirmation, Closure record, Early‑life review note | Does the Acceptance Authority know exactly what is being accepted, and what improvements or lessons should be recorded? |

### How to use the steps

- **Tailor depth**. For low‑risk or small enhancements, steps 0 and 1 may be combined into a quick discussion recorded in the Work Brief. Modules may be simple features; use cases may be short bullet points.  
- **Iterate**. Steps 3–7 repeat in loops: draft roles and modules, review, build a module slice, collect evidence, refine design, then proceed to the next module.  
- **Activate domains as needed**. If the solution involves sensitive data or external integrations, the Data Governance and Security/Privacy domains become active; if new operations or support processes are required, the Operational Readiness domain is active; if user change is significant, the User Adoption domain is active.  
- **Plan evidence early**. Do not wait until delivery to think about testing. The acceptance criteria and evidence plan should be part of the design.  
- **Keep artefacts human‑readable**. Write design documents in plain language, referencing FC‑IDs, SM‑IDs and UC‑IDs rather than technical jargon. Summaries and tables should help non‑technical stakeholders understand the solution.  
- **Use AI responsibly**. AI tools can draft, transform, translate and summarise documents; they can propose lists of modules or use cases; they can check traceability; they can generate test cases. They must not define scope, decide acceptance, or invent evidence. Always check AI output for accuracy and alignment with the authorized baseline.

## 4. Detailed guidance by step

### Step 0: Confirm problem, outcomes & assumptions

Before drafting any Functional Capabilities, the team must ensure that the work is addressing the right problem. The **Initiative Definition Document** or **Work Brief** must make visible:
- The problem statement and why it matters.
- The intended outcomes and success measures.
- Key assumptions and constraints.
- Any explicit exclusions (what the solution will not do).
- Stakeholders and affected parties.

If any of these are unclear, return to Stage 2 for clarification. Without this alignment, scope control becomes meaningless.

### Step 1: Select domains & depth

Review the **Standard Deliverables Guide** and ask the domain trigger questions:
- Does this initiative create or alter governed data?  
- Does it introduce or modify sensitive access, approvals or compliance exposure?  
- Does it create new operational ownership or recovery obligations?  
- Does it materially change user behavior, training or adoption needs?  

Activate the domains that matter and decide the minimum viable depth for each. Record the decision along with rationale. This ensures that operational, data, security and adoption considerations influence the design.

### Step 2: Define the authorized scope via Functional Capabilities

Functional Capabilities (FC‑###) are short, unambiguous statements of what the system must enable, written in business language without design detail. Each FC should:
- Be traceable to a problem or outcome.
- Be atomic (a single ability).
- Have any assumptions or exclusions stated.
- Not include workflows, screens, technical solution, or actors.

Once approved, FC‑IDs become the baseline that all downstream design artifacts must trace back to. They should not change unless the Stage 2 baseline changes.

### Step 3: Define actor & control model

Determine who interacts with the solution and why. The **User Roles, Personas & Access Model** document should:
- Identify user roles based on responsibilities, not job titles.
- Define personas if user context affects behavior (e.g., novice vs. expert).
- Specify default‑deny access rules and least‑privilege principles.
- Highlight control‑sensitive actions, separation‑of‑duties needs, and auditability requirements.

If the access model introduces new privileged actions or sensitive data handling, activate the Security/Privacy/Compliance domain deliverables such as data classification and control designs.

### Step 4: Structure the solution into modules and use cases

Organize the solution around **Solution Modules (SM‑###)**. A module is a logical grouping of related behaviors that can be delivered, reviewed and accepted together. For each module, produce:
- A row in the **Solution Modules Register** summarizing its purpose and supporting FC‑IDs.
- A **Solution Module Definition** file (SM‑###) that describes the module boundary, included use cases, dependencies, high‑level flow, key decisions, risks and assumptions.
- A set of **Use Case Narratives (UC‑###)** that describe each user goal in business language. Use cases should define:
  - Actor goal and trigger.
  - Preconditions and postconditions.
  - Success outcome and alternative paths.
  - Access expectations and auditability.
  - Observable acceptance criteria.

Modules and use cases must not introduce new scope. They are elaborations of the approved FC‑IDs. They enable traceable development and acceptance.

### Step 5: Shape readiness in parallel

As modules and use cases are defined, begin drafting domain‑specific deliverables. Examples include:
- **Technical Design Document** – architecture, component design, technology choices, patterns, high‑level data flows.
- **DevOps Guide** – CI/CD pipelines, environment setup, configuration and secret management, monitoring and alerting.
- **Operations & Support Model** – roles and responsibilities for support, monitoring procedures, escalation paths, contact points.
- **Backup, Restore & Recovery Plan** – data protection strategy, RPO/RTO targets, test procedures.
- **Data Models and Governance Artifacts** – data flows, classifications, stewardship, retention.
- **Security & Privacy Artifacts** – threat models, control designs, compliance mapping.
- **User Adoption & Change Enablement Plans** – training, communications, enablement materials.

Drafting these in parallel ensures that technical, operational, data, security and adoption requirements shape module design rather than being bolted on later.

### Step 6: Plan evidence & acceptance

For each module and use case, plan how acceptance will be demonstrated. Determine:
- **Acceptance criteria** – observable statements tied to use case outcomes and control requirements.
- **Test approach** – unit tests, integration tests, end‑to‑end tests, security tests, performance tests.
- **Evidence plan** – what evidence will be collected (test results, screen captures, system logs, audit trails), where it will be stored, and how it will be linked to FC‑IDs, SM‑IDs and UC‑IDs.
- **Defect/condition thresholds** – what constitutes a blocker or condition for acceptance.

Document these plans to guide the delivery team and to avoid last‑minute guessing about what constitutes “done”.

### Step 7: Build, validate & evidence incrementally

Execute development in module‑sized increments:
- Build the module according to the design.
- Validate it against the related use cases and acceptance criteria.
- Collect evidence as the work progresses.
- Record any defects or conditions and address them.
- Update the **Deployed Solution** record with version, configuration and environment details.

This iterative approach makes progress visible and prevents large unreviewed drops. Modules may be delivered concurrently or sequentially depending on dependencies.

### Step 8: Confirm cross‑domain readiness

Before seeking formal acceptance, run a cross‑domain readiness checkpoint. For each active domain:
- **Solution** – are all delivered behaviors traceable to FC‑IDs and evidenced? Are defects closed or accepted?  
- **Operational Readiness** – are support roles identified? Are monitoring and runbooks in place? Are backup and recovery procedures tested?  
- **Data Governance** – are data models approved? Are data migration and retention plans executed?  
- **Security/Privacy/Compliance** – have controls been implemented and tested? Are audit and access logs enabled?  
- **User Adoption** – are users trained? Are enablement materials delivered?  

If any domain is not ready, return to Step 5 and close gaps. Only proceed when the readiness package is complete.

### Step 9: Accept, transition & capture early‑life learning

Formal acceptance must be given by the named **Acceptance Authority**. The **Acceptance Record** should link each deliverable (FC‑IDs, SM‑IDs, UC‑IDs) to evidence demonstrating compliance with acceptance criteria. After acceptance:
- Transfer operational ownership and confirm the handover with a **Transition Record**.
- Close the work with a **Closure Record** summarizing outcomes, residual actions and lessons.
- For initiatives with material operational or behavioral change, conduct an early‑life review after a defined period (e.g., 30–60 days). Capture observations, support tickets, user feedback and improvement opportunities. Record them to inform future iterations or enhancements.

## 5. Traceability and numbering

Assign stable identifiers:
- **FC‑###** for Functional Capabilities.
- **SM‑###** for Solution Modules.
- **UC‑###** for Use Case Narratives.
- **TS‑###** for test scripts or test suites (if used).
- **EV‑###** for evidence records.

Each artifact should reference the IDs it supports. Modules and use cases must link back to FC‑IDs. Evidence must link back to FC‑IDs, SM‑IDs and UC‑IDs. This ensures traceability from approval through design to acceptance.

## 6. AI‑assisted authoring guidance

Use AI to:
- Draft modules and use cases from supplied Functional Capabilities.
- Transform, translate and summarise existing specifications.
- Generate bullet lists of risks, assumptions, dependencies and test cases.
- Check whether scope is being expanded inadvertently.
- Produce tables linking FC‑IDs to modules, use cases and tests.
- Highlight ambiguous or conflicting statements in drafts.

**Do not** use AI to:
- Invent new scope, requirements, user roles or acceptance criteria.
- Decide which deliverables are needed.
- Provide final acceptance or evidence.
- Hide or overwrite source material.

Follow the [AI Assisted Authoring Standard](ai_assisted_authoring_standard.md) at all times.

## 7. Change control

If the authorized scope (Functional Capabilities) or high‑level outcomes must change, return to the appropriate work stage:
- Minor changes may be handled in Stage 4 if they do not alter outcomes, acceptance criteria, budgets or schedules. Document the change with decision records.
- Material changes require a **Major Change Decision** and may send the initiative back to Stage 2 for redefinition and authorization.
- All changes must be recorded with decision authority, rationale and effect on scope, cost, time and risk.

---

This process ensures that solution design is **outcome‑aligned, risk‑based, traceable, supportable and human‑comprehensible**. Use it flexibly; scale the depth of each step to the size and risk of the work; always maintain the core principles of scope control and formal acceptance.
