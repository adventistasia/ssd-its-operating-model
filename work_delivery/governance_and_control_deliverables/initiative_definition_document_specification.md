# Initiative Definition Document Specification

## 1. What This Artifact Is For

The Initiative Definition Document explains what an initiative is, why it exists, what outcomes it is intended to achieve, what boundaries govern delivery, and what must be delivered for the initiative to be accepted.

It is the main governance baseline for initiative intent, scope, ownership, deliverable expectations, and approval context. A useful Initiative Definition Document supports authorization, downstream planning, controlled change, and later acceptance without becoming a catch-all repository for detailed design or execution content.

In this specification, an approved definition means the version of the Initiative Definition Document that has been formally authorized as the baseline the initiative will be governed against.

Intended readers include: Sponsor and sponsoring body, Decision Authorities, Outcome Owner, Delivery Owner, delivery team, Acceptance Authorities, operations and support teams, audit, and future maintainers.

## 2. When to Use It

This artifact is the default Stage 2 — Work Definition baseline for projects, major enhancements, and planned initiatives that change systems, services, data, security posture, support load, or cost in a material way.

For appropriately small governed work, use the [Work Brief](../work_brief/work_brief_specification.md) as the scaled Stage 2 artifact instead.

Use this artifact during initiative definition and keep it as the authoritative baseline once the initiative is authorized. It is most useful where intent, scope, ownership, and deliverables must remain visible across multiple downstream artifacts and across change over time.

This document should anchor project chartering, scope control, deliverable definition, authorization decisions, and downstream acceptance. It should remain understandable to leadership and maintainers while still being operationally useful to delivery and governance roles.

## 3. Stage Fit and Handoffs

This artifact is produced in Stage 2 — Work Definition. It is authorized in Stage 3 — Work Authorization and kept current throughout Stages 4–7.

**Upstream sources:**

- [Work Assessment Report](../work_assessment/work_assessment_report_specification.md) — carries forward validated need, outcomes, risks, dependencies, and recommended Stage 2 focus
- Other initiation inputs that materially affect scope, ownership, risk, or deliverables

**Downstream artifacts anchored by this document:**

- [Project Charter Specification](project_charter_specification.md) — Stage 3 authorization baseline
- [Delivery Charter Specification](delivery_charter_specification.md) — Stage 5 mobilization reference
- [Delivery Roadmap Specification](delivery_roadmap_specification.md) — delivery sequencing alignment
- Functional capabilities and domain-specific solution deliverables
- [Decision Record Log](decision_record_log_specification.md) — ongoing decision traceability
- Operational readiness artifacts
- [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md) — Stage 7 closure reference

Where delivery is broken into smaller controlled work items, this document may also anchor one or more [Work Briefs](../work_brief/work_brief_specification.md) used as child work orders. Those Work Briefs must stay within the initiative's approved scope, ownership, deliverable expectations, and authorization boundaries.

The Project Charter must not contradict this document. If authorization, funding, scope, ownership, required deliverables, or major impacts change materially, update this document first or in controlled parallel with the related governance decision.

## 4. Before You Start

Before drafting, confirm you have:

- completed Stage 1 work assessment outputs, particularly the [Work Assessment Report](../work_assessment/work_assessment_report_specification.md)
- a clear problem or opportunity statement and at least draft intended outcomes
- named Outcome Owner, Delivery Owner, and Sponsor
- sufficient understanding of scope boundaries (in/out), major risks, and dependencies
- awareness of any material financial, operational, regulatory, or security implications

If any of these are missing or unclear, label the document as a **working draft** and identify the missing inputs explicitly.

## 5. How to Draft It

1. **Start from the Work Assessment Report.** Carry forward the validated need, desired outcomes, major risks, dependencies, stakeholder context, and recommended Stage 2 focus.
2. **Draft the executive summary and business need sections.** Confirm why the initiative exists, what it will achieve, and what the organization is being asked to commit.
3. **Define outcomes and scope boundaries.** Make in-scope and out-of-scope content explicit. Include material assumptions and constraints. Reference functional capabilities if scope requires it.
4. **Define the deliverables and acceptance structure.** List required deliverables or Deliverable Domains, their owners, Acceptance Authorities, and acceptance focus for each.
5. **Summarize risks, dependencies, and major impacts.** Make governance-level financial, operational, regulatory, and support implications visible.
6. **Add the operational support summary.** Include run and support ownership, tier model, and links to operational readiness artifacts where relevant.
7. **Complete the document identity and control section.** Fill all fields including owners, Decision Authorities, and authorization reference or path.
8. **Check against the validation guide** before submitting for authorization review.

## 6. Minimum Structure

### 6.1. Document identity and control

Must include:

- initiative name
- initiative or project ID where used
- version
- status (Draft, Active, or Final)
- last updated date
- Outcome Owner
- Delivery Owner
- Sponsor
- sponsoring body where different from the Sponsor
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

When Deliverable Domains are first mentioned, reference the [Standard Deliverables Guide](../standard_deliverables_guide.md) so the reader can understand the domain structure being used.

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

Link to supporting operational readiness material rather than restating detailed support content here.

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

## 7. Writing Rules

Include enough detail to support decision-making, clarify scope boundaries, define deliverable expectations, make ownership explicit, and show key risk, financial, operational, and support implications. Use references for detailed design, planning, testing, and operating material rather than embedding them.

> Include enough information to make a sound decision and to understand what the initiative is, what it will deliver, who is accountable, and what material implications must be accepted. Put detailed content in separate artifacts and reference them from this document.

For appropriately small initiatives, it is acceptable for all relevant information to remain in the Initiative Definition Document. Spinning off a separate artifact to hold detailed content is at the discretion of the practitioner, provided the document remains readable and governable.

Keep the following out:

- detailed architecture and configuration
- full runbooks or procedures
- detailed test scripts
- sprint or task plans
- repeated copies of downstream deliverables
- detailed risk register entries better managed elsewhere
- technical specifications beyond what is needed to understand scope, risk, or approval implications

## 8. Traceability, Ownership, and Review

The Delivery Owner usually coordinates the document with input from the Outcome Owner and Sponsor.

It should be reviewed by key owners and Decision Authorities before authorization. Formal approval normally sits with the Sponsor or delegated Decision Authority, with the approval reference recorded in the document control section.

This document traces back to the [Work Assessment Report](../work_assessment/work_assessment_report_specification.md). It feeds forward to the [Project Charter](project_charter_specification.md), functional capabilities, domain deliverables, decision records, operational readiness artifacts, and the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md).

## 9. Maintenance Expectations

This is a living governance document. Keep deliverables, owners, decision references, scope status, major impacts, and acceptance status current. Use references to detailed artifacts rather than embedding large downstream content.

At minimum:

- keep the deliverables section current
- keep the change log current for material updates
- keep authorization and decision references traceable
- keep major cost, risk, and support implications visible at governance level

Changes that alter outcomes, scope boundaries, required deliverables, Acceptance Authorities, ownership, authorization basis, or major cost or risk must:

1. be recorded as a controlled update to this document
2. be reviewed by the relevant owners and decision-makers
3. be re-authorized where the change is material

## 10. Done When

The document is ready for authorization review when:

- executive summary, business need, outcomes, and scope boundaries are complete and unambiguous
- Outcome Owner, Delivery Owner, Sponsor, and all Decision Authorities are named
- all required deliverables are listed with Delivery Owners, Acceptance Authorities, and acceptance focus
- major risks, dependencies, and financial implications are visible at governance level
- the authorization path is confirmed and the document control section is complete
- operational support implications are addressed where the initiative impacts a service or system

## 11. Validation Guide

Use this checklist when reviewing a produced Initiative Definition Document. Compare the document against each item and identify any gaps, ambiguity, missing ownership, or misplaced detail.

### Understanding and purpose

1. A new reader can understand what the initiative is, why it exists, and what it intends to achieve from the executive summary, business need, and outcomes sections.
2. The intended outcomes and success measures are clearly stated and, where possible, measurable.

### Scope and accountability

3. In-scope and out-of-scope boundaries are explicit and unambiguous.
4. Outcome Owner, Delivery Owner, Sponsor, and Decision Authorities are present and named.
5. The authorization basis is visible and traceable.

### Deliverables and acceptance

6. All required deliverables are clearly listed, either by domain or as a consolidated list.
7. Each deliverable has a named Delivery Owner and Acceptance Authority.
8. The acceptance focus is clearly defined for each deliverable, or acceptance criteria are stated where the Initiative Definition Document is the sole artifact.
9. Excluded, deferred, or still-to-be-confirmed deliverables are visible with reasons.
10. Deliverable status uses the defined status values: Draft, Planned, In Progress, Delivered, or Accepted.
11. If Deliverable Domains are used, the document references the [Standard Deliverables Guide](../standard_deliverables_guide.md) when domains are first introduced.

### Living document expectations

12. Each listed deliverable has a current status.
13. Where a deliverable is delivered, a reference to the delivered artifact exists.
14. Where evidence is required, the evidence exists and is referenced.
15. Where a deliverable is accepted, the acceptance record is referenced and the acceptance date is recorded.
16. The document is current and the change log reflects material updates.

### Operational and financial viability

17. Major risks, dependencies, and feasibility concerns are visible enough for governance review.
18. CapEx, OpEx, budget position, and material financial assumptions are visible at the right level.
19. If the initiative impacts a service or system, run ownership, support ownership, and ongoing support implications are visible and the document links to relevant operational readiness artifacts.

### Change control

20. Material changes are handled through controlled update and re-authorization where required.

## 12. What Comes Next

1. Submit the document to the Sponsor and Decision Authorities for authorization review.
2. Produce the [Project Charter](project_charter_specification.md) to formally record the Stage 3 authorization decision.
3. Use the authorized scope and deliverables to select required artifacts using the [Standard Deliverables Guide](../standard_deliverables_guide.md).
4. Begin Stage 4 elaboration of functional capabilities and domain deliverables, staying within the approved baseline.
5. Keep this document current throughout delivery, updating status, references, and the change log as the initiative progresses.

## 13. Prompt Guide

### Starter prompt

```
Draft an Initiative Definition Document for this initiative.
Explain the business need, intended outcomes, scope boundaries, owners, deliverables, acceptance structure, major risks and dependencies, financial implications, and governance references.
Keep it readable for leadership, delivery teams, and future reviewers, and keep detailed design or execution content out.
```

### Validation prompt

```
Check whether this Initiative Definition Document can act as a clear governance baseline for downstream scope, design, delivery, and acceptance artifacts.
Rewrite any section that has drifted into detailed design, task planning, duplicated downstream content, or unclear accountability.
```
