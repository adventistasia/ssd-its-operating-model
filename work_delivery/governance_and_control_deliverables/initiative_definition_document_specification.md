# Initiative Definition Document Specification

## 1. What This Artifact Is For

The Initiative Definition Document is the main governance baseline for an initiative. It explains what the initiative is, why it exists, what outcomes it must achieve, what boundaries govern delivery, and what must be delivered for the initiative to be accepted.

A well-written IDD supports authorization, downstream planning, controlled scope change, and final acceptance. It is not a design document, a task plan, or a repository for detailed execution content.

**Approved definition** means the version of the IDD that has been formally authorized as the baseline the initiative will be governed against. All downstream artifacts are tested against this baseline.

## 2. When to Use It

Use this artifact as the default Stage 2 - Work Definition baseline for:

- projects and major enhancements
- planned initiatives that change systems, services, data, security posture, support load, or cost in a material way

For appropriately small, contained, or low-risk work, use a [Work Brief](../work_brief/work_brief_specification.md) instead. Do not force a full IDD when a Work Brief is sufficient.

## 3. Stage Fit and Handoffs

- **Stage 1:** consume the [Work Assessment Report](../work_assessment/work_assessment_report_specification.md) and carry forward the validated need, desired outcomes, major risks, dependencies, and stakeholder context.
- **Stage 2:** draft and baseline this document. It governs scope, deliverables, ownership, and authorization.
- **Stage 3:** use this document as the primary input to the [Project Charter](project_charter_specification.md) authorization decision.
- **Stage 4 onward:** this document governs scope control, deliverable expectations, and acceptance authority throughout delivery and closure.

Upstream source:

- [Work Assessment Report Specification](../work_assessment/work_assessment_report_specification.md)

Downstream artifacts fed by this document:

- [Project Charter Specification](project_charter_specification.md)
- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)
- domain-specific solution, operational readiness, and acceptance artifacts
- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)

## 4. Audience and Context

Write for the full governance audience: Sponsor, Decision Authorities, Outcome Owner, Delivery Owner and team, Acceptance Authorities, operations and support, audit, and future maintainers.

The document must be understandable to leadership and to delivery teams at the same time. Achieve this by using plain language, keeping governance-level content in the IDD, and pointing to specialist artifacts for detail.

## 5. Before You Start

Make sure you have:

- the completed Stage 1 work assessment or equivalent initiation inputs
- a validated business need and intended outcomes
- confirmed or proposed Outcome Owner, Delivery Owner, and Sponsor
- a known or proposed authorization path
- agreed scope boundaries or enough input to draft them
- awareness of material risks, dependencies, and operational impacts

If any of these are missing, label the output as a working draft and state the gaps.

## 6. How to Draft It

1. Start from the Stage 1 outputs. Carry forward the validated need, outcomes, risks, dependencies, and stakeholder context.
2. Write the executive summary first so the document's purpose is clear before writing section by section.
3. Write scope boundaries explicitly - list both in-scope and out-of-scope content. Ambiguous scope becomes a control problem later.
4. Build the deliverables table before writing detailed content. Knowing what must be delivered keeps the rest of the document focused.
5. Write risks, financial implications, and operational support at governance level. Point to detailed artifacts for depth.
6. Use references to downstream artifacts rather than embedding their content here.
7. Review for accountability gaps: every deliverable needs a named Delivery Owner and Acceptance Authority before authorization.

The governing principle: include enough information to make a sound decision and to understand what the initiative is, what it will deliver, who is accountable, and what material implications must be accepted. Put detailed content in separate artifacts and reference them.

## 7. Minimum Structure

### 7.1. Document identity and control

Include:

- initiative name
- initiative or project ID where used
- version and status (Draft, Active, or Final)
- last updated date
- Outcome Owner
- Delivery Owner
- Sponsor
- sponsoring body where different from the Sponsor
- Decision Authorities, including the type of decision each is authorized to make
- authorization record or reference to the formal approval basis
- change log or equivalent version history

### 7.2. Executive summary

Include:

- plain-language description of the initiative
- why the initiative exists now
- intended outcomes
- high-level statement of what will be delivered
- estimated one-time cost or CapEx where applicable
- estimated ongoing annual operating cost or OpEx where applicable
- approved budget and current expenditure position where already available

Write this so a decision-maker can understand the initiative and the scale of commitment being requested without reading further.

### 7.3. Business need and rationale

Include:

- current problem or opportunity
- who is affected
- why action is justified now
- consequences of inaction where relevant

### 7.4. Outcomes and success measures

Include:

- intended outcomes
- measurable success indicators
- important non-goals or things that should not be treated as success

### 7.5. Scope boundaries

Include:

- in-scope content
- out-of-scope content
- assumptions
- key constraints

If functional scope is material to understanding the initiative, include a concise summary of required capabilities or a reference to a separate [Functional Capabilities](../solution_deliverables/functional_capabilities_specification.md) artifact.

This section is the primary boundary control for the initiative. Make it explicit.

### 7.6. Deliverables and acceptance structure

Include:

- required deliverables or Deliverable Domains
- Delivery Owner for each deliverable
- Acceptance Authority for each deliverable or domain
- acceptance focus (what matters for sign-off)
- current status
- note of any deliverables or domains intentionally excluded, deferred, or to be confirmed later, with reason

Recommended table:

| Deliverable or domain | Description | Delivery Owner | Acceptance Authority | Acceptance focus | Status | Reference |
| --- | --- | --- | --- | --- | --- | --- |

When Deliverable Domains are first mentioned, reference the [Standard Deliverables Guide](../standard_deliverables_guide.md) so the reader understands the domain structure being used.

If the IDD is the sole artifact for the initiative, the acceptance focus may be written directly as acceptance criteria.

Use these status values:

- Draft
- Planned
- In Progress
- Delivered
- Accepted

Where applicable, also include: reference to the delivered artifact, reference to supporting evidence, reference to the acceptance record, and acceptance date.

**Control rule:** a deliverable is only accepted when the named Acceptance Authority has formally confirmed that the acceptance focus has been met.

### 7.7. Key risks, dependencies, and major impacts

Include:

- major delivery or feasibility risks
- material dependencies
- major operational, financial, regulatory, security, or support implications
- material assumptions about funding, risk tolerance, service ownership, or organizational readiness that decision-makers are being asked to accept

Where financial detail is relevant, make visible:

- estimated CapEx and OpEx
- approved budget if available
- actual spend and variance if already in flight

### 7.8. Operational support summary

Required when the initiative materially impacts a service or system.

Include only what is needed to show operational sustainability has been considered:

- operational or run owner
- support owner
- intended support tier model and escalation path at summary level
- monitoring and recovery intent at summary level
- expected ongoing support effort or cost impact
- reference to the relevant operational readiness artifact where detailed support arrangements will be maintained

Link to the supporting operational readiness material. Do not restate detailed support content here.

### 7.9. Related references and supporting decisions

Include:

- links to upstream assessments
- key policy or strategy references
- standards used where relevant
- related initiatives or dependencies
- relevant decision or approval records
- contracts, licensing, or external references that materially shape scope or obligations

## 8. What to Keep Out

Keep the following out of this document:

- detailed architecture and configuration
- full runbooks or procedures
- detailed test scripts
- sprint or task plans
- repeated copies of downstream deliverables
- detailed risk register entries better managed elsewhere
- technical specifications beyond what is needed to understand scope, risk, or approval implications

## 9. Writing Rules

- Write at governance level. Make decisions and commitments clear, not activity detail.
- Use plain language. Write for a reader who understands the business but not the technical specifics.
- Be explicit about scope. "In scope" and "out of scope" must leave no room for different interpretations.
- Use references, not copies. Point to separate artifacts for design, plans, and detailed content.
- Name owners. Every deliverable, risk, condition, and accountability must have a named person.
- Use the deliverables table. Structured rows are easier to review and maintain than prose lists.
- Keep financial and operational implications at the summary level needed for governance decisions.
- For small initiatives where all content fits here, keeping everything in one document is acceptable. Readability and governability are the tests.

## 10. Traceability and Ownership Minimum

**Upstream:** this document should be created from the completed Stage 1 work assessment outputs and any other initiation inputs that affect scope, ownership, risk, or deliverables.

**Downstream:** this document anchors the Project Charter, Functional Capabilities, domain-specific solution and operational readiness deliverables, decision records, and final acceptance and closure records.

**Work Briefs under this document:** where delivery is broken into smaller controlled work items, the IDD may anchor child Work Briefs. Those Work Briefs must stay within the initiative's approved scope, ownership, and authorization boundaries.

**Project Charter alignment:** the Project Charter must not contradict this document. If authorization, funding, scope, ownership, or required deliverables change materially, update this document first or in controlled parallel with the related governance decision.

**Ownership:**

- The Delivery Owner coordinates the document with input from the Outcome Owner and Sponsor.
- Key owners and Decision Authorities review before authorization.
- Formal approval normally sits with the Sponsor or delegated Decision Authority, with the approval reference recorded in the document control section.

## 11. Maintenance Expectations

This is a living governance document. Keep it current across the full initiative lifecycle.

**At minimum, keep current:**

- deliverable status and references
- change log for material updates
- authorization and decision references
- major cost, risk, and support implications at governance level

**Change control rule:** changes that alter outcomes, scope boundaries, required deliverables, Acceptance Authorities, ownership, authorization basis, or major cost or risk must:

1. be recorded as a controlled update to this document
2. be reviewed by the relevant owners and decision-makers
3. be re-authorized where the change is material

**Lifecycle points:**

- **Stage 2 (definition):** create from Stage 1 outputs; confirm outcomes, scope, owners, deliverables, and expected authorization path
- **Stage 3 (authorization):** use as primary authorization input; once approved, update status to Active and record the approval reference
- **Stage 4–6 (delivery):** keep deliverable status and governance-relevant changes current; do not let it become a design pack or task tracker
- **Stage 7 (closure):** confirm accepted deliverables, acceptance dates, final ownership, and final financial position; update status to Final

## 12. Done When

This artifact is ready for authorization when:

- a new reader can understand what the initiative is, why it exists, and what it will deliver from sections 7.2–7.4 alone
- in-scope and out-of-scope boundaries are explicit and unambiguous
- every deliverable has a named Delivery Owner and Acceptance Authority, with a defined acceptance focus
- excluded, deferred, or to-be-confirmed deliverables are visible with reasons
- Outcome Owner, Delivery Owner, Sponsor, and Decision Authorities are named
- major risks, financial implications, and operational impacts are visible at governance level
- if Deliverable Domains are used, the [Standard Deliverables Guide](../standard_deliverables_guide.md) is referenced where domains are first introduced
- no detailed design, task plans, or copies of downstream deliverables have leaked in

## 13. Prompt Guide

### 13.1. Starter prompt

```text
Draft an Initiative Definition Document for this initiative.
Explain the business need, intended outcomes, scope boundaries, owners, deliverables,
acceptance structure, major risks and dependencies, financial implications, and governance references.
Keep it readable for leadership, delivery teams, and future reviewers.
Keep detailed design and execution content out.
```

### 13.2. Section prompts

```text
Draft the scope boundaries and deliverables sections so a reviewer can see what is in scope,
what is out, what is deferred, who must deliver each major artifact, and who can accept it.
```

```text
Draft the risks, dependencies, impacts, and operational support summary sections so major
delivery, operational, financial, and governance implications are visible without becoming
a full risk register, business case, or runbook.
```

### 13.3. Validation prompt

```text
Check whether this Initiative Definition Document can act as a clear governance baseline
for downstream scope, design, delivery, and acceptance artifacts.
Rewrite any section that has drifted into detailed design, task planning,
duplicated downstream content, or unclear accountability.
```
