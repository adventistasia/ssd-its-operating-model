# Initiative Definition Document Specification

## 1. Purpose and Intended Outcome

The Initiative Definition Document explains what the initiative is, why it exists, what outcomes it is intended to achieve, what boundaries govern delivery, and what must be delivered for the initiative to be accepted.

It is the main governance baseline for initiative intent, scope, ownership, deliverable expectations, and approval context. A useful Initiative Definition Document supports authorization, downstream planning, controlled change, and later acceptance without becoming a catch-all repository for detailed design or execution content.

In this specification, an approved definition means the version of the Initiative Definition Document that has been formally authorized as the baseline the initiative will be governed against.

The intended outcome is that the initiative has a single authoritative baseline for outcomes, scope boundaries, ownership, required deliverables, major impacts, and decision references that downstream work can align to and be tested against.

## 2. When It Is Required

This artifact is the default Stage 2 - Work Definition baseline for projects, major enhancements, and planned initiatives that change systems, services, data, security posture, support load, or cost in a material way.

For appropriately small governed work, a Work Brief may be used as the scaled Stage 2 artifact instead.

## 3. Intended Readers and Users

- Sponsor and sponsoring body where applicable
- Decision Authorities
- Outcome Owner
- Delivery Owner and delivery team
- Acceptance Authorities
- Operations and support
- Audit and future maintainers

## 4. Intended Project Context

Use this artifact during initiative definition and keep it as the authoritative baseline once the initiative is authorized. It is most useful where intent, scope, ownership, and deliverables must remain visible across multiple downstream artifacts and across change over time.

This document should anchor project chartering, scope control, deliverable definition, authorization decisions, and downstream acceptance. It should remain understandable to leadership and maintainers while still being operationally useful to delivery and governance roles.

## 5. How Much Detail to Include

Include enough detail to support decision-making, clarify scope boundaries, define deliverable expectations, make ownership explicit, and show key risk, financial, operational, and support implications. Use references for detailed design, planning, testing, and operating material rather than embedding them.

The governing principle is:

> Include enough information to make a sound decision and to understand what the initiative is, what it will deliver, who is accountable, and what material implications must be accepted. Put detailed content in separate artifacts and reference them from this document.

At authorization time, this document should contain enough clarity to support informed approval. During delivery, it should remain current enough to govern scope, deliverables, and acceptance without drifting into detailed design or task management.

For appropriately small initiatives, it is acceptable for all relevant information to remain in the Initiative Definition Document. Spinning off a separate artifact to hold detailed content is at the discretion of the practitioner, provided the document remains readable and governable.

## 6. Required Content or Minimum Structure

### 6.1. Document identity and control

Must include:

- initiative name
- initiative or project ID where used
- version
- status such as Draft, Active, or Final
- last updated date
- Outcome Owner
- Delivery Owner
- sponsor
- sponsoring body where different from the sponsor
- Decision Authorities, including the level or type of decision each is authorized to make where needed
- authorization record or reference to the formal approval basis
- change log or equivalent version history

This section identifies the controlled governance baseline and who has authority over it.

### 6.2. Executive summary

Must include:

- plain-language description of the initiative
- why the initiative exists now
- intended outcomes
- high-level statement of what will be delivered
- estimated one-time cost or CapEx where applicable
- estimated ongoing annual operating cost or OpEx where applicable
- approved budget and current expenditure position where already available

This section should allow a decision-maker to understand the initiative quickly and see the scale of commitment being requested.

### 6.3. Business need and rationale

Must include:

- current problem or opportunity
- who is affected
- why action is justified
- consequences of inaction where relevant

This section explains the case for the initiative.

### 6.4. Outcomes and success measures

Must include:

- intended outcomes
- measurable success indicators
- important non-goals or things that should not be treated as success

This section helps downstream artifacts remain aligned to intended value.

### 6.5. Scope boundaries

Must include:

- in-scope content
- out-of-scope content
- assumptions
- key constraints

If functional scope is material to understanding the initiative, include either a concise summary of required functional capabilities or a reference to the separate functional capabilities artifact.

This section is the main boundary control for the initiative.

### 6.6. Deliverables and acceptance structure

Must include:

- required deliverables or Deliverable Domains
- Delivery Owner for each deliverable
- Acceptance Authority for each deliverable or domain
- acceptance focus or what matters for sign-off
- current status
- note of any deliverables or domains intentionally excluded, deferred, or to be confirmed later, with reason

Recommended columns:

| Deliverable or domain | Description | Delivery Owner | Acceptance Authority | Acceptance focus | Status | Reference |
| --- | --- | --- | --- | --- | --- | --- |

When Deliverable Domains are first mentioned in an Initiative Definition Document, reference the [Standard Deliverables Guide](../standard_deliverables_guide.md) so the reader can understand the domain structure being used.

If the Initiative Definition Document is the sole artifact for the initiative, the acceptance focus may be expressed directly as the acceptance criteria.

Use the following status values for deliverables:

- Draft
- Planned
- In Progress
- Delivered
- Accepted

Where applicable, also include:

- reference to the delivered artifact
- reference to supporting evidence
- reference to the acceptance record
- acceptance date

Control rule: a deliverable is only accepted when the named Acceptance Authority has formally confirmed that the acceptance focus has been met.

This section turns the initiative from an idea into an accountable delivery baseline.

### 6.7. Key risks, dependencies, and major impacts

Must include:

- major delivery or feasibility risks
- material dependencies
- major operational, financial, regulatory, security, or support implications
- material assumptions about funding, risk tolerance, service ownership, or organizational readiness that decision-makers are being asked to accept

Where financial detail is relevant, make visible:

- estimated CapEx
- estimated OpEx
- approved budget if available
- actual spend and variance if already in flight

This section helps define what decision-makers are being asked to commit to.

### 6.8. Operational support summary

Required when the initiative materially impacts a service or system.

Include only the minimum governance-level summary needed to show that operational sustainability has been considered. Detailed support design should remain in operational readiness artifacts.

Recommended content:

- operational or run owner
- support owner
- intended support tier model and escalation path at summary level
- monitoring and recovery intent at summary level
- expected ongoing support effort or cost impact
- reference to the relevant operational readiness artifact or artifacts where detailed support arrangements will be maintained

Encourage the practitioner to link to the relevant supporting operational readiness material rather than restating detailed support content here.

This section keeps the governance baseline connected to supportability without turning the document into a runbook.

### 6.9. Related references and supporting decisions

Should include:

- links to upstream assessments
- key policy or strategy references
- standards used where relevant
- related initiatives or dependencies
- relevant decision or approval records
- contracts, licensing, or external references that materially shape scope or obligations

This section prevents duplication while preserving traceability.

## 7. What to Keep Out

Keep the following out of this artifact:

- detailed architecture and configuration
- full runbooks or procedures
- detailed test scripts
- sprint or task plans
- repeated copies of downstream deliverables
- detailed risk register entries better managed elsewhere
- technical specifications beyond what is needed to understand scope, risk, or approval implications

## 8. Relationships to Other Artifacts

This artifact should normally be created from the completed Stage 1 assessment outputs, especially the [Work Assessment Report](../work_assessment/work_assessment_report_specification.md), plus any other initiation inputs that materially affect scope, ownership, risk, or deliverables.

For work that is intentionally scaled and can be governed as one small work item, use the [Work Brief Specification](../work_brief/work_brief_specification.md) instead of forcing a full Initiative Definition Document.

This artifact anchors the Project Charter, Functional Capabilities, domain-specific deliverables, decision records, operational readiness artifacts, and final acceptance and closure records.

Where delivery is broken into smaller controlled work items, the Initiative Definition Document may also anchor one or more Work Briefs used as child work orders under the approved initiative baseline.

Those Work Briefs should stay within the initiative's approved scope, ownership, deliverable expectations, and authorization boundaries. They should define and control discrete pieces of work without replacing the Initiative Definition Document as the main governance baseline.

The Project Charter should not contradict this document. If authorization, funding, scope, ownership, required deliverables, or major impacts change materially, the Initiative Definition Document should be updated first or in controlled parallel with the related governance decision.

## 9. Ownership, Review, and Acceptance Expectations

The Delivery Owner usually coordinates the document with input from the Outcome Owner and Sponsor.

It should be reviewed by key owners and Decision Authorities before authorization. Formal approval normally sits with the Sponsor or delegated Decision Authority, with the approval reference recorded in the document control section.

## 10. Maintenance Expectations

This is a living governance document. Keep deliverables, owners, decision references, scope status, major impacts, and acceptance status current. Use references to detailed artifacts rather than embedding large downstream content.

At minimum:

- keep the deliverables section current
- keep the change log current for material updates
- keep authorization and decision references traceable
- keep major cost, risk, and support implications visible at governance level

## 11. Lifecycle and Change Control

### 11.1. Definition stage

Create the document from the completed Stage 1 work assessment outputs and other initiation inputs. In normal use, this means starting from the [Work Assessment Report](../work_assessment/work_assessment_report_specification.md) and carrying forward the validated need, desired outcomes, major risks, dependencies, stakeholder context, and recommended Stage 2 focus.

Confirm outcomes, scope boundaries, owners, deliverables, Acceptance Authorities, major impacts, and the expected authorization path.

### 11.2. Authorization stage

Use the draft document as part of the approval basis. Once formally authorized, update status to Active and record the approval reference.

### 11.3. Delivery stage

Keep deliverable status, references, acceptance information, and major governance-relevant changes current. Improve clarity as needed, but do not use this document as a design pack or task tracker.

### 11.4. Closure stage

Confirm accepted deliverables, acceptance dates, final ownership visibility, and final financial position where relevant. Update status to Final.

### 11.5. Change rule

Changes that alter outcomes, scope boundaries, required deliverables, Acceptance Authorities, ownership, authorization basis, or major cost or risk must:

1. be recorded as a controlled update to this document
2. be reviewed by the relevant owners and decision-makers
3. be re-authorized where the change is material

## 12. Agent Validation Instruction Checklist

Use this checklist when reviewing a produced or written Initiative Definition Document. Compare the document against each instruction and identify any gaps, ambiguity, missing ownership, or misplaced detail.

### 12.1. Understanding and purpose

1. Confirm that a new reader can understand what the initiative is, why it exists, and what it intends to achieve from the executive summary, business need, and outcomes sections.
2. Confirm that the intended outcomes and success measures are clearly stated and, where possible, measurable.

### 12.2. Scope and accountability

3. Confirm that in-scope and out-of-scope boundaries are explicit and unambiguous.
4. Confirm that Outcome Owner, Delivery Owner, Sponsor, and Decision Authorities are present and named.
5. Confirm that the authorization basis is visible and traceable.

### 12.3. Deliverables and acceptance

6. Confirm that all required deliverables are clearly listed, either by domain or as a consolidated list.
7. Confirm that each deliverable has a named Delivery Owner and Acceptance Authority.
8. Confirm that the acceptance focus is clearly defined for each deliverable, or that acceptance criteria are stated where the Initiative Definition Document is the sole artifact.
9. Confirm that excluded, deferred, or still-to-be-confirmed deliverables are visible with reasons.
10. Confirm that deliverable status uses the defined status values: Draft, Planned, In Progress, Delivered, or Accepted.
11. If Deliverable Domains are used, confirm that the document references the [Standard Deliverables Guide](../standard_deliverables_guide.md) when the domains are first introduced.

### 12.4. Living document expectations

12. Confirm that each listed deliverable has a current status.
13. Where a deliverable is delivered, confirm that a reference to the delivered artifact exists.
14. Where evidence is required, confirm that the evidence exists and is referenced.
15. Where a deliverable is accepted, confirm that the acceptance record is referenced and the acceptance date is recorded.
16. Confirm that the document is current and that the change log reflects material updates.

### 12.5. Operational and financial viability

17. Confirm that major risks, dependencies, and feasibility concerns are visible enough for governance review.
18. Confirm that CapEx, OpEx, budget position, and material financial assumptions are visible at the right level.
19. If the initiative impacts a service or system, confirm that run ownership, support ownership, and ongoing support implications are visible and that the document links to the relevant operational readiness artifact or artifacts.

### 12.6. Change control

20. Confirm that material changes are handled through controlled update and re-authorization where required.

## 13. Prompt Guide for Drafting the Artifact

### 13.1. Starter prompt

> Draft an Initiative Definition Document for this initiative.
> Explain the business need, intended outcomes, scope boundaries, owners, deliverables, acceptance structure, major risks and dependencies, financial implications, and governance references.
> Keep it readable for leadership, delivery teams, and future reviewers, and keep detailed design or execution content out.

### 13.2. Section prompts

> Draft the scope boundaries and deliverables sections so a reviewer can see what is in scope, what is out, what is deferred, who must deliver each major artifact, and who can accept it.

> Draft the risks, dependencies, impacts, and operational support summary sections so major delivery, operational, financial, and governance implications are visible without becoming a full risk register, business case, or runbook.

### 13.3. Validation prompts

> Check whether this Initiative Definition Document can act as a clear governance baseline for downstream scope, design, delivery, and acceptance artifacts.

> Rewrite any section that has drifted into detailed design, task planning, duplicated downstream content, or unclear accountability.
