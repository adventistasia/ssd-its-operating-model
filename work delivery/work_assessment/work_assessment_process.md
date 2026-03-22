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

### Supporting Assessment Specifications

- [Work Request Challenges and Needs Specification](work_request_challenges_and_needs_specification.md)
- [Current State Analysis Report Specification](current_state_analysis_report_specification.md)
- [Business Process Stage Analysis Specification](business_process_stage_analysis_specification.md)

### Reference Guides

- [Types of Diagrams Guide](types_of_diagrams_guide.md)

### Practitioner Forms

- [Initial Review Form](initial_review_form.md)
- [Validation Assessment Form](validation_assessment_form.md)
- [Work Assessment Report Form](work_assessment_report_form.md)

## Quick Start

Use this guide when a request, problem, risk, or opportunity needs to be screened before Work Definition begins.

This process gives practitioners a practical way to stop weak work early, deepen scrutiny only where justified, and pass forward only the work that is worth defining.

Follow this order:

1. Complete the [Initial Review](initial_review_specification.md) as a quick IT-side sanity check on whether the request is worth more time and broadly aligns with what the organization does.
2. Complete the [Validation Assessment](validation_assessment_specification.md) with the requester's subject matter experts and immediate team to decide whether focused analysis is justified and what minimum questions it must answer.
3. Complete the [Work Assessment Report](work_assessment_report_specification.md) as the culmination of that right-sized analysis to decide whether the initiative should enter Work Definition.

Use the following supporting artifacts only where they make the assessment clearer and more reusable without turning Work Assessment into Work Definition:

- [Work Request Challenges and Needs Specification](work_request_challenges_and_needs_specification.md) - optional early problem-framing support when the request is still solution-shaped or unclear
- [Current State Analysis Report Specification](current_state_analysis_report_specification.md) - situational current-state evidence artifact when a brief snapshot is not enough
- [Business Process Stage Analysis Specification](business_process_stage_analysis_specification.md) - situational process-flow support artifact when stage-by-stage flow, handoffs, or control points materially shape the assessment

The normal handoff is:

`Work Assessment Report -> Initiative Definition Document`

The report is the final work assessment decision basis. The Initiative Definition Document then becomes the normal definition baseline when work proceeds.

For appropriately small governed work, the next definition artifact may be a [Work Brief](../work_brief/work_brief_specification.md) instead of a full Initiative Definition Document.

What this process is for:

- stopping weak or unsupported work early
- identifying whether deeper definition effort is justified
- making sponsorship, risk, and timing concerns visible before commitment
- giving definition a clean, practical starting point
- capturing a small definition-ready baseline so definition does not need to rediscover basic need, current-state, stakeholder, and requirement context
- making deeper problem, current-state, and business-process understanding reusable when supporting artifacts are needed

What this process is not for:

- delivery authorization
- detailed solution design
- detailed requirements or implementation planning
- vendor selection or build-ready specification work

## 1. Purpose

This document is the practical operating guide for Work Assessment.

It shows teams how to assess proposed work through three increasing levels of scrutiny so that:

- low-value or weakly supported requests can stop quickly
- promising work can be tested before deeper effort is invested
- the final output is decision-ready and usable as input to Work Definition
- only the minimum analysis needed to support a sound work assessment decision and definition handoff is performed

## 2. Where This Process Fits

This process can be used on its own as the front-end assessment path for planned work. Where the broader [Work Delivery Framework](../work_delivery_framework.md) is used, it aligns to Work Assessment and feeds Work Definition. It does not replace later decision or authorization controls.

Use it before:

- drafting the Initiative Definition Document
- seeking Work Authorization
- producing detailed solution or operational design artifacts

The normal progression is:

`Initial Review -> Validation Assessment -> Work Assessment Report -> Initiative Definition Document`

This process decides whether the work is worth defining. Work Definition then defines what should actually be authorized.

Proceeding from Work Assessment is not delivery authorization.

## 3. Who Does What

| Role | What to focus on in this guide |
| --- | --- |
| Requestor / Submitter | Provide the need, trigger, and context for why the request exists |
| IT Assessment Owner | Drive the stage, keep it time-boxed, and produce a usable recommendation |
| Sponsor / Sponsor Candidate | Confirm the work matters and is worth advocating for if it proceeds |
| Outcome Owner Candidate | Clarify what meaningful improvement is being sought |
| ITS Leadership / Intake Governance | Decide whether to stop, defer, or let the work advance |
| Requester SMEs and Immediate Team | Contribute business context, boundaries, outcomes, and practical constraints during Validation |
| Analysis Lead / Business Analysis Lead | Produce the right-sized analysis that culminates in the Work Assessment Report |
| Subject Matter Leads | Contribute targeted evidence where risk, support, security, data, operations, or compliance matter |

## 4. Before You Start

Before drafting a work assessment artifact, make sure you have at least:

- a short description of the request or opportunity
- the current step inside Work Assessment
- the named Assessment Owner
- the expected decision-maker for the next gate
- enough source context to avoid pure guesswork

If these are missing, you can still create a working draft, but label it clearly as incomplete and do not treat it as ready for a decision.

## 5. Step Summary

| Step | Minimum inputs | Required outputs | Completion check | Accountable owner |
| --- | --- | --- | --- | --- |
| 1. Initial Review | request summary, source, problem signal, basic stakeholder context, optional problem-framing notes where needed | Initial Review, initial decision record, optional Work Request Challenges and Needs artifact | the need is understandable, obvious dealbreakers are checked, and the recommendation is explicit | IT Assessment Owner |
| 2. Validation Assessment | approved Initial Review, requester SME input, basic current-state facts, optional Work Request Challenges and Needs artifact | Validation Assessment, recommendation on whether to do focused analysis, situational Current State Analysis Report and Business Process Stage Analysis where needed | the need is validated, sponsorship is tested, outcomes and scope boundaries are clearer, and the case for focused analysis is explicit | IT Assessment Owner with requester SMEs and sponsor candidate |
| 3. Work Assessment Report | completed focused analysis, validated scope and outcome context, stakeholder position, risk and feasibility view, preferred path, any supporting assessment artifacts used | Work Assessment Report, final work assessment decision record, handoff notes, recommended next definition artifact (Initiative Definition Document or Work Brief) | decision-makers can see whether Work Definition is justified, under what conditions, and what must be clarified next | Analysis lead with sponsor and ITS leadership |

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

Use this supporting artifact only when the request needs clearer problem framing before triage is trustworthy:

- [Work Request Challenges and Needs Specification](work_request_challenges_and_needs_specification.md)

Produce:

- Initial Review
- decision record

Do not:

- design the solution
- estimate effort in detail
- keep exploring once a clear stop signal already exists

### 6.2. Step 2 - Validation Assessment

Goal:
Validate that the opportunity is strong enough to justify focused analysis and not obviously blocked by sponsorship, strategy, business alignment, risk, supportability, capability, or funding concerns.

Use this spec:

- [Validation Assessment Specification](validation_assessment_specification.md)

Do this:

1. Refine the problem statement using input from the requester's subject matter experts and immediate team.
2. Confirm organizational alignment, primary beneficiary, desired outcomes, success measures, current-state constraints, key stakeholder needs, and scope boundaries.
3. Describe high-level requirements or capabilities and compare credible conceptual options, including doing nothing.
4. Surface major risk and feasibility signals across sponsorship, strategy, security, operations, delivery capability, and funding.
5. Decide whether focused analysis is justified and record what that analysis must answer if the work proceeds.

Use these supporting artifacts only where they materially improve the assessment:

- [Work Request Challenges and Needs Specification](work_request_challenges_and_needs_specification.md) when the business problem basis still needs sharpening
- [Current State Analysis Report Specification](current_state_analysis_report_specification.md) when a brief current-state snapshot is not enough
- [Business Process Stage Analysis Specification](business_process_stage_analysis_specification.md) when process stages, handoffs, actors, or control points materially shape the work

Produce:

- Validation Assessment
- recommendation to stop, defer, or proceed to focused analysis

Do not:

- turn capabilities into detailed requirements
- write vendor comparisons
- begin delivery planning

### 6.3. Step 3 - Work Assessment Report

Goal:
Produce the final work assessment and recommendation on whether the work should enter Work Definition, using the completed focused analysis as the decision basis.

Use this spec:

- [Work Assessment Report Specification](work_assessment_report_specification.md)

Do this:

1. Synthesize the analysis findings, validated need, current state, stakeholder needs, high-level requirements, options, risks, timing, and likely value.
2. State the preferred direction clearly, including why that path is better than the alternatives.
3. Show that there is enough information to make an informed decision to define the initiative and move it toward authorization.
4. Describe the recommended definition starting boundary without trying to define the full initiative yet.
5. Record what the next definition step must confirm, define, or resolve if work proceeds.
6. Record the final work assessment decision and handoff basis.

Carry forward any material findings from supporting artifacts so definition does not need to rediscover:

- the core problem basis from the Work Request Challenges and Needs artifact where used
- the accepted current-state facts from the Current State Analysis Report where used
- the process-stage, handoff, and control findings from the Business Process Stage Analysis where used

Produce:

- Work Assessment Report
- final work assessment decision record
- definition handoff notes

Do not:

- treat the report as an Initiative Definition Document
- treat a recommendation to proceed as delivery approval
- bury unresolved issues in narrative text

## 7. Practical Timebox Guidance

Keep the stage practical.

Typical working expectations:

- Initial Review: days, not weeks
- Validation Assessment: usually 1 to 2 weeks
- Focused analysis and Work Assessment Report: only as much effort as needed to support an informed work assessment decision and a usable definition starting point

## 8. Optional Assessment Work Brief

The existing "opportunity assessment work brief" pattern is still useful when the assessment effort itself needs explicit time-boxing, ownership, or capacity approval.

Use a short internal work brief only when needed to clarify:

- who is doing the assessment
- what questions must be answered
- what is in and out of scope for the assessment effort
- what decision is being requested at the end of the assessment

This is optional support material. It is not one of the three core gating artifacts in this process.

## 9. Handoff to Work Definition

If the final assessment decision is to proceed, Work Definition should start from the Work Assessment Report and not re-discover the same basics.

At minimum, the handoff should carry forward:

- validated statement of need
- underlying business challenges and unmet needs that materially shaped the assessment
- desired outcomes
- success measures
- sponsor and owner candidates
- preferred title or working label for the item being defined
- the recommended path or preferred option
- why that path is the recommended basis for definition
- major constraints, dependencies, and unresolved questions
- the recommended next definition artifact and why
- any ownership or authority gaps that definition must close early
- the specific issues definition must clarify before authorization

Work Assessment should not try to complete the full definition artifact. It should, however, hand over a small definition-ready baseline so definition starts from accepted assessment conclusions rather than rediscovering them.

For work that proceeds, the handoff package should be explicit enough that definition can immediately carry forward:

- the approved problem statement and intended outcome
- the accepted problem-framing view of who is affected, what the issue is, and why it matters now where a Work Request Challenges and Needs artifact was used
- a concise current-state summary covering the systems, workflows, constraints, or prior attempts that materially shape definition
- any accepted Current State Analysis Report findings or Business Process Stage Analysis findings that materially shape the work
- the success measures to preserve
- the key stakeholder groups and their material needs or requirements
- the high-level requirements or capabilities any viable solution must address
- the proposed in-scope and out-of-scope boundary
- the preferred option to define, including the reason for that direction
- named sponsor, Outcome Owner, Delivery Owner, and Decision Authority signals, or a clear statement of which roles are still unresolved
- the likely deliverable domains that definition will need to make visible, and which of those domains appear material enough to require authorization-level coverage
- the assumptions definition must either preserve, validate, or resolve explicitly
- operational, support, security, privacy, compliance, funding, or dependency concerns that materially shape definition work

### 9.1. Standard definition-ready baseline

Use the following core outputs when a work item is being handed from Work Assessment into Initiative Definition or a Work Brief.

| Core work assessment handoff output | Minimum content | Primary use in definition |
| --- | --- | --- |
| Problem / Opportunity Statement | validated need, why it matters now, consequence of inaction | becomes the basis for the Initiative Definition business need and executive summary |
| Current State Summary | relevant systems, workflows, pain points, constraints, dependencies, or prior attempts | gives definition the current-state context needed for scope, risk, and support discussions |
| Stakeholders | sponsor and owner signals, affected stakeholder groups, and their material needs | helps definition confirm ownership, acceptance involvement, and change impact early |
| High-Level Requirements | what any viable answer must achieve, without design detail | gives definition a concise baseline before detailed elaboration starts |
| Risks / Constraints | material delivery, security, support, funding, compliance, or timing concerns | informs the Initiative Definition risk, dependency, and major-impact view |
| Assumptions | working assumptions that shape the recommendation and still need confirmation | shows definition what must be validated rather than silently carried forward |

Keep these outputs concise. They are not six separate large documents. In normal use they should be captured inside the Work Assessment Report as the definition-ready baseline.

### 9.2. Deliverable selection guide

Scale the handoff depth to the work, not to a fixed template burden.

| Work profile | Typical signals | Handoff expectation | Normal next definition path |
| --- | --- | --- | --- |
| Small / low risk | one team or a narrow change, limited integration, low support or compliance impact, ownership is straightforward | capture the six core outputs briefly inside the Work Assessment Report and keep the recommendation concise | usually a Work Brief |
| Medium | cross-team coordination, moderate dependency or service impact, some unresolved ownership or acceptance detail | use the standard six-output set in full, with a clear preferred path and explicit open questions for definition | Initiative Definition Document or Work Brief if the work still behaves like one clear governed item |
| Large / complex | multiple teams, significant data, security, operational, funding, or regulatory impact, or materially uncertain ownership or scope | use the standard six-output set plus expanded analysis only where it changes the decision, definition boundary, or required deliverable domains | Initiative Definition Document |

If additional analysis does not change the recommendation, the definition boundary, the ownership model, or the likely deliverable domains, do not add it just for completeness.

The next definition step then produces the Initiative Definition Document and supporting authorization-level artifacts, or uses a Work Brief where the work is intentionally scaled and still governed.

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
- the Work Assessment Report gives definition a clean starting point
- the recommendation is explicit and attributable

Warning signs:

- every request jumps straight into definition
- initial screening includes design, requirements, or vendor detail
- kill risks are visible but ignored
- definition is forced to rediscover basic problem, stakeholder, and risk context
- "proceed" is treated as approval to deliver
