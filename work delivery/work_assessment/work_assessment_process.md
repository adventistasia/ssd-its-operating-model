# Work Assessment Process

## Related Documents

### Core Context

- [Work Delivery Framework](../work_delivery_framework.md)
- [Standard Deliverables Guide](../standard_deliverables_guide.md)
- [Deliverable Specifications Index](../deliverable_specifications_index.md)
- [AI-Assisted Authoring Standard](../ai_assisted_authoring_standard.md)

### Work Assessment Specifications

- [Initial Review Specification](initial_review_specification.md)
- [Validation Assessment Specification](validation_assessment_specification.md)
- [Work Assessment Report Specification](work_assessment_report_specification.md)

### Practitioner Forms

- [Initial Review Form](initial_review_form.md)
- [Validation Assessment Form](validation_assessment_form.md)
- [Work Assessment Report Form](work_assessment_report_form.md)

## Quick Start

Use this guide when a request, problem, risk, or opportunity needs to be screened before Work Definition begins.

This process sits inside **Stage 1 - Work Assessment** of the [Work Delivery Framework](../work_delivery_framework.md). It gives practitioners a practical way to stop weak work early, deepen scrutiny only where justified, and pass forward only the work that is worth defining.

Follow this order:

1. Complete the [Initial Review](initial_review_specification.md) as a quick IT-side sanity check on whether the request is worth more time and broadly aligns with what the organization does.
2. Complete the [Validation Assessment](validation_assessment_specification.md) with the requester's subject matter experts and immediate team to decide whether full business analysis is justified.
3. Complete the [Work Assessment Report](work_assessment_report_specification.md) as the culmination of that full business analysis to decide whether the initiative should enter Work Definition.

The normal handoff is:

`Work Assessment Report -> Initiative Definition Document`

The report is the final Stage 1 decision basis. The Initiative Definition Document then becomes the formal Stage 2 governance baseline.

For appropriately small governed work, the Stage 2 artifact may be a [Work Brief](../work_brief/work_brief_specification.md) instead of a full Initiative Definition Document.

What this process is for:

- stopping weak or unsupported work early
- identifying whether deeper definition effort is justified
- making sponsorship, risk, and timing concerns visible before commitment
- giving Stage 2 a clean, practical starting point

What this process is not for:

- delivery authorization
- detailed solution design
- detailed requirements or implementation planning
- vendor selection or build-ready specification work

## 1. Purpose

This document is the practical operating guide for Stage 1 - Work Assessment.

It shows teams how to assess proposed work through three increasing levels of scrutiny so that:

- low-value or weakly supported requests can stop quickly
- promising work can be tested before deeper effort is invested
- the final Stage 1 output is decision-ready and usable as input to Work Definition

## 2. Where This Process Fits

This process works inside Stage 1 of the [Work Delivery Framework](../work_delivery_framework.md). It does not replace stage decisions or authorization controls.

Use it before:

- drafting the Initiative Definition Document
- seeking Work Authorization
- producing detailed solution or operational design artifacts

The normal progression is:

`Initial Review -> Validation Assessment -> Work Assessment Report -> Initiative Definition Document`

Stage 1 decides whether the work is worth defining. Stage 2 defines what should actually be authorized.

Proceeding from Stage 1 is not delivery authorization.

## 3. Who Does What

| Role | What to focus on in this guide |
| --- | --- |
| Requestor / Submitter | Provide the need, trigger, and context for why the request exists |
| IT Assessment Owner | Drive the stage, keep it time-boxed, and produce a usable recommendation |
| Sponsor / Sponsor Candidate | Confirm the work matters and is worth advocating for if it proceeds |
| Outcome Owner Candidate | Clarify what meaningful improvement is being sought |
| ITS Leadership / Intake Governance | Decide whether to stop, defer, or let the work advance |
| Requester SMEs and Immediate Team | Contribute business context, boundaries, outcomes, and practical constraints during Validation |
| Business Analysis Leads | Produce the deeper analysis that culminates in the Work Assessment Report |
| Subject Matter Leads | Contribute targeted evidence where risk, support, security, data, operations, or compliance matter |

## 4. Before You Start

Before drafting a work assessment artifact, make sure you have at least:

- a short description of the request or opportunity
- the current step inside Stage 1
- the named Assessment Owner
- the expected decision-maker for the next gate
- enough source context to avoid pure guesswork

If these are missing, you can still create a working draft, but label it clearly as incomplete and do not treat it as ready for a decision.

## 5. Step Summary

| Step | Minimum inputs | Required outputs | Completion check | Accountable owner |
| --- | --- | --- | --- | --- |
| 1. Initial Review | request summary, source, problem signal, basic stakeholder context | Initial Review, initial decision record | the need is understandable, obvious dealbreakers are checked, and the recommendation is explicit | IT Assessment Owner |
| 2. Validation Assessment | approved Initial Review, requester SME input, basic current-state facts | Validation Assessment, recommendation on whether to do full business analysis | the need is validated, sponsorship is tested, outcomes and scope boundaries are clearer, and the case for full business analysis is explicit | IT Assessment Owner with requester SMEs and sponsor candidate |
| 3. Work Assessment Report | completed business analysis, validated scope and outcome context, stakeholder position, risk and feasibility view, preferred path | Work Assessment Report, final Stage 1 decision record, Stage 2 handoff notes, recommended Stage 2 starting artifact (Initiative Definition Document or Work Brief) | decision-makers can see whether Work Definition is justified, under what conditions, and what Stage 2 must clarify next | Business analysis lead with sponsor and ITS leadership |

## 6. Guided Workflow

### 6.1. Step 1 - Initial Review

Goal:
Decide quickly whether the request is worth any further assessment effort from the IT side.

Use this spec:

- [Initial Review Specification](initial_review_specification.md)

Do this:

1. Capture the problem, risk, or opportunity in plain language.
2. Record the desired improvement without describing a solution.
3. Note who is affected, why it matters, and what happens if nothing changes.
4. Check for obvious dealbreakers such as no mandate, no value, clear misalignment, or impossible constraints.
5. Record one of three recommendations: stop, defer, or proceed to Validation Assessment.

Produce:

- Initial Review
- decision record

Do not:

- design the solution
- estimate effort in detail
- keep exploring once a clear stop signal already exists

### 6.2. Step 2 - Validation Assessment

Goal:
Validate that the opportunity is strong enough to justify full business analysis and not obviously blocked by sponsorship, strategy, business alignment, risk, supportability, capability, or funding concerns.

Use this spec:

- [Validation Assessment Specification](validation_assessment_specification.md)

Do this:

1. Refine the problem statement using input from the requester's subject matter experts and immediate team.
2. Confirm organizational alignment, primary beneficiary, desired outcomes, success measures, and scope boundaries.
3. Describe required capabilities at high level and compare credible conceptual options, including doing nothing.
4. Surface major risk and feasibility signals across sponsorship, strategy, security, operations, delivery capability, and funding.
5. Decide whether full business analysis is justified and record what that analysis must answer if the work proceeds.

Produce:

- Validation Assessment
- recommendation to stop, defer, or proceed to full business analysis

Do not:

- turn capabilities into detailed requirements
- write vendor comparisons
- begin delivery planning

### 6.3. Step 3 - Work Assessment Report

Goal:
Produce the final Stage 1 assessment and recommendation on whether the work should enter Work Definition, using the completed business analysis as the decision basis.

Use this spec:

- [Work Assessment Report Specification](work_assessment_report_specification.md)

Do this:

1. Synthesize the business analysis findings, validated need, options, risks, timing, stakeholder position, and likely value.
2. State the preferred direction clearly, including why that path is better than the alternatives.
3. Show that there is enough information to make an informed decision to define the initiative and move it toward authorization.
4. Describe the recommended Stage 2 starting boundary without trying to define the full initiative yet.
5. Record what Stage 2 must confirm, define, or resolve if work proceeds.
6. Record the final Stage 1 decision and handoff basis.

Produce:

- Work Assessment Report
- final Stage 1 decision record
- Stage 2 handoff notes

Do not:

- treat the report as an Initiative Definition Document
- treat a recommendation to proceed as delivery approval
- bury unresolved issues in narrative text

## 7. Practical Timebox Guidance

Keep the stage practical.

Typical working expectations:

- Initial Review: days, not weeks
- Validation Assessment: usually 1 to 2 weeks
- Full business analysis and Work Assessment Report: only as much effort as needed to support an informed Stage 1 decision

## 8. Optional Assessment Work Brief

The existing "opportunity assessment work brief" pattern is still useful when the business analysis effort itself needs explicit time-boxing, ownership, or capacity approval.

Use a short internal work brief only when needed to clarify:

- who is doing the assessment
- what questions must be answered
- what is in and out of scope for the assessment effort
- what decision is being requested at the end of the assessment

This is optional support material. It is not one of the three core Stage 1 gating artifacts.

## 9. Handoff to Work Definition

If the final Stage 1 decision is to proceed, Stage 2 should start from the Work Assessment Report and not re-discover the same basics.

At minimum, the handoff should carry forward:

- validated statement of need
- desired outcomes
- sponsor and owner candidates
- the recommended path or preferred option
- major constraints, dependencies, and unresolved questions
- the specific issues Stage 2 must define before authorization

Stage 2 then produces the Initiative Definition Document and supporting authorization-level artifacts, or uses a Work Brief where the work is intentionally scaled and still governed.

## 10. AI-Assisted Authoring Workflow

When AI is helping with work assessment artifacts, use this simple loop:

1. Human states the assessment step, objective, source inputs, and decision needed.
2. AI drafts only within that step boundary.
3. Human reviews for clarity, sponsorship, risk visibility, and practical usefulness.
4. AI revises using explicit feedback.
5. Human confirms the recommendation and decision record.

AI can help:

- summarize intake notes
- structure the problem statement
- draft options, comparisons, and recommendation wording
- identify obvious gaps or contradictions in the assessment package

AI must not:

- make the go / no-go decision
- claim sponsorship, funding, or authority that has not been confirmed
- treat assumptions as approvals
- invent evidence or stakeholder support

## 11. Governance Health Signals

Good signs:

- work stops early when value or sponsorship is weak
- the level of effort increases only when the previous step justifies it
- the Work Assessment Report gives Stage 2 a clean starting point
- the recommendation is explicit and attributable

Warning signs:

- every request jumps straight into definition
- initial screening includes design, requirements, or vendor detail
- kill risks are visible but ignored
- Stage 2 is forced to rediscover basic problem, stakeholder, and risk context
- "proceed" is treated as approval to deliver
